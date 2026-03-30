---
title: 有限深度
position_number: 17
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **请求格式**: `depth@{symbol},{levels},{interval}`

    档位选项: `5, 10, 20, 50`

    时间间隔选项: `100, 250, 500, 1000`（默认频率: `1000ms`）

    示例: `depth@btc_usdt,50,1000ms`
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["depth@btc_usdt,50,1000ms"],
              "id": "test"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "depth",
              "event": "depth@btc_usdt,20",
              "data": {
                "id": "1234",
                "s": "btc_index",
                "a": [
                  ["50000", "0.1"],
                  ["50001", "0.2"]
                ],
                "b": [
                  ["49999", "0.1"],
                  ["48888", "0.2"]
                ],
                "t": 123456789
              }
            }
        title: Response
        language: json
---
