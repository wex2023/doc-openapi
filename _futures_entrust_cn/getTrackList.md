---
title: "获取跟踪单列表（所有活跃）"
position_number: 16
type: get
description: /future/trade/v1/entrust/track-list
parameters:
    -
        name: page
        type: integer
        mandatory: false
        default: "1"
        description: 页码
        ranges:
    -
        name: size
        type: integer
        mandatory: false
        default: "10"
        description: 每页数量
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default:
        description: 结束时间
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default:
        description: 开始时间
        ranges:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对
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
                "items": [
                  {
                    "activationPrice": 0,
                    "avgPrice": 0,
                    "callback": "",
                    "callbackVal": 0,
                    "configActivation": false,
                    "createdTime": 0,
                    "currentPrice": 0,
                    "desc": "",
                    "executedQty": 0,
                    "orderSide": "",
                    "ordinary": true,
                    "origQty": 0,
                    "positionSide": "",
                    "price": 0,
                    "state": "",
                    "stopPrice": 0,
                    "symbol": "",
                    "trackId": 0,
                    "triggerPriceType": "",
                    "updatedTime": 0
                  }
                ],
                "page": 1,
                "ps": 10,
                "total": 20
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
