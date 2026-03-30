---
title: See Trigger Orders by EntrustId
position_number: 5
type: get
description: /future/trade/v1/entrust/plan-detail
parameters:
    -
        name: entrustId
        type: integer
        mandatory: true
        default:
        description: Order ID
        ranges:
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_entrust_Id | Invalid order ID |

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
