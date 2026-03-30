---
title: 提交批量订单
position_number: 5
type: post
description: /v4/batch-order
parameters:
    -
        name: clientBatchId
        type: string
        mandatory: false
        default:
        description: '客户端批次号。正则规则：^[a-zA-Z0-9_]{4,32}$'
        ranges:
    -
        name: items
        type: array
        mandatory: true
        default:
        description: 订单数组
        ranges:
    -
        name: item.symbol
        type: string
        mandatory: true
        default:
        description: 交易对
        ranges:
    -
        name: item.clientOrderId
        type: string
        mandatory: false
        default:
        description: '客户端订单号。正则规则：^[a-zA-Z0-9_]{4,32}$'
        ranges:
    -
        name: item.side
        type: string
        mandatory: true
        default:
        description: 买卖方向
        ranges: BUY, SELL
    -
        name: item.type
        type: string
        mandatory: true
        default:
        description: 订单类型
        ranges: LIMIT, MARKET
    -
        name: item.timeInForce
        type: string
        mandatory: true
        default:
        description: 有效方式
        ranges: GTC, FOK, IOC, GTX
    -
        name: item.bizType
        type: string
        mandatory: true
        default:
        description: 业务类型
        ranges: SPOT, LEVER
    -
        name: item.price
        type: number
        mandatory: false
        default:
        description: 价格。LIMIT 必填，MARKET 可为空
        ranges:
    -
        name: item.quantity
        type: number
        mandatory: false
        default:
        description: 数量。LIMIT 必填，或按数量下 MARKET 订单时必填
        ranges:
    -
        name: item.quoteQty
        type: number
        mandatory: false
        default:
        description: 金额。LIMIT 必填，或按金额下 MARKET 订单时必填
        ranges:
content_markdown: >-
    #### **限流规则**

    30次/秒/apikey
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
                    "batchId": "123",
                    "items": [
                      {
                        "index": "0",
                        "clientOrderId": "123",
                        "orderId": "123",
                        "reject": "false",
                        "reason": "invalid price precision"
                      }
                    ]
                  }
                }
        title: Response
        language: json
---
