# 接口地址

请求方式：`GET`

返回格式：`JSON`、`PNG`

```API
https://api.nxvav.cn/api/web/
```

# 请求示例

[https://api.nxvav.cn/api/web/?url=baidu.com](https://api.nxvav.cn/api/web/?url=baidu.com)

[https://api.nxvav.cn/api/web/?url=baidu.com&type=json](https://api.nxvav.cn/api/web/?url=baidu.com&type=json)

# 使用场景

<!-- tabs:start -->

#### **html**

```html
等待编辑...
```

<!-- tabs:end -->

# 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ------ | ----- | ---- | --- |
| url | 必填 | 网站域名不加http(s) | 网站域名 |

| 参数名 | 类型 | 示例 | 说明 |
| ------ | ----- | ---- | --- |
| type | 参数一(可空) | &type=请求参数 | 请求类型 |
| json | 可空 | &type=json | 输出为百度pc，m，搜狗，谷歌 |
| baidupc | 可空 | &type=baidupc | 输出百度PC权重的图片 |
| baidum | 可空 | &type=baidupc | 输出百度m权重的图片 |
| sougou | 可空 | &type=sougou | 输出搜狗权重的图片 |
| google | 可空 | &type=google | 输出谷歌权重的图片 |

# 返回参数

| 返回参数 | 说明 |
| ------ | ---- |
| code | 状态码 |
| host | 查询的域名 |
| baidupc | 百度pc的权重 |
| baidum | 百度m的权重 |
| sougou | 搜狗的权重 |
| google | 谷歌的权重 |

# 状态代码

| 返回状态 | 说明 |
| ------- | ---- |
| 200 | 返回正常 |

# 返回示例

```json
{
    "code": 200,
    "host": "baidu.com",
    "data": {
        "baidupc": "10",
        "baidum": "10",
        "sougou": "10",
        "google": "10"
    }
}
```
