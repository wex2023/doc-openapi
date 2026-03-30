---
title: Query Historical Take-Profit & Stop-Loss Orders
position_number: 24
type: get
description: /future/trade/v1/entrust/profit-list-history
parameters:
    -
        name: id
        type: integer
        mandatory: false
        default: "1"
        description: Page number
        ranges:
    -
        name: limit
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
        mandatory: false
        default:
        description: Trading pair
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: Pagination direction
        ranges: NEXT;PREVIOUS
content_markdown: >-
    #### Rate Limit


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_direction | Direction incorrect |

    | invalid_limit | Invalid limit parameter |

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
                    "profitId": "",
                    "symbol": "BTCUSDT",
                    "positionSide": "LONG",
                    "origQty": "0.020",
                    "leverage": 20,
                    "triggerPriceType": "MARK_PRICE",
                    "triggerProfitPrice": "68500.00",
                    "triggerStopPrice": "59500.00",
                    "entryPrice": "63250.80",
                    "positionSize": "0.020",
                    "isolatedMargin": "63.25",
                    "executedQty": "0.020",
                    "avgPrice": "68320.50",
                    "positionType": "ISOLATED",
                    "delegateQty": "0.020",
                    "delegatePrice": "68200.00",
                    "profitDelegateOrderType": "1",
                    "profitDelegateTimeInForce": "1",
                    "profitDelegatePrice": "68200.00",
                    "stopDelegateOrderType": "2",
                    "stopDelegateTimeInForce": "3",
                    "stopDelegatePrice": null,
                    "closeType": "ALL",
                    "state": "TRIGGERED",
                    "desc": "",
                    "triggerPriceSide": "PROFIT",
                    "createdTime": 1735689000000,
                    "updatedTime": 1735690123000,
                    "sourceType": "WEB",
                    "profitType": 0,
                    "mmrThreshold": null
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
