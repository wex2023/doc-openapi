---
title: 查询成交记录
position_number: 1
type: get
description: /v4/trade
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对，如不填写则代表所有
        ranges:
    -
        name: bizType
        type: string
        mandatory: false
        default:
        description: "业务类型：SPOT-现货, LEVER-杠杆"
        ranges:
    -
        name: orderSide
        type: string
        mandatory: false
        default:
        description: "订单方向：BUY-买, SELL-卖"
        ranges:
    -
        name: orderType
        type: string
        mandatory: false
        default:
        description: "订单类型：LIMIT-限价, MARKET-市价"
        ranges:
    -
        name: orderId
        type: number
        mandatory: false
        default:
        description: 订单ID
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
        description: "查询方向：PREV, NEXT"
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
        description: "开始时间（例如：1657682804112）"
        ranges:
    -
        name: endTime
        type: number
        mandatory: false
        default:
        description: 结束时间
        ranges:
content_markdown: >-
    此接口用于查询成交记录。支持按交易对、业务类型、订单方向、订单类型、时间范围进行筛选，并支持分页查询。
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
                        "symbol": "BTC_USDT",                    // 交易对
                        "tradeId": "6316559590087222001",        // 成交ID
                        "orderId": "6216559590087220004",        // 订单ID
                        "orderSide": "BUY",                      // 订单方向
                        "orderType": "LIMIT",                    // 订单类型
                        "bizType": "SPOT",                       // 业务类型
                        "time": 1655958915583,                   // 成交时间
                        "price": "40000",                        // 成交价格
                        "quantity": "1.2",                       // 成交数量
                        "quoteQty": "48000",                     // 成交金额
                        "baseCurrency": "BTC",                   // 基础币种
                        "quoteCurrency": "USDT",                 // 计价币种
                        "takerMaker": "taker",                   // 吃单方/挂单方
                        "deductType": "COUPON",                  // 手续费抵扣类型：COUPON / PLATFORM_CURRENCY / null
                        "deductFee": "0.003",                    // 使用优惠券时的抵扣费用金额；否则为null
                        "fee": "0.5",                            // 手续费金额（或使用平台币抵扣时的平台币数量）
                        "feeCurrency": "USDT",                   // 手续费币种
                        "couponAmount": "0.002",                 // 使用优惠券时的优惠券金额；否则为null
                        "couponCurrency": "usdt"                 // 使用优惠券时的优惠券币种；否则为null
                      }
                    ]
                  }
                }
        title: Response
        language: json
---
