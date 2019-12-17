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
### Naming variables
Variables should preferable use lower-case underscore notation.
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
Constanst should preferably use full upper-case notation. This sets the constants appart from class names.
```php
// Good
define("MY_CONSTANT", 0);

// Bad
define("my_constant", 0);
define("My_Constant", 0);
```

## Variables
- Variables should **always** be defined with a value. If a variable should not have a defined starting value, set the variable to ```null```: 
```php
    $foo = 0;
    $bar = null;
```
