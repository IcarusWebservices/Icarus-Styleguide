<div align="center">
    <img src="http://icarusws.nl/js-content/resources/logo_geen_background.png" height="100px">
    <h1>Icarus CSS Styleguide</h1>
</div>

# Table of contents
1. [Variables](#variables)
2. [Indentation](#indentation)
3. [Syntax](#syntax)
4. [Comments](#comments)

# Variables
- The use of CSS variables is permitted and recommended.
    > Variables prevent spaghetti code from occuring
- You should declare variables within the `html` selector to keep your variables in one place.
    ```css
    /* ----- Bad ----- */
    .container {
      --color-primary: red;
      color: var(--color-primary);
    }
    ```
    
    ```css
    /* ----- Good ----- */
    html {
      --color-primary: red;
    }
    
    .container {
      color: var(--color-primary);
    }
    ```

# Indentation
- You should use an indentation of 2 spaces
    > This makes the CSS more readable, since having 2 spaces makes the lines shorter

    ```css
    /* ----- Bad ----- */
    html {
        color: red;
    }
    
    /* ----- Good ----- */
    html {
      color: red;
    }
    ```

# Syntax
- It is recommended to start your code by removing the automatic padding and margins.
    > Most browsers automatically add margins and padding to the page. You should remove these to have more control over the styling. Remove them with the `*`, `*::after` and `*::before` selector.

    ```css
    *, *::before, *::after {
      margin: 0;
      padding: 0;
    }
    ```

# Comments
- It is allowed to manipulate comments for use as visual dividers in your code.

    ```css
    /* ----------------------------------------
    Example divider
    ---------------------------------------- */
    main {
      width: 100%;
    }
    
    /* -------------------- Example divider -------------------- */
    main {
      width: 100%;
    }
    ```
