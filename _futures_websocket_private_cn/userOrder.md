---
title: 用户订单
position_number: 10
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **Topic**: `order`

    订阅用户订单事件。订单状态变化时推送。
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["order@{ListenKey}"],
              "id": "{id}"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "order",
              "event": "order@123456",
              "data": {
                "symbol": "btc_usdt",
                "orderId": "1234",
                "origQty": "34244",
                "avgPrice": "123",
                "price": "1111",
                "executedQty": "34244",
                "orderSide": "BUY",
                "timeInForce": "IOC",
                "positionSide": "LONG",
                "marginFrozen": "123",
                "sourceType": "default",
                "type": "ORDER",
                "state": "FILLED",
                "createdTime": 1731231231,
                "leverage": 20,
                "positionType": "ISOLATED",
                "orderType": "MARKET"
              }
            }
        title: Response
        language: json
---
