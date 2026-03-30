---
title: Fund Rate
position_number: 18
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **Request format**: `fund_rate@{symbol}`

    Example: `fund_rate@btc_usdt`

    Push rate: `60s`
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["fund_rate@btc_usdt"],
              "id": "test"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "fund_rate",
              "event": "fund_rate@btc_usdt",
              "data": {
                "s": "btc_usdt",
                "r": "0.01",
                "t": 123124124
              }
            }
        title: Response
        language: json
---
