---
title: Incremental Depth
position_number: 16
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **Request format**: `depth_update@{symbol},{interval}`

    Interval options: `100, 250, 500, 1000` (default: `100ms`)

    Example: `depth_update@btc_usdt,100ms`
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["depth_update@btc_usdt,100ms"],
              "id": "test"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "depth_update",
              "event": "depth_update@btc_usdt",
              "data": {
                "s": "btc_usdt",
                "pu": 120,
                "fu": 121,
                "u": 123,
                "a": [
                  ["34000", "1.2"],
                  ["34001", "2.3"]
                ],
                "b": [
                  ["32000", "0.2"],
                  ["31000", "0.5"]
                ],
                "t": 123456789
              }
            }
        title: Response
        language: json
---
