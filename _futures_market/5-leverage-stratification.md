---
title: See Leverage Stratification of Single Trading Pair
position_number: 5
type: get
description: /future/market/v1/public/leverage/bracket/detail
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair eg:eth_usdt
        ranges:
content_markdown: >-
    This method does not require a signature.
left_code_blocks:
    -
        code_block: |-
            public void getLeverageBracket() {
                String text = HttpUtil.get("https://fapi.wexex.io/future/market/v1/public/leverage/bracket/detail?symbol=eth_usdt");
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
              "result": {
                "leverageBrackets": [
                  {
                    "bracket": 0,            // Level
                    "maintMarginRate": 0,    // Maintain margin rate
                    "maxLeverage": 0,        // Maximum leverage
                    "maxNominalValue": 0,    // Maximum notional value
                    "maxStartMarginRate": 0, // Maximum initial margin rate
                    "minLeverage": 0,        // Minimum leverage
                    "startMarginRate": 0,    // Initial margin rate
                    "symbol": ""             // Trading pair
                  }
                ],
                "symbol": ""
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
