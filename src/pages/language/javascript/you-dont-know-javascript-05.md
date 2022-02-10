---
title: 《你知道的JavaScript（上卷）》05 语法 - 读书笔记
date: 2020-11-25
cover: https://xinghe-blog-bucket.oss-cn-beijing.aliyuncs.com/img/you-dont-know-javascript.jpg
---

<route lang="yaml">
meta:
  layout: empty
</route>

[[toc]]

# 05 语法

## 语法

### 语句和表达式

#### 表达式的副作用

**=**

``` js
if (str && (matches = str.match( /[aeiou]/g ))) {
    return matches;
}
```

**++**

``` js
var a = 3
var b = a++
var c = (a++, a)
a // 5
b // 3
c // 5
```

**delete**

``` js
function deleteProperty (obj, propertyName) {
    // true or false
    return delete obj[propertyName]
}
```

特殊情况 

``` js
[] + {} // "[object Object]" 可以理解为 '' + {} {} 被理解成空对象是一个值
{} + [] // 0 可以理解为 {} 是一个空代码块不执行任何操作，而+[] 是对[]的强制类型转换
```

else if 不是 JavaScript 内置语法，只是我们利用了简便写法

``` js
if (true) { console.log('x')}
if (true) console.log()

if (a) {
    doSomething(a)
} else {
    if (b) {
        doSomething(b)
    }
    else {
        doNothing()
    }
}

if (a) doSomething(a)
else if (b) doSomething(b)
     else doNothing()
```

try finally 

``` js
function foo() {
  try {
    return 42;
  }
  finally {
    console.log( "Hello" );
  }

  console.log( "never runs" );
}

console.log( foo() );
// Hello
// 42
```

::: info
- finally 的代码会始终执行，
- 如果 finally 中抛出异常 try 的返回值会被抛弃
- finally 中的返回值会覆盖 try 中的返回值
:::


#### 上下文规则


### 运算符优先级

#### 短路

#### 更强的绑定

#### 关联


### 自动分号


### 错误

提前使用变量

### 函数参数


### try..finally


### switch