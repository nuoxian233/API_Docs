## 接口地址

```API
https://api.nxvav.cn/api/webrank/
```

## 请求示例

[https://api.nxvav.cn/api/webrank/?url=baidu.com](https://api.nxvav.cn/api/webrank/?url=baidu.com)

[https://api.nxvav.cn/api/webrank/?url=baidu.com&type=json](https://api.nxvav.cn/api/webrank/?url=baidu.com&type=json)

<!-- tabs:start -->

#### **Shell**

```shell
curl https://api.nxvav.cn/api/webrank -X POST -d 'url=baidu.com'
```

#### **PHP**

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
   CURLOPT_URL => 'https://api.nxvav.cn/api/webrank/?url=baidu.com&type=json',
   CURLOPT_RETURNTRANSFER => true,
   CURLOPT_ENCODING => '',
   CURLOPT_MAXREDIRS => 10,
   CURLOPT_TIMEOUT => 0,
   CURLOPT_FOLLOWLOCATION => true,
   CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
   CURLOPT_CUSTOMREQUEST => 'GET',
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;
?>
```

<!-- tabs:end -->

## 请求参数

| 参数名 | 类型 | 必填  | 说明 |
| - | - | - | - |
| url | string | 是 | 网站域名，不加http(s) |
| type | string | 否 | 请求网站权重类型，可选值`json`，`baidupc`，`baidum`，`sougou`，`google`，默认`baidupc`，除`json`其他均图片输出 |

## 返回参数

| 返回参数 | 类型 | 说明 |
| - | - | - |
| code | string | 状态码 |
| host | string | 查询域名 |
| data | string | 查询数据 |
| data > baidupc | string | 百度pc的权重 |
| data > baidum | string | 百度m的权重 |
| data > sougou | string | 搜狗的权重 |
| data > google | string | 谷歌的权重 |

## 返回示例

<!-- tabs:start -->

#### **成功(200)**

```json
{
    "code": 200,
    "host": "baidu.com",
    "data": {
        "baidupc": "10",
        "baidum": "10",
        "sougou": "10",
        "google": "10"
    }
}
```

#### **失败(201)**

```json
{
    "code": 201,
    "msg": "错误"
}
```

<!-- tabs:end -->