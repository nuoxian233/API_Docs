# 接口地址

请求方式：`GET`

返回格式：`JSON`

```API
https://api.nxvav.cn/api/qun/
```

# 请求示例

[https://api.nxvav.cn/api/qun/?qun=445202136](https://api.nxvav.cn/api/qun/?qun=445202136)

[https://api.nxvav.cn/api/qun/?qun=445202136&type=301](https://api.nxvav.cn/api/qun/?qun=445202136&type=301)

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
| qun | 必填 | ?qun=QQ群号 | 想要生成的QQ群号 |

| 参数名 | 类型 | 示例 | 说明 |
| ------ | ----- | ---- | --- |
| type | 参数一(可空) | &type=请求参数 | 请求类型 |
| 301 | 可空 | &type=301 | 直接跳转 |

# 返回参数

| 返回参数 | 说明 |
| ------ | ---- |
| code | 状态码 |
| uid | 加入的群号 |
| idkey | 所请求到的加群密钥 |
| url | 加群的链接 |

# 状态代码

| 返回状态 | 说明 |
| ------- | ---- |
| 200 | 返回正常 |

# 返回示例

```json
{
    "code": 200,
    "data": {
        "uid": 445202136,
        "idkey": "26c53858a1e519013218e1e9e9e3cfe949bca461fca5400658fd8dc9e3b2fb72",
        "url": "http://wp.qq.com/wpa/qunwpa?idkey=26c53858a1e519013218e1e9e9e3cfe949bca461fca5400658fd8dc9e3b2fb72"
    }
}
```
