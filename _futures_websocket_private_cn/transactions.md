---
title: 成交记录
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
    **Topic**: `trade`

    订阅用户成交记录事件。
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["trade@{ListenKey}"],
              "id": "{id}"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "trade",
              "event": "trade@123456",
              "data": {
                "orderId": "12312312",
                "clientOrderId": "123456",
                "price": "34244",
                "quantity": "123",
                "marginUnfrozen": "123",
                "timestamp": 1731231231,
                "symbol": "btc_usdt",
                "orderSide": "BUY",
                "positionSide": "LONG",
                "isMaker": true,
                "fee": 0.0002
              }
            }
        title: Response
        language: json
---
