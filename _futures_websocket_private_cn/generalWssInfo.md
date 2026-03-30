---
title: 通用 WSS 信息
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
    **WebSocket 基础地址**: `wss://fstream.xt.com/ws/user`（用户私人频道）

    &nbsp;

    **请求头**

    发送建立 WebSocket 连接的 HTTP 请求时，建议添加压缩扩展协议的请求头：

    `Sec-Websocket-Extensions: permessage-deflate`

    &nbsp;

    **订阅步骤**

    1. 调用接口获取 **ListenKey**：`GET https://fapi.xt.com/future/user/v1/user/listen-key`
    2. 建立 WebSocket 后，订阅用户相关事件时发送订阅 JSON

    &nbsp;

    **可用 Topic**: `order`, `trade`, `balance`, `position`, `notify`

    &nbsp;

    **心跳检测**: 每个客户端连接必须定期发送文本 `ping` 消息。服务器将回复文本 `pong`。如果服务器在 **30 秒** 内未收到 `ping`，将主动断开连接。

    &nbsp;

    **错误码**

    | 错误码 | 描述 |
    | --- | --- |
    | {topic}@invalid_listenkey | ListenKey 过期或无效，请重新申请 |
    | Invalid Parameter | 参数错误，请检查 JSON 字符串 |
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
