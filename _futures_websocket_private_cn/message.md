---
title: 用户订阅消息
position_number: 11
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **Topic**: `notify`

    订阅系统通知事件（强平警告、ADL 等）。

    **notifyType 值**: WARN（警告，即将被强制平仓）、PARTIAL（部分强制平仓）、LIQUIDATION（强制平仓）、ADL（自动减仓）
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["notify@{ListenKey}"],
              "id": "{id}"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "notify",
              "event": "notify",
              "data": {
                "symbol": "btc_usdt",
                "positionType": "ISOLATED",
                "positionSide": "LONG",
                "positionSize": "123",
                "notifyType": "WARN"
              }
            }
        title: Response
        language: json
---
