# curl 例子 Example

##### 通过 curl 获取 CAS编号为「50-00-0」的「GHS 版本」 SDS 文档 Use curl to obtain the SDS document of the 「GHS type」 with the CAS number 「50-00-0」
```
curl "https://dlfrsthy47.execute-api.cn-north-1.amazonaws.com.cn/production/v1/sds/html?cas=50-00-0" \
  -H "Content-Type: application/json" \
  -H "X-Api-Key: ..."
```
