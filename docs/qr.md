## 接口地址

```API
https://api.nxvav.cn/api/qr/
```

## 请求示例

[https://api.nxvav.cn/api/qr/?text=https://api.nxvav.cn/&size=100](https://api.nxvav.cn/api/qr/?text=https://api.nxvav.cn/&size=100)

[https://api.nxvav.cn/api/qr/?text=你现在访问的是nuoxian的公共API服务哦！](https://api.nxvav.cn/api/qr/?text=你现在访问的是nuoxian的公共API服务哦！)

<!-- tabs:start -->

#### **Shell**

```shell
curl https://api.nxvav.cn/api/qr -X POST -d 'text=https://api.nxvav.cn/'
```

#### **HTTP**

```php
<?php

$curl = curl_init();

$url = 'https://api.nxvav.cn/api/qr/?text=https://api.nxvav.cn/&size=100';
$outputFilePath = 'qrcode.png';

curl_setopt_array($curl, array(
    CURLOPT_URL => $url,
    CURLOPT_RETURNTRANSFER => true,
    CURLOPT_BINARYTRANSFER => true,
    CURLOPT_FOLLOWLOCATION => true,
));

$response = curl_exec($curl);

if ($response === false) {
    $error = curl_error($curl);
    echo "cURL Error: $error";
} else {
    file_put_contents($outputFilePath, $response);
    echo "QR Code saved to $outputFilePath";
}

curl_close($curl);
?>
```

<!-- tabs:end -->

## 请求参数

| 参数名 | 类型 | 必填 | 说明 |
| - | - | - | - |
| text | string | 是 | 返回文本/网址二维码 |
| size | number | 否 | 返回文本/网站二维码像素大小 |

## 返回参数

| 返回参数 | 类型 | 说明 |
| - | - | - |
| image | image/png | 返回的二维码图片，图片格式为PNG |

## 返回示例

<!-- tabs:start -->

#### **成功(200)**

Content-Type: image/png

![QRCode](https://api.nxvav.cn/api/qr/?text=https://api.nxvav.cn/&size=100)

#### **失败(201)**

```text
参数错误或没有内容！
```

<!-- tabs:end -->