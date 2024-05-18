# 接口描述

> 可以查询各个城市的天气状况，仅限国内

# 接口地址

请求方式：`GET`

返回格式：`JSON`

```API
https://api.nxvav.cn/api/weather/
```

# 请求示例

[https://api.nxvav.cn/api/weather/?city=北京](https://api.nxvav.cn/api/weather/?city=北京)

[https://api.nxvav.cn/api/weather/?city=香港](https://api.nxvav.cn/api/weather/?city=香港)

[https://api.nxvav.cn/api/weather/?city=深圳](https://api.nxvav.cn/api/weather/?city=深圳)

# 使用场景

<!-- tabs:start -->

#### **html**

```html
等待编辑...
```

<!-- tabs:end -->

# 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ------ | ---- | ---- | ---- |
| city | 必填 | 城市名字 | 城市名字，可使用拼音 |

# 返回参数

| 返回参数 | 说明 |
| ------ | ----- |
| code | 信息数据 |
| name | 城市名 |
| country | 国家 |
| path | 国家、所属省份、城市 |
| text | 天气现象文字 |
| code | 天气现象代码 |
| temperature | 温度，单位为c摄氏度 |

# 状态代码

| 返回状态 | 说明 |
| -------- | ---- |
| code | 状态码 |

# 返回示例

```json
{
    "code": 200,
    "location": {
        "name": "上海",
        "country": "CN",
        "path": "上海,上海,中国"
    },
    "now": {
        "text": "多云",
        "code": "4",
        "temperature": "26"
    },
    "last_update": "2023-06-21T01:00:07+08:00"
}
```
