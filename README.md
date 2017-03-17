## dateStyle and timeStyle option on Intl.DateTimeFormat API Specification [draft]

### Status

Current Stage:

 * 🚀 __Stage 0__

Spec Text:

 * https://rawgit.com/zbraniecki/proposal-ecma402-datetime-style/master/out/

### Authors

 * Zibi Braniecki  (@zbraniecki)

### Reviewers

 * ?

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
