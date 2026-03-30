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
content_markdown:
left_code_blocks:
    -
        code_block: |-
            {
                "method": "subscribe",
                "params": [
                    "{topic}@{arg},{arg}",
                    "{topic}@{arg}"
                ],
                "id": "{id}"    //回调 ID
            }
        title: 订阅
        language: javascript
    -
        code_block: |-
            {
                "method": "unsubscribe",
                "params": [
                    "{topic}@{arg},{arg}"
                ],
                "id": "{id}"   //回调 ID
            }
        title: 取消订阅
        language: javascript
right_code_blocks:
    -
        code_block: |-
            {
                "code": 0,
                "msg": "success"
            }
        title: 响应
        language: json
---
