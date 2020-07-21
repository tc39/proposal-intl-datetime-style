## dateStyle and timeStyle option on Intl.DateTimeFormat API Specification [draft]

This proposal adds two options to `Intl.DateTimeFormat`: `dateStyle` and `timeStyle`. These options give a compact way to request the appropriate, locale-specific way to ask for a date and time of given lengths.

### Status

Current Stage:

 * __Stage 4__

Spec Text:

 * https://tc39.github.io/proposal-intl-datetime-style/

### Authors

 * Zibi Braniecki  (@zbraniecki)

### Reviewers

 * Frank Tang (@FrankYFTang)
 * Nathan Hammond (@nathanhammond)

### Informative

This proposal is based on the CLDR Date/Time Patterns:

 * http://cldr.unicode.org/translation/date-time-patterns#TOC-Basic-Time-Formats
 * http://cldr.unicode.org/translation/date-time-patterns#TOC-Basic-Date-Formats
 * http://unicode.org/reports/tr35/tr35-dates.html

### Usage

```javascript
let o = new Intl.DateTimeFormat("en" , {
  timeStyle: "short"
});
console.log(o.format(Date.now())); // "13:31"

let o = new Intl.DateTimeFormat("en" , {
  dateStyle: "short"
});
console.log(o.format(Date.now())); // "21.03.2012"

let o = new Intl.DateTimeFormat("en" , {
  timeStyle: "medium",
  dateStyle: "short"
});
console.log(o.format(Date.now())); // "21.03.2012, 13:31"
```


### Render Spec

```bash
npm install
npm run build
open index.html
```

### Backpointers

 * https://github.com/tc39/ecma402/issues/108
