---
title: Request message format
position_number: 2
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
    **param format**

    \{topic\}@\{arg\},\{arg\},…

    &nbsp;

    - listenKey must be applied via the **/v4/ws-token** endpoint.

    - id is a custom request identifier for matching responses.
left_code_blocks:
    -
        code_block: |-
            {
                "method": "subscribe",
                "params": [
                    "{topic}@{arg},{arg}",    //event
                    "{topic}@{arg}"
                ],
                "listenKey": "512312356123123123",   //the listener Key, Apply accessToken through /v4/ws-token interface
                "id": "{id}"
            }
        title: Subscribe
        language: javascript
    -
        code_block: |-
            {
                "method": "unsubscribe",
                "params": [
                    "{topic}@{arg},{arg}",    //event
                    "{topic}@{arg}"
                ],
                "listenKey": "512312356123123123",   //the listener Key, Apply accessToken through /v4/ws-token interface
                "id": "{id}"
            }
        title: Unsubscribe
        language: javascript
right_code_blocks:
    -
        code_block:
        title: Response
        language: json
---
