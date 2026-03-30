---
title: 创建订单
position_number: 1
type: post
description: /future/trade/v1/order/create
parameters:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: 客户订单 ID
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
        name: orderType
        type: string
        mandatory: true
        default:
        description: 订单类型
        ranges: LIMIT;MARKET
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
        name: timeInForce
        type: string
        mandatory: false
        default: GTC
        description: 有效方式
        ranges: GTC;IOC;FOK;GTX
    -
        name: triggerProfitPrice
        type: number
        mandatory: false
        default:
        description: 止盈价格
        ranges:
    -
        name: triggerStopPrice
        type: number
        mandatory: false
        default:
        description: 止损价格
        ranges:
    -
        name: positionSide
        type: string
        mandatory: true
        default:
        description: 仓位方向
        ranges: LONG;SHORT
content_markdown: >-
    #### OrigQty 计算公式


    `origQty = Truncate((Balance * Percent * Leverage) / (Mark_price * Contract_size))`


    - **Truncate**：取整数部分

    - **Balance**：`(walletBalance - openOrderMarginFrozen)`，API：`/future/user/v1/compat/balance/list`

    - **Percent**：用户输入，例如：`0.2`

    - **Leverage**：杠杆倍数，例如：`20`

    - **Mark_price**：市场标记价格，例如：`88888`（btc_usdt）

    - **Contract_size**：合约面值，API：`/future/market/v1/public/symbol/detail`


    举例：`truncate(10000 * 0.2 * 20 / 88888 / 0.0001) = 4500`


    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | contract_not_open | 合约未开户 |

    | exist_bonus_positon_not_create_reverse_position | 无法创建反向仓位 |

    | account_error | 账户无体验金权限 |

    | symbol_is_not_open_position | 交易对未开市 |

    | invalid_params | 参数填写错误 |

    | invalid_quantity_scale | origQty 必须是整数 |

    | coupon_unavailable | 优惠券不可用 |

    | welfare_coupon_not_exist | 优惠券不存在 |

    | coupon_exceed_max_leverage | 优惠券超过最大杠杆 |

    | exceed_max_leverage | 超过最大杠杆 |

    | gateway_decommission_ip_country | 很遗憾，我们无法向受限制国家/地区的用户提供服务 |

    | gateway_decommission_kyc_country | 很遗憾，我们无法向受限制国家/地区的用户提供服务 |

    | GATEWAY_0003 | 当前用户触发风控，您的操作已被暂时禁止 |

    | GATEWAY_0006 | 由于您触发风控规则，账户被锁定 |

    | GATEWAY_0007 | 由于您触发风控规则，账户被锁定 |

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
