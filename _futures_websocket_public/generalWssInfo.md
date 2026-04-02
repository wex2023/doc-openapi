---
title: General WSS Information
position_number: 1
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **Base URL**: `wss://fstream.wexex.io/ws/market` (Public channels; no listenKey required)

    &nbsp;

    **Request Headers**

    `Sec-Websocket-Extensions: permessage-deflate`

    &nbsp;

    **Subscription Steps**

    1. Establish a WebSocket connection.
    2. Subscribe to a public channel event by sending: `{"method":"SUBSCRIBE","params":["{topic}@{symbol}"],"id":"{id}"}`

    &nbsp;

    **Push Message Format**

    `{"topic":"topic","event":"{topic}@{symbol}","data":{}}`

    &nbsp;

    **Heartbeat**: Each client must periodically send a text `ping`. Server replies `pong`. If no `ping` within **30 seconds**, the connection is closed.

    &nbsp;

    **Error Codes**

    | Error Code | Description |
    | --- | --- |
    | 400 | Bad request payload. Please check it. |
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": [
                "{topic1}@{arg1},{arg2}",
                "{topic2}@{arg}"
              ],
              "id": "id_field_could_call_whatever_you_want"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "id": "{id}",
              "code": 0,
              "msg": ""
            }
        title: Response
        language: json
---
