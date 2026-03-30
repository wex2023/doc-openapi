---
title: 签名生成
position_number: 5
parameters:
- name:
content:
content_markdown: >-

    以 https://sapi.wexex.io/v4/order 为例。


    以下 **appKey/secret** **仅用于演示**（Linux bash 使用 `echo`、`openssl`、`curl`）：


    appKey: 3976eb88-76d0-4f6e-a6b2-a57980770085


    secretKey: bc6630d0231fda5cd98794f52c4998659beda290




    必需的请求头：

        validate-algorithms: HmacSHA256

        validate-appkey: 3976eb88-76d0-4f6e-a6b2-a57980770085

        validate-recvwindow: 5000

        validate-timestamp: 1641446237201

        validate-signature: 2b5eb11e18796d12d88f13dc27dbbd02c2cc51ff7059765ed9821957d82bb4d9



    请求体示例：

        {
          "type": "LIMIT",
          "timeInForce": "GTC",
          "side": "BUY",
          "symbol": "btc_usdt",
          "price": "39000",
          "quantity": "2"
        }



    **1. 数据部分拼接 (Y)**

        method: 大写的 HTTP 方法，如 GET、POST、DELETE、PUT

        path: 填充变量后的具体 RESTful 路径，如 /sign/test/bb/aa

        query: 按 key 字典序排序所有 key=value，用 & 连接，例如：userName=dfdfdf&password=ggg

        body:
            JSON: 使用原始 JSON 字符串（不转换/排序）

            x-www-form-urlencoded: 按 key 字典序排序所有 key=value，用 & 连接，例如：userName=dfdfdf&password=ggg

            form-data: 不支持

        如果存在多种形式，按顺序拼接：path -> query -> body。


    方法 method 示例：

        POST

    路径 path 示例：

        /v4/order

        上述拼接值记作为 path



    参数通过 query 示例：

        symbol=btc_usdt

        上述值拼接记作 query



    参数通过 body 示例：

        x-www-form-urlencoded:

            symbol=btc_usdt&side=BUY&type=LIMIT&timeInForce=GTC&quantity=1&price=0.1

            上述值拼接记作 body

        json:

            {"symbol":"btc_usdt","side":"BUY","type":"LIMIT","timeInForce":"GTC","quantity":2,"price":39000}

            上述值拼接记作 body



    混合使用 query 与 body（分为表单与 json 两种格式）：

        query:
            symbol=btc_usdt&side=BUY&type=LIMIT
            上述拼接值记作 query

        body:
            {"symbol":"btc_usdt","side":"BUY","type":"LIMIT"}
            上述拼接值记作 body



    最终用 # 拼接，带前导标记：

        Y = #method#path#query#body

    注意：

        query 存在，body 为空：Y = #method#path#query

        query 为空，body 存在：Y = #method#path#body

        都存在：Y = #method#path#query#body




    **2. 请求头部分拼接 (X)**

        将以下请求头键按自然升序字母顺序排序，然后用 & 连接：

            validate-algorithms=HmacSHA256&validate-appkey=3976eb88-76d0-4f6e-a6b2-a57980770085&validate-recvwindow=5000&validate-timestamp=1641446237201



    **3. 生成签名**

        拼接 original = X + Y（除了 Y 中已有的 # 外没有分隔符），然后计算：

        signature = org.apache.commons.codec.digest.HmacUtils.hmacSha256Hex(secretKey, original);

        将生成的值添加到请求头：validate-signature: <signature>


    **4. 完整示例**

        原始签名消息示例：

            validate-algorithms=HmacSHA256&validate-appkey=2063495b-85ec-41b3-a810-be84ceb78751&validate-recvwindow=60000&validate-timestamp=1666026215729#POST#/v4/order#{"symbol":"XT_USDT","side":"BUY","type":"LIMIT","timeInForce":"GTC","bizType":"SPOT","price":3,"quantity":2}

        注意事项：

            确保 Content-Type、签名原始消息和最终请求载荷保持一致。

            validate-timestamp 应为发送时间的毫秒数；配合合理的 validate-recvwindow 来容忍网络抖动。

            当 body 是 JSON 时，使用原始 JSON 字符串进行签名（不要重新排序键或美化格式）。


left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---
