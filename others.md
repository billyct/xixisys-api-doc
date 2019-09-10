# 其他问题

### API 返回的文档 URL 有效期
15 分钟

### 使用 Iframe 加载 SDS
为了解决 Iframe 不能 100% 定义高度，SDS 的 HTML 已经内置通过 [postMessage](https://developer.mozilla.org/en-US/docs/Web/API/Window/postMessage) 来返回高度，可以通过如下示例代码获取高度：
```javascript
// 高度通过一个对象返回 {xixisys:{height}}
window.addEventListener('message', function(e) {
    if (e.data.xixisys) {
        var height = e.data.xixisys.height;
        if (height) {
            // 定义高度
            document.querySelector('#iframe').height = height;
        }
    }
})
```