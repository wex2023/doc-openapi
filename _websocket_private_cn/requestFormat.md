---
title: 请求消息格式
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
    **参数格式**

    \{topic\}@\{arg\},\{arg\},…

    &nbsp;

    - 请求消息用于**订阅**或**取消订阅** WebSocket 主题。

    - listenKey 必须通过 **/v4/ws-token** 接口获取。

    - id 是用于匹配响应的自定义请求标识符。
left_code_blocks:
    -
        code_block: |-
            {
                "method": "subscribe",
                "params": [
                    "{topic}@{arg},{arg}",    //事件订阅
                    "{topic}@{arg}"
                ],
                "listenKey": "512312356123123123",   //监听Key，通过/v4/ws-token接口获取accessToken
                "id": "{id}"
            }
        title: 订阅
        language: javascript
    -
        code_block: |-
            {
                "method": "unsubscribe",
                "params": [
                    "{topic}@{arg},{arg}",    //事件订阅
                    "{topic}@{arg}"
                ],
                "listenKey": "512312356123123123",   //监听Key，通过/v4/ws-token接口获取accessToken
                "id": "{id}"
            }
        title: 取消订阅
        language: javascript
right_code_blocks:
    -
        code_block:
        title: 响应
        language: json
---
