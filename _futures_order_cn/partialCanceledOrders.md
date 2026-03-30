---
title: 查询部分成交部分撤销订单
position_number: 13
type: get
description: /future/trade/v2/order/partial-canceled-orders
parameters:
    -
        name: page
        type: integer
        mandatory: true
        default: 1
        description: 页码
        ranges:
    -
        name: size
        type: integer
        mandatory: true
        default: 10
        description: 单页数量
        ranges:
    -
        name: startTime
        type: integer
        mandatory: true
        default:
        description: 开始时间（起止毫秒时间戳间隔要在300000毫秒内）
        ranges:
    -
        name: endTime
        type: integer
        mandatory: true
        default:
        description: 结束时间
        ranges:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对
        ranges:
content_markdown: >-
    #### 备注


    该接口限制只能查询五分钟内的数据。


    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_symbol | 交易对不合法 |

    | invalid_time_in_force | 时间设定有误 |

    | the_number_of_orders_has_reached_the_maximum | 区间数据过多，超限 |

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
              "result": {
                "hasNext": false,
                "hasPrev": false,
                "items": [
                  {
                    "clientOrderId": "",
                    "avgPrice": 0,
                    "closePosition": false,
                    "closeProfit": 0,
                    "createdTime": 0,
                    "executedQty": 0,
                    "forceClose": false,
                    "marginFrozen": 0,
                    "orderId": 0,
                    "orderSide": "",
                    "orderType": "",
                    "origQty": 0,
                    "positionSide": "",
                    "price": 0,
                    "sourceId": 0,
                    "state": "PARTIALLY_CANCELED",
                    "symbol": "",
                    "timeInForce": "",
                    "triggerProfitPrice": 0,
                    "triggerStopPrice": 0,
                    "canceledQty": 0
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
