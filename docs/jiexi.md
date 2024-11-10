# 接口地址

请求方式：`GET`

返回格式：`JSON`

```API
https://api.nxvav.cn/api/jiexi/
```

# 请求示例

[https://api.nxvav.cn/api/jiexi/?url=https://www.douyin.com/video/6682652170002730251](https://api.nxvav.cn/api/jiexi/?url=https://www.douyin.com/video/6682652170002730251)

[https://api.nxvav.cn/api/jiexi/?url=https://v.kuaishou.com/beDrMO/](https://api.nxvav.cn/api/jiexi/?url=https://v.kuaishou.com/beDrMO/)

> 支持解析以下视频

| 视频平台 | 视频平台 | 视频平台 |
| ------- | ------- | ------- |
| 抖音 | 皮皮虾 | 火山 |
| 微视 | 微博 | 绿洲 |
| 最右 | 轻视频 | 快手 |
| 全民小视频 | 皮皮搞笑 | 巴塞电影 |
| 陌陌 | Before避风 | 开眼 |
| Vue Vlog | 小咖秀 | 全民K歌 |

# 使用场景

<!-- tabs:start -->

#### **html**

```html
等待编辑...
```

#### **php**

```php
<?php
// 定义头部信息
header('Access-Control-Allow-Origin:*');
header('content-type:application/json');
// API接口
$url  = 'https://api.nxvav.cn/api/jiexi/?url=https://www.douyin.com/video/6682652170002730251';

// 设置URL和相应的选项
$curl = curl_init();
curl_setopt($curl, CURLOPT_URL, $url);
curl_setopt($curl, CURLOPT_RETURNTRANSFER, 1);
// 抓取URL并把它传递给data参数
$data = curl_exec($curl);
// 关闭cURL资源，并且释放系统资源
curl_close($curl);

// 状态码
$data = json_decode(trim($data,chr(239).chr(187).chr(191)));

// 输出状态码
echo $data -> code;
// 输出返回信息
echo $data -> msg;
// 输出视频数据 > 作者信息
echo $data -> data -> author;
// 输出视频数据 > 作者ID
echo $data -> data -> uid;
// 输出视频数据 > 作者头像直链
echo $data -> data -> avatar;
// 输出视频数据 > 视频点赞数量
echo $data -> data -> like;
// 输出视频数据 > 视频发布时间
echo $data -> data -> time;
// 输出视频数据 > 视频标题
echo $data -> data -> title;
// 输出视频数据 > 视频封面
echo $data -> data -> cover;
// 输出视频数据 > 视频直链
echo $data -> data -> url;
// 输出音乐数据 > 音乐作者
echo $data -> music -> author;
// 输出音乐数据 > 音乐封面
echo $data -> music -> avatar;
?>
```

<!-- tabs:end -->

# 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ------ | ---- | ---- | ---- |
| url | 必填 | 不能带中文字、特殊符号 | 视频平台分享的链接地址 |

# 返回参数

| 返回参数 | 说明 |
| -------- | ---- |
| code | 状态码 |
| msg | 返回信息 |
| data | 视频数据 |
| data > author | 作者名字 |
| data > uid | 作者id |
| data > avatar | 作者头像 |
| data > like | 视频点赞数量 |
| data > time | 发布时间(时间戳) |
| data > title | 视频标题 |
| data > cover | 视频封面 |
| data > url | 视频直链地址 |
| data > music | 音乐信息 |
| data > music > author | 音乐作者 |
| data > music > avatar | 音乐封面 |

# 状态代码

| 返回状态 | 说明 |
| -------- | ---- |
| 200 | 正常 |
| 201 | 错误 |

# 返回示例

```json
{
    "code": 200,
    "msg": "解析成功",
    "data": {
        "author": "人民日报",
        "uid": "rmrbxmt",
        "avatar": "https://p26.douyinpic.com/aweme/100x100/aweme-avatar/tos-cn-avt-0015_21b4383e542b8991bcd33d33eeda7d8d.jpeg?from=327834062",
        "like": 13101165,
        "time": 1555982844,
        "title": "人民海军生日快乐！重温2009国庆阅兵海军方队的风采。期待今天的海上阅兵！",
        "cover": "https://p3-sign.douyinpic.com/179d10014283e5888d5c7~tplv-dy-resize-walign-adapt-aq:720:q75.webp?x-expires=1732446000&x-signature=3tnyVWeOdbqyefiUpAihXIZlm9E%3D&from=327834062&s=PackSourceEnum_DOUYIN_REFLOW&se=false&sc=cover&biz_tag=aweme_video&l=20241110191548C144116C1F8758FD053F",
        "url": "https://aweme.snssdk.com/aweme/v1/play/?video_id=v0200ff80000biv6jt2gd9fj4om8m8ag&ratio=720p&line=0",
        "music": {
            "author": "人民日报",
            "avatar": "https://p3.douyinpic.com/aweme/1080x1080/aweme-avatar/tos-cn-avt-0015_21b4383e542b8991bcd33d33eeda7d8d.jpeg?from=327834062"
        }
    }
}
```
