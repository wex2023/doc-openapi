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
    **WebSocket Base URL**: `wss://fstream.xt.com/ws/user` (User private channel)

    &nbsp;

    **Request Headers**

    When initiating the WebSocket upgrade request, enable per-message compression:

    `Sec-Websocket-Extensions: permessage-deflate`

    &nbsp;

    **Subscription Steps**

    1. Call the API to obtain a **ListenKey**: `GET https://fapi.xt.com/future/user/v1/user/listen-key`
    2. After WebSocket connection is established, subscribe to user events:

    &nbsp;

    **Available Topics**: `order`, `trade`, `balance`, `position`, `notify`

    &nbsp;

    **Heartbeat**: Each client must periodically send a text `ping` message. Server replies with `pong`. If no `ping` is received within **30 seconds**, the server closes the connection.

    &nbsp;

    **Error Codes**

    | Error Code | Description |
    | --- | --- |
    | {topic}@invalid_listenkey | ListenKey expired or invalid. Please request again. |
    | Invalid Parameter | Invalid parameters. Please check the JSON string. |
left_code_blocks:
    -
        code_block: |-
            {
              "method": "SUBSCRIBE",
              "params": [
                "order@{ListenKey}",
                "trade@{ListenKey}",
                "balance@{ListenKey}",
                "position@{ListenKey}",
                "notify@{ListenKey}"
              ],
              "id": "{id}"
            }
        title: Request
        language: json
right_code_blocks:
    -
        code_block: |-
            {
              "id": "{id}",
              "code": 0,
              "msg": "success"
            }
        title: Response
        language: json
---
