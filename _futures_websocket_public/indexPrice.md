---
title: Index Price
position_number: 14
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **Request format**: `index_price@{symbol}`

    Example: `index_price@btc_usdt`

    Push rate: `1000ms`
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["index_price@btc_usdt"],
              "id": "test"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "index_price",
              "event": "index_price@btc_usdt",
              "data": {
                "s": "btc_usdt",
                "p": "50000",
                "t": 123124124
              }
            }
        title: Response
        language: json
---
