# [ 每日·壹题 ] 题解

链接: https://muyiy.vip/question/


### [99. 编程算法题](https://muyiy.vip/question/#%E7%AC%AC-99-%E9%A2%98%EF%BC%9A%E7%BC%96%E7%A8%8B%E7%AE%97%E6%B3%95%E9%A2%98)
1. 递归版本
```js
function reverseInt(n) {
  if (!n) return '';

  let last = n % 10;
  let temp = parseInt(n / 10);
  return '' + (last ? last : '') + reverseInt(temp);
}

// reverseInt(1230) -> "321"
// reverseInt(1234) -> "4321"
```
2. 迭代版本
```js
function reverseInt(n) {
  let ans = '';

  let last;
  while (true) {
    [last, n] = [n % 10, parseInt(n / 10)];

    ans += last || '';

    if (!n) break;
  }

  return ans;
}
```
