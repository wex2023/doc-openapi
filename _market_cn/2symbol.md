---
title: 获取交易对信息
position_number: 3
type: get
description: /v4/public/symbol
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对 例如：btc_usdt
        ranges:
    -
        name: symbols
        type: array
        mandatory: false
        default:
        description: '交易对集合，优先级高于symbol。例如：btc_usdt,eth_usdt'
        ranges:
    -
        name: version
        type: string
        mandatory: false
        default:
        description: |-
            版本号，如果请求版本等于响应版本，将不返回列表（减少 IO）。
            例如：2e14d2cd5czcb2c2af2c1db6
        ranges:
content_markdown: >-
    #### **限流规则**


    1\.单个交易对：10次/秒/IP


    2\.多个交易对：10次/秒/IP


    ---


    #### **过滤器**


    ---


    ##### **价格过滤器 PRICE FILTER**


    * `min`：允许的最小价格

    * `max`：允许的最大价格

    * `tickSize`：步进间隔 → price = minPrice + (整数 * tickSize)


    逻辑伪代码：


    * price &gt;= min

    * price &lt;= max

    * (price-minPrice) % tickSize == 0


    ---


    ##### **数量过滤器 QUANTITY FILTER**


    * `min`：允许的最小值

    * `max`：允许的最大值

    * `tickSize`：步进间隔


    逻辑伪代码：


    * quantity &gt;= min

    * quantity &lt;= max

    * (quantity-minQuantity) % tickSize == 0


    ---


    ##### **报价数量过滤器 QUOTE\_QTY FILTER**


    * 如果 `min` 为 null → 无限制

    * 限价单 → price \* quantity &gt;= min

    * 市价买单 → quoteQty &gt;= min


    ---


    ##### **限价保护过滤器 PROTECTION\_LIMIT FILTER**


    * `buyMaxDeviation`、`buyPriceLimitCoefficient`、`sellMaxDeviation`、`sellPriceLimitCoefficient`


    买入：price &gt;= latestPrice - latestPrice \* buyMaxDeviation


    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;price &lt;= latestPrice + latestPrice \* buyPriceLimitCoefficient


    卖出：price &lt;= latestPrice + latestPrice \* sellMaxDeviation


    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;price &gt;= latestPrice - latestPrice \* sellPriceLimitCoefficient


    ---


    ##### **市价保护过滤器 PROTECTION\_MARKET FILTER**


    * `maxDeviation`：最大偏差


    买入：latestPrice + latestPrice \* maxDeviation &gt;= sellBestPrice


    卖出：latestPrice - latestPrice \* maxDeviation &lt;= buyBestPrice


    ---


    ##### **上线保护过滤器 PROTECTION\_ONLINE FILTER**


    * `maxPriceMultiple`、`durationSeconds`


    price &lt;= openPrice \* maxPriceMultiple



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
                  "rc": 0,
                  "mc": "SUCCESS",
                  "ma": [],
                  "result": {
                    "time": 1662444177871,                          //时间
                    "version": "7cd2cfab0dc979339f1de904bd90c9cb",  //内容版本
                    "symbols": [
                      {
                        "symbol": "btc_usdt",                       //交易对
                        "state": "ONLINE",                          //交易对状态[ONLINE=上线的;OFFLINE=下线的,DELISTED=退市]
                        "tradingEnabled": true,                     //是否启用交易
                        "openapiEnabled": true,                     //是否启用OPENAPI
                        "nextStateTime": null,                      //下一个状态时间
                        "nextState": null,                          //下一个状态
                        "depthMergePrecision": 5,                   //深度合并精度
                        "baseCurrency": "btc",                      //标的资产
                        "baseCurrencyPrecision": 5,                 //标的资产精度
                        "quoteCurrency": "usdt",                    //报价资产
                        "quoteCurrencyPrecision": 6,                //报价资产精度
                        "pricePrecision": 4,                        //交易价格精度
                        "quantityPrecision": 6,                     //交易数量精度
                        "takerFeeRate": 0.001,                      //吃单手续费率
                        "makerFeeRate": 0.002,                      //挂单手续费率
                        "orderTypes": [                             //订单类型[LIMIT=限价单;MARKET=市价单]
                          "LIMIT",
                          "MARKET"
                        ],
                        "timeInForces": [                           //有效方式[GTC=成交为止,一直有效; IOC=无法立即成交(吃单)的部分就撤销; FOK=无法全部立即成交就撤销; GTX=无法成为挂单方就撤销]
                          "GTC",
                          "FOK",
                          "IOC",
                          "GTX"
                        ],
                        "displayWeight": 1,                         //展示权重，越大越靠前
                        "displayLevel": "FULL",                     //展示级别,[FULL=完全展示,SEARCH=搜索展示,DIRECT=直达展示,NONE=不展示]
                        "filters": [                                //过滤器
                          {
                            "filter": "PROTECTION_LIMIT",
                            "buyMaxDeviation": "0.8",
                            "sellMaxDeviation": "0.8"
                          },
                          {
                            "filter": "PROTECTION_MARKET",
                            "maxDeviation": "0.1"
                          },
                          {
                            "filter": "PROTECTION_ONLINE",
                            "durationSeconds": "300",
                            "maxPriceMultiple": "5"
                          },
                          {
                            "filter": "PRICE",
                            "min": null,
                            "max": null,
                            "tickSize": null
                          },
                          {
                            "filter": "QUANTITY",
                            "min": null,
                            "max": null,
                            "tickSize": null
                          },
                          {
                            "filter": "QUOTE_QTY",
                            "min": null
                          }
                        ]
                      }
                    ]
                  }
                }
        title: Response
        language: json
---
