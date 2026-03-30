---
title: Query trade
position_number: 1
type: get
description: /v4/trade
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair, if not filled, represents all
        ranges:
    -
        name: bizType
        type: string
        mandatory: false
        default:
        description: "Business type: SPOT, LEVER"
        ranges:
    -
        name: orderSide
        type: string
        mandatory: false
        default:
        description: "Order side: BUY, SELL"
        ranges:
    -
        name: orderType
        type: string
        mandatory: false
        default:
        description: "Order type: LIMIT, MARKET"
        ranges:
    -
        name: orderId
        type: number
        mandatory: false
        default:
        description: Order ID
        ranges:
    -
        name: fromId
        type: number
        mandatory: false
        default:
        description: Start ID
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default:
        description: "Query direction: PREV, NEXT"
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '20'
        description: Limit number, max 100
        ranges:
    -
        name: startTime
        type: number
        mandatory: false
        default:
        description: "Start time (e.g. 1657682804112)"
        ranges:
    -
        name: endTime
        type: number
        mandatory: false
        default:
        description: End time
        ranges:
content_markdown: >-
    This endpoint retrieves trade records. Supports filtering by trading pair, business type, side, order type, time range, and pagination.
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
                        "symbol": "BTC_USDT",                    // Trading pair
                        "tradeId": "6316559590087222001",        // Trade ID
                        "orderId": "6216559590087220004",        // Order ID
                        "orderSide": "BUY",                      // Order direction
                        "orderType": "LIMIT",                    // Order type
                        "bizType": "SPOT",                       // Business type
                        "time": 1655958915583,                   // Trade time
                        "price": "40000",                        // Trade price
                        "quantity": "1.2",                       // Trade quantity
                        "quoteQty": "48000",                     // Trade amount
                        "baseCurrency": "BTC",                   // Base currency
                        "quoteCurrency": "USDT",                 // Quote currency
                        "takerMaker": "taker",                   // Taker/Maker
                        "deductType": "COUPON",                  // Fee deduction type: COUPON / PLATFORM_CURRENCY / null
                        "deductFee": "0.003",                    // Deducted fee amount if using coupon; otherwise null
                        "fee": "0.5",                            // Fee amount (or platform currency amount if deducted)
                        "feeCurrency": "USDT",                   // Fee currency
                        "couponAmount": "0.002",                 // Coupon amount if used; otherwise null
                        "couponCurrency": "usdt"                 // Coupon currency if used; otherwise null
                      }
                    ]
                  }
                }
        title: Response
        language: json
---
