---
title: 查询不分页的成交明细
position_number: 29
type: get
description: /future/trade/v1/order/trade-list-all
parameters:
    -
        name: orderId
        type: integer
        mandatory: false
        default:
        description: 订单id
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default:
        description: 开始时间
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default:
        description: 结束时间
        ranges:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_limit | limit参数设置不正确 |

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
              "result": [
                {
                  "orderId": "1876543210987654321",
                  "execId": "2876543210987654322",
                  "symbol": "BTCUSDT",
                  "contractSize": 0.001,
                  "quantity": "0.015",
                  "price": "67234.80",
                  "fee": "10.08522",
                  "couponDeductFee": "3.00000",
                  "bonusDeductFee": "2.00000",
                  "feeCoin": "USDT",
                  "timestamp": 1735698765432,
                  "takerMaker": "TAKER",
                  "orderSide": "BUY",
                  "positionSide": "LONG"
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
