---
title: "See Order History (Quant)"
position_number: 15
type: get
description: /future/trade/v1/order/quant/list-history
parameters:
    -
        name: id
        type: long
        mandatory: false
        default:
        description: Cursor ID for pagination, the last orderId from previous response
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
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair
        ranges:
    -
        name: forceClose
        type: boolean
        mandatory: false
        default: "false"
        description: Whether to query forced liquidation orders
        ranges:
    -
        name: startTime
        type: long
        mandatory: false
        default:
        description: Start time (millisecond timestamp), earliest 90 days ago
        ranges:
    -
        name: endTime
        type: long
        mandatory: false
        default:
        description: End time (millisecond timestamp)
        ranges:
    -
        name: origType
        type: integer
        mandatory: false
        default:
        description: "Conditional order type: 1=Limit TP, 2=Limit SL, 3=Market TP, 4=Market SL"
        ranges:
    -
        name: orderSide
        type: integer
        mandatory: false
        default:
        description: "Order side: 1=Buy, 2=Sell"
        ranges:
    -
        name: states
        type: list
        mandatory: false
        default:
        description: "Order states: 2=Partially Filled, 3=Filled, 4=Canceled, 6=Expired"
        ranges:
    -
        name: orderOrigType
        type: integer
        mandatory: false
        default:
        description: "Order type: 1=Limit, 2=Market, 3=Limit TP/SL, 4=Market TP/SL, 5=MMR Stop Loss"
        ranges:
    -
        name: welfareAccount
        type: boolean
        mandatory: false
        default: "false"
        description: Whether to query bonus account
        ranges:
content_markdown: >-
    Quant account dedicated historical order query interface, supports cursor pagination, returns up to 2000 records.


    #### Limit Flow Rules


    200/s/apikey


    #### Cursor Pagination Guide


    1. **First request**: Do not pass the `id` parameter

    2. **Next page**: Use the last record's ID from the previous response as the `id` parameter, with `direction=NEXT`

    3. **Previous page**: Use the first record's ID from the current list as the `id` parameter, with `direction=PREV`

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
                    "orderId": 123456789,
                    "clientOrderId": "",
                    "symbol": "btc_usdt",
                    "orderSide": "BUY",
                    "orderType": "LIMIT",
                    "positionSide": "LONG",
                    "price": "50000.00",
                    "origQty": "0.1",
                    "executedQty": "0.1",
                    "avgPrice": "50000.00",
                    "state": "FILLED",
                    "closePosition": false,
                    "closeProfit": "100.00",
                    "marginFrozen": "0",
                    "forceClose": false,
                    "sourceId": 0,
                    "timeInForce": "GTC",
                    "triggerProfitPrice": "0",
                    "triggerStopPrice": "0",
                    "createdTime": 1703520000000,
                    "updatedTime": 1703520100000
                  }
                ]
              }
            }
        title: Response
        language: json
---
