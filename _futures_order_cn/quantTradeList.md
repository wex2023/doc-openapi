---
title: "查看成交明细（量化）"
position_number: 16
type: get
description: /future/trade/v1/order/quant/trade-list
parameters:
    -
        name: id
        type: long
        mandatory: false
        default:
        description: 游标ID，用于翻页（上一次返回的最后一条Trade的execId）
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
        name: orderId
        type: long
        mandatory: false
        default:
        description: 订单ID
        ranges:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对
        ranges:
    -
        name: startTime
        type: long
        mandatory: false
        default:
        description: 开始时间（毫秒时间戳）
        ranges:
    -
        name: endTime
        type: long
        mandatory: false
        default:
        description: 结束时间（毫秒时间戳）
        ranges:
    -
        name: welfareAccount
        type: boolean
        mandatory: false
        default: "false"
        description: 是否查询体验金账户
        ranges:
content_markdown: >-
    量化账号专用成交明细查询接口，支持游标分页，最大返回2000条记录。


    #### 限流规则


    200/s/apikey


    #### 游标分页使用说明


    1. **首次请求**：不传 `id` 参数

    2. **下一页**：使用上一次返回列表中最后一条记录的 `execId` 作为 `id` 参数，`direction=NEXT`

    3. **上一页**：使用当前列表第一条记录的 `execId` 作为 `id` 参数，`direction=PREV`

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
                    "execId": 987654321,
                    "orderId": 123456789,
                    "symbol": "btc_usdt",
                    "price": "50000.00",
                    "quantity": "0.05",
                    "quoteQty": "2500.00",
                    "fee": "1.25",
                    "feeCoin": "USDT",
                    "takerMaker": "TAKER",
                    "timestamp": 1703520050000
                  }
                ]
              }
            }
        title: Response
        language: json
---
