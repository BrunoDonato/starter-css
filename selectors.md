# Selectors

Conecta um elemento HTML com o CSS

## Tipos

* Global selector `*`
* Element/Type selector `h1, h2, p, div`
* ID Selector `#box, #container`
* Class Selector `.red, .m4`
* Attribute selector, Pseudo-class, Pseudo-element, e outros

```css
/* Global selector */
* {
    margin: 0;
}

/* Element/Type selector */
h1 {
    color: blue;
    font-size: 60px;
    background: gray;
}

/* ID Selector */
#container {
    width: 200px;
}

/* Class Selector */
.m-40 {
    margin: 40px;
}

/* Posso agrupar Seletores */
h1, h2 {
    color: blue;
    font-size: 60px;
    background: gray;
}
```