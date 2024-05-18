# 接口描述

> 查询网站的收录数量

# 接口地址

请求方式：`GET`

返回格式：`JSON`

```API
https://api.nxvav.cn/api/site/
```

# 请求示例

[https://api.nxvav.cn/api/site/?url=nxvav.cn](https://api.nxvav.cn/api/site/?url=nxvav.cn)

[https://api.nxvav.cn/api/site/?url=api.nxvav.cn](https://api.nxvav.cn/api/site/?url=api.nxvav.cn)

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

# 返回参数

| 返回参数 | 说明 |
| ------ | ---- |
| code | 状态码 |
| url | 查询的域名 |
| baidu | 百度收录的数量 |
| haoso | 360收录的数量 |
| sogou | 搜狗收录的数量 |

# 状态代码

| 返回状态 | 说明 |
| ------- | ---- |
| 200 | 返回正常 |

# 返回示例

```json
{
    "code": 200,
    "data": {
        "url": "nxvav.cn",
        "baidu": " 0",
        "haoso": "1",
        "sogou": "6"
    }
}
```
