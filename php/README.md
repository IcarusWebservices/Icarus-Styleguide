<div align="center">
    <img src="http://icarusws.nl/js-content/resources/logo_geen_background.png" height="100px">
    <h1>Icarus PHP Styleguide</h1>
</div>

## Table of Contents
1. [Naming Practices](#naming-practices)
    - [Variables](#naming-variables)
    - [Constants](#naming-constants)
    - [Functions](#naming-functions)
    - [Classes](#naming-classes)
        - [General](#general)
        - [Class proporties](#class-proporties)
        - [Class methods](#class-methods)
2. [Variables](#variables)
3. [Functions](#functions)
4. [Classes](#classes)
5. [Documentation & Comments](#documentation--comments)
6. [Indentation](#Indentation)
7. [PHP Built-in functions & variables](#php-built-in-functions--variables)

&nbsp;

## Naming Practices
Most common casing styles:
- <span id="snake">**Snake casing**</span>: All words should be stringed together with an underscore. All characters should be lower-case. Example: ```this_variable```

- <span id="pascal">**Pascal casing**</span>: All words should be stringed together without a devider character. All words should start with a capital letter. Example: ```ThisVariable```

- <span id="camel">**Camel casing**</span>: All words should be stringed together without a devider character. All words **except the first** should start with a capital letter. Example: ```thisVariable```
- <span id="upper">**UPPER**</span>: All words should be stringed together with an underscore. All characters should be upper-case. Example: ```THIS_VARIABLE```


### Naming variables
- Variables should use [snake casing](#snake) notation.
    ```php
    $my_variable = 12;
    ```
- If the variables are specific to a project and you want to include the name of the project, you can add the name to the beginning.
    ```php
    $my_project_variable = 12;
    ```

### Naming constants
- Constanst should use [UPPER](#upper) notation. This sets the constants appart from class names.
    ```php
    define("MY_CONSTANT", 0);
    ```
- If constants are specific to a project and you want to include the name of the project, you can add the name to the beginning.
    ```php
    define("MY_PROJECT_CONSTANT", 0);
    ```

### Naming functions
- Functions should use [snake casing](#snake) notation.
    ```php
    function foo_bar() {
        return null;
    }
    ```
- Arguments should be treated the same as normal variables, so they should use [snake casing](#snake).
    ```php
    function foo_bar( $foo_has_bar ) {
        return $foo_has_bar;
    }
    ```

### Naming classes
#### General
- The class name should use [Pascal casing](#pascal) notation.
    ```php
    class MyClass {  }
    ```
- If you wish to add the name of your project to the class name, you can add the name to the beginning of the class name.
    ```php
    class MyProjectClass {  }
    ```
- Abstract classes should use all of these rules

#### Class Proporties
- Proporties should use the **same casing as variables (snake casing)**. This is because proporties basically act like variables within classes, so using the same notation helps.
    ```php
    class MyClass {
        
        public $my_proporty = 12;
        
    }
    ```
#### Class methods
- Methods should use [camel casing](#camel) to easily differantiate methods from proporties.
- Method arguments should use the same notation as function arguments: [snake casing](#snake).
    ```php
    class MyClass {
        
        public function myMethod( $my_argument ) {
            return $my_argument;
        }
        
    }
    ```

**[⬆ back to top](#table-of-contents)**
&nbsp;
## Variables
- Variables should **always** be defined with a value. If a variable should not have a defined starting value, set the variable to ```null```: 
    ```php
    $foo = 0;
    $bar = null;
    ```
- `strings` that do **not** include HTML should be defined with double quotes (").
    ```php
    $my_string = "My string";
    ```
- `strings` that include HTML should also use single quotes ("). Strings within the HTML (for example the HTML element attributes) should use escaped double quotes.
    ```php
    $my_html = "<a href=\"my-website.com\">My website</a>";
    ```
**[⬆ back to top](#table-of-contents)**

## Functions
- Everything that applies to functions, also applies to class methods.
- When calling a function with arguments, you should leave a space after the first bracket, leave a space after each comma and leave a space before the last bracket.
    ```php
    function my_amazing_function( $argument1, $argument2 ) {
        return 0;
    }
    ```
- Arguments should never be redefined within the function
    ```php
    function test_function( $argument ) {
        // This is not allowed!
        $argument = 2;
    }
    ```

**[⬆ back to top](#table-of-contents)**

## Classes
- All proporties should always be declared within the class. In addition, they should always be assigned a value. Proporties that should not have a value, should be set to `null`. If you really want to not assign a value, make at least sure that a value is assigned within the constructor.
    > Declaring the proporties makes it easier to read a class

    ```php
    class MyClass {
        public $my_proporty = 0;
    }
    ```
- All proporties and methods should declare its visibility. This is mandatory for proporties by default within PHP. 
    Visibility can be one of these terms: <br>
    `public` - This method or proporty can be accessed from anywhere within the code.<br>
    `private` - This method or proporty can only be accessed from within the class itself.<br>
    `protected` - This method or proporty can only be access from within the class itself OR classes that inherit the class.<br>
    > Visibility helps with defining what can and cannot be accessed. It also works with Intellisense.

    ```php
    class MyClass {
        
        public $my_proporty = 12;
        
        protected function myMethod() {
            
        }
        
        private function myMethod2() {
            
        }
        
    }
    ```
- The order of keywords should be `[visibility] [static] [final] [method or proporty name]`
    > Having visibility first helps order a class into a public, private and protected side. Static is the second most important (it determines whether this method or proporty should be accessed through an instance or through the class itself). Final is the least important keyword, and should thus be last.

    ```php
        class MyClass {
            
            public static final function myPublicFinalStaticFunction() {
                return null;
            }
            
            public static function myPublicStaticFunction() {
                return null;
            }
            
            public final function myPublicFinalFunction() {
                return null;
            }
            
            public static final $my_proporty;
            
            public final $my_other_proporty;
            
            public static $my_other_other_proporty;
            
        }
    ```
**[⬆ back to top](#table-of-contents)**

## Documentation & Comments
### Comments
- PHP Supports three types of comments: Multiline comments (`/* */ `), Single line comments (double slash, `//`) and Single line comments (hash, `#`).
- Multiline comments should be used for documentation (see [Documentation](#documentation)) and for comments that are too long for one line. They can also be used to create large headers.
    ```php
    # Example one
    
    /*
        This comment is too long for one line,
        so it is split up in two
    */
    
    # Example two
    
    /*===================================================================================================
            Large Header
    ===================================================================================================*/
    ```
- Double slash single line comments should be the primary way to create comments. These comments should be used to add remarks to the code, making the code easier to read.
    ```php
    // These comments should be used to add remarks to the code, making the code easier to read
    ```
- Hash single line comments should be used to create headers to your code or add TODO's.
    ```php
    # Example 1
    // Some code here
    
    # TODO: add code to 'Example 1'
    ```
    Comments can also reference hash headers, like seen in the example above.

### Documentation
- Documentation should follow the PHPDoc guidelines, as mentioned [here](https://docs.phpdoc.org/references/phpdoc/index.html).
    > PHPDoc is an excellent way to document code. Intellisense in, for example, Visual Studio Code supports PHPDoc.
- PHPDoc example:
    ```php
    /**
     * My Amazing Function
     * @param array $my_array This is my array
     * @return void
     */
    function my_amazing_function( $my_array ) {
        // return void
    }
    ```
**[⬆ back to top](#table-of-contents)**

## Indentation
- For PHP use an indentation of 4 spaces
    > Four spaces makes the code more readable. It allows you and your co-developers to more easily see what parts of the code are within different blocks, that being if-statements, functions, classes and more.
- HTML within PHP should also use an indentation of 4 spaces, as is highlighted within the HTML styleguide.

**[⬆ back to top](#table-of-contents)**

## PHP Built-in functions & variables
- PHP has a few "keyword functions". These are functions that can be called through a keyword instead of a propper function call (Functions like `echo`, `include` and `require`).
    These functions should preferable be called as an actual function.
    > This helps to make the code seem more clean. Having a consistent syntax is good for your code.

    ```php
    // Non-prefered way:
    echo "This is using a keyword function";
    include "my-application.php";
    
    // Prefered way:
    echo( "This is using a keyword function" );
    include( "my-application" );
    ```
- If you are creating a `<?php ?>` tag only to echo something you should use the `<?= ?>` tag. End the string or variable name with a `;`.
    > This reduces the amount of code needed drastically.

    ```php
    <h1><?= $my_title; ?></h1>
    ```
    
**[⬆ back to top](#table-of-contents)**