---
title: Message (Notifications)
position_number: 11
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **Topic**: `notify`

    Subscribe to system notification events (liquidation warnings, ADL, etc.).

    **notifyType values**: WARN (warning, about to be liquidated), PARTIAL (partial liquidation), LIQUIDATION (forced liquidation), ADL (auto-deleveraging)
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": ["notify@{ListenKey}"],
              "id": "{id}"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "topic": "notify",
              "event": "notify",
              "data": {
                "symbol": "btc_usdt",
                "positionType": "ISOLATED",
                "positionSide": "LONG",
                "positionSize": "123",
                "notifyType": "WARN"
              }
            }
        title: Response
        language: json
---
