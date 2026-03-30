---
title: 更新订单
position_number: 2
type: post
description: /future/trade/v1/order/update
parameters:
    -
        name: orderId
        type: number
        mandatory: true
        default:
        description: 订单 ID
        ranges:
    -
        name: price
        type: number
        mandatory: true
        default:
        description: 目标价格
        ranges:
    -
        name: origQty
        type: number
        mandatory: true
        default:
        description: 目标数量（张）
        ranges:
    -
        name: triggerProfitPrice
        type: number
        mandatory: false
        default:
        description: 止盈目标价格
        ranges:
    -
        name: triggerStopPrice
        type: number
        mandatory: false
        default:
        description: 止损价格
        ranges:
    -
        name: triggerPriceType
        type: string
        mandatory: false
        default: LATEST_PRICE
        description: 触发价格类型
        ranges: INDEX_PRICE; MARK_PRICE; LATEST_PRICE
    -
        name: profitDelegateOrderType
        type: string
        mandatory: false
        default:
        description: 止盈订单类型
        ranges: LIMIT; MARKET
    -
        name: profitDelegateTimeInForce
        type: string
        mandatory: false
        default:
        description: 止盈订单有效方式
        ranges: GTC; IOC; FOK; GTX
    -
        name: profitDelegatePrice
        type: number
        mandatory: false
        default:
        description: 止盈订单价格
        ranges:
    -
        name: stopDelegateOrderType
        type: string
        mandatory: false
        default:
        description: 止损订单类型
        ranges: LIMIT; MARKET
    -
        name: stopDelegateTimeInForce
        type: string
        mandatory: false
        default:
        description: 止损订单有效方式
        ranges: GTC; IOC; FOK; GTX
    -
        name: stopDelegatePrice
        type: number
        mandatory: false
        default:
        description: 止损订单价格
        ranges:
    -
        name: followUpOrder
        type: boolean
        mandatory: false
        default:
        description: 如果为 true，表示追单
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_order | Order id 不存在 |

    | invalid_params | 参数设置有误 |

    | invalid_quantity | origQty必须为整数 |

    | invalid_price | price设置不合法 |

    | invalid_trigger_profit_price | 止盈价格设置不合法 |

    | invalid_trigger_stop_price | 止损价格设置不合法 |

    | trigger_profit_price_less_than_order_delegate_price | 触发止盈价格不可小于订单委托价格（多） |

    | trigger_profit_price_more_than_order_delegate_price | 触发止盈价格不可大于订单委托价格（空） |

    | trigger_stop_price_more_than_order_delegate_price | 触发止损价格不可大于订单委托价格（多） |

    | trigger_stop_price_less_than_order_delegate_price | 触发止损价格不可小于订单委托价格（空） |

    | invalid_time_in_force | 无效的订单有效期 |

    | on_board_30_minutes_limit_order_price_limit | 上板后30分钟内限价订单价格限制 |

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
