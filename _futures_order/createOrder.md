---
title: Create Orders
position_number: 1
type: post
description: /future/trade/v1/order/create
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
        name: orderType
        type: string
        mandatory: true
        default:
        description: Order type
        ranges: LIMIT;MARKET
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
        name: timeInForce
        type: string
        mandatory: false
        default: GTC
        description: Valid way
        ranges: GTC;IOC;FOK;GTX
    -
        name: triggerProfitPrice
        type: number
        mandatory: false
        default:
        description: Stop profit price
        ranges:
    -
        name: triggerStopPrice
        type: number
        mandatory: false
        default:
        description: Stop loss price
        ranges:
    -
        name: positionSide
        type: string
        mandatory: true
        default:
        description: Position side
        ranges: LONG;SHORT
content_markdown: >-
    #### OrigQty Calculation Formula


    `origQty = Truncate((Balance * Percent * Leverage) / (Mark_price * Contract_size))`


    - **Truncate**: Take the integer part (discard decimals).

    - **Balance**: `(walletBalance - openOrderMarginFrozen)`, API: `/future/user/v1/compat/balance/list`

    - **Percent**: User input value, e.g., `0.2`

    - **Leverage**: Leverage multiplier, e.g., `20`

    - **Mark_price**: Market mark price, e.g., `88888` (`btc_usdt`)

    - **Contract_size**: Contract face value, API: `/future/market/v1/public/symbol/detail`


    Example: `truncate(10000 * 0.2 * 20 / 88888 / 0.0001) = 4500`


    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | contract_not_open | Contract not opened |

    | exist_bonus_positon_not_create_reverse_position | Unable to create reverse position |

    | account_error | Account has no trial fund permission |

    | symbol_is_not_open_position | Trading pair is not open |

    | invalid_params | Invalid parameters |

    | invalid_quantity_scale | origQty must be an integer |

    | coupon_unavailable | Coupon unavailable |

    | welfare_coupon_not_exist | Coupon does not exist |

    | coupon_exceed_max_leverage | Coupon exceeds maximum leverage |

    | exceed_max_leverage | Exceeds maximum leverage |

    | gateway_decommission_ip_country | Services not available to users from restricted countries/regions |

    | gateway_decommission_kyc_country | Services not available to users from restricted countries/regions |

    | GATEWAY_0003 | The user has triggered risk control; operation temporarily prohibited |

    | GATEWAY_0006 | Account locked due to triggering risk control rules |

    | GATEWAY_0007 | Account locked due to triggering risk control rules |

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
