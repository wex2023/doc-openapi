---
title: 增量深度
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
    **请求格式**: `depth_update@{symbol},{interval}`

    时间间隔选项: `100, 250, 500, 1000`（默认频率: `100ms`）

    示例: `depth_update@btc_usdt,100ms`
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
