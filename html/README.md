<div align="center">
    <img src="http://icarusws.nl/js-content/resources/logo_geen_background.png" height="100px">
    <h1>Icarus HTML Styleguide</h1>
</div>

## Table Of Contents
1. [Indentation](#indentation)
2. [Elements](#elements)

## Indentation
- HTML should use an indentation of 4 spaces, especially when integrating HTML into PHP. If you are however creating an HTML file without PHP 2 spaces is permitted but not recommended.
    > 4 spaces helps with the readability within PHP (4 spaces is required for PHP according to the PHP styleguide).
    > For files without PHP, 2 spaces is permitted (and even recommended by some other styleguides). This is up for your own preference, although we prefer 4 spaces.

## Elements
- The tagname of an element should always be lowercase, both in the start & closing tag.
    > This is concidered common practice in HTML and almost all websites use this style.

    ```html
        <!-- Correct -->
        <h1>My Header</h1>
        <span>My Span</span>
        
        <!-- Incorrect -->
        <H1>My Header</H1>
        <SPAN>My Span</SPAN>
    ```
- Attributes should use double quotes.
    > This looks better in general

    ```html
    <!-- Correct -->
    <span id="my-id">my span</span>
    
    <!-- Incorrect -->
    <span id='my-id'>my span</span>
    ```
- Custom attributes on default HTML5 elements are **only** permitted as part of an element's dataset.
    > This helps to differentiate HTML5 attributes from custom attributes

    ```html
    <!-- Correct -->
    <span id="12" data-custom-attribute="my-custom-attribute"></span>
    
    <!-- Incorrect -->
    <span id="12" custom-attribute="my-custom-attribute"></span>
    ```
    
- Custom attributes are permitted on custom elements (also known as Web Components).