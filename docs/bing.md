# 接口地址

请求方式：`GET`

返回格式：`JPG` / `JSON`

```API
https://api.nxvav.cn/api/bing/
```

# 请求示例

[https://api.nxvav.cn/api/bing/?encode=json](https://api.nxvav.cn/api/bing/?encode=json)

[https://api.nxvav.cn/api/bing/](https://api.nxvav.cn/api/bing/)

# 使用场景

<!-- tabs:start -->

#### **html**

```html
<img src="https://api.nxvav.cn/api/bing" />
```

<!-- tabs:end -->

# 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ----- | ---- | ---- | ---- |
| encode | 可空 | json | 输出格式,默认直链 |

# 返回参数

| 返回参数 | 说明 |
| ------- | ---- |
| code | 状态码 |
| startdate | 壁纸模糊开始日期 |
| fullstartdate | 壁纸具体开始日期 |
| enddate | 壁纸结束日期 |
| title | 壁纸标题 |
| url | 壁纸直链 |
| copyright | 壁纸版权 |

# 状态代码

| 返回状态 | 说明 |
| ------- | ----- |
| 200 | 正常 |

# 返回示例

```json
{
    "code": 200,
    "startdate": "20220924",
    "fullstartdate": "202209241600",
    "enddate": "20220925",
    "title": "匆匆而逝的河流",
    "url": "https://cn.bing.com/th?id=OHR.AmazonMangroves_ZH-CN2154443859_1920x1080.jpg&rf=LaDigue_1920x1080.jpg&pid=hp",
    "copyright": "亚马逊河鸟瞰图，巴西 (© Curioso.Photography/Shutterstock)"
}
```
