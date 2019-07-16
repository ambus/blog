# Short 0003

2019-07-10

## Konwertowanie wartości w tablicy na tym string, number lub boolean

Aby przekonwertować wartości z tablicy na typ _string_, _number_ lub _boolean_, należy wykorzystać właściwości funkcji `Array.prototype.map()` oraz obiektów opakowujących (ang. wrapper).

Konwersja na typ _string_:
```js
let a = ["2", "3", "4", 5, true, false, 0, -1, {}, undefined];
a = a.map(String);
console.log(a); //'2', '3', '4', '5', 'true', 'false', '0', '-1', '[object Object]', 'undefined'
```

Konwersja na typ _number_:
```js
let a = ["2", "3", "4", 5, true, false, 0, -1, {}, undefined];
a = a.map(Number);
console.log(a); //[ 2, 3, 4, 5, 1, 0, 0, -1, NaN, NaN ]
```
Uwaga! Wartość `true` jest zmieniana na liczbę `1`.
W przypadku danych które nie mogą zostać zmienione w liczbę zwracana jest wartość NaN.


Konwersja na wartość logiczną `true/false`:
```js
let a = ["2", "3", "4", 5, true, false, 0, -1, {}, undefined];
a = a.map(Boolean);
console.log(a); //[ true, true, true, true, true, false, false, true, true, false ]
```

Więcej info na [MDN Map](https://developer.mozilla.org/pl/docs/Web/JavaScript/Referencje/Obiekty/Array/map).
Więcej info na [MDN Boolean](https://developer.mozilla.org/pl/docs/Web/JavaScript/Referencje/Obiekty/Boolean).
