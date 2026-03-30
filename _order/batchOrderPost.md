---
title: Submit batch order
position_number: 5
type: post
description: /v4/batch-order
parameters:
    -
        name: clientBatchId
        type: string
        mandatory: false
        default:
        description: 'Client batch number. Pattern: ^[a-zA-Z0-9_]{4,32}$'
        ranges:
    -
        name: items
        type: array
        mandatory: true
        default:
        description: Array
        ranges:
    -
        name: item.symbol
        type: string
        mandatory: true
        default:
        description: Trading pair
        ranges:
    -
        name: item.clientOrderId
        type: string
        mandatory: false
        default:
        description: 'Pattern: ^[a-zA-Z0-9_]{4,32}$'
        ranges:
    -
        name: item.side
        type: string
        mandatory: true
        default:
        description: Order side
        ranges: BUY, SELL
    -
        name: item.type
        type: string
        mandatory: true
        default:
        description: Order type
        ranges: LIMIT, MARKET
    -
        name: item.timeInForce
        type: string
        mandatory: true
        default:
        description: Effective way
        ranges: GTC, FOK, IOC, GTX
    -
        name: item.bizType
        type: string
        mandatory: true
        default:
        description: Business type
        ranges: SPOT, LEVER
    -
        name: item.price
        type: number
        mandatory: false
        default:
        description: Price. Required if it is LIMIT; blank if it is MARKET
        ranges:
    -
        name: item.quantity
        type: number
        mandatory: false
        default:
        description: Quantity. Required if it is LIMIT or MARKET by quantity
        ranges:
    -
        name: item.quoteQty
        type: number
        mandatory: false
        default:
        description: Amount. Required if it is LIMIT or MARKET by amount
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**

    30/s/apikey
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
