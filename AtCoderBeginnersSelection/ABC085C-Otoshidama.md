```js
function main(input) {
  const arg = input.split(' ').map(val => Number(val))
  let tenThousand = -1
  let fiveThousand = -1
  let oneThousand = -1
  
  let flag = false
  
  for(let a = 0; a <= arg[0]; a++) {
    for (let b = 0; b + a <= arg[0]; b++) {
      const c = arg[0] - a - b
      const total = a * 10000 + b * 5000 + c * 1000
      
      if (total === arg[1]) {
        tenThousand = a
        fiveThousand = b
        oneThousand = c
      }
    }
  }
  console.log(`${tenThousand} ${fiveThousand} ${oneThousand}`)
}

main(require("fs").readFileSync("/dev/stdin", "utf8"))
```