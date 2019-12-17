<div align="center">
    <img src="http://icarusws.nl/js-content/resources/logo_geen_background.png" height="100px">
    <h1>Icarus PHP Styleguide</h1>
</div>

## Table of Contents
1. [Naming Practices](#naming-practices)
    - [Variables](#naming-variables)
    - [Constants](#naming-constants)
2. [Variables](#variables)

## Naming Practices
Most common casing styles:
- <span id="snake">**Snake casing**</span>: All words should be stringed together with an underscore. All characters should be lower-case. Example: ```this_variable```

- <span id="pascal">**Pascal casing**</span>: All words should be stringed together without a devider character. All words should start with a capital letter. Example: ```ThisVariable```

- <span id="camel">**Camel casing**</span>: All words should be stringed together without a devider character. All words **except the first** should start with a capital letter. Example: ```thisVariable```
- <span id="upper">**UPPER**</span>: All words should be stringed together with an underscore. All characters should be upper-case. Example: ```THIS_VARIABLE```
### Naming variables
- Variables should use [snake casing](#snake) notation.
- If the variables are specific to a project and you want to include the name of the project, you can add the name to the beginning.
```php
// Good
$my_variable = 12;
# With project name
$project_my_variable = 12;

// Bad
$myVariable = 12;

$MYVARIABLE = 12;

$My_Variable = 12;

$MyVariable = 12;
```

### Naming constants
- Constanst should use [UPPER](#upper) notation. This sets the constants appart from class names.
```php
// Good
define("MY_CONSTANT", 0);

// Bad
define("my_constant", 0);
define("My_Constant", 0);
```

### Naming functions
- Functions should use [snake casing](#snake) notation.
```php
// Good
function foo_bar() {
    return null;
}

//=== Bad ===//
# No camel-casing
function fooBar() { return null; }
# No 
function FooBar() { return null; }
```

## Variables
- Variables should **always** be defined with a value. If a variable should not have a defined starting value, set the variable to ```null```: 
```php
    $foo = 0;
    $bar = null;
```
