### 介绍
Web Worker 工作线程，分类：
* 专用线程（Dedicated Web Worker）
* 共享线程（Shared Web Worker）

用途
[image:6E5503FF-EFC7-4D11-B6E5-04308FBC3998-21278-000135930F148392/4B887DE8-F143-484F-BD78-13D685DA91EB.png]

是游览器下的对象
```javascript
window.Worker

window.SharedWorker
```
Worker 和 SharedWorker 创建后，通过 port 端口监听和传递消息。

```javascript
// 创建 Worker，传递消息，监听消息，关闭
// 主线程
var worker = new Worker('xxx.js’, { type: ‘xxx’, name: ‘xxx’, credentials: ‘xxx’ })
worker.postMessage([10, 11])
worker.onmessage = (event) => {
console.log(event.data)
}

// Worker 线程
onmessage = (e) => {
if (e.data.length > 1) {
  postMessage(e.data[1] - e.data[0])
}
}


// 主线程
worker.terminate()

// Dedicated Worker 线程中
self.close()

// Shared Worker 线程中
self.port.close()
```