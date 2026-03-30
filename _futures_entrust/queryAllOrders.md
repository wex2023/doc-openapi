---
title: Query All Orders
position_number: 30
type: get
description: /future/trade/v1/order-entrust/list
parameters:
    -
        name: page
        type: integer
        mandatory: false
        default: "1"
        description: Page number
        ranges:
    -
        name: size
        type: integer
        mandatory: false
        default: "10"
        description: Page size
        ranges:
    -
        name: startTime
        type: long
        mandatory: false
        default:
        description: Start time
        ranges:
    -
        name: endTime
        type: long
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
    -
        name: type
        type: string
        mandatory: false
        default: ORDER
        description: "Type of entrust order: ORDER (limit/market) or ENTRUST (plan order)"
        ranges:
    -
        name: state
        type: string
        mandatory: false
        default:
        description: Order state
        ranges: NEW;PARTIALLY_FILLED;FILLED;CANCELED;REJECTED;PLACED;UNFINISHED;HISTORY
    -
        name: forceClose
        type: bool
        mandatory: false
        default: "false"
        description: Whether forced liquidation
        ranges:
content_markdown: >-
    #### Rate Limit


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_size | Invalid size parameter |

    | invalid_page | Invalid page parameter |

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
              "result": {
                "page": 1,
                "ps": 10,
                "total": 99,
                "items": [
                  {
                    "id": "1876543210987654321",
                    "type": "ORDER",
                    "symbol": "BTCUSDT",
                    "orderType": "LIMIT",
                    "orderSide": "BUY",
                    "positionSide": "LONG",
                    "timeInForce": "GTC",
                    "closePosition": false,
                    "price": "67200.00",
                    "origQty": "0.015",
                    "avgPrice": "67234.50",
                    "executedQty": "0.015",
                    "marginFrozen": "50.42",
                    "leverage": 25,
                    "state": "FILLED",
                    "createdTime": 1735698000000,
                    "updatedTime": 1735698765000,
                    "positionType": "ISOLATED"
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
