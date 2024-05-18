## 接口描述

> 生成一个指定文本或指向url的二维码

## 接口地址

请求方式：`GET`

返回格式：`PNG`

```API
https://api.nxvav.cn/api/qr/
```

## 请求示例

[https://api.nxvav.cn/api/qr/?text=https://nxvav.cn/&size=100](https://api.nxvav.cn/api/qr/?text=https://nxvav.cn/&size=100)

[https://api.nxvav.cn/api/qr/?text=Hello,nuoxian'sAPI&size=100](https://api.nxvav.cn/api/qr/?text=Hello,nuoxian'sAPI&size=100)

[https://api.nxvav.cn/api/qr/?text=你现在访问的是nuoxian的公共API服务哦！](https://api.nxvav.cn/api/qr/?text=你现在访问的是nuoxian的公共API服务哦！)

#### 使用场景

<!-- tabs:start -->

#### **HTML**

```html
<!-- 获取内容 -->
<img src="https://api.nxvav.cn/api/qr/?txet=23333&size=320" alt="文本内容为23333，图片像素大小320" />
```

<!-- tabs:end -->

## 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ----- | ---- | ---- | ---- |
| text | 必填 | 文字或者网址 | 要生成二维码的内容 |

| 参数名 | 类型 | 示例 | 说明 |
| ----- | ---- | ---- | ---- |
| size | 参数二(可空) | 单位像素 | 生成二维码大小 |

## 返回参数

| 返回参数 | 说明 |
| ------- | ---- |
| 无 | 无 |

## 状态代码

| 返回状态 | 说明 |
| ------- | ---- |
| 无 | 无 |

## 返回示例

```html
无
```