---
title: 批量查询
position_number: 4
type: get
description: /v4/batch-order
parameters:
    -
        name: orderIds
        type: string
        mandatory: true
        default:
        description: '订单 ID 列表，例如: 6216559590087220004, 6216559590087220005'
        ranges:
content_markdown: >-
    返回字段信息与 **查询单个订单接口** 相同。
left_code_blocks:
    -
        code_block: |-
            public String batchOrderGet(){


            }
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
                      "rc": 0,
                      "mc": "string",
                      "ma": [
                        {}
                      ],
                      "result": [
                        {
                          "symbol": "BTC_USDT",
                          "orderId": "6216559590087220004",
                          "clientOrderId": "16559590087220001",
                          "baseCurrency": "string",
                          "quoteCurrency": "string",
                          "side": "BUY",
                          "type": "LIMIT",
                          "timeInForce": "GTC",
                          "price": "40000",
                          "origQty": "2",
                          "origQuoteQty": "48000",
                          "executedQty": "1.2",
                          "leavingQty": "string",
                          "tradeBase": "2",
                          "tradeQuote": "48000",
                          "avgPrice": "42350",
                          "fee": "string",
                          "feeCurrency": "string",
                          "state": "NEW",
                          "time": 1655958915583,
                          "ip": "127.0.0.1",
                          "updatedTime": 1655958915583
                        }
                      ]
                    }
        title: Response
        language: json
---
