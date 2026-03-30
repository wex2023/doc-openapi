---
title: See Transaction Details
position_number: 12
type: get
description: /future/trade/v1/order/trade-list
parameters:
    -
        name: orderId
        type: integer
        mandatory: false
        default:
        description: Order ID
        ranges:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair
        ranges:
    -
        name: page
        type: integer
        mandatory: false
        default: 1
        description: Page
        ranges:
    -
        name: size
        type: integer
        mandatory: false
        default: 10
        description: Quantity of a single page
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
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_page | Page number must be a positive integer |

    | invalid_size | The maximum value of size is 100 |

    | invalid_symbol | The trading pair does not exist |

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
                    "fee": 0,
                    "feeCoin": "",
                    "orderId": 0,
                    "execId": 0,
                    "price": 0,
                    "quantity": 0,
                    "symbol": "",
                    "timestamp": 0,
                    "takerMaker": "TAKER"
                  }
                ],
                "page": 0,
                "ps": 0,
                "total": 0
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
