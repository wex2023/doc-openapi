---
title: 查询当前挂单
position_number: 7
type: get
description: /v4/open-order
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对，不填则表示全部
        ranges:
    -
        name: bizType
        type: string
        mandatory: false
        default:
        description: "业务类型 SPOT, LEVER"
        ranges:
    -
        name: side
        type: string
        mandatory: false
        default:
        description: "订单方向 BUY, SELL"
        ranges:
content_markdown: >-
    #### **限频规则**

    10次/秒/每apikey
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
