---
title: 仓位变化
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
    **Topic**: `position`

    订阅用户仓位变化事件。
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["position@{ListenKey}"],
              "id": "{id}"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "position",
              "event": "position@123456",
              "data": {
                "symbol": "btc_usdt",
                "contractType": "PERPUTUAL",
                "positionType": "ISOLATED",
                "positionSide": "LONG",
                "positionSize": "123",
                "closeOrderSize": "100",
                "availableCloseSize": "23",
                "realizedProfit": "123",
                "entryPrice": "213",
                "isolatedMargin": "213",
                "openOrderMarginFrozen": "123",
                "underlyingType": "",
                "leverage": 20
              }
            }
        title: Response
        language: json
---
