---
title: Create Trigger Orders
position_number: 1
type: post
description: /future/trade/v1/entrust/create-plan
parameters:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: Client order ID
        ranges:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair
        ranges:
    -
        name: orderSide
        type: string
        mandatory: true
        default:
        description: Order side
        ranges: BUY;SELL
    -
        name: entrustType
        type: string
        mandatory: true
        default:
        description: "Order type: TAKE_PROFIT (Take Profit Limit); STOP (Stop Limit); TAKE_PROFIT_MARKET (Take Profit Market); STOP_MARKET (Stop Loss Market)"
        ranges: TAKE_PROFIT;STOP;TAKE_PROFIT_MARKET;STOP_MARKET
    -
        name: origQty
        type: number
        mandatory: true
        default:
        description: Quantity (Cont)
        ranges:
    -
        name: price
        type: number
        mandatory: false
        default:
        description: Price
        ranges:
    -
        name: stopPrice
        type: number
        mandatory: true
        default:
        description: Trigger price
        ranges:
    -
        name: timeInForce
        type: string
        mandatory: true
        default:
        description: "Valid way: GTC; IOC; FOK; GTX. Market orders only support IOC"
        ranges: GTC;IOC;FOK;GTX
    -
        name: triggerPriceType
        type: string
        mandatory: true
        default:
        description: "Trigger price type"
        ranges: INDEX_PRICE;MARK_PRICE;LATEST_PRICE
    -
        name: positionSide
        type: string
        mandatory: true
        default:
        description: Position side
        ranges: LONG;SHORT
content_markdown: >-
    Content-Type = application/x-www-form-urlencoded && application/json


    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | deposit_coupon_exists | Margin coupon already exists |

    | exist_bonus_positon_not_create_reverse_position | Reverse position not allowed when a bonus position exists |

    | invalid_params | Required parameter missing |

    | invalid_price | Invalid price; take-profit/stop-loss limit price validation failed |

    | market_plan_entrust_must_be_ioc_or_fok | Market TP/SL order must use IOC or FOK |

    | invalid_stop_price | Invalid stop price |

    | invalid_quantity_scale | Order quantity must be an integer |

    | invalid_trigger_profit_price | Invalid take-profit trigger price |

    | invalid_time_in_force | timeInForce validation failed for planned take-profit order |

    | on_board_30_minutes_limit_order_price_limit | Limit order price restriction within first 30 minutes after listing |

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
              "result": {},
              "returnCode": 0
            }
        title: Response
        language: json
---
