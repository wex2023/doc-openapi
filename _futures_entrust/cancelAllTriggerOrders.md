---
title: Cancel All Trigger Orders
position_number: 3
type: post
description: /future/trade/v1/entrust/cancel-all-plan
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair
        ranges: e.g. btc_usdt
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
              "result": {},
              "returnCode": 0
            }
        title: Response
        language: json
---
