```js
const main = (input) => {
  const cards = input.split('\n')[1].split(' ').map(n => Number(n));
  let aliceCardPoints = 0
  let bobCardPoints = 0
  
  const sort = cards.sort((a, b) => b - a)
  
  sort.forEach((val, index) => {
  	if (index % 2 === 0) {
	  aliceCardPoints += val
    } else {
      bobCardPoints += val
    }
  })
  
  console.log(aliceCardPoints - bobCardPoints)
}


main(require('fs').readFileSync('/dev/stdin', 'utf8'));
```