---
title: See Stop Limit
position_number: 10
type: get
description: /future/trade/v1/entrust/profit-list
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair (if not provided, query all pairs)
        ranges:
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
        description: Number per page
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
        name: state
        type: string
        mandatory: true
        default:
        description: "Order state"
        ranges: NOT_TRIGGERED;TRIGGERING;TRIGGERED;USER_REVOCATION;PLATFORM_REVOCATION;EXPIRED;UNFINISHED;HISTORY
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_symbol | Trading pair does not exist |

    | invalid_position_type | Invalid position type |

    | invalid_position_side | Invalid position side |

    | invalid_state | Invalid state type |

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
                    "triggerStopPrice": 0,
                    "profitDelegateOrderType": "LIMIT",
                    "profitDelegatePrice": 0,
                    "profitDelegateTimeInForce": "GTC",
                    "stopDelegateOrderType": "LIMIT",
                    "stopDelegatePrice": 0,
                    "stopDelegateTimeInForce": "GTC"
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
