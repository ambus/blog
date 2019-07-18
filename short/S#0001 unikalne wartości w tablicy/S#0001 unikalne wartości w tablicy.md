# Short 0001 
2019-07-10

## Unikalne wartości w tablicy
W jaki sposób uzyskać unikalne wartości w tablicy? Najprościej jest wykorzystać w tym celu obiektu `Set`.

``` js
var j = [...new Set([1, 2, 3, 3])]
console.log(j) // [1, 2, 3]
```

### Obiekt `Set`
>Obiekt `Set` umożliwia przechowywanie unikalnych wartości każdego typu, zarówno prymitywów jak i obiektów.

Składnia `Set`:
```javascript
new Set([iterable]);
```

Więcej info na [MDN](https://developer.mozilla.org/pl/docs/Web/JavaScript/Referencje/Obiekty/Set).

### Tagi
set, javascript, array
