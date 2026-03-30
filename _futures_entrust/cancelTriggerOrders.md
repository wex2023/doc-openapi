---
title: Cancel Trigger Orders
position_number: 2
type: post
description: /future/trade/v1/entrust/cancel-plan
parameters:
    -
        name: entrustId
        type: string
        mandatory: true
        default:
        description: Plan order ID
        ranges:
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_params | The provided parameter is empty or incorrect |

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
