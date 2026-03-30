---
title: 批量下单（新）
position_number: 4
type: post
description: /future/trade/v2/order/atomic-create-batch
parameters:
    -
        name: (JSON Array Body)
        type: array
        mandatory: true
        default:
        description: 请求体为 JSON 数组，每个元素代表一笔独立订单
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | gateway_decommission_ip_country | 很遗憾，我们无法向受限制国家/地区的用户提供服务 |

    | gateway_decommission_kyc_country | 很遗憾，我们无法向受限制国家/地区的用户提供服务 |

    | GATEWAY_0003 | 当前用户触发风控，您的操作已被暂时禁止 |

    | GATEWAY_0006 | 由于您触发风控规则，账户被锁定 |

    | GATEWAY_0007 | 由于您触发风控规则，账户被锁定 |

    | invalid_symbol | 交易对不存在 |

    | symbol_is_not_trading | 交易对当前不可交易 |

    | openapi_not_supported | 该交易对当前不支持API操作 |

    | symbol_is_not_open_position | 交易对当前不可持仓 |

    | invalid_params | 参数设置有误 |

    | invalid_quantity | origQty必须为整数 |

    | quantity_can_not_less_than * | origQty必须大于 * |

    | user_can_not_trade | 账户当前禁止交易 |

    | sub_account_not_trade | 子账户当前不可交易 |

    | user_can_not_open_position | 账户当前无法开仓 |

    | invalid_time_in_force | 时间设置不合法 |

    | invalid_price | 价格设置不合法 |

    | invalid_trigger_profit_price | 不合法的止盈价格 |

    | invalid_trigger_stop_price | 不合法的止损价格 |

    | trigger_profit_price_more_than_sell_one_price | 止盈触发价格需大于卖一价（多） |

    | trigger_profit_price_less_than_buy_one_price | 止盈触发价格需小于买一价（空） |

    | trigger_stop_price_more_than_sell_one_price | 止损触发价格需小于卖一价（多） |

    | trigger_stop_price_less_than_buy_one_price | 止损触发价格需大于买一价（空） |

    | trigger_profit_price_less_than_order_delegate_price | 触发止盈价格不可小于订单委托价格（多） |

    | trigger_profit_price_more_than_order_delegate_price | 触发止盈价格不可大于订单委托价格（空） |

    | trigger_stop_price_more_than_order_delegate_price | 触发止损价格不可大于订单委托价格（多） |

    | trigger_stop_price_less_than_order_delegate_price | 触发止损价格不可小于订单委托价格（空） |

    | on_board_30_minutes_limit_order_price_limit | 上板后30分钟内限价订单价格限制 |

    | order_create_size_exceed | 单次批量订单数超过上限，最大上限20订单 |

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
