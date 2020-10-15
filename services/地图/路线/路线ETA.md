## 接口描述
请求路径：`https://mapapi-routes.apigw-gz.didiyunapi.com/api/v1/routeeta`

请求方法：GET
## 输入参数
|参数名称 | 必选 | 默认值 | 描述|
|--------|-----|-----|-----|
|route| 是 | 无 |路线坐标点串：lng,lat&#124;lng,lat&#124;…。经纬度小数点后建议不超过6位。至少输入3个点；|

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
curl -X GET \
  'https://mapapi-routes.apigw-gz.didiyunapi.com/api/v1/routeeta?route=116.358529,39.954762|116.359591,39.954343|116.360804,39.954408'
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
