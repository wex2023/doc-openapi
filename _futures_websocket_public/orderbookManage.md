---
title: Orderbook Management
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
    **How to maintain a local order book correctly**

    1. Connect to `wss://fstream.wexex.io/ws/market`, subscribe to `depth_update@btc_usdt`.
    2. Buffer events received from the stream.
    3. Fetch a depth snapshot: `https://fapi.wexex.io/future/market/v1/public/depth?symbol=btc_usdt&level=500`.
    4. Discard any event where `u <= lastUpdateId` in the snapshot.
    5. The first processed event should satisfy `fu <= lastUpdateId + 1` and `u >= lastUpdateId + 1`.
    6. While listening, each new event's `fu` should equal the previous event's `u + 1`.
    7. The data in each event represents the **absolute** quantity at each price level.
    8. If a quantity is `0`, remove that price level.
    9. Receiving deletion events for a local price level that does not exist may occur and is normal.

    &nbsp;

    **Notes**: Due to the limited number of price levels in the depth snapshot, levels with no changes after the initial snapshot will not appear in the incremental depth stream. For most use cases, a 500-level depth limit is sufficient.
left_code_blocks:
    -
        code_block:
        title: Request
        language: json
right_code_blocks:
    -
        code_block:
        title: Response
        language: json
---
