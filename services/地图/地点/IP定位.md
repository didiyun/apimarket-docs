## 接口描述
请求路径：https://mapapi-places.apigw-gz.didiyunapi.com/api/v1/place/ip

请求方法：GET
## 输入参数


| 参数名称       | 必填 | 默认值 | 说明ip                                                  |
| -------------- | ---- | ----- | ------------------------------------------------------------ |
| ip | 是   | 无 | 滴滴poi id |

## 输出参数
|参数名称  | 类型 | 描述|
|--------|-----|-----|
|status | int  |状态码 |
|info|string|状态说明	|
|result | [Result](#Result)|请求返回数据 |

<span id="Result"></span>
Result：

|参数名称  | 类型 | 描述 |
|--------|-----|-----|
|province | string |省份名称|
|city | string |城市名称|

## 错误码
[错误码：](/static/apimarket-docs/services/地图/错误码.md#errorCode)

## 示例

请求：
``` shell
curl -X GET \
  'https://mapapi-places.apigw-gz.didiyunapi.com/api/v1/place/ip?ip=114.247.88.20'\
  --header 'Authorization: AppCode XXX'
```

输出：
``` json
{
    "status":0,
    "info":"OK",
    "result":{
        "city":"北京市",
        "province":"北京市"
    }
}
```
