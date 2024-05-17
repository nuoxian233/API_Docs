# 接口地址

请求方式 `GET`

返回格式 `TEXT` / `JSON`

```
https://api.nxvav.cn/api/yiyan/
```

# 请求示例

[https://api.nxvav.cn/api/yiyan/?encode=json&charset=utf-8](https://api.nxvav.cn/api/yiyan/?encode=json&charset=utf-8)

[https://api.nxvav.cn/api/yiyan/?encode=js&charset=gbk](https://api.nxvav.cn/api/yiyan/?encode=js&charset=gbk)

[https://api.nxvav.cn/api/yiyan/?encode=js1&charset=gbk](https://api.nxvav.cn/api/yiyan/?encode=js1&charset=gbk)

[https://api.nxvav.cn/api/yiyan/?encode=text&charset=utf-8](https://api.nxvav.cn/api/yiyan/?encode=text&charset=utf-8)

# 使用场景

<!-- tabs:start -->

#### **HTML**

```json
<!-- 获取仙言，建议放在<head>内 -->
<script type="text/javascript" src="https://api.nxvav.cn/api/yiyan/?encode=js1&charset=utf-8"></script>
<!-- 返回仙言信息 -->
<script>yiyan()</script>
```

<!-- tabs:end -->

# 请求参数

| 参数名  | 类型 | 示例      | 说明                  |
| ------- | ---- | --------- | --------------------- |
| charset | 参数一(可空) | 输出 gbk / utf-8 | 输出编码，默认为utf-8 |
| gbk | 可空 | 输出gbk格式，在json下无法显示 | |
| utf-8 | 可空 | 输出utf-8格式 |  |

| 参数名  | 类型 | 示例      | 说明                  |
| ------- | ---- | --------- | --------------------- |
| encode  | 参数二(可空) | 输出 js / json   | 输出的方式，默认json              |
| js  | 可空 | 输出js   |               |
| js1  | 可空 | 输出js1,旧样式   |               |
| json  | 可空 | 输出json   |              |
| text  | 可空 | 输出纯文本   |              |

# 返回参数

| 返回参数 | 说明     |
| -------- | -------- |
| id       | 一言标识   |
| yiyan  | 一言正文。编码方式 unicode。使用 utf-8。 |
| createTime  | 13位时间戳 |
| nick  | 发布者 |

# 状态代码

| 返回状态 | 说明 |
| ------- | ---- |
| 无      | 无    |

# 返回示例

```json
{
    "id": 101177,
    "yiyan": "你总盼着遇贵人，贵人不曾记得你，因为贵人多忘事。",
    "createTime": 1612054332000,
    "nick": "包子再咬两个没关系阿"
}
```