# 如何获取 SDS 文档

### HTTP 请求
`GET https://dlfrsthy47.execute-api.cn-north-1.amazonaws.com.cn/production/v1/sds/html`

### Query 参数

|参数|默认值|介绍|是否必须|
|---|-----|----|------|
|cas|无|CAS 号码|是|
|edition|ghs|SDS 版本类型`ghs/cn`|否|

### 返回
```js
// 请求成功返回 json 如下
{data: 'SDS 的 url'}
```

### 例子

```
// 请求获取 CAS 号「50-00-0」的「中文版」 SDS
https://..../v1/sds/html?cas=50-00-0&edition=cn

// 请求获取 CAS 号「1333-09-1」的「GHS 版」 SDS
https://..../v1/sds/html?cas=1333-09-1&edition=ghs
```

### 错误 Errors
|错误|状态码|error|
|----|----|------|
|CAS 是必须的|400|`cas is required`|
|CAS 找不到|404|`cas is not found`|
|其他错误|500|`server error`|
