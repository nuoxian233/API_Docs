# 接口描述

> 可以获取哔哩哔哩视频的视频直链（获取时可能比较慢，需要耐心等待）

# 接口地址

请求方式：`GET`

返回格式：`JSON`

```API
https://api.nxvav.cn/api/bilivideo/
```

# 请求示例

[https://api.nxvav.cn/api/bilivideo/?av=430366930&p=1&q=32&otype=json](https://api.nxvav.cn/api/bilivideo/?av=430366930&p=1&q=32&otype=json)

[https://api.nxvav.cn/api/bilivideo/?av=430366930&p=1&q=32&otype=dplayer](https://api.nxvav.cn/api/bilivideo/?av=430366930&p=1&q=32&otype=dplayer)

# 使用场景

<!-- tabs:start -->

#### **html**

```html
等待编辑...
```

<!-- tabs:end -->

# 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ----- | ---- | --- | ---- |
| av / bv | 可空 | av430366930 / BV15G411V72W | B站视频号 |
| ep | 可空 | ep604279 | 剧集编号 |
| p | 可空 | p=1 | 视频集数，默认1 |
| q | 可空 | 16/32/64/80 | 视频清晰度，默认32 |
| type | 可空 | video / bangumi | 视频类型，默认video |
| format | 可空 | flv / dash / mp4 | 视频格式，默认flv |
| otype | 可空 | json / url / dplayer | 输出格式，默认json |

# 返回参数

| 返回参数 | 说明 |
| ------ | ----- |
| code | 状态码 |
| quality | 视频清晰度 |
| accept_quality | 可获取的视频质量 |
| url | 视频直链 |

# 状态代码

| 返回状态 | 说明 |
| -------- | ---- |
| 0 | 获取成功 |

# 返回示例

```json
{"code":0,"quality":32,"accept_quality":[116,80,64,32,16],"url":"http:\/\/upos-sz-mirrorhw.bilivideo.com\/upgcxcode\/13\/25\/826612513\/826612513-1-32.flv?e=ig8euxZM2rNcNbN3hwdVhoMgnwdVhwdEto8g5X10ugNcXBlqNxHxNEVE5XREto8KqJZHUa6m5J0SqE85tZvEuENvNC8xNEVE9EKE9IMvXBvE2ENvNCImNEVEK9GVqJIwqa80WXIekXRE9IMvXBvEuENvNCImNEVEua6m2jIxux0CkF6s2JZv5x0DQJZY2F8SkXKE9IB5QK==&deadline=1663242266&gen=playurl&nbs=1&oi=794886705&os=hwbv&platform=pc&trid=a9ab966e16cb40e48b70b4d830c3fe85&uipk=5&upsig=60806c7b2700628db8b86bbc94f883bf&uparams=e,deadline,gen,nbs,oi,os,platform,trid,uipk&mid=0"}
```
