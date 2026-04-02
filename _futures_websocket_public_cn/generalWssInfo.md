---
title: WebSocket 基本信息
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
    **WebSocket 基础地址**: `wss://fstream.wexex.io/ws/market`（公共频道，无需 listenKey）

    &nbsp;

    **请求头**

    `Sec-Websocket-Extensions: permessage-deflate`

    &nbsp;

    **订阅步骤**

    1. 建立 WebSocket 连接。
    2. 订阅公共频道的 WebSocket 事件时，发送：`{"method":"SUBSCRIBE","params":["{topic}@{你关注的交易对}"],"id":"{id}"}`

    &nbsp;

    **推送消息格式**

    `{"topic":"topic","event":"{topic}@{symbol}","data":{}}`

    &nbsp;

    **心跳检测**: 每个客户端连接必须定期发送文本 `ping` 消息。服务器将回复文本 `pong`。如果服务器在 **30 秒** 内未收到 `ping`，将主动断开连接。

    &nbsp;

    **错误码**

    | 错误码 | 描述 |
    | --- | --- |
    | 400 | 请求消息有误，请检查 |
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
