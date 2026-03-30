---
title: Change of order
position_number: 7
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
    **Subscription format:** order

    &nbsp;

    This push notification is triggered when an **order status** changes.

    Possible order states (st):

    - NEW - New order created

    - PARTIALLY\_FILLED - Partially filled

    - FILLED - Fully filled

    - CANCELED - Order canceled

    - REJECTED - Order rejected

    - EXPIRED - Order expired
left_code_blocks:
    -
        code_block: |-
            {
                "method": "subscribe",
                "params": ["order"],
                "listenKey": "512312356123123123"
            }
        title: Subscribe
        language: json
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "order",
                "event": "order",
                "data": {
                    "s": "btc_usdt",                // symbol
                    "bc": "btc",                    // base currency
                    "qc": "usdt",                   // quotation currency
                    "t": 1656043204763,             // happened time (ms)
                    "ct": 1656043204663,            // create time (ms)
                    "i": "6216559590087220004",     // order id
                    "ci": "test123",                // client order id
                    "st": "PARTIALLY_FILLED",       // state NEW/PARTIALLY_FILLED/FILLED/CANCELED/REJECTED/EXPIRED
                    "sd": "BUY",                    // side BUY/SELL
                    "tp": "LIMIT",                  // type LIMIT/MARKET
                    "oq": "4",                      // original quantity
                    "oqq": 48000,                   // original quotation quantity
                    "eq": "2",                      // executed quantity
                    "lq": "2",                      // remaining quantity
                    "p": "4000",                    // price
                    "ap": "30000",                  // avg price
                    "f": "0.002"                    // fee
                }
            }
        title: Push
        language: json
---
