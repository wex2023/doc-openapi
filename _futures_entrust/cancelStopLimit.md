---
title: Cancel Stop Limit
position_number: 8
type: post
description: /future/trade/v1/entrust/cancel-profit-stop
parameters:
    -
        name: profitId
        type: integer
        mandatory: true
        default:
        description: Profit/Stop order ID
        ranges:
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_entrust | Invalid order ID |

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
