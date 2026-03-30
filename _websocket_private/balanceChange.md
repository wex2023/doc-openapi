---
title: Change of balance
position_number: 5
type:
description:

parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **Subscription format:** balance

    &nbsp;

    This push notification is triggered when a user's account balance changes.
    Supports both **SPOT** and **LEVER** business types.
    Useful for tracking real-time balance changes after trades, deposits, withdrawals, or transfers.
left_code_blocks:
    -
        code_block: |-
            {
                "method": "subscribe",
                "params": ["balance"],
                "listenKey": "512312356123123123"
            }
        title: Subscribe
        language: json
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "balance",
                "event": "balance",
                "data": {
                    "a": "123",           // accountId
                    "t": 1656043204763,   // time happened time (ms)
                    "c": "btc",           // currency
                    "b": "123",           // balance total spot balance
                    "f": "11",            // frozen amount
                    "z": "SPOT",          // bizType [SPOT,LEVER]
                    "s": "btc_usdt"       // symbol
                }
            }
        title: Push
        language: json
---
