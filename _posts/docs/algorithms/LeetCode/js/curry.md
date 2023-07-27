## 实现curry函数
curry函数是一个加工函数的函数，将任何一个函数(a)传入curry函数处理之后，会得到一个可以记住参数的函数(a1)，调用a1并传参，当参数数量不满足a的要求时，a1可以缓存这些参数并返回新的函数供链式调用，当传入的参数数量足够时则执行a并返回结果。具体示例代码如下：（PS：实际使用过程中a函数的参数数量不一定是3个，可以是任意多个。function.length属性可以获取一个函数的形参数量）

```js
function a(x, y, z){
  return x+y+z
}

const a1 = curry(a)
a1(1)(2)(3) //6
a1(1, 2)(3) //6
a1(1)(2, 3) //6
a1(1,2, 3) //6
```

```js
function curry (fn) {
  const arity = fn.length; // 函数需要的参数个数
  const arglist = [];
  return function pre (...arg){
    arglist.push(...arg);
    if (arglist.length === arity) { // 检查当前函数是否已满足需要
      return fn.apply(this, arglist);
    } else {
      return pre;
    }
  }
}
// 本题解题的关键在于提前保存fn的length（形参数量）、创建参数缓存列表（arglist）和function pre对自身的递归调用。
// 加分项是在执行fn时运用apply方法绑定this。
```