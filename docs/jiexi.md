## 接口描述

> 支持解析以下视频

| 视频平台 | 视频平台 | 视频平台 |
| ------- | ------- | ------- |
| 抖音 | 皮皮虾 | 火山 |
| 微视 | 微博 | 绿洲 |
| 最右 | 轻视频 | 快手 |
| 全民小视频 | 皮皮搞笑 | 巴塞电影 |
| 陌陌 | Before避风 | 开眼 |
| Vue Vlog | 小咖秀 | 全民K歌 |

## 接口地址

请求方式：`GET`

返回格式：`JSON`

```API
https://api.nxvav.cn/api/jiexi/
```

## 请求示例

[https://api.nxvav.cn/api/jiexi/?url=https://v.douyin.com/e28ypsB/](https://api.nxvav.cn/api/jiexi/?url=https://v.douyin.com/e28ypsB/)

[https://api.nxvav.cn/api/jiexi/?url=https://v.kuaishou.com/beDrMO/](https://api.nxvav.cn/api/jiexi/?url=https://v.kuaishou.com/beDrMO/)

#### 使用场景

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
$url  = 'https://api.nxvav.cn/api/jiexi/?url=https://v.douyin.com/e28ypsB/';

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
// 输出音乐数据 > 音乐直链
echo $data -> music -> url;
?>
```

<!-- tabs:end -->

## 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ------ | ---- | ---- | ---- |
| url | 必填 | 不能带中文字、特殊符号 | 视频平台分享的链接地址 |

## 返回参数

| 返回参数 | 说明 |
| -------- | ---- |
| code | 状态码 |
| msg | 返回信息 |
| data | 视频数据 |
| author | 作者名字 |
| uid | 作者id |
| avatar | 作者头像 |
| like | 视频点赞数量 |
| time | 发布时间(时间戳) |
| title | 视频标题 |
| cover | 视频封面 |
| url | 视频直链地址 |
| music | 音乐信息 |
| author | 音乐作者 |
| avatar | 音乐封面 |
| url | 音乐直链地址 |

## 状态代码

| 返回状态 | 说明 |
| -------- | ---- |
| 200 | 正常 |
| 201 | 错误 |

## 返回示例

```json
{
    "code": 200,
    "msg": "解析成功",
    "data": {
        "author": "人民日报",
        "uid": "rmrbxmt",
        "avatar": "https://p11.douyinpic.com/aweme/1080x1080/30ed2000aad26be101cad.jpeg?from=116350172",
        "like": 4357115,
        "time": 1555982844,
        "title": "人民海军生日快乐！重温2009国庆阅兵海军方队的风采。期待今天的海上阅兵！",
        "cover": "https://p26.douyinpic.com/1f8dd000451fc169d0e77~tplv-dy-360p.jpeg?from=4257465056&s=&se=false&sh=&sc=&l=2021061322273601021207802223B2B6E9&biz_tag=feed_cover",
        "url": "http://v3-dy-o.zjcdn.com/831ad2fd66a4790819e9c720b3327c53/60c623f8/video/m/220933054381c144d469dc1d9fcff4e73b61161e3f25000017f6feb628c0/?a=1128&br=2510&bt=2510&btag=3&cd=0%7C0%7C0&ch=0&cr=0&cs=0&cv=1&dr=0&ds=3&er=&l=2021061322273801020405923425D3DD54&lr=&mime_type=video_mp4&net=0&pl=0&qs=0&rc=ajs7cm08anc5bDMzO2kzM0ApaTRnaDZmaDtpNzc0NzM2M2cpaGRqbGRoaGRmXmpqMWNhL2dzXy0tYy0vc3NiNWItNDVjMl5jXzIzNWEvOmNwb2wrbStqdDo%3D&vl=&vr=",
        "music": {
            "author": "人民日报",
            "avatar": "https://p6.douyinpic.com/aweme/1080x1080/30ed2000aad26be101cad.jpeg?from=116350172",
            "url": "https://sf3-cdn-tos.douyinstatic.com/obj/ies-music/1631518807291940.mp3"
        }
    }
}
```