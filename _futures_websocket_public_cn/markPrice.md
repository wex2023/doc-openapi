---
title: 标记价格
position_number: 15
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **请求格式**: `mark_price@{symbol}`

    示例: `mark_price@btc_usdt`

    推送频率: `1000ms`
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["mark_price@btc_usdt"],
              "id": "test"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "mark_price",
              "event": "mark_price@btc_usdt",
              "data": {
                "s": "btc_usdt",
                "p": "50000",
                "t": 123124124
              }
            }
        title: Response
        language: json
---
