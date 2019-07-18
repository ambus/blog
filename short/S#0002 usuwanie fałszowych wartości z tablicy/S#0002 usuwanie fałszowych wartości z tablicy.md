# Short 0002

2019-07-10

## Usuwanie wartości negatywnych z tablicy

Czasami każdy z nas ma potrzebę usunięcia _negatywnych_ `false` wartości z tablicy. Można to wykonać w przy wykorzystaniu funkcji `filter` oraz `Boolean`.

```js
let a = [0, undefined, null, false, 1, 2];
a = a.filter(Boolean);
console.log(a); //[1, 2]
```

### Obiekt `Boolean`

Obiekt `Boolean` jest obiektem opak
owującym (ang.wrapper ) dla wartości logicznych.
Wartość przekazana jako pierwszy parametr jest w razie konieczności konwertowana do wartości logicznej. Jeśli wartość zostanie pominięta lub będzie równa 0, -0, null, false, NaN, będzie pustym łańcuchem znaków ("") lub będzie niezdefiniowana, obiekt przyjmie początkową wartość false. Dowolna inna wartość, włączając łańcuch znaków "false", spowoduje utworzenie obiektu z początkową wartością true.

Obiekt `Boolean` jest wraperem dla wartości logicznych `true/false`. Wartość przekazana w konstruktorze konwertowana jest na wartość logiczną.
Dla:

- 0
- -0
- null
- false
- NaN
- pusty ciąg znaków: ""
- niezdefiniowana wartość
  powoduje że obiekt przyjmuje jao początkową wartość `false`, w innych wypadkach jest to `true`.

Np.

```js
let a = "";
console.log(new Boolean(a)); //Boolean false {}

let b = "false";
console.log(new Boolean(b)); //Boolean true {}

let c = 0;
console.log(new Boolean(c)); //Boolean false {}
```

Nie można mylić wartości prostych `true` i `false` z obiektem Boolean. Obiekt Boolean przechowujący wartość false w przypadku warunków logicznych jest traktowany jako `true`.
Np.:

```js
let a = "";
console.log(new Boolean(a)); //Boolean false {}

if (new Boolean(a)) {
  // ta część kodu zostanie wykonana
}
```

Więcej info na [MDN](https://developer.mozilla.org/pl/docs/Web/JavaScript/Referencje/Obiekty/Boolean).

### Tagi
Boolean, boolean, javascript, array, filter
