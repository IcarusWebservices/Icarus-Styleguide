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
- **Snake casing**: All words should be stringed together with an underscore. All characters should be lower-case. Example: ```this_variable```

- **Pascal casing**: All words should be stringed together without a devider character. All words should start with a capital letter. Example: ```ThisVariable```

- **Camel casing**: All words should be stringed together without a devider character. All words **except the first** should start with a capital letter. Example: ```thisVariable```
- **UPPER**: All words should be stringed together with an underscore. All characters should be upper-case. Example: ```THIS_VARIABLE```
### Naming variables
- Variables should use snake-case notation.
```php
// Good
$my_variable = 12;

// Bad
$myVariable = 12;

$MYVARIABLE = 12;

$My_Variable = 12;

$MyVariable = 12;
```

### Naming constants
- Constanst should use full upper-case notation. This sets the constants appart from class names.
```php
// Good
define("MY_CONSTANT", 0);

// Bad
define("my_constant", 0);
define("My_Constant", 0);
```

### Naming functions
- Functions should use snake-case notation.
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
