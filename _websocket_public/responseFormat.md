---
title: Response message format
position_number: 3
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
                "id": "{id}",   //call back ID
                "code": 1,      //result 0=success;1=fail;2=listenKey invalid
                "msg": ""
            }
        title: Format
        language: javascript
right_code_blocks:
    -
        code_block: '{"id":"123", "code": 0, "msg": "success"}'
        title: Response-success
        language: json
    -
        code_block: '{"id":"123", "code": 401, "msg": "token expire"}'
        title: Response-token invalid
        language: json
---
