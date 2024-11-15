## 接口地址

```API
https://api.nxvav.cn/api/qqimg/
```

## 请求示例

[https://api.nxvav.cn/api/qqimg/?qq=123456](https://api.nxvav.cn/api/qqimg/?qq=123456)

<!-- tabs:start -->

#### **Shell**

```shell
curl https://api.nxvav.cn/api/qqimg -X POST -d 'qq=123456'
```

#### **PHP**

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
   CURLOPT_URL => 'https://api.nxvav.cn/api/qqimg/?qq=123456',
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

| 参数名 | 类型 | 必填 | 说明 |
| - | - | - | - |
| qq | string | 是 | 需要获取的QQ头像的QQ号码 |

## 返回参数

| 返回参数 | 类型 | 说明 |
| - | - | - |
| image | image/jpg | 返回的QQ头像图片链接地址 |

## 请求示例

<!-- tabs:start -->

#### **成功(200)**

Content-Type: image/jpg

<img src="https://api.nxvav.cn/api/qqimg/?qq=123456" />

#### **失败(201)**

```text
qq为必须参数！
```

<!-- tabs:end -->