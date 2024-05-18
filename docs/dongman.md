# 接口描述

> 获取随机动漫图片

# 接口地址

请求方式：`GET`

返回格式：`JPG` / `JSON`

```API
https://api.nxvav.cn/api/dongman/
```

# 请求示例

[https://api.nxvav.cn/api/dongman/](https://api.nxvav.cn/api/dongman/)

[https://api.nxvav.cn/api/dongman/?type=m](https://api.nxvav.cn/api/dongman/?type=m)

[https://api.nxvav.cn/api/dongman/?type=pc](https://api.nxvav.cn/api/dongman/?type=pc)

[https://api.nxvav.cn/api/dongman/?type=pc](https://api.nxvav.cn/api/dongman/?encode=json)

# 使用场景

<!-- tabs:start -->

#### **html**

```html
<img src="https://api.nxvav.cn/api/dongman/" />
```

<!-- tabs:end -->

# 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ------ | ---- | ---- | ---- |
| type | 可空 | pc m | 根据设备尺寸自动切换 |
| encode | 可空 | json | 返回json格式 |

# 返回参数

| 返回参数 | 说明 |
| ------- | ---- |
| 无 | 无 |

# 状态代码

| 返回状态 | 说明 |
| ------- | ---- |
| 无 | 无 |

# 返回示例

```html
无
```
