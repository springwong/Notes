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
