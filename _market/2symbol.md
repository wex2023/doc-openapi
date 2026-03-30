---
title: Get symbol information
position_number: 3
type: get
description: /v4/public/symbol
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: trading pair eg:btc_usdt
        ranges:
    -
        name: symbols
        type: array
        mandatory: false
        default:
        description: 'Collection of trading pairs. Priority is higher than symbol. eg: btc_usdt,eth_usdt'
        ranges:
    -
        name: version
        type: string
        mandatory: false
        default:
        description: |-
            Version number, if request version equals response version, list will not be returned (reduce IO).
            eg: 2e14d2cd5czcb2c2af2c1db6
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**


    1\.single symbol：10/s/ip


    2\.multiple symbols：10/s/ip


    ---


    #### **FILTER**


    ---


    ##### **PRICE FILTER**


    * `min`: minimum price allowed

    * `max`: maximum price allowed

    * `tickSize`: step interval → price = minPrice + (integer * tickSize)


    Logical pseudocode:


    * price &gt;= min

    * price &lt;= max

    * (price-minPrice) % tickSize == 0


    ---


    ##### **QUANTITY FILTER**


    * `min`: minimum allowed

    * `max`: maximum allowed

    * `tickSize`: step interval


    Logical pseudocode:


    * quantity &gt;= min

    * quantity &lt;= max

    * (quantity-minQuantity) % tickSize == 0


    ---


    ##### **QUOTE\_QTY FILTER**


    * If `min` is null → no restriction

    * LIMIT orders → price \* quantity &gt;= min

    * MARKET BUY orders → quoteQty &gt;= min


    ---


    ##### **PROTECTION\_LIMIT FILTER**


    * `buyMaxDeviation`, `buyPriceLimitCoefficient`, `sellMaxDeviation`, `sellPriceLimitCoefficient`


    Buy: price &gt;= latestPrice - latestPrice \* buyMaxDeviation


    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;price &lt;= latestPrice + latestPrice \* buyPriceLimitCoefficient


    Sell: price &lt;= latestPrice + latestPrice \* sellMaxDeviation


    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;price &gt;= latestPrice - latestPrice \* sellPriceLimitCoefficient


    ---


    ##### **PROTECTION\_MARKET FILTER**


    * `maxDeviation`: maximum deviation


    Buy: latestPrice + latestPrice \* maxDeviation &gt;= sellBestPrice


    Sell: latestPrice - latestPrice \* maxDeviation &lt;= buyBestPrice


    ---


    ##### **PROTECTION\_ONLINE FILTER**


    * `maxPriceMultiple`, `durationSeconds`


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
                    "time": 1662444177871,
                    "version": "7cd2cfab0dc979339f1de904bd90c9cb",
                    "symbols": [
                      {
                        "symbol": "btc_usdt",         //trading pair
                        "state": "ONLINE",            //trading pair status [ONLINE=online;OFFLINE=offline,DELISTED=delisted]
                        "tradingEnabled": true,        //is trading enabled
                        "openapiEnabled": true,        //is OPENAPI enabled
                        "nextStateTime": null,         //next state timestamp
                        "nextState": null,             //next state
                        "depthMergePrecision": 5,      //depth merge precision
                        "baseCurrency": "btc",         //base asset
                        "baseCurrencyPrecision": 5,    //base asset precision
                        "quoteCurrency": "usdt",       //quote asset
                        "quoteCurrencyPrecision": 6,   //quote asset precision
                        "pricePrecision": 4,           //price precision
                        "quantityPrecision": 6,        //quantity precision
                        "takerFeeRate": 0.001,         //taker fee rate
                        "makerFeeRate": 0.002,         //maker fee rate
                        "orderTypes": [                //order types [LIMIT=limit order;MARKET=market order]
                          "LIMIT",
                          "MARKET"
                        ],
                        "timeInForces": [              //time-in-force [GTC=good till canceled; IOC=immediate or cancel; FOK=fill or kill; GTX=post-only cancel]
                          "GTC",
                          "FOK",
                          "IOC",
                          "GTX"
                        ],
                        "displayWeight": 1,            //display weight, higher value is displayed first
                        "displayLevel": "FULL",        //display level [FULL=full display;SEARCH=search display;DIRECT=direct access;NONE=do not display]
                        "filters": [
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
