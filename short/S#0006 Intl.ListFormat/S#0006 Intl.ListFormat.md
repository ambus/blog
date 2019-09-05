# Short 0006

2019-09-05

## Intl.ListFormat

Konstruktor dla obiektu któru zapewnia formatowanie listy z uwzględnieniem wybranego jezyka.
Np. dla listy `['Frank', 'Szymon', 'Monika']` zwróci stinga w postaci `"Frank, Szymon i Monika"`
Unicode Common Locale Data [CLDR](http://cldr.unicode.org/translation/lists) zawiera informację jak w danym jezyku ma wyglądać formatowanie list. Dzięki Intl.ListFormat nie musimy sami implementować tego rozwiązania.

### Składnia

JavaScript:

```javascript
new Intl.ListFormat([locales[, options]])
```

Typescript:

```ts
new Intl.ListFormat([locales[, options]]) //brak wsparcia dla typów
```

- `locales` string z tagiem językowym [BCP 47](https://tools.ietf.org/html/bcp47) np: `pl-PL`
- `options` opcje
  - `localeMatcher` algorytm dopasowujący ustawienia regionalne. Możliwe opcje: `lookup`, `best fit`
  - `type` format wynikowej wiadomości - w jezyku polskim odpowiada on temu czy ma być łącznik `i` czy `lub`. Możliwe opcje: `conjunction`(domyślne), `disjunction`, `unit`.
  - `style` styl formatowania. Możliwe opcje: `long` (domyślne, wynik - `A, B i C`); `short`(wynik - `A, B, C`); `narrow` (wynik - `A B C`)

### Przykład

```js
const list = ["Monika", "Szymon", "Iga"];

console.log(
  new Intl.ListFormat("pl-PL", { style: "long", type: "conjunction" }).format(
    list
  )
);
// Monika, Szymon and Iga

console.log(
  new Intl.ListFormat("pl-PL", { style: "short", type: "disjunction" }).format(
    list
  )
);
// Monika, Szymon or Iga

console.log(
  new Intl.ListFormat("en-GB", { style: "narrow", type: "unit" }).format(list)
);
// Monika Szymon Iga
```

### Przeglądarki

Wsparcie tylko w Chrome 72+, Node 12+ oraz Opera 60+
[MDN compatibility table](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ListFormat#Browser_compatibility)

Więcej info na [V2 Docs](https://v8.dev/features/intl-listformat) [MDN Intl.ListFormat](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ListFormat)..

### Tagi

javascript, array, every
