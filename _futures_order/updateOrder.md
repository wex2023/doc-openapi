---
title: Update Orders
position_number: 2
type: post
description: /future/trade/v1/order/update
parameters:
    -
        name: orderId
        type: number
        mandatory: true
        default:
        description: Order ID
        ranges:
    -
        name: price
        type: number
        mandatory: true
        default:
        description: Target price
        ranges:
    -
        name: origQty
        type: number
        mandatory: true
        default:
        description: Target quantity (cont)
        ranges:
    -
        name: triggerProfitPrice
        type: number
        mandatory: false
        default:
        description: Profit target price
        ranges:
    -
        name: triggerStopPrice
        type: number
        mandatory: false
        default:
        description: Stop-Loss price
        ranges:
    -
        name: triggerPriceType
        type: string
        mandatory: false
        default: LATEST_PRICE
        description: Trigger price type
        ranges: INDEX_PRICE; MARK_PRICE; LATEST_PRICE
    -
        name: profitDelegateOrderType
        type: string
        mandatory: false
        default:
        description: Take-Profit order type
        ranges: LIMIT; MARKET
    -
        name: profitDelegateTimeInForce
        type: string
        mandatory: false
        default:
        description: Take-Profit order validity method
        ranges: GTC; IOC; FOK; GTX
    -
        name: profitDelegatePrice
        type: number
        mandatory: false
        default:
        description: Take-Profit order price
        ranges:
    -
        name: stopDelegateOrderType
        type: string
        mandatory: false
        default:
        description: Stop-Loss order type
        ranges: LIMIT; MARKET
    -
        name: stopDelegateTimeInForce
        type: string
        mandatory: false
        default:
        description: Stop-Loss order validity method
        ranges: GTC; IOC; FOK; GTX
    -
        name: stopDelegatePrice
        type: number
        mandatory: false
        default:
        description: Stop-Loss order price
        ranges:
    -
        name: followUpOrder
        type: boolean
        mandatory: false
        default:
        description: If true, indicates chase order
        ranges:
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_order | Order ID does not exist |

    | invalid_params | Invalid parameter setting |

    | invalid_quantity | origQty must be an integer |

    | invalid_price | Invalid price setting |

    | invalid_trigger_profit_price | Invalid take-profit price setting |

    | invalid_trigger_stop_price | Invalid stop-loss price setting |

    | trigger_profit_price_less_than_order_delegate_price | Take-profit trigger price cannot be lower than the order price (Long) |

    | trigger_profit_price_more_than_order_delegate_price | Take-profit trigger price cannot be higher than the order price (Short) |

    | trigger_stop_price_more_than_order_delegate_price | Stop-loss trigger price cannot be higher than the order price (Long) |

    | trigger_stop_price_less_than_order_delegate_price | Stop-loss trigger price cannot be lower than the order price (Short) |

    | invalid_time_in_force | Invalid order time-in-force |

    | on_board_30_minutes_limit_order_price_limit | Limit order price restriction within 30 minutes after listing |

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
