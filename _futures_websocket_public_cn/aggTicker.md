---
title: 聚合行情
position_number: 12
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **请求格式**: `agg_ticker@{symbol}`

    示例: `agg_ticker@btc_usdt`

    推送频率: `1000ms`
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["agg_ticker@btc_usdt"],
              "id": "test"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "agg_ticker",
              "event": "agg_ticker@btc_usdt",
              "data": {
                "s": "btc_index",
                "o": "49000",
                "c": "50000",
                "h": "0.1",
                "l": "0.1",
                "a": "0.1",
                "v": "0.1",
                "ch": "0.21",
                "i": "0.21",
                "m": "0.21",
                "bp": "0.21",
                "ap": "0.21",
                "t": 123124124
              }
            }
        title: Response
        language: json
---
