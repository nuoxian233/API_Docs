# 接口地址

请求方式：`GET`

返回格式：`JSON` / `XML`

```API
https://api.nxvav.cn/api/ip/
```

# 请求示例

[https://api.nxvav.cn/api/ip/](https://api.nxvav.cn/api/ip/)

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
$url  = 'https://api.nxvav.cn/ip/';

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
?>
```

<!-- tabs:end -->

# 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ------ | ---- | ---- | ---- |
|  |  |  |  |

# 返回参数

| 返回参数 | 说明 |
| -------- | ---- |
| code | 状态码 |
| ip | 查询的ip |
| ip_start | 查询的起始ip |
| ip_end | 查询的结束ip |
| address | ip地址 |
| location | ip运营商 |
| country | 查询的ip国家 |
| province | 查询的省 |
| city | 查询的城市 |
| area | 查询的地区 |

# 状态代码

| 返回状态 | 说明 |
| -------- | ---- |
| 200 | 正常 |
| 201 | 查询错误 / 参数为空 |

# 返回示例

```json
{
    "code": 200,
    "ip": "123.4.4.4",
    "ip_start": "123.4.0.0",
    "ip_end": "123.4.10.255",
    "address": "河南省濮阳市",
    "location": "联通",
    "country": "中国",
    "province": "河南省",
    "city": "濮阳市",
    "area": ""
}
```
