# Short 0005

2019-07-19

## Array.prototype.every()

Metoda dodana w ECMAScript 5. Sprawdza czy wszystkie elementy tablicy przechodzą test.
Wywołuje przekazaną funkcę `callback` do momentu aż któryś z elementów tablic nie przejdzie testu - `callback` zwróci `false`.
W momencie otrzymania wartości `false` z `callback` przerywane jest wywoływanie testu dla kolejnych elementów tablicy i zwracana wartość `false` dla całego testu. W przypadku gdy wszystkie elementy tablicy przedją test funkcja `every` zwróci `true`.

### Składnia

JavaScript:

```javascript
arr.every(callback[, thisArg])
```

Typescript:

```ts
Array<T>.every(callbackFn: (element: T, index: number, array: T[] ) => unknown,  thisObject?: any): boolean
```

- `callback` funkcja wykonująca test dla każdego elementu tablicy. Przyjmuje trzy argumenty:
  - `element` bieżący element tablicy
  - `index` index bieżącego elementu
  - `array` tablica na której została wywołana funkcja
- `thisObject` parametr nie wymagany, obiekt na który będzie wskazywał `this` podczas wykonywania funkcji `callback`

### Przykład

```js
function isTooYoung(element, index, array) {
  return element > 18;
}
let canTheyBuyBeer = [20, 26, 12, 13, 44, 53].every(isTooYoung);
console.log(canTheyBuyBeer); //false

let secondtry = [20, 26, 44, 53].every(isTooYoung);
console.log(secondtry); //true
```

Przykład z funkcją strzałkową

```js
let canTheyBuyBeer = [20, 26, 12, 13, 44, 53].every(element => element > 18);
console.log(canTheyBuyBeer); //false

let secondtry = [20, 26, 44, 53].every(element => element > 18);
console.log(secondtry); //true
```

### Przeglądarki

Metoda `every` w
spierana jest przez wszystkie nowoczesne przeglądarki
[ECMAScript 5 compatibility table](http://kangax.github.io/compat-table/es5/#test-Array_methods)



Więcej info na [MDN Array.prototype.every()](https://developer.mozilla.org/pl/docs/Web/JavaScript/Referencje/Obiekty/Array/every).

### Tagi

javascript, array, every
