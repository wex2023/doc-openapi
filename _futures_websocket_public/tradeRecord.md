---
title: Trade Record
position_number: 8
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **Request format**: `trade@{symbol}`

    Example: `trade@btc_usdt`

    Push rate: real-time
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["trade@btc_usdt"],
              "id": "test"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "trade",
              "event": "trade@btc_usdt",
              "data": {
                "s": "btc_usdt",
                "p": "50000",
                "a": "0.1",
                "m": "BID",
                "t": 123124124
              }
            }
        title: Response
        language: json
---
