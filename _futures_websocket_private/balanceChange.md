---
title: Balance Change
position_number: 7
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **Topic**: `balance`

    Subscribe to balance change events for the user account.
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["balance@{ListenKey}"],
              "id": "{id}"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "balance",
              "event": "balance@123456",
              "data": {
                "coin": "usdt",
                "underlyingType": 1,
                "walletBalance": "123",
                "openOrderMarginFrozen": "123",
                "isolatedMargin": "213",
                "crossedMargin": "0"
              }
            }
        title: Response
        language: json
---
