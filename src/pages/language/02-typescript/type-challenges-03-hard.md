---
title: TypeScript 类型挑战 (三) Hard
index: Language.TypeScript.Practice
---

[[toc]]
  
- 项目地址 [Github](https://github.com/type-challenges/type-challenges)
- 项目描述: 高质量的类型可以帮助提高项目的可维护性，同时避免潜在的错误。


## Simple Vue

`#this`, `#application`, `#vue`

实现 TS 内置的 `ReturnType<T>`，但不可以使用它。

实现类似Vue的类型支持的简化版本。

``` ts
const instance = SimpleVue({
  data() {
    return {
      firstname: 'Type',
      lastname: 'Challenges',
      amount: 10,
    }
  },
  computed: {
    fullname() {
      return this.firstname + ' ' + this.lastname
    }
  },
  methods: {
    hi() {
      alert(this.fullname.toLowerCase())
    }
  }
})
```

答案

``` ts
type Maped<T extends object> = {
  [J in keyof T]: T[J] extends (args: any[])=>infer R ? R : T[J]
}

type T<
    S extends object,
    C extends object,
    M extends object
> = {
    data(this: void): S,
    computed: C & ThisType<S>,
    methods: M & ThisType<S & M & Maped<C>>
} 

declare function SimpleVue<
  S extends object,
  C extends object,
  M extends object
>(options:T<S, C, M>): unknown

``` 

## 柯里化 1

Currying 是一种将带有多个参数的函数转换为每个带有一个参数的函数序列的技术。
传递给 Currying 的函数可能有多个参数，您需要正确键入它。
在此挑战中，curried 函数一次仅接受一个参数。分配完所有参数后，它应返回其结果。

``` ts
const add = (a: number, b: number) => a + b
const three = add(1, 2)

const curriedAdd = Currying(add)
const five = curriedAdd(2)(3)
```

答案

``` ts
declare function Currying(fn: any): any
```