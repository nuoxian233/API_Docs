## 接口地址

请求方式：`GET`

返回格式：`JSON` / `XML` / `JS` / `JSONP` / `TEXT`

```API
https://api.nxvav.cn/api/ip/
```

IP地址位置数据由 <a href="https://www.cz88.net" target="_blank">纯真CZ88</a> 提供支持

## 请求示例

[https://api.nxvav.cn/api/ip/](https://api.nxvav.cn/api/ip/)

## 使用场景

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
$url  = 'https://api.nxvav.cn/api/ip/';

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

## 请求参数

| 参数名 | 类型 | 示例 | 说明 |
| ------ | ---- | ---- | ---- |
| ip | 可空 |  |  |
| format | 可空 |  |  |

## 返回参数

| 返回参数 | 说明 |
| -------- | ---- |
| code | 状态码 |
| ip | ip地址 |
| country | 国家 |
| province | 省份 |
| city | 城市 |
| district | 地区 |
| provider | 运营商

## 状态代码

| 返回状态 | 说明 |
| -------- | ---- |
| 200 | 正常 |
| 201 | 查询错误 / 参数为空 |

## 返回示例

```json
{
    "code": 200,
    "data": {
        "ip": "114.114.114.114",
        "country": "中国",
        "province": "江苏",
        "city": "南京",
        "district": null,
        "provider": "南京信风网络科技有限公司GreatbitDNS服务器"
    }
}
```
