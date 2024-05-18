# 接口描述

> 获取蓝奏网盘的直链下载地址

# 接口地址

请求方式：`GET`

返回格式：`JSON`

```API
https://api.nxvav.cn/api/lanzou/
```

# 请求示例

[https://api.nxvav.cn/api/lanzou/?url=https://wwi.lanzoui.com/i1nm7fp8z0d](https://api.nxvav.cn/api/lanzou/?url=https://wwi.lanzoui.com/i1nm7fp8z0d)

[https://api.nxvav.cn/api/lanzou/?url=https://wwi.lanzoui.com/i7ryube&pwd=2333](https://api.nxvav.cn/api/lanzou/?url=https://wwi.lanzoui.com/i7ryube&pwd=2333)

[https://api.nxvav.cn/api/lanzou/?url=https://wwi.lanzoui.com/i1nm7fp8z0d&type=down](https://api.nxvav.cn/api/lanzou/?url=https://wwi.lanzoui.com/i1nm7fp8z0d&type=down)

# 使用场景

<!-- tabs:start -->

#### **html**

```html
等待编辑...
```

<!-- tabs:end -->

# 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ----- | ---- | ---- | ---- |
| url | 必填 | 蓝奏外链链接 | 蓝奏外链链接 |

| 参数名 | 类型 | 示例 | 说明 |
| ----- | ---- | ---- | ---- |
| pwd | 参数一(可空) | 蓝奏外链密码 | 蓝奏外链密码 |

| 参数名 | 类型 | 示例 | 说明 |
| -----  | ---- | ---- | ----- |
| type |  参数二(可空) | 下载类型 | 下载类型 |
| down | 可空 | 直接下载文件 |  直接下载文件 |

# 返回参数

| 返回参数 | 说明 |
| ------- | ---- |
| code | 状态码 |
| data | 数据 |
| name | 文件名 |
| author | 分享者 |
| time | 分享时间 |
| size | 文件大小 |
| url | 文件直链 |

# 状态代码

| 返回状态 | 说明 |
| ------- | ---- |
| 200 | 解析成功 |
| 201 | 链接错误 |
| 202 | 密码错误/密码为空 |

# 返回示例

```json
{
    "code": 200,
    "data": {
        "name": "Game Activation Code v1.00.exe ",
        "author": "诺仙上神 ",
        "time": "2019-12-01 ",
        "size": " 1.3 M ",
        "url": "https://developer82.baidupan.com/090723bb/2019/12/01/b92af6b2b254ec99541a7a63b35aae7e.exe?st=gYuY6pX345veOeIVNCm7Ag&e=1631032018&b=VUABYABtUTFXIl5JVWZQIFZqCyFRMQV3VmxYOlU8U3EJGAxjVTEHZwVwACAAYVR_bBGELZwUqCmkELwpi&fi=14789784&pid=212-95-155-107&up=2"
    }
}
```
