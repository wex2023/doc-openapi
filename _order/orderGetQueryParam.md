---
title: Query single
position_number: 1
type: get
description: /v4/order
parameters:
    -
        name: orderId
        type: number
        mandatory: false
        default:
        description: Order ID
        ranges:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: Client order ID
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**

    50/s/apikey
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
                        "symbol": "BTC_USDT",
                        "orderId": "6216559590087220004",
                        "clientOrderId": "16559590087220001",
                        "baseCurrency": "string",
                        "quoteCurrency": "string",
                        "side": "BUY",                      //Order side: BUY, SELL
                        "type": "LIMIT",                    //Order type: LIMIT, MARKET
                        "timeInForce": "GTC",               //Effective way: GTC, IOC, FOK, GTX
                        "price": "40000",
                        "origQty": "2",                     //Original quantity
                        "origQuoteQty": "48000",            //Original amount
                        "executedQty": "1.2",               //Executed quantity
                        "leavingQty": "string",             //Remaining quantity (0 if cancelled or rejected)
                        "tradeBase": "2",                   //Transaction quantity
                        "tradeQuote": "48000",              //Transaction amount
                        "avgPrice": "42350",                //Average transaction price
                        "fee": "string",                    //Handling fee
                        "feeCurrency": "string",
                        "state": "NEW",                     //Order state
                        "time": 1655958915583,              //Order creation time
                        "updatedTime": 1655958915583        //Last updated time
                      }
                    }
        title: Response
        language: json
---
