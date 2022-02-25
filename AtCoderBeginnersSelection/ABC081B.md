```js
const main = (input) => {
  const flatArg = input.split('\n')
  let blackBordNumbers = flatArg[1].split(' ').map(val => Number(val))
  
  let total = 0
  
  const isAllEven = (blackBordNumbers) => {
    return blackBordNumbers.every(val => val % 2 === 0)
  }
  
  while (isAllEven(blackBordNumbers)) {
    total++
    blackBordNumbers = blackBordNumbers.map(val => val / 2)
  }
  
  console.log(total)
}


main(require('fs').readFileSync('/dev/stdin', 'utf8'));
```