---
title: Query Historical Filled Orders
position_number: 28
type: get
description: /future/trade/v1/order/trade-history
parameters:
    -
        name: limit
        type: integer
        mandatory: false
        default: "10"
        description: Quantity (Max 500)
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default:
        description: "Start time (default: query data from 90 days ago)"
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default:
        description: End time
        ranges:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair
        ranges:
content_markdown: >-
    #### Rate Limit


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_symbol | Invalid trading pair |

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
              "result": [
                {
                  "symbol": "BTCUSDT",
                  "orderSide": "BUY",
                  "avgPrice": "67234.50",
                  "origQty": "0.012",
                  "executedQty": "0.012",
                  "updatedTime": 1735698765000
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
