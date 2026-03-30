---
title: See Stop Limit by ProfitId
position_number: 11
type: get
description: /future/trade/v1/entrust/profit-detail
parameters:
    -
        name: profitId
        type: integer
        mandatory: true
        default:
        description: Profit and Stop order ID
        ranges:
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_profit_id | Profit ID does not exist |

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
                "createdTime": 0,
                "entryPrice": 0,
                "executedQty": 0,
                "isolatedMargin": 0,
                "origQty": 0,
                "positionSide": "",
                "positionSize": 0,
                "profitId": 0,
                "state": "",
                "symbol": "",
                "triggerProfitPrice": 0,
                "triggerStopPrice": 0
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
