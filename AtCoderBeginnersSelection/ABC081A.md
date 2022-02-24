```js
const main = (input) => {
  const insertArgIntoArray = [...input]
  const filterOnlyOne = insertArgIntoArray.filter(val => val === '1')

  console.log(filterOnlyOne.length)
 }

main(require('fs').readFileSync('/dev/stdin', 'utf8'));
```