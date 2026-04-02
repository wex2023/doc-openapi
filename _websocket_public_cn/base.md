---
title: WebSocket 基础信息
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
    **基础地址**

    wss://stream.wexex.io/public

    &nbsp;

    **请求头**

    Sec-WebSocket-Extensions: permessage-deflate
left_code_blocks:
    -
        code_block: |-
            # Python 最小示例 (websocket-client)
            # pip install websocket-client
            import websocket

            url = "wss://stream.wexex.io/public"
            headers = ["Sec-WebSocket-Extensions: permessage-deflate"]

            ws = websocket.WebSocket()
            ws.connect(url, header=headers)
            print("已连接到 XT 公共 WSS")
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
