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
