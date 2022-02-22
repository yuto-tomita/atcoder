# 問題文
高橋君はデータの加工が行いたいです。

整数 a,b,cと、文字列 s が与えられます。 a+b+c の計算結果と、文字列 s を並べて表示しなさい。

# 制約
1≤a,b,c≤1,000
1≤∣s∣≤100

# 入力
入力は以下の形式で与えられる。

```
a
b c
s
```

# 出力
a+b+c と s を空白区切りで 1 行に出力せよ。

# 入力例 1 

```
1
2 3
test
```

# 出力例 1

```
6 test
```

1+2+3 は 6 なので、上記のように出力します。

# 入力例 2

```
72
128 256
myonmyon
```

# 出力例 2

```
456 myonmyon
```
72+128+256 は 456 なので、上記のように出力します。

# 回答

```js
const main = (input) => {
  const flatArg = input.split('\n')
  const splitBlank = flatArg[1].split(' ')
  const reducer = (accumulator, curr) => Number(accumulator) + Number(curr)
  
  const total = [...splitBlank, flatArg[0]].reduce(reducer)
 
  console.log(total + ' '  + flatArg[2])
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'));
```
