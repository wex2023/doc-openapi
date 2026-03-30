---
title: 取消所有跟踪单
position_number: 17
type: post
description: /future/trade/v1/entrust/cancel-all-track
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_symbol | 交易对不存在 |

    | fail | 内部异常 |

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
