---
title: 根据EntrustId查看触发订单
position_number: 5
type: get
description: /future/trade/v1/entrust/plan-detail
parameters:
    -
        name: entrustId
        type: integer
        mandatory: true
        default:
        description: 订单ID
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_entrust_Id | 订单ID有误 |

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
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
