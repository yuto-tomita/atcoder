```js
const main = (input) => {
  const main = (input) => {
  const flatArg = input.split('\n').map(val => Number(val))
  const expectNumber = flatArg[3]

  const fiveHundredYens = [...Array(flatArg[0] + 1)].map((_) => 500)
  const oneHundredYens = [...Array(flatArg[1] + 1)].map((_) => 100)
  const fiftyYens = [...Array(flatArg[2] + 1)].map((_) => 50)
  let counta = 0
  
  fiveHundredYens.forEach((five, a) => {
    oneHundredYens.forEach((one, b) => {
     fiftyYens.forEach((fifty, c) => {
       if ((five * a) + (one * b) + (fifty * c) === expectNumber) {
         counta++
       }
     })
    })
  })
  
  console.log(counta)
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'));
}
```

// TODO: より良いコードを他の回答者のコードを参考に考える