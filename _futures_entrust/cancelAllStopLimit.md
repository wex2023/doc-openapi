---
title: Cancel All Stop Limit
position_number: 9
type: post
description: /future/trade/v1/entrust/cancel-all-profit-stop
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: "Trading pair, e.g., btc_usdt"
        ranges:
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_symbol | Trading pair does not exist |

    | fail | Internal error |

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
              "result": true,
              "returnCode": 0
            }
        title: Response
        language: json
---
