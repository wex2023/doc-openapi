---
title: "See Transaction Details (Quant)"
position_number: 16
type: get
description: /future/trade/v1/order/quant/trade-list
parameters:
    -
        name: id
        type: long
        mandatory: false
        default:
        description: Cursor ID for pagination (the last execId from previous response)
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: Pagination direction
        ranges: PREV;NEXT
    -
        name: limit
        type: integer
        mandatory: false
        default: 10
        description: Number of records per page, max 2000
        ranges:
    -
        name: orderId
        type: long
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
        name: startTime
        type: long
        mandatory: false
        default:
        description: Start time (millisecond timestamp)
        ranges:
    -
        name: endTime
        type: long
        mandatory: false
        default:
        description: End time (millisecond timestamp)
        ranges:
    -
        name: welfareAccount
        type: boolean
        mandatory: false
        default: "false"
        description: Whether to query bonus account
        ranges:
content_markdown: >-
    Quant account dedicated transaction details query interface, supports cursor pagination, returns up to 2000 records.


    #### Limit Flow Rules


    200/s/apikey


    #### Cursor Pagination Guide


    1. **First request**: Do not pass the `id` parameter

    2. **Next page**: Use the last record's `execId` from the previous response as the `id` parameter, with `direction=NEXT`

    3. **Previous page**: Use the first record's `execId` from the current list as the `id` parameter, with `direction=PREV`

    4. **Check for more data**: Use `hasNext` and `hasPrev` fields


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | not_quantification_account | Not a quant account, no permission to access this interface |

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
              "returnCode": 0,
              "msgInfo": "",
              "error": {
                "code": "",
                "msg": ""
              },
              "result": {
                "hasPrev": false,
                "hasNext": true,
                "items": [
                  {
                    "execId": 987654321,
                    "orderId": 123456789,
                    "symbol": "btc_usdt",
                    "price": "50000.00",
                    "quantity": "0.05",
                    "quoteQty": "2500.00",
                    "fee": "1.25",
                    "feeCoin": "USDT",
                    "takerMaker": "TAKER",
                    "timestamp": 1703520050000
                  }
                ]
              }
            }
        title: Response
        language: json
---
