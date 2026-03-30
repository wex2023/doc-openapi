---
title: 心跳
position_number: 5
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
content_markdown: >-
    客户端的每个连接需要定期发送文本 **"ping"**，服务器将回复 **"pong"**。
    如果服务器在 1 分钟内没有收到客户端的 ping 消息，将主动断开连接。
left_code_blocks:
    -
        code_block: |-
            "ping"
        title: 请求
        language: json
right_code_blocks:
    -
        code_block: |-
            "pong"
        title: 响应
        language: json
---
