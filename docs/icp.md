# 接口地址

请求方式：`GET`

返回格式：`JSON`

```API
https://api.nxvav.cn/api/icp/
```

# 请求示例

[https://api.nxvav.cn/api/icp/?url=www.baidu.com](https://api.nxvav.cn/api/icp/?url=www.baidu.com)

[https://api.nxvav.cn/api/icp/?url=4399.com](https://api.nxvav.cn/api/icp/?url=4399.com)

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
$url  = 'https://api.nxvav.cn/api/icp/?url=www.baidu.com';

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
// 输出主办单位名称
echo $data -> data -> name;
// 输出主办单位性质
echo $data -> data -> nature;
// 输出备案号
echo $data -> data -> icp;
// 输出网站名称
echo $data -> data -> sitename;
// 输出网站首页地址
echo $data -> data -> index;
// 输出审核通过日期
echo $data -> data -> time;
?>
```

<!-- tabs:end -->

# 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ------ | ---- | ---- | ---- |
| url | 必填 | 网站域名不加http(s) | 获取备案信息的网站 |

# 返回参数

| 返回参数 | 说明 |
| ------- | ---- |
| code | 状态码 |
| data | 备案信息 |
| name | 主办单位名称 |
| nature | 主办单位性质 |
| icp | 备案号 |
| sitename | 网站名称 |
| index | 网站首页地址 |
| time | 审核通过日期 |

# 状态代码

| 返回状态 | 说明 |
| ------- | ---- |
| 200 | 获取备案信息成功 |
| 201 | 未查询到备案信息 |

# 请求示例

```json
{
    "code": 200,
    "data": {
        "name": "北京百度网讯科技有限公司",
        "nature": "企业",
        "icp": "京ICP证030173号-1",
        "sitename": "百度",
        "index": "www.baidu.com",
        "time": "2021-06-10"
    }
}
```
