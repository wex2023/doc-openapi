---
title: Order filled
position_number: 8
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
    **Subscription format:** trade

    &nbsp;

    This push notification is triggered when a trade (order fill) occurs.
    Indicates execution details including trade ID, order ID, price, quantity, and maker/taker info.
    Useful for tracking completed trades in real time.
left_code_blocks:
    -
        code_block: |-
            {
                "method": "subscribe",
                "params": ["trade"],
                "listenKey": "512312356123123123"
            }
        title: Subscribe
        language: json
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "trade",
                "event": "trade",
                "data": {
                    "s": "btc_usdt",                // symbol
                    "i": 6316559590087222000,       // tradeId
                    "t": 1655992403617,             // trade time (ms)
                    "oi": 6616559590087222666,      // orderId
                    "p": "43000",                   // price
                    "q": "0.21",                    // quantity
                    "v": "9030",                    // quoteQty trade amount
                    "b": true,                      // whether buyer is maker (true=buyerMaker)
                    "tm": 1                         // taker/maker: 1 = taker, 2 = maker
                }
            }
        title: Push
        language: json
---
