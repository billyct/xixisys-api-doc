# 如何获取 SDS 文档 How to get a SDS

### HTTP 请求 HTTP Request
`GET https://dlfrsthy47.execute-api.cn-north-1.amazonaws.com.cn/production/v1/sds/html`

### 请求参数 Query parameters

|参数 parameter|默认值 default value|介绍 Description|是否必须 Required|
|---|-----|----|------|
|cas|无 none|CAS|是 Yes|
|edition|ghs|SDS 版本类型 SDS Type `ghs/cn`|否 No|

### 返回 Return
```js
// 请求成功返回 json 如下 The request successfully returns JSON as follows
{data: 'SDS url'}
```

### 例子 Example

```
// 请求获取 CAS 号「50-00-0」的「中文版」 SDS. Request to obtain the "China type" SDS of the CAS number "50-00-0"
https://..../v1/sds/html?cas=50-00-0&edition=cn

// 请求获取 CAS 号「1333-09-1」的「GHS 版」 SDS. Request to obtain the "GHS type" SDS of the CAS number "1333-09-1".
https://..../v1/sds/html?cas=1333-09-1&edition=ghs
```

### 错误 Errors
|错误 Error|状态码 Code|错误信息 Error message |
|----|----|------|
|CAS 是必须的|400|`cas is required`|
|CAS 找不到|404|`cas is not found`|
|其他错误|500|`server error`|
