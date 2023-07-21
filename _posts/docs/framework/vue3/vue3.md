---
title: vue3基础
author: teen
date: 2023-08-10
category: framework
layout: post
---

# vue3

## 生命周期
![vue3-lifecycle](/assets/img/framework/vue3/lifecycle-vue3.png)

## 条件指令
| 指令 | 含义 |
|:---|:-----|
| v-if | |
| v-else | |
| v-else-if  | |
| v-show | |
| v-for | |
|v-on | 监听事件 ,简写 @ |


事件处理器的四种种方式 
- `内联事件处理器`：`@click="count++"`
- `方法事件处理器`：`@click="greet"`
- `内联处理器中调用方法`：`@click="say('hello')"`
- `在内联事件处理器中访问事件参数`：`@click="warn('Form cannot be submitted yet.', $event)"`

| @click 事件修饰符 | 含义 |
|:---|:-----|
| 事件修饰符| `.stop`、`.prevent`、`.self`、`.capture`、`.once`、`.passive` |
| 按键修饰符 |`.enter`、`.tab`、`.delete`、`.esc`、`.space`、`.up`、`.down`、`.left`、`.right`、`.ctrl`、`.alt`、`.shift`、`.meta`|
| 鼠标修饰符 |`.left`、`.right`、`.middle`、|
| 系统按键修饰符 |`.exact`|


## 响应式状态

**reactive()**


setup() 函数接收两个参数 props 和 context。
第一个参数 props，它是响应式的，当传入新的 prop 时，它将被更新。
第二个参数 context 是一个普通的 JavaScript 对象，它是一个上下文对象，暴露了其它可能在 setup 中有用的值。


## Composition API

Vue3 组合式 API（Composition API） 主要用于在大型组件中提高代码逻辑的可复用性。
在 setup 中，我们可以按逻辑关注点对部分代码进行分组，然后提取逻辑片段并与其他组件共享代码。因此，组合式 API（Composition API） 允许我们编写更有条理的代码。

Options API 和 Composition API 之间的映射

|Vue2 Options-based API |	Vue Composition API |
|:---|:-----|
| beforeCreate | setup() |
| created | setup() |
| beforeMount | onBeforeMount |
| mounted | onMounted |
| beforeUpdate | onBeforeUpdate |
| updated | onUpdated |
| beforeDestroy | onBeforeUnmount |
| destroyed | onUnmounted |
| errorCaptured | onErrorCaptured |

**ref**
作为模板使用的 ref 的行为与任何其他 ref 一样：它们是响应式的，可以传递到 (或从中返回) 复合函数中。

**侦听模板引用**
侦听模板引用的变更可以替代前面例子中演示使用的生命周期钩子。

但与生命周期钩子的一个关键区别是，watch() 和 watchEffect() 在 DOM 挂载或更新之前运行会有副作用，所以当侦听器运行时，模板引用还未被更新。