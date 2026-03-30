---
title: 取消单个跟踪单
position_number: 14
type: post
description: /future/trade/v1/entrust/cancel-track
parameters:
    -
        name: trackId
        type: integer
        mandatory: true
        default:
        description: 跟踪单ID
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_track_entrust | 跟踪单不存在 |

left_code_blocks:
    -
        code_block:
        title: Java
        language: java
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
              "error": {
                "code": "",
                "msg": ""
              },
              "msgInfo": "",
              "result": {},
              "returnCode": 0
            }
        title: Response
        language: json
---
