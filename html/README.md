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
    ```html
    <my-component my-custom-attribute="My amazing attribute"></my-component>
    ```
- Using the `style` argument on elements is discouraged.
    > Create a seperate .css file and link it through the header. To style an individuel element, use an ID.

    ```html
    <!-- Avoid -->
    <a href="#" style="color:red;">This link</a>
    ```
- The `html` element should always include the `lang` attribute. You should set this to the language code of the language of the page.
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <!-- Your website -->
    </html>
    ```
    
## Layout
- You should always start your document with the `<!DOCTYPE html>` tag.
- You should always create an organized document structure.
    > We mean that you should put all of your HTML within `<html>` tags, all of your page body within `<body>` tags and all the headers within `<head>` tags.

    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <title>Welcome to the website</title>
        </head>
        <body>
            <h1>My header</h1>
        </body>
    </html>
    ```
- You should always use the `meta viewport` tag to make your webpage responsible.
    Preferable use this tag: `<meta name="viewport" content="width=device-width, initial-scale=1">`.
    > This makes sure that the webpage responds to changes in device width.

    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <title>Welcome to the website</title>
        </head>
        <body>
            <h1>My header</h1>
        </body>
    </html>
    ```
    
