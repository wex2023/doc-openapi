---
title: Get Configuration Information for Listed And Tradeable Symbols
position_number: 4
type: get
description: /future/market/v3/public/symbol/list
parameters:
    -
        name:
        type:
        mandatory: false
        default:
        description:
        ranges:
content_markdown: >-
    This method does not require a signature.
left_code_blocks:
    -
        code_block: |-
            public void getSymbolList() {
                String text = HttpUtil.get("https://fapi.xt.com/future/market/v3/public/symbol/list");
                System.out.println(text);
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
              "error": {
                "code": "",
                "msg": ""
              },
              "msgInfo": "",
              "result": [
                {
                  "baseCoin": "",                    //Target Assets
                  "baseCoinDisplayPrecision": 0,     //Displayed target currency precision
                  "cnDesc": "",                      //Contract description
                  "cnName": "",                      //Contract name
                  "cnRemark": "",                    //Contract Remarks
                  "contractSize": 0,                 //Contract multiplier(face value)
                  "contractType": "",                //Contract type, perpetual, delivery
                  "deliveryCompletion": false,
                  "deliveryDate": 0,
                  "deliveryPrice": 0,
                  "depthPrecisionMerge": 0,
                  "enDesc": "",
                  "enName": "",
                  "enRemark": "",
                  "initLeverage": 0,
                  "initPositionType": "",
                  "isDisplay": false,
                  "isOpenApi": false,
                  "labels": [],
                  "liquidationFee": 0,
                  "makerFee": 0,
                  "marketTakeBound": 0,
                  "maxEntrusts": 0,
                  "maxNotional": 0,
                  "maxOpenOrders": 0,
                  "maxPrice": 0,
                  "minNotional": 0,
                  "minPrice": 0,
                  "minQty": 0,
                  "minStepPrice": 0,
                  "multiplierDown": 0,
                  "multiplierUp": 0,
                  "onboardDate": 0,
                  "pair": "",
                  "plates": [],
                  "predictEventParam": "",
                  "predictEventSort": "",
                  "predictEventType": "",
                  "pricePrecision": 0,
                  "productType": "",
                  "quantityPrecision": 0,            // Deprecated
                  "quoteCoin": "",
                  "quoteCoinDisplayPrecision": 0,
                  "quoteCoinPrecision": 0,
                  "baseCoinPrecision": 0,
                  "state": 0,
                  "supportEntrustType": "",
                  "supportOrderType": "",
                  "supportPositionType": "",
                  "supportTimeInForce": "",
                  "offTime": "",                     // Contract plan de-listing time
                  "symbol": "",
                  "symbolGroupId": 0,
                  "takerFee": 0,
                  "tradeSwitch": false,
                  "underlyingType": ""
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
