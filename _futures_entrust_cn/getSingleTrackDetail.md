---
title: 获取单个跟踪单详情
position_number: 15
type: get
description: /future/trade/v1/entrust/track-detail
parameters:
    -
        name: trackId
        type: integer
        mandatory: true
        default:
        description: 跟踪单ID
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_track_Id | 跟踪单不存在 |

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
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
