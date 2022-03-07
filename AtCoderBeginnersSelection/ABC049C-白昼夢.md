```js
function main(input) {
  input = input.split("\n")[0]
  console.log(/^(dream|dreamer|erase|eraser)*$/.test(input) ? 'YES' : 'NO')
}

main(require("fs").readFileSync("/dev/stdin", "utf8"))
```