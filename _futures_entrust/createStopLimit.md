---
title: Create Stop Limit
position_number: 7
type: post
description: /future/trade/v1/entrust/create-profit
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair
        ranges:
    -
        name: origQty
        type: integer
        mandatory: true
        default:
        description: Quantity (contracts)
        ranges:
    -
        name: triggerProfitPrice
        type: integer
        mandatory: true
        default:
        description: Take-profit trigger price
        ranges:
    -
        name: triggerStopPrice
        type: integer
        mandatory: true
        default:
        description: Stop-loss trigger price
        ranges:
    -
        name: expireTime
        type: integer
        mandatory: true
        default:
        description: Expiration time (timestamp)
        ranges:
    -
        name: positionSide
        type: string
        mandatory: true
        default:
        description: Position side
        ranges: LONG;SHORT
    -
        name: profitDelegateOrderType
        type: string
        mandatory: true
        default:
        description: Take-profit order type
        ranges: LIMIT;MARKET
    -
        name: profitDelegateTimeInForce
        type: string
        mandatory: true
        default:
        description: Take-profit order time in force
        ranges: GTC;FOK;IOC;GTX
    -
        name: profitDelegatePrice
        type: number
        mandatory: false
        default:
        description: Take-profit order price
        ranges:
    -
        name: stopDelegateOrderType
        type: string
        mandatory: true
        default:
        description: Stop-loss order type
        ranges: LIMIT;MARKET
    -
        name: stopDelegateTimeInForce
        type: string
        mandatory: true
        default:
        description: Stop-loss order time in force
        ranges: GTC;FOK;IOC;GTX
    -
        name: stopDelegatePrice
        type: number
        mandatory: false
        default:
        description: Stop-loss order price
        ranges:
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_time_in_force | Failed to set time-in-force for TP/SL |

    | invalid_params | Invalid or missing parameters |

    | invalid_quantity_scale | Quantity must be a positive integer |

    | invalid_trigger_profit_price | Invalid take-profit trigger price |

    | invalid_trigger_stop_price | Invalid stop-loss trigger price |

    | quantity_can_not_less_than | Order quantity is below the minimum limit |

    | invalid_price | Invalid price setting |

    | more_than_available | Exceeds available quantity |

    | trigger_profit_price_less_than_entry_price | Take-profit price must be higher than entry price (LONG) |

    | trigger_profit_price_less_than_mark_price | Take-profit price must be higher than mark price (LONG) |

    | trigger_profit_price_less_than_index_price | Take-profit price must be higher than index price (LONG) |

    | trigger_profit_price_more_than_entry_price | Take-profit price must be lower than entry price (SHORT) |

    | trigger_profit_price_more_than_mark_price | Take-profit price must be lower than mark price (SHORT) |

    | trigger_profit_price_more_than_index_price | Take-profit price must be lower than index price (SHORT) |

    | trigger_stop_price_less_than_entry_price | Stop-loss price must be higher than entry price (SHORT) |

    | trigger_stop_price_less_than_mark_price | Stop-loss price must be higher than mark price (SHORT) |

    | trigger_stop_price_less_than_index_price | Stop-loss price must be higher than index price (SHORT) |

    | trigger_stop_price_more_than_entry_price | Stop-loss price must be lower than entry price (LONG) |

    | trigger_stop_price_more_than_mark_price | Stop-loss price must be lower than mark price (LONG) |

    | trigger_stop_price_more_than_index_price | Stop-loss price must be lower than index price (LONG) |

    | user_can_not_trade | Account prohibited from trading |

    | sub_account_not_trade | Sub-account not allowed to trade |

    | user_can_not_open_position | Account restricted from opening positions |

    | invalid_symbol | Trading pair does not exist |

    | symbol_is_not_trading | Trading pair is not in trading state |

    | symbol_is_not_open_position | Trading pair not open for position |

    | symbol_not_support_openapi | The trading pair does not support placing orders through OpenAPI |

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
              "result": true,
              "returnCode": 0
            }
        title: Response
        language: json
---
