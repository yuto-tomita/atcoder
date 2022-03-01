# 回答1(間違い)
```js
const main = (input) => {
  const arg = input.split(' ').map(val => Number(val))
  const [a, b, c] = arg
  
  let sum = 0
  
  for (let i = 1; i < a; i++) {
    const numberDigit = String(i).length
    
    if (b <= i && i <= c) {
      sum = sum + i
    }
    
    if (numberDigit > 1) {
      const total = [...String(i)].reduce((sum, element) => {
        return Number(sum) + Number(element)
      }, 0);
      
      if (b <= total && total <= c) {
        sum = sum + i
      }
    }
  }
  
  sum = sum + a
  console.log(sum)
}
```

# 回答2(AC)
```js
const main = (input) => {
  const [a, b, c] = input.split(' ').map(val => Number(val))
  
  let sum = 0
  
  for (let i = 1; i <= a; i++) {
    const total = [...String(i)].reduce((s, v) => {
      return Number(s) + Number(v)
    }, 0);

    if (b <= total && total <= c) {
      sum += i
    }
  }
  console.log(sum)
}


main(require('fs').readFileSync('/dev/stdin', 'utf8'));
```