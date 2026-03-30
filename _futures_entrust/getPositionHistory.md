---
title: Get Position History
position_number: 33
type: get
description: /future/trade/v1/position/list-history
parameters:
    -
        name: id
        type: integer
        mandatory: false
        default: "1"
        description: Page number
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: Pagination direction
        ranges: NEXT;PREVIOUS
    -
        name: limit
        type: integer
        mandatory: false
        default: "10"
        description: Page size
        ranges:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair
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
        name: positionType
        type: integer
        mandatory: false
        default:
        description: "Position mode (1 Cross, 2 Isolated; empty = all)"
        ranges:
    -
        name: isFullClose
        type: integer
        mandatory: false
        default:
        description: "Close type (0 Partial, 1 Full; empty = all)"
        ranges:
content_markdown: >-
    #### Rate Limit


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_direction | Direction incorrect |

    | invalid_limit | Limit parameter incorrect |

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
                    "id": "1987654321098765432",
                    "positionSide": "LONG",
                    "contractType": "PERPETUAL",
                    "symbol": "BTCUSDT",
                    "positionType": 2,
                    "closeProfit": "127.83",
                    "closePositionSize": "0.050",
                    "closeOpenPrice": "63250.80",
                    "closePrice": "65808.60",
                    "maxPositionSize": "0.080",
                    "openTime": 1735608000000,
                    "closeTime": 1735699200000,
                    "startLeverage": 25,
                    "endLeverage": 25,
                    "working": false,
                    "force": false,
                    "forceMarkPrice": null,
                    "totalFee": "18.92",
                    "totalFundFee": "3.41",
                    "welfareAccount": false
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
