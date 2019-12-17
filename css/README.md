<div align="center">
    <img src="http://icarusws.nl/js-content/resources/logo_geen_background.png" height="100px">
    <h1>Icarus CSS Styleguide</h1>
</div>

# Table of contents
- [Variables](#variables)
- [Indentation](#indentation)

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
