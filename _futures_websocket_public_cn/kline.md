---
title: K线
position_number: 9
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **请求格式**: `kline@{symbol},{interval}`

    时间间隔: `1m, 3m, 5m, 15m, 30m, 1h, 2h, 4h, 6h, 8h, 12h, 1d, 3d, 1w, 1M`

    示例: `kline@btc_usdt,5m`

    推送频率: `1000ms`
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["kline@btc_usdt,5m"],
              "id": "test"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "kline",
              "event": "kline@btc_usdt,5m",
              "data": {
                "s": "btc_index",
                "o": "49000",
                "c": "50000",
                "h": "0.1",
                "l": "0.1",
                "a": "0.1",
                "v": "0.1",
                "ch": "0.21",
                "t": 123124124
              }
            }
        title: Response
        language: json
---
