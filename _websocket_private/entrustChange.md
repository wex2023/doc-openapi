---
title: Change of entrust
position_number: 6
display: 0
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
    **Subscription format:** trigger

    &nbsp;

    This push notification is triggered when a **trigger/entrust order** changes.
    Useful for tracking creation, updates, and state changes of trigger orders.
left_code_blocks:
    -
        code_block: |-
            {
                "method": "subscribe",
                "params": ["trigger"],
                "listenKey": "512312356123123123"
            }
        title: Subscribe
        language: json
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "trigger",
                "event": "trigger",
                "data": {
                    "s": "btc_usdt",                // symbol
                    "t": 1656043204763,             // time happened time (ms)
                    "i": "6216559590087220004",     // triggerId
                    "st": "NEW"                     // state (e.g. NEW, FILLED, CANCELED)
                }
            }
        title: Push
        language: json
---
