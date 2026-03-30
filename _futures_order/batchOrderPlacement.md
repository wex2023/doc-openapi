---
title: Batch Order Placement
position_number: 4
type: post
description: /future/trade/v2/order/atomic-create-batch
parameters:
    -
        name: (JSON Array Body)
        type: array
        mandatory: true
        default:
        description: Request body is a JSON array, where each element represents an individual order
        ranges:
content_markdown: >-
    #### Rate Limit


    200 requests/second per apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | gateway_decommission_ip_country | Services not available to users from restricted countries/regions |

    | gateway_decommission_kyc_country | Services not available to users from restricted countries/regions |

    | GATEWAY_0003 | The user has triggered risk control; operation temporarily blocked |

    | GATEWAY_0006 | Account locked due to risk control |

    | GATEWAY_0007 | Account locked due to risk control |

    | invalid_symbol | The trading pair does not exist |

    | symbol_is_not_trading | The trading pair is not currently available for trading |

    | openapi_not_supported | The trading pair does not support OpenAPI operations |

    | symbol_is_not_open_position | The trading pair cannot open positions |

    | invalid_params | Invalid parameters |

    | invalid_quantity | origQty must be an integer |

    | quantity_can_not_less_than * | origQty must be greater than * |

    | user_can_not_trade | The account is currently prohibited from trading |

    | sub_account_not_trade | The sub-account is not allowed to trade |

    | user_can_not_open_position | The account cannot open new positions |

    | invalid_time_in_force | Invalid timeInForce parameter |

    | invalid_price | Invalid price setting |

    | invalid_trigger_profit_price | Invalid take-profit trigger price |

    | invalid_trigger_stop_price | Invalid stop-loss trigger price |

    | trigger_profit_price_more_than_sell_one_price | Take-profit trigger price must be higher than the best ask (long position) |

    | trigger_profit_price_less_than_buy_one_price | Take-profit trigger price must be lower than the best bid (short position) |

    | trigger_stop_price_more_than_sell_one_price | Stop-loss trigger price must be lower than the best ask (long position) |

    | trigger_stop_price_less_than_buy_one_price | Stop-loss trigger price must be higher than the best bid (short position) |

    | trigger_profit_price_less_than_order_delegate_price | Take-profit trigger price cannot be lower than the order price (long) |

    | trigger_profit_price_more_than_order_delegate_price | Take-profit trigger price cannot be higher than the order price (short) |

    | trigger_stop_price_more_than_order_delegate_price | Stop-loss trigger price cannot be higher than the order price (long) |

    | trigger_stop_price_less_than_order_delegate_price | Stop-loss trigger price cannot be lower than the order price (short) |

    | on_board_30_minutes_limit_order_price_limit | Limit order price restrictions apply within 30 minutes of listing |

    | order_create_size_exceed | The number of orders in a single batch exceeds the maximum limit (20 orders) |

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
              "result": "",
              "returnCode": 0
            }
        title: Response
        language: json
---
