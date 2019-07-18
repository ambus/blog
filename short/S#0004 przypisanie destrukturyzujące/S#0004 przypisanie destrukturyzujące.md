# Short 0004
2019-07-18

## Przypisanie destrukturyzujące - _Destructuring Aliases_

> Składnia przypisania destrukturyzującego jest wyrażeniem w JavaScript, które pozwala na wyciągnięcie danych z tablic bądź obiektów do odrębnych zmiennych.

```js
var x = [1, 2, 3, 4, 5];
var [y, z] = x;
console.log(y); // 1
console.log(z); // 2
```

#### Zmiennej możemy przypisać także domyślne wartości:

```js
let x, y;
[x = 2, y = 3] = [1];
console.log(x); // 2
console.log(y); // 3
```

#### Zamiana miejscami:

```js
let x = 2;
let y = 3;
[x, y] = [y, x];
console.log(x); // 3
console.log(y); // 2
```

#### Przypisanie reszty tablicy do zmiennej:

```js
let [x, ...y] = [1,2,3];
console.log(x); // 1
console.log(y); // [2,3]
```

Więcej info na [MDN Przypisanie destrukturyzujące](https://developer.mozilla.org/pl/docs/Web/JavaScript/Referencje/Operatory/Destructuring_assignment).

### Tagi
javascript, array, destructuring aliases, 
