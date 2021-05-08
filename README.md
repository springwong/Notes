# Notes

## Mobile Native

## React

## Node.js

### Debugging

https://nodejs.org/en/docs/guides/debugging-getting-started/

```
// simple one, listen on 127.0.0.1:9229
node --inspect index.js

// Break before code starts
node --inspect-brk index.js

// listen on other ports
node --inspect=[host:port] index.js

// Chrome inspector, in chrome url, open:
chrome://inspect

// Visual Studio Code, start debug mode
Terminal > DropDown > 'Create Javascript Debug Terminal'
```

## CSS

### CSS Preprocessor
PostCSS
https://postcss.org/

Sass
https://sass-lang.com/

Stylus
https://stylus-lang.com/

Less
https://lesscss.org/

### Box Model
![](./assets/box-model.png)

### Flex Box
Single  Columns/rows
```
.flex {
    display: flex;
    justify-content: center;
    align-items: center;
}
```

### Grid
multiple columns/rows
```
.grid {
    display: grid;
    grid-template-columns: 1fr 500px 1fr;
    grid-template-rows: 100px 200px;
    place-items: center;
}
```

### Responsive Layout
Simple way
```
.size {
    width: 50%;
}

@media only screen and (max-width:600px) {
    .size {
        width: 200px;
    }
}

@media only screen and (min-width: 1200px) {
    .size {
        width: 800px;
    }
}
```

Advance way:
```
.size {
    width: clamp(200px, 50%, 600px);
}
```

### Ratio
```
.ratio {
    width: 100%;
    aspect-ratio: 16/9;
}
```

### CSS Variables
```
// :root is global scope of variables. To use local scope, declare it inside the selector.
:root {
    --text-color: rgb(255, 0, 0);
    --r: 128;
    --g: 0;
    --b: 0;
    --another-color: rgb(var(--r), var(--g), var(--b));
}

p {
    color: var(--text-color);
}

// override text-color in local scope
h1 {
    --text-color: rgb(0, 0, 0);
    color: var(--text-color);
}

h2 {
    color: var(--another-color);
}
```

### calculation values
```
width: calc(100vm - 80px);
font-size: calc(1rem * 1.25);
padding: calc(5% + 2px);

// calc X variables to achieve smooth delay
.order {
    animation-delay: calc(var(--order) * 100ms);
}
<i class="drop" style="--order: 1">1</i>
<i class="drop" style="--order: 2">2</i>
<i class="drop" style="--order: 3">3</i>
```

### CSS Counter (State)
```
:root {
    counter-reset: headings;
}

h1 {
    counter-increment: headings;
}

h1::before {
    content: counter(headings);
}
```

### Focus control
```
button:foucs-within .dropdown {
    opacity: 1;
    visibility: visible;
}
```

### CSS Units
```
// Fixed units
h1 {
    font-size: 14px;
}

// Relative units, em / rem
// em relative to parent's font size
// if parent font size is 12px, 2em = 12px * 2 = 24px
// rem relaive to root font size
h1 {
    font-size: 1em;
    padding: 1rem;
}

// character width, ch, definition of character here is width of "0"
// in this example, width is from minimum 45 characters to 75 characters
.card {
    width: clamp(45ch, 50%, 75ch);
}

// relative to viewport, vw / vh, unit is x% of viewport width / height
// vmin / vmax is relative to 1% of viewport's smaller / larger dimension
h1 {
    font-size: 20vw;
}

```

### CSS color format
1. rgb
rgb(255, 0, 0)

2. hsl
hsl(0, 35%, 50%)

### Scroll
```
article {
    scroll-padding: 1rem 0 0 0;
}
```

### Future
content-visibility
https://developer.mozilla.org/en-US/docs/Web/CSS/content-visibility

### Performance
1. multiple css for media
```
<!-- style.css contains only the minimal styles needed for the page rendering -->
<link rel="stylesheet" href="styles.css" media="all" />
<!-- Following stylesheets have only the styles necessary for the form factor -->
<link rel="stylesheet" href="sm.css" media="(min-width: 20em)" /><link rel="stylesheet" href="md.css" media="(min-width: 64em)" /><link rel="stylesheet" href="lg.css" media="(min-width: 90em)" /><link rel="stylesheet" href="ex.css" media="(min-width: 120em)" /><link rel="stylesheet" href="print.css" media="print" />
```

2. Parallel / in-series call on css files

## Useful tools

### Diagram
https://sequencediagram.org/
https://www.gliffy.com/

### Online Complier
#### JS
https://jsbin.com/?html

#### Website Scanning
https://www.ssllabs.com/ssltest/

### UIUX Prototype
https://app.zeplin.io/projects

https://overflow.io/

https://www.invisionapp.com/

### Data Model
https://app.quicktype.io/
