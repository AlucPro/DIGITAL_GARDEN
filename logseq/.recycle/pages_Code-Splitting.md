-
### 在构建时分割代码块 Bundling

构建工具的作用，把 import 集中到一个 file，再被引用。但是这样随着项目的进展，file 会变得很大。
所以可以*通过构建工具*，在 bundling 时进行切割，按需引用。
App

```javascript
// app.js
import { add } from "./math.js";
console.log(add(a, b));
```

```javascript
//math.js
export function add(a, b) {
// do sth
}
```

Bundle

```javascript
function add() {
// do sth
}

console.log(add(a, b));
```
- ### dynamic import()
  ![CE314878-3848-4185-832F-4F6BB1949FCD.png](../assets/CE314878-3848-4185-832F-4F6BB1949FCD_1650801341039_0.png){:height 694, :width 778}
- ### React.lazy
  ![5C8073F5-B930-45A2-904A-02FE2A69F85F.png](../assets/5C8073F5-B930-45A2-904A-02FE2A69F85F_1650801348721_0.png) 
  
  应用场景:
- 一开始不需要展示的组件（非首屏加载的组件）
	- 弹层性质组件
	- 一开始被隐藏的组件
- 异常捕获边界
- 基于路由的代码分割
  ![D9B24302-5DC7-412B-8DF3-89ECE8B6AB8E.png](../assets/D9B24302-5DC7-412B-8DF3-89ECE8B6AB8E_1650801356714_0.png)
  ![4DF0E340-C1BE-4F71-9B54-7721BF42583D.png](../assets/4DF0E340-C1BE-4F71-9B54-7721BF42583D_1650801361718_0.png)
### 参考文献

https://reactjs.org/docs/code-splitting.html
[基于 React.Suspense 和 React.lazy 的前端性能优化 - 前端](https://juejin.im/entry/6844903809232158734)