---
title: 获取客户端IP
position_number: 1
type: get
description: /future/public/client
parameters:
    -
        name:
        type:
        mandatory: false
        default:
        description:
        ranges:
content_markdown: >-
    此方法不需要签名。
left_code_blocks:
    -
        code_block: |-
            public void getClientIp() {
                String text = HttpUtil.get("https://fapi.xt.com/future/public/client");
                System.out.println(text);
            }
        title: Java
        language: java
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
              "returnCode": 0,
              "msgInfo": "success",
              "error": null,
              "result": {
                "ip": "192.168.1.1"
              }
            }
        title: Response
        language: json
---
