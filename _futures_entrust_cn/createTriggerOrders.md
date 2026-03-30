---
title: 创建触发订单
position_number: 1
type: post
description: /future/trade/v1/entrust/create-plan
parameters:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: 客户端订单ID
        ranges:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对
        ranges:
    -
        name: orderSide
        type: string
        mandatory: true
        default:
        description: 订单方向
        ranges: BUY;SELL
    -
        name: entrustType
        type: string
        mandatory: true
        default:
        description: "委托类型：TAKE_PROFIT（止盈限价单）；STOP（止损限价单）；TAKE_PROFIT_MARKET（止盈市价单）；STOP_MARKET（止损市价单）"
        ranges: TAKE_PROFIT;STOP;TAKE_PROFIT_MARKET;STOP_MARKET
    -
        name: origQty
        type: number
        mandatory: true
        default:
        description: 数量（张）
        ranges:
    -
        name: price
        type: number
        mandatory: false
        default:
        description: 价格
        ranges:
    -
        name: stopPrice
        type: number
        mandatory: true
        default:
        description: 触发价格
        ranges:
    -
        name: timeInForce
        type: string
        mandatory: true
        default:
        description: "有效方式：GTC；IOC；FOK；GTX。市价单仅支持IOC"
        ranges: GTC;IOC;FOK;GTX
    -
        name: triggerPriceType
        type: string
        mandatory: true
        default:
        description: "触发价格类型"
        ranges: INDEX_PRICE;MARK_PRICE;LATEST_PRICE
    -
        name: positionSide
        type: string
        mandatory: true
        default:
        description: 持仓方向
        ranges: LONG;SHORT
content_markdown: >-
    Content-Type = application/x-www-form-urlencoded && application/json


    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | deposit_coupon_exists | 保证金优惠券已存在 |

    | exist_bonus_positon_not_create_reverse_position | 不允许创建反向仓位（存在赠金仓位） |

    | invalid_params | 有必填参数未填写 |

    | invalid_price | 某个价格参数填写有误；计划止盈/止损限价校验失败 |

    | market_plan_entrust_must_be_ioc_or_fok | 市价止盈/止损委托必须为 IOC 或 FOK |

    | invalid_stop_price | 止损价格有误 |

    | invalid_quantity_scale | 下单数量必须是整数 |

    | invalid_trigger_profit_price | 触发止盈价格有误 |

    | invalid_time_in_force | 计划委托止盈的 timeInForce 校验失败 |

    | on_board_30_minutes_limit_order_price_limit | 上板后 30 分钟内限价单价格限制 |

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
