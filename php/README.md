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
2. [Variables](#variables)

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
            returns $my_argument;
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
