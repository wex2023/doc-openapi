---
title: 余额变化
position_number: 7
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **Topic**: `balance`

    订阅用户账户余额变化事件。
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["balance@{ListenKey}"],
              "id": "{id}"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "balance",
              "event": "balance@123456",
              "data": {
                "coin": "usdt",
                "underlyingType": 1,
                "walletBalance": "123",
                "openOrderMarginFrozen": "123",
                "isolatedMargin": "213",
                "crossedMargin": "0"
              }
            }
        title: Response
        language: json
---
