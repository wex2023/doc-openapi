---
title: "Query All Trade Details (No pagination)"
position_number: 29
type: get
description: /future/trade/v1/order/trade-list-all
parameters:
    -
        name: orderId
        type: integer
        mandatory: false
        default:
        description: Order ID
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default:
        description: Start time
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
        mandatory: false
        default:
        description: Trading pair
        ranges:
content_markdown: >-
    #### Rate Limit


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_limit | Invalid limit parameter setting |

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
                  "orderId": "1876543210987654321",
                  "execId": "2876543210987654322",
                  "symbol": "BTCUSDT",
                  "contractSize": 0.001,
                  "quantity": "0.015",
                  "price": "67234.80",
                  "fee": "10.08522",
                  "couponDeductFee": "3.00000",
                  "bonusDeductFee": "2.00000",
                  "feeCoin": "USDT",
                  "timestamp": 1735698765432,
                  "takerMaker": "TAKER",
                  "orderSide": "BUY",
                  "positionSide": "LONG"
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
