---
title: 修改止盈止损
position_number: 12
type: post
description: /future/trade/v1/entrust/update-profit-stop
parameters:
    -
        name: profitId
        type: integer
        mandatory: true
        default:
        description: 止盈止损订单ID
        ranges:
    -
        name: triggerProfitPrice
        type: number
        mandatory: false
        default:
        description: 止盈触发价格
        ranges:
    -
        name: triggerStopPrice
        type: number
        mandatory: false
        default:
        description: 止损触发价格
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_entrust | Profit ID 不存在 |

    | user_can_not_trade | 账户禁止交易 |

    | sub_account_not_trade | 子账户不可交易 |

    | user_can_not_open_position | 账户禁止开仓 |

    | invalid_order_type | 无效订单类型 |

    | invalid_trigger_profit_price | 止盈价格不合法 |

    | invalid_trigger_stop_price | 止损价格不合法 |

    | invalid_origQty | 下单数量不合法 |

    | invalid_quantity_scale | 下单数量必须为整数 |

    | invalid_time_in_force | 时间设置不合法 |

    | trigger_profit_price_less_than_entry_price | 止盈价格必须高于开仓价（多） |

    | trigger_profit_price_less_than_mark_price | 止盈价格必须高于当前标记价（多） |

    | trigger_profit_price_less_than_index_price | 止盈价格必须高于当前指数价（多） |

    | trigger_profit_price_more_than_entry_price | 止盈价格必须低于开仓价（空） |

    | trigger_profit_price_more_than_mark_price | 止盈价格必须低于当前标记价（空） |

    | trigger_profit_price_more_than_index_price | 止盈价格必须低于当前指数价（空） |

    | trigger_stop_price_less_than_entry_price | 止损价格必须高于开仓价（空） |

    | trigger_stop_price_less_than_mark_price | 止损价格必须高于当前标记价（空） |

    | trigger_stop_price_less_than_index_price | 止损价格必须高于当前指数价（空） |

    | trigger_stop_price_more_than_entry_price | 止损价格必须低于开仓价（多） |

    | trigger_stop_price_more_than_mark_price | 止损价格必须低于当前标记价（多） |

    | trigger_stop_price_more_than_index_price | 止损价格必须低于当前指数价（多） |

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
