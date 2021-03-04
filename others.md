# 备注 Remarks

### API 返回的文档 URL 有效期 Validity period of the document URL returned by the API
15 分钟 15 minutes

### 使用 Iframe 加载 SDS Use Iframe to load SDS
为了解决 Iframe 不能 100% 定义高度，SDS 的 HTML 已经内置通过 [postMessage](https://developer.mozilla.org/en-US/docs/Web/API/Window/postMessage) 来返回高度，可以通过如下示例代码获取高度：

In order to solve the problem that Iframe cannot define the height 100%, the HTML of SDS has built-in [postMessage](https://developer.mozilla.org/en-US/docs/Web/API/Window/postMessage) to return the height, which can be passed as follows Sample code to get the height:

```javascript
// 高度通过一个对象返回 {xixisys:{height}} The height is returned by an object {xixisys:{height}}
window.addEventListener('message', function(e) {
    if (e.data.xixisys) {
        var height = e.data.xixisys.height;
        if (height) {
            // 定义高度 Define height
            document.querySelector('#iframe').height = height;
        }
    }
})
```