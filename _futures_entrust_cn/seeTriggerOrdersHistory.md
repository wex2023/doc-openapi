---
title: 查看触发订单历史
position_number: 6
type: get
description: /future/trade/v1/entrust/plan-list-history
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对（不传则查询所有交易对）
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: 查询方向
        ranges: PREV;NEXT
    -
        name: id
        type: integer
        mandatory: false
        default:
        description: ID
        ranges:
    -
        name: limit
        type: integer
        mandatory: false
        default: "10"
        description: 数量限制
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default:
        description: 开始时间
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default:
        description: 结束时间
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey

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
              "error": {
                "code": "",
                "msg": ""
              },
              "msgInfo": "",
              "result": {
                "hasNext": false,
                "hasPrev": false,
                "items": [
                  {
                    "clientOrderId": "",
                    "closePosition": false,
                    "createdTime": 0,
                    "entrustId": 0,
                    "entrustType": "",
                    "marketOrderLevel": 0,
                    "orderSide": "",
                    "ordinary": true,
                    "origQty": 0,
                    "positionSide": "",
                    "price": 0,
                    "state": "",
                    "stopPrice": 0,
                    "symbol": "",
                    "timeInForce": "",
                    "triggerPriceType": ""
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
