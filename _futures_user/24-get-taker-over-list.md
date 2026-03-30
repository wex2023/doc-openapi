---
title: Get Taker Over List
position_number: 24
type: get
description: /future/user/v1/taker-over/list
parameters:
    -
        name: id
        type: integer
        mandatory: false
        default: '1'
        description: Page number
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: Direction
        ranges: NEXT;PREVIOUS
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
        description: Start time
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
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void getTakerOverList() {

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
                    "requestId": 9876543210987654321,
                    "tenantId": 10001,
                    "accountId": 900123456789,
                    "userId": 55667788,
                    "userGroupId": 3001,
                    "symbolId": 1,
                    "symbolGroupId": 10,
                    "positionType": 2,
                    "positionSide": 1,
                    "riskAccountId": 900123456789,
                    "riskUserId": 55667788,
                    "riskUserGroupId": 3001,
                    "success": true,
                    "positionSize": "0.05200000",
                    "entryPrice": "6325080000",
                    "balance": "1523487654321",
                    "symbol": "BTCUSDT",
                    "markPrice": "6712345000000",
                    "marginRate": "01250000",
                    "createdTime": 1735701234567
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
