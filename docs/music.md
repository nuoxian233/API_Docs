# 接口地址

请求方式：`GET`

返回格式：`MP4` / `JSON`

```API
https://api.nxvav.cn/api/music/
```

# 请求示例

[https://api.nxvav.cn/api/music/?type=url&id=1436502055](https://api.nxvav.cn/api/music/?type=url&id=1436502055)

[https://api.nxvav.cn/api/music/?type=lrc&id=1495881305](https://api.nxvav.cn/api/music/?type=lrc&id=1495881305)

[https://api.nxvav.cn/api/music/?type=playlist&id=5420609323](https://api.nxvav.cn/api/music/?type=playlist&id=5420609323)

# 使用场景

<!-- tabs:start -->

#### **html**

```html
<audio controls="controls" height="100" width="100">
    <source src="https://api.nxvav.cn/api/music/?type=url&id=1436502055" type="audio/mpeg">
</audio>
```

<!-- tabs:end -->

# 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ----- | ---- | ---- | ---- |
| id | 必填 | 歌曲id | 歌曲id |

| 参数名 | 类型 | 示例 | 说明 |
| ----- | ---- | ---- | ---- |
| server | 参数一(可空) | 数据源 | 数据源 |
| netease | 可空 | 网易云音乐 | 网易云音乐 |
| tencent | 可空 | QQ音乐 | QQ音乐 |

| 参数名 | 类型 | 示例 | 说明 |
| ----- | ---- | ---- | ---- |
| type | 参数二(必填) | 看下方填写 | 看下方填写 |
| name | 可空 | 获取歌曲名 | 获取歌曲名 |
| artist | 可空 | 获取歌手 | 获取歌手名 |
| url | 可空 | 歌曲直链 | 输出音乐直链 |
| cover | 可空 | 歌曲封面 | 输出歌曲封面 |
| lrc | 可空 | 歌曲台词 | 输出歌曲台词 |
| single | 可空 | 歌曲信息 | 输出歌曲信息 |
| playlist | 可空 | 歌单信息 | 输出歌单信息 |

# 返回参数

| 返回参数 | 说明 |
| ------- | ---- |
| 无 | 无 |

# 状态代码

| 返回状态 | 说明 |
| ------- | ---- |
| 无 | 无 |

# 返回示例

<audio controls="controls" height="100" width="100">
    <source src="https://api.nxvav.cn/api/music/?type=url&id=1436502055" type="audio/mpeg">
</audio>
