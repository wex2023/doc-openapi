---
title: Get Open Order List
position_number: 10
type: post
description: /future/trade/v1/order/list-open-order
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: "Trading pair name (e.g. eth_usdt, btc_usdt)"
        ranges:
content_markdown: >-
    #### Rate Limit


    10/s/apikey

left_code_blocks:
    -
        code_block:
        title: Java
        language: java
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
              "orderId": "538511221008857280",
              "clientOrderId": "myOrder123",
              "symbol": "eth_usdt",
              "contractSize": 0.01,
              "orderType": "LIMIT",
              "orderSide": "BUY",
              "positionSide": "LONG",
              "positionType": "ISOLATED",
              "timeInForce": "GTC",
              "price": "4009.94",
              "origQty": "12",
              "avgPrice": "0",
              "executedQty": "0",
              "marginFrozen": "80.48751569",
              "remark": null,
              "sourceId": null,
              "sourceType": "DEFAULT",
              "leverage": 6,
              "openPrice": null,
              "state": "NEW",
              "createdTime": 1758093080143,
              "updatedTime": 1758093080371,
              "welfareAccount": false,
              "triggerPriceType": null,
              "triggerProfitPrice": null,
              "profitDelegateOrderType": null,
              "profitDelegateTimeInForce": null,
              "profitDelegatePrice": null,
              "triggerStopPrice": null,
              "stopDelegateOrderType": null,
              "stopDelegateTimeInForce": null,
              "stopDelegatePrice": null,
              "markPrice": "4543.73",
              "desc": null
            }
        title: Response
        language: json
---
