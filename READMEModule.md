# 我的项目计划

这是一个 **非常重要的** 项目，旨在*简化工作流程*。

## 今日任务

- [x] 创建项目仓库
- [ ] 编写核心模块
- [ ] 编写单元测试

## 核心功能列表

1.  **用户认证**
    *   登录/注册
    *   密码重置
2.  **数据管理**
    *   导入 CSV 文件
    *   生成可视化图表

## 代码示例

我们使用以下函数进行初始化：

```javascript
function init() {
    console.log("项目启动！");
}
```
JavaScript 中的 Promise 是一个构造函数，它包含了一系列用于处理异步操作的静态方法（直接通过类调用）和实例方法（通过 Promise 对象调用）。下面的表格清晰地展示了其核心方法：  

| 类型 | 方法名 | 作用描述 |  
------|------|------
| 构造函数|new Promise(executor) | 创建一个新的 Promise 对象。executor 函数接收 resolve 和 reject 两个参数。
| 静态方法|Promise.resolve(value) | 返回一个已兑现的 Promise 对象，其值即为给定的 value。
|      | Promise.reject(reason)	| 返回一个已拒绝的 Promise 对象，原因即为 reason。
|       | Promise.all(iterable)	| 接受一个 Promise 对象集合，并返回一个新的 Promise。只有集合中所有 Promise 都成功，它才会成功，返回值是所有结果的数组；一旦有一个失败，则立即失败，原因是第一个失败的 Promise 的原因。|  
|       | Promise.allSettled(iterable)	| 接受一个 Promise 对象集合。等到所有 Promise 都完成（无论成功或失败）后，它才成功完成，返回一个描述每个 Promise 结果的对象数组。|  
|       | Promise.race(iterable)|	接受一个 Promise 对象集合。返回的 Promise 会采用最先敲定（无论成功或失败）的那个 Promise 的状态和结果。|  
|       |  Promise.any(iterable)|	接受一个 Promise 对象集合。返回的 Promise 会采用最先成功的那个 Promise 的结果。只有当所有 Promise 都失败时，它才失败。|  
|实例方法 | 	.then(onFulfilled, onRejected)|	为 Promise 实例添加状态改变时的回调，并返回一个新的 Promise，支持链式调用。|  
|        | .catch(onRejected)	|是 .then(null, onRejected) 的语法糖，用于指定失败时的回调。|  
|        |  .finally(onFinally)|	无论成功还是失败，都会执行的回调，常用于执行清理操作。|  

类型 | 方法名 | 作用描述
------|------|------
构造函数 | new Promise(executor) | 创建一个新的 Promise 对象。executor 函数接收 resolve 和 reject 两个参数。
------|------|------
静态方法 | Promise.resolve(value)

