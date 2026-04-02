---
title: 获取交易对币种
position_number: 2
type: get
description: /future/market/v1/public/symbol/coins
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
            public void getSymbolCoins() {
                String text = HttpUtil.get("https://fapi.wexex.io/future/market/v1/public/symbol/coins");
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
              "error": {
                "code": "",
                "msg": ""
              },
              "msgInfo": "",
              "result": [],
              "returnCode": 0
            }
        title: Response
        language: json
---
