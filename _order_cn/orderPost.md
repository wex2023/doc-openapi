---
title: 提交订单
position_number: 2
type: post
description: /v4/order
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对
        ranges:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: '自定义订单号，正则: ^[a-zA-Z0-9_]{4,22}$'
        ranges:
    -
        name: side
        type: string
        mandatory: true
        default:
        description: "订单方向 BUY, SELL"
        ranges:
    -
        name: type
        type: string
        mandatory: true
        default:
        description: "订单类型 LIMIT, MARKET"
        ranges:
    -
        name: timeInForce
        type: string
        mandatory: true
        default:
        description: 有效方式 GTC, FOK, IOC, GTX
        ranges:
    -
        name: bizType
        type: string
        mandatory: true
        default:
        description: "业务类型 SPOT, LEVER"
        ranges:
    -
        name: price
        type: number
        mandatory: false
        default:
        description: 价格。当为 LIMIT 订单时必填；MARKET 订单不需要填写
        ranges:
    -
        name: quantity
        type: number
        mandatory: false
        default:
        description: 数量。当为 LIMIT 订单或按数量市价单时必填
        ranges:
    -
        name: quoteQty
        type: number
        mandatory: false
        default:
        description: 金额。当为 LIMIT 订单或按金额市价单时必填
        ranges:
    -
        name: nftId
        type: string
        mandatory: false
        default:
        description: NFT ID
        ranges:
content_markdown: >-
    #### 备注

    创建买入市价单时，quantity 必须为空，quoteQty 必填。创建卖出市价单时，quoteQty 必须为空，quantity 必填。

    #### **限流规则**

    20/s/apikey

left_code_blocks:
    -
        code_block: |-
            public String orderPost(){


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
                  "result": {
                    "orderId": "6216559590087220004",
                    "ip": "127.0.0.1"
                  }
                }
        title: Response
        language: json
---
