---
title: Get Profit List History
position_number: 25
type: get
description: /future/trade/v1/entrust/profit-list-history
parameters:
    -
        name: id
        type: integer
        mandatory: false
        default: '1'
        description: Page number
        ranges:
    -
        name: limit
        type: integer
        mandatory: false
        default: '10'
        description: Page size
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default:
        description: Start time (Default query 90 days ago)
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default:
        description: End time
        ranges:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: Direction
        ranges: NEXT;PREVIOUS
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void getProfitListHistory() {

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
                "hasNext": false,
                "hasPrev": false,
                "items": [
                  {
                    "profitId": ""  // Entrust ID (Long to string)
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
