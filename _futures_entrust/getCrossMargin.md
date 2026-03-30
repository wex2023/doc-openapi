---
title: Get Cross Margin
position_number: 34
type: get
description: "/future/trade/v1/position/cross-margin/{symbol}"
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: >-
    The symbol is passed as a path parameter in the URL, e.g., `/future/trade/v1/position/cross-margin/eth_usdt`


    #### Rate Limit


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_symbol | Trading pair does not exist |

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
              "result": "result",
              "returnCode": 0
            }
        title: Response
        language: json
---
