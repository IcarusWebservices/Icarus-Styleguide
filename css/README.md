<div align="center">
    <img src="http://icarusws.nl/js-content/resources/logo_geen_background.png" height="100px">
    <h1>Icarus CSS Styleguide</h1>
</div>

# Table of contents
- [Variables](#variables)
- [Indentation](#indentation)
- [Syntax](#syntax)

# Variables
- The use of CSS variables is permitted and recommended.
- Always initialize CSS variables in a HTML tag to keep them in one place.
```css
/* ----- Bad ----- */
.container {
  --color-primary: red;
  color: var(--color-primary);
}

/* ----- Good ----- */
html {
  --color-primary: red;
}

.container {
  color: var(--color-primary);
}
```

# Indentation
- For readability, always use two spaces for indentation.
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
```css
*, *::before, *::after {
  margin: 0;
  padding: 0;
}
```

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
