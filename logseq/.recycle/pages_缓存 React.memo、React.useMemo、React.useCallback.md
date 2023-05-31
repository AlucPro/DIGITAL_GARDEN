title:: 缓存 React.memo、React.useMemo、React.useCallback

-
### React.memo
用户函数式组件。
相当于 PureComponent。
当 props 不变的时候，组件不会重新渲染。
```javascript
// 逻辑
const MyComp = React.memo((props) => {
	return <>xxx</>
})
// 当 props 的浅比较不变的时候，MyComp 不会被重新渲染
// 场景：OutComp 重新渲染时，作为内部组件的 MyComp 也会被重新渲染。当 props 不变时，其实没必要重新渲染。 -> React.memo 性能优化
```
### React.useMemo
用于组件内部的方法结果的缓存。
当 xxx 不变的时候，foo 的结果也不变。不必重新 run 函数。
```javascript
const MyComp = React.memo((props) => {
	const foo = React.useMemo(() => {
{
	a: 'xx',
	b: xxx,
}
	}, [xxx])
	return <OtherComp data={foo()}>xxx</OtherComp>
})
```
### React.useCallback
对 function 的缓存。
当组件重新渲染的时候，内部 funcHandle 也会重新渲染。func 对象变了（指针）。所以用 useCallback 缓存（一般是纯函数）。
```javascript
const MyComp = React.memo((props) => {
	const foo = React.useCallback(() => {
{
	a: 'xx',
	b: xxx,
}
	}, [xxx])
	return <OtherComp fn={foo)}>xxx</OtherComp>
})
```
### 参考文献
[react Hook之useMemo、useCallback及memo](https://juejin.cn/post/6844903954539626510)