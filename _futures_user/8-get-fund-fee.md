---
title: Get Fund Fee Information
position_number: 8
type: get
description: /future/user/v1/balance/funding-rate-list
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair (queries all if not passed)
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: "Direction (PREV: Previous page; NEXT: Next page)"
        ranges: PREV;NEXT
    -
        name: id
        type: integer
        mandatory: false
        default:
        description: Record ID
        ranges:
    -
        name: limit
        type: integer
        mandatory: false
        default: '10'
        description: Limit
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default:
        description: Start time
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default:
        description: End time
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void getFundingRateList() {

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
                "hasNext": false, // Is there a next page
                "hasPrev": false, // Is there a previous page
                "items": [
                  {
                    "cast": 0,          // Fund fee
                    "coin": "",         // Currency
                    "createdTime": 0,   // Time
                    "id": 0,            // ID
                    "positionSide": "", // Direction
                    "symbol": ""        // Trading pair
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
