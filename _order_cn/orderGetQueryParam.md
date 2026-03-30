---
title: 查询单个订单
position_number: 1
type: get
description: /v4/order
parameters:
    -
        name: orderId
        type: number
        mandatory: false
        default:
        description: 订单 ID
        ranges:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: 客户订单 ID
        ranges:
content_markdown: >-
    #### **限流规则**

    50次/秒/每个API Key
left_code_blocks:
    -
        code_block: |-
            public String orderGet(){


            }
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
                      "rc": 0,
                      "mc": "string",
                      "ma": [
                        {}
                      ],
                      "result": {
                        "symbol": "BTC_USDT",                   //交易对
                        "orderId": "6216559590087220004",       //订单号
                        "clientOrderId": "16559590087220001",   //客户端订单号
                        "baseCurrency": "string",               //标的币种
                        "quoteCurrency": "string",              //报价币种
                        "side": "BUY",                          //订单方向 BUY=买单, SELL=卖单
                        "type": "LIMIT",                        //订单类型 LIMIT=限价单, MARKET=市价单
                        "timeInForce": "GTC",                   //有效方式 GTC, IOC, FOK, GTX
                        "price": "40000",                       //价格
                        "origQty": "2",                         //原始数量
                        "origQuoteQty": "48000",                //原始金额
                        "executedQty": "1.2",                   //已成交数量
                        "leavingQty": "string",                 //剩余未成交数量 (若取消或拒绝则为 0)
                        "tradeBase": "2",                       //成交数量
                        "tradeQuote": "48000",                  //成交金额
                        "avgPrice": "42350",                    //平均成交价格
                        "fee": "string",                        //手续费
                        "feeCurrency": "string",                //手续费币种
                        "state": "NEW",                         //订单状态
                        "time": 1655958915583,                  //下单时间
                        "updatedTime": 1655958915583            //最后更新时间
                      }
                    }
        title: Response
        language: json
---
