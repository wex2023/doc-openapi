---
title: 交易对市场成交记录
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
    **请求格式**: `trade@{symbol}`

    示例: `trade@btc_usdt`

    推送频率: 实时
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
