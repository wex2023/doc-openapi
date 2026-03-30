---
title: 所有行情
position_number: 12
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
    **请求**

    格式: tickers

    频率: 1000ms（只推送有变化部分）
left_code_blocks:
    -
        code_block:
        title: 请求
        language: json
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "tickers",
                "event": "tickers",
                "data": [ ]  // 同 ticker
            }
        title: 响应
        language: json
---
