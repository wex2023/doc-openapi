---
title: 创建止盈止损
position_number: 7
type: post
description: /future/trade/v1/entrust/create-profit
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对
        ranges:
    -
        name: origQty
        type: integer
        mandatory: true
        default:
        description: 数量（张）
        ranges:
    -
        name: triggerProfitPrice
        type: integer
        mandatory: true
        default:
        description: 止盈触发价格
        ranges:
    -
        name: triggerStopPrice
        type: integer
        mandatory: true
        default:
        description: 止损触发价格
        ranges:
    -
        name: expireTime
        type: integer
        mandatory: true
        default:
        description: 过期时间（timestamp）
        ranges:
    -
        name: positionSide
        type: string
        mandatory: true
        default:
        description: 持仓方向
        ranges: LONG;SHORT
    -
        name: profitDelegateOrderType
        type: string
        mandatory: true
        default:
        description: 止盈委托订单类型
        ranges: LIMIT;MARKET
    -
        name: profitDelegateTimeInForce
        type: string
        mandatory: true
        default:
        description: 止盈委托订单有效期
        ranges: GTC;FOK;IOC;GTX
    -
        name: profitDelegatePrice
        type: number
        mandatory: false
        default:
        description: 止盈委托价格
        ranges:
    -
        name: stopDelegateOrderType
        type: string
        mandatory: true
        default:
        description: 止损委托订单类型
        ranges: LIMIT;MARKET
    -
        name: stopDelegateTimeInForce
        type: string
        mandatory: true
        default:
        description: 止损委托订单有效期
        ranges: GTC;FOK;IOC;GTX
    -
        name: stopDelegatePrice
        type: number
        mandatory: false
        default:
        description: 止损委托价格
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_time_in_force | 止盈止损时间设置失败 |

    | invalid_params | 参数设置有误或置空 |

    | invalid_quantity_scale | 数量须为正整数 |

    | invalid_trigger_profit_price | 止盈触发价格有误 |

    | invalid_trigger_stop_price | 止损触发价格有误 |

    | quantity_can_not_less_than | 下单数量小于最小限制 |

    | invalid_price | 价格设置有误 |

    | more_than_available | 超过了可提供的数量 |

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

    | user_can_not_trade | 账户禁止交易 |

    | sub_account_not_trade | 子账户禁止交易 |

    | user_can_not_open_position | 账户限制开仓 |

    | invalid_symbol | 不存在该交易对 |

    | symbol_is_not_trading | 交易对未在交易状态 |

    | symbol_is_not_open_position | 交易对未在开启状态 |

    | symbol_not_support_openapi | 该交易对当前不支持通过 OpenAPI 下单 |

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
