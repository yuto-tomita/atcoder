```js
function main(input) {
  input = input.split("\n");
  let mochi = [];
 
  var n = parseInt(input[0], 10);
  for(var i = 1; i < n+1; i++) {
    mochi[i-1] = parseInt(input[i], 10);
  }
 
  const array2 = [...new Set(mochi)]
  console.log(array2.length)
}
 
Main(require("fs").readFileSync("/dev/stdin", "utf8"))
```