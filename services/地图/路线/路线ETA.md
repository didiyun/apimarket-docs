## 接口描述
请求路径：`https://mapapi-routes.apigw-gz.didiyunapi.com/api/v1/eta/route`

请求方法：GET Content-Type=application/json
## 输入参数
|参数名称 | 类型 | 必选 | 默认值 | 描述|
|--------|-----|-----|-----|-----|
|route | array<[Route](#Route)> | 是 | 无 |路线坐标点串，至少输入3个点，最多支持2000个点；|

<span id="Route"></span>
Route:

|参数名称  | 类型 | 必选| 默认值 |  描述 |
|--------|-----|-----|-----|-----|
|longitude  | float  |是 | 无 |经度，建议小数点不超过6位 |
|latitude   | float  |是 | 无 |纬度，建议小数点不超过6位 |

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
|distance   | int  |距离，单位：米 |
|duration   | int  |时间，单位：秒 |

## 错误码
[错误码](/static/apimarket-docs/services/地图开放平台/错误码.md#errorCode)

## 示例

请求：
``` shell
curl -X GET 'https://mapapi-routes.apigw-gz.didiyunapi.com/api/v1/eta/route' \
  --header 'Authorization: AppCode XXX' \
  --header 'Content-Type: application/json' \
  --data '{
    "route":[
        {
            "longitude":116.24664,
            "latitude":40.07198
        },
        {
            "longitude":116.24618,
            "latitude":40.07291
        },
        {
            "longitude":116.24673,
            "latitude":40.07181
        },
        {
            "longitude":116.24664,
            "latitude":40.07198
        }
    ]
}'
```
输出：
``` json
{
    "status": 0,
    "info": "OK",
    "result": {
        "distance": 237,
        "duration": 106
    }
}
```
