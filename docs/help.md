# 快速开始

> 欢迎使用nuoxian's API 公开接口服务！这里将讲解怎样快速开始使用API哦！

# 什么是API?

用知乎上一个比较生动的例子来说明：

> 有一天，轮子哥写了一个专门抓取知乎小黄文的API，轮子哥写的这个API每天都会自动查阅小黄文文章并且点赞。恰好你也是小黄文爱好者，那么轮子哥的账号对你来说就是API接口，你要做的唯一事情就是关注轮子哥账号，每天只需要查阅轮子哥的点赞动态就能看到轮子哥点赞的小黄文，但是不用关心轮子哥到底是用什么方法找到这么多小黄文的！

怎么样，是不是更好理解了呢？

# 适合群体

API大多数是为了网站开发者、程序开发者的使用。当然普通群体也是可以使用的。

# 使用API

以热门视频解析的API来说明使用。我们需要将抖音平台的一个视频弄成一个无水印视频。抖音视频地址为：v.douyin.com/e28ypsB/，一般抖音APP内下载视频是会在视频里`有水印和结束动画`的，我们的目的是`无水印无结束动画`。

热门视频解析的接口地址：[https://api.nxvav.cn/api/jiexi/](https://api.nxvav.cn/api/jiexi/)

我们可以先查看该接口的文档，来方便我们更好的使用和理解。

热门视频解析的接口文档：[https://api.nxvav.cn/doc/#/jiexi](https://api.nxvav.cn/doc/#/jiexi)

可以看到接口文档的`请求参数`中有个url是必须填写的，并且说明写的是`视频平台分享的链接地址`且`不能带中文字、特殊符号`

| 参数名 | 类型 | 示例 | 说明 |
| ------ | ---- | ---- | ---- |
| url | 必填 | 不能带中文字、特殊符号 | 视频平台分享的链接地址 |

`请求参数`的`参数名`下方有个`url`，就是我们所要携带的参数内容了，那么就是（每一个请求接口第一位都需要带上?，例如：xxx.com/?a=1&b=2&c=3 后面的一定要是&来作为附带请求参数）：api.nxvav.cn/api/jiexi/?url=`视频平台分享的链接地址`，那么就是[https://api.nxvav.cn/api/jiexi/?url=https://v.douyin.com/e28ypsB/](https://api.nxvav.cn/api/jiexi/?url=https://v.douyin.com/e28ypsB/)

然后看到接口文档的`返回参数`，以下是该说明文档的信息：

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

访问以上的链接，得到了以下`JSON`格式的信息。为了方便理解，我们特地将下方的json信息加上注释（注释就是对代码的解释和说明。目的是为了让别人和自己很容易看懂，一看就知道这段代码是做什么用的。）

```json
// 以下的都是在返回参数中的说明可以了解到的内容

{
    "code": 200, // 状态码
    "msg": "解析成功", // 返回信息
    "data": { // 视频数据
        "author": "人民日报", // 作者名字
        "uid": "rmrbxmt", // 作者id
        "avatar": "https://p6.douyinpic.com/aweme/1080x1080/30ed2000aad26be101cad.jpeg?from=116350172", // 作者头像
        "like": 4352174, // 视频点赞数量
        "time": 1555982844, // 发布时间(时间戳)
        "title": "人民海军生日快乐！重温2009国庆阅兵海军方队的风采。期待今天的海上阅兵！", // 视频标题
        "cover": "https://p9.douyinpic.com/1f8dd000451fc169d0e77~tplv-dy-360p.jpeg?from=4257465056&s=&se=false&sh=&sc=&l=2021090715471901021215216645015FCB&biz_tag=feed_cover", // 视频封面
        "url": "http://v3-dy-o.zjcdn.com/774360cc9bf046a9222f6f5d80c90e7f/61372726/video/m/220933054381c144d469dc1d9fcff4e73b61161e3f25000017f6feb628c0/?a=1128&amp;br=2510&amp;bt=2510&amp;btag=3&amp;cd=0%7C0%7C0&amp;ch=0&amp;cr=0&amp;cs=0&amp;cv=1&amp;dr=0&amp;ds=3&amp;er=&amp;ft=dlb~O-eTzzyhWH6Cu7apb&amp;l=2021090715472001021120213401018DA4&amp;lr=&amp;mime_type=video_mp4&amp;net=0&amp;pl=0&amp;qs=0&amp;rc=ajs7cm08anc5bDMzO2kzM0ApaTRnaDZmaDtpNzc0NzM2M2cpaGRqbGRoaGRmXmpqMWNhL2dzXy0tYy0vc3NiNWItNDVjMl5jXzIzNWEvOmNwb2wrbStqdDo%3D&amp;vl=&amp;vr=", // 视频直链地址
        "music": { // 音乐信息
            "author": "人民日报", // 音乐作者
            "avatar": "https://p6.douyinpic.com/aweme/1080x1080/30ed2000aad26be101cad.jpeg?from=116350172", // 音乐封面
            "url": "https://sf3-cdn-tos.douyinstatic.com/obj/ies-music/1631518807291940.mp3" // 音乐直链地址
        }
    }
}
```

我们通过`返回参数`得到了`url`是视频直链地址，那么我们找到了2个`url`，一个是在`data`的下面，一个是在`data`的`music`的下面。`url`的等于后面就是我们要的`无水印无结束动画`的视频直链了！

那么怎么看那个是视频直链呢？？看到接口文档的`返回参数`，我们也发现了返回参数中有着2个`url`，但是它们的说明是不一样的。一个是视频直链地址，一个是音乐直链地址。

看到说明文档的倒数第四个，它是music（音乐信息），那么它所有下面的返回参数都是音乐信息相关的。这样我们就知道获取第一个url了，而不是music的url。

```json
需要的："url": "http://v3-dy-o.zjcdn.com/774360cc9bf046a9222f6f5d80c90e7f/61372726/video/m/220933054381c144d469dc1d9fcff4e73b61161e3f25000017f6feb628c0/?a=1128&amp;br=2510&amp;bt=2510&amp;btag=3&amp;cd=0%7C0%7C0&amp;ch=0&amp;cr=0&amp;cs=0&amp;cv=1&amp;dr=0&amp;ds=3&amp;er=&amp;ft=dlb~O-eTzzyhWH6Cu7apb&amp;l=2021090715472001021120213401018DA4&amp;lr=&amp;mime_type=video_mp4&amp;net=0&amp;pl=0&amp;qs=0&amp;rc=ajs7cm08anc5bDMzO2kzM0ApaTRnaDZmaDtpNzc0NzM2M2cpaGRqbGRoaGRmXmpqMWNhL2dzXy0tYy0vc3NiNWItNDVjMl5jXzIzNWEvOmNwb2wrbStqdDo%3D&amp;vl=&amp;vr=",

不需要的："url": "https://sf3-cdn-tos.douyinstatic.com/obj/ies-music/1631518807291940.mp3"
```

# 效果视频

##### 有水印视频

<video width="100%" height="500px" controls>
    <source src="https://one.nxvav.cn/Video/%E6%9C%89%E6%B0%B4%E5%8D%B0%E8%A7%86%E9%A2%91.mp4" type="video/mp4">
</video>

##### 无水印视频

<video width="100%" height="500px" controls>
    <source src="https://one.nxvav.cn/Video/%E6%97%A0%E6%B0%B4%E5%8D%B0%E8%A7%86%E9%A2%91.mp4" type="video/mp4">
</video>

# 视频：什么是API?

<iframe src="//player.bilibili.com/player.html?aid=584075248&bvid=BV1v64y1F7XN&cid=220828223&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="100%" height="500px"> </iframe>
