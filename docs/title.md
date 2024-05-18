## 接口描述

> 获取网站标题信息

## 接口地址

请求方式：`GET`

返回格式：`JSON`

```API
https://api.nxvav.cn/api/title/
```

## 请求示例

[https://api.nxvav.cn/api/title/?url=nxvav.cn](https://api.nxvav.cn/api/title/?url=nxvav.cn)

[https://api.nxvav.cn/api/title/?url=www.baidu.com](https://api.nxvav.cn/api/title/?url=www.baidu.com)

#### 使用场景

<!-- tabs:start -->

#### **html**

```html
等待编辑...
```

<!-- tabs:end -->

## 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ----- | ---- | ---- | ---- |
| url | 必填 | 网站域名 | 不带http(s) |

## 返回参数

| 返回参数 | 说明 |
| ----- | ---- |
| code | 状态码 |
| data | 信息数据 |
| title | 网站标题 |
| description | 网站描述 |
| keywords | 网站标签 |

## 状态代码

| 返回状态 | 说明 |
| ------- | ---- |
| 200 | 正常 |
| 202 | 获取错误 |

## 返回示例

```json
{
    "code": 200,
    "data": {
        "title": "诺仙の客栈",
        "description": "这里是诺仙の客栈，我在这里记录和分享我的点点滴滴！客官来看看啊~",
        "keywords": "诺仙の客栈,nuoxian,诺仙仙君,教程,技术"
    }
}
```