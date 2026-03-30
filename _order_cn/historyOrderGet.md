---
title: 查询历史订单
position_number: 9
type: get
description: /v4/history-order
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对，不填表示全部
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
        description: "买卖方向 BUY, SELL"
        ranges:
    -
        name: type
        type: string
        mandatory: false
        default:
        description: "订单类型 LIMIT, MARKET"
        ranges:
    -
        name: state
        type: string
        mandatory: false
        default:
        description: "订单状态 PARTIALLY_FILLED, FILLED, CANCELED, REJECTED, EXPIRED"
        ranges:
    -
        name: fromId
        type: number
        mandatory: false
        default:
        description: 起始ID
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default:
        description: "查询方向: PREV, NEXT"
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '20'
        description: 限制数量，最大100
        ranges:
    -
        name: startTime
        type: number
        mandatory: false
        default:
        description: "开始时间（示例：1657682804112）"
        ranges:
    -
        name: endTime
        type: number
        mandatory: false
        default:
        description: 结束时间
        ranges:
    -
        name: hiddenCanceled
        type: bool
        mandatory: false
        default:
        description: 是否隐藏已取消订单
        ranges:
content_markdown: >-
    #### **限流规则**

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
              "result": {
                "hasPrev": true,
                "hasNext": true,
                "items": [
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
            }
        title: Response
        language: json
---
