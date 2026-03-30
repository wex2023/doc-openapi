---
title: 创建跟踪单
position_number: 13
type: post
description: /future/trade/v1/entrust/create-track
parameters:
    -
        name: callback
        type: string
        mandatory: true
        default:
        description: 回调幅度配置
        ranges: FIXED;PROPORTION
    -
        name: callbackVal
        type: number
        mandatory: true
        default:
        description: 回调值（大于0）
        ranges: ">0"
    -
        name: orderSide
        type: string
        mandatory: true
        default:
        description: 订单方向
        ranges: BUY;SELL
    -
        name: origQty
        type: number
        mandatory: true
        default:
        description: 原始数量（张）
        ranges:
    -
        name: positionSide
        type: string
        mandatory: true
        default:
        description: 持仓方向
        ranges: BOTH;LONG;SHORT
    -
        name: positionType
        type: string
        mandatory: true
        default:
        description: 持仓类型
        ranges: CROSSED;ISOLATED
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对
        ranges:
    -
        name: triggerPriceType
        type: string
        mandatory: true
        default:
        description: 触发价格类型
        ranges: INDEX_PRICE;MARK_PRICE;LATEST_PRICE
    -
        name: activationPrice
        type: number
        mandatory: false
        default:
        description: 激活价格
        ranges:
    -
        name: clientMedia
        type: string
        mandatory: false
        default:
        description: 客户端媒介
        ranges:
    -
        name: clientMediaChannel
        type: string
        mandatory: false
        default:
        description: 客户端媒介渠道
        ranges:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: 客户端订单ID
        ranges:
    -
        name: expireTime
        type: integer
        mandatory: false
        default:
        description: 过期时间
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_symbol | 交易对不存在 |

    | symbol_is_not_trading | 交易对当前无法交易 |

    | symbol_not_support_openapi | 该交易对当前不支持通过 OpenAPI 下单 |

    | deposit_coupon_exists | 该抵扣券已领取或已绑定 |

    | exist_bonus_positon_not_create_reverse_position | 不可创建反向仓位 |

    | invalid_params | 参数设置有误或置空了 |

    | invalid_exceed_max_rate_limit | 回调幅度设置不能超过最大值 |

    | invalid_below_min_rate_limit | 回调幅度设置不能低于最小值 |

    | invalid_exceed_max_price_limit | 回调幅度设置不能超过最新成交价 |

    | invalid_exceed_min_price_limit | 回调率设置不能低于最新成交价 |

    | invalid_activation_price | 触发价格不合法 |

    | invalid_quantity_scale | 数量必须为整数 |

    | user_can_not_trade | 账户禁止交易 |

    | sub_account_not_trade | 子账户不可交易 |

    | user_can_not_open_position | 账户禁止开仓 |

    | symbol_is_not_open_position | 当前交易对已暂停开新仓 |

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
