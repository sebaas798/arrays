# Quita los extraños — filtrar arrays en JavaScript

Ejercicio de JAP sobre métodos de arrays.

## El problema

En `script.js` hay un array "extraño" que mezcla de todo: textos, números, `null`, `undefined`, objetos, arrays y funciones. Hay que mostrar en la página **solo los textos, ordenados alfabéticamente**, dentro de la lista `#list`.

## La solución

```js
strangeArray
  .filter(item => typeof item === "string") // me quedo solo con los strings
  .map(item => item.toUpperCase())          // los paso a mayúsculas
  .sort();                                  // y los ordeno
```

La función `showList()` recorre el resultado y crea un `<li>` por cada elemento. Pasarlos a mayúsculas antes de ordenar hace que el orden no dependa de mayúsculas y minúsculas.

## Cómo probarlo

Abrí `index.html` en el navegador.

## Tecnología

- HTML y JavaScript vanilla (`filter`, `map`, `sort`, manipulación del DOM)
