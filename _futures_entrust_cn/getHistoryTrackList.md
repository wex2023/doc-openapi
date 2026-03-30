---
title: "获取历史跟踪单列表（非活跃）"
position_number: 19
type: get
description: /future/trade/v1/entrust/track-list-history
parameters:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: 翻页方向
        ranges: PREV;NEXT
    -
        name: limit
        type: integer
        mandatory: false
        default: "10"
        description: 数量限制
        ranges:
    -
        name: id
        type: integer
        mandatory: false
        default:
        description: 记录ID
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


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_symbol | 交易对不存在 |

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
                "hasNext": true,
                "hasPre": true,
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
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
