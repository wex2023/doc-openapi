---
title: Cancel Orders
position_number: 7
type: post
description: /future/trade/v1/order/cancel
parameters:
    -
        name: orderId
        type: integer
        mandatory: true
        default:
        description: Order ID
        ranges:
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_params | Parameter error or order does not exist |

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
              "result": "",
              "returnCode": 0
            }
        title: Response
        language: json
---
