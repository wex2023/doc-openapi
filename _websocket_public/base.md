---
title: General WSS information
position_number: 1
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
    **Base Address**

    wss://stream.xt.com/public

    &nbsp;

    **Request Header**

    Sec-WebSocket-Extensions: permessage-deflate
left_code_blocks:
    -
        code_block: |-
            # Minimal Python example (websocket-client)
            # pip install websocket-client
            import websocket

            url = "wss://stream.xt.com/public"
            headers = ["Sec-WebSocket-Extensions: permessage-deflate"]

            ws = websocket.WebSocket()
            ws.connect(url, header=headers)
            print("Connected to XT public WSS")
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
                "rc": 0,
                "mc": "SUCCESS",
                "ma": [],
                "result": {}
            }
        title: Response
        language: json
---
