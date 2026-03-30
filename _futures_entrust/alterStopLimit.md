---
title: Alter Stop Limit
position_number: 12
type: post
description: /future/trade/v1/entrust/update-profit-stop
parameters:
    -
        name: profitId
        type: integer
        mandatory: true
        default:
        description: Profit and Stop order ID
        ranges:
    -
        name: triggerProfitPrice
        type: number
        mandatory: false
        default:
        description: Take-profit trigger price
        ranges:
    -
        name: triggerStopPrice
        type: number
        mandatory: false
        default:
        description: Stop-loss trigger price
        ranges:
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_entrust | Profit ID does not exist |

    | user_can_not_trade | Account prohibited from trading |

    | sub_account_not_trade | Sub-account cannot trade |

    | user_can_not_open_position | Account restricted from opening positions |

    | invalid_order_type | Invalid order type |

    | invalid_trigger_profit_price | Invalid take-profit price |

    | invalid_trigger_stop_price | Invalid stop-loss price |

    | invalid_origQty | Invalid order quantity |

    | invalid_quantity_scale | Order quantity must be an integer |

    | invalid_time_in_force | Invalid time-in-force setting |

    | trigger_profit_price_less_than_entry_price | Take-profit price must be higher than entry price (long) |

    | trigger_profit_price_less_than_mark_price | Take-profit price must be higher than current mark price (long) |

    | trigger_profit_price_less_than_index_price | Take-profit price must be higher than current index price (long) |

    | trigger_profit_price_more_than_entry_price | Take-profit price must be lower than entry price (short) |

    | trigger_profit_price_more_than_mark_price | Take-profit price must be lower than current mark price (short) |

    | trigger_profit_price_more_than_index_price | Take-profit price must be lower than current index price (short) |

    | trigger_stop_price_less_than_entry_price | Stop-loss price must be higher than entry price (short) |

    | trigger_stop_price_less_than_mark_price | Stop-loss price must be higher than current mark price (short) |

    | trigger_stop_price_less_than_index_price | Stop-loss price must be higher than current index price (short) |

    | trigger_stop_price_more_than_entry_price | Stop-loss price must be lower than entry price (long) |

    | trigger_stop_price_more_than_mark_price | Stop-loss price must be lower than current mark price (long) |

    | trigger_stop_price_more_than_index_price | Stop-loss price must be lower than current index price (long) |

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
