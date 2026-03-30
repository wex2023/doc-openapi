---
title: Get Leverage Info
position_number: 32
type: get
description: /future/trade/v1/position/leverage/list
parameters:
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

    | invalid_symbol | Trading pair does not exist |

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
                    "symbol": "BTCUSDT",
                    "accountId": "",
                    "positionType": "ISOLATED",
                    "positionSide": "LONG",
                    "contractType": "PERPETUAL",
                    "leverage": 25
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
