---
title: 获取签名
position_number: 3
parameters:
- name:
content:
content_markdown: >-
    #### 获取签名


    注：`${?}` 、`$?` 表示对变量 `?` 的引用。


    要生成签名 `signature`，需要利用申请 API Key 获取的 **SECRET KEY** 对 `unencrypted_string` 进行加密。


    #### 规则说明


    - **若 HTTP 请求参数放在 QueryString 中：** 则 `unencrypted_string = ${fixed_header}#${end_point}#${query_string}` 当 `query_string` 有多个键值对时，需按键名 **字典序排序** 并以 `&` 连接，例如：`keya=value&keyb=value&keyc=value`


    - **若 HTTP 请求参数放在 RequestBody 中：** 则 `unencrypted_string = ${fixed_header}#${end_point}#${request_body}`


    #### fixed_header 规则


    `fixed_header = "validate-appkey=${your_appkey}&validate-timestamp=${current_timestamp}"`


    `unencrypted_string` 的每个部分由 `#` 符号连接。


    #### 举例说明


    当前时间戳为 ***** ，你的 APPKEY 为 ++++++


    `fixed_header="validate-appkey=++++++&validate-timestamp=*****"`

    `end_point="/future/user/v1/balance/detail"`

    `query_string="coin=btc"`


    则：`unencrypted_string="validate-appkey=++++++&validate-timestamp=*****#/future/user/v1/balance/detail#coin=btc"`


    #### 生成签名


    获取 unencrypted_string 后，可用加密算法与 SECRETKEY 将 unencrypted_string 获取签名 SIGNATURE。


    获取该签名后，将 `SIGNATURE` 填入 HTTP 请求头中的 `validate-signature` 字段。

left_code_blocks:
- code_block: |-
    # 生成签名示例
    SIGNATURE=$(echo -n "$unencrypted_string" | \
      openssl dgst -sha256 -hmac "$SECRETKEY" | \
      awk '{print $2}')
    echo $SIGNATURE
  title: Shell
  language: bash
right_code_blocks:
- code_block:
  title:
  language:
---
