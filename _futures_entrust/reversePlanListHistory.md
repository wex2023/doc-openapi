---
title: Query Historical Reverse Plan
position_number: 27
type: get
description: /future/trade/v1/entrust/reverse-plan-list-history
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
    **Note:** This API can only query data within the last **5 minutes**.


    #### Rate Limit


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_position_type | Position type incorrect |

    | invalid_position_side | Position side incorrect |

    | invalid_profit_close_type | Position close type incorrect |

    | invalid_state | State incorrect |

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
                "hasNext": false,
                "hasPrev": false,
                "items": [
                  {
                    "entrustId": "",
                    "symbol": "",
                    "entrustType": "",
                    "orderSide": "",
                    "positionSide": "",
                    "timeInForce": "",
                    "closePosition": false,
                    "price": 0,
                    "origQty": 0,
                    "stopPrice": "",
                    "triggerPriceType": "",
                    "executedQty": 0,
                    "avgPrice": "",
                    "state": "",
                    "createdTime": "",
                    "updatedTime": "",
                    "clientOrderId": "",
                    "reverseOpenExecutedQty": 0,
                    "reverseOpenAvgPrice": 0,
                    "desc": ""
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
