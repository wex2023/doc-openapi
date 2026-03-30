---
title: "查看历史订单（量化）"
position_number: 15
type: get
description: /future/trade/v1/order/quant/list-history
parameters:
    -
        name: id
        type: long
        mandatory: false
        default:
        description: 游标ID，用于翻页，上一次返回的最后一个orderId
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: 翻页方向
        ranges: PREV;NEXT
    -
        name: limit
        type: integer
        mandatory: false
        default: 10
        description: 每页数量，最大2000
        ranges:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对
        ranges:
    -
        name: forceClose
        type: boolean
        mandatory: false
        default: "false"
        description: 是否强平订单
        ranges:
    -
        name: startTime
        type: long
        mandatory: false
        default:
        description: 开始时间（毫秒时间戳），最早90天前
        ranges:
    -
        name: endTime
        type: long
        mandatory: false
        default:
        description: 结束时间（毫秒时间戳）
        ranges:
    -
        name: origType
        type: integer
        mandatory: false
        default:
        description: "条件委托类型：1=限价止盈、2=限价止损、3=市价止盈、4=市价止损"
        ranges:
    -
        name: orderSide
        type: integer
        mandatory: false
        default:
        description: "下单方向：1=买、2=卖"
        ranges:
    -
        name: states
        type: list
        mandatory: false
        default:
        description: "订单状态：2=部分成交、3=全部成交、4=用户撤销、6=已过期"
        ranges:
    -
        name: orderOrigType
        type: integer
        mandatory: false
        default:
        description: "历史订单类型：1=限价委托、2=市价委托、3=限价止盈止损、4=市价止盈止损、5=MMR止损"
        ranges:
    -
        name: welfareAccount
        type: boolean
        mandatory: false
        default: "false"
        description: 是否查询体验金账户
        ranges:
content_markdown: >-
    量化账号专用历史订单查询接口，支持游标分页，最大返回2000条记录。


    #### 限流规则


    200/s/apikey


    #### 游标分页使用说明


    1. **首次请求**：不传 `id` 参数

    2. **下一页**：使用上一次返回列表中最后一条记录的 ID 作为 `id` 参数，`direction=NEXT`

    3. **上一页**：使用当前列表第一条记录的 ID 作为 `id` 参数，`direction=PREV`

    4. **判断是否有更多数据**：通过 `hasNext` 和 `hasPrev` 字段判断


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | not_quantification_account | 非量化账号，无权访问此接口 |

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
              "returnCode": 0,
              "msgInfo": "",
              "error": {
                "code": "",
                "msg": ""
              },
              "result": {
                "hasPrev": false,
                "hasNext": true,
                "items": [
                  {
                    "orderId": 123456789,
                    "clientOrderId": "",
                    "symbol": "btc_usdt",
                    "orderSide": "BUY",
                    "orderType": "LIMIT",
                    "positionSide": "LONG",
                    "price": "50000.00",
                    "origQty": "0.1",
                    "executedQty": "0.1",
                    "avgPrice": "50000.00",
                    "state": "FILLED",
                    "closePosition": false,
                    "closeProfit": "100.00",
                    "marginFrozen": "0",
                    "forceClose": false,
                    "sourceId": 0,
                    "timeInForce": "GTC",
                    "triggerProfitPrice": "0",
                    "triggerStopPrice": "0",
                    "createdTime": 1703520000000,
                    "updatedTime": 1703520100000
                  }
                ]
              }
            }
        title: Response
        language: json
---
