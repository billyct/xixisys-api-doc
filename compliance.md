# 如何获取合规文档

### HTTP 请求
`GET https://dlfrsthy47.execute-api.cn-north-1.amazonaws.com.cn/production/v1/compliance/html`

### Query 参数

|参数|默认值|介绍|是否必须|
|---|-----|----|------|
|cas|无|CAS 号码|是|

### 返回
```js
// 请求成功返回 json 如下
{data: '合规文档 的 url'}
```

### 例子

```
// 请求获取 CAS 号「50-00-0」的合规文档
https://..../v1/compliance/html?cas=50-00-0

```

### 错误 Errors
|错误|状态码|error|
|----|----|------|
|CAS 是必须的|400|`cas is required`|
|CAS 找不到|404|`cas is not found`|
|其他错误|500|`server error`|
