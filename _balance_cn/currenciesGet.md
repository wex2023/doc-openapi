---
title: 获取币种信息
position_number: 1
type: get
description: /v4/public/currencies
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description: 无需请求参数
        ranges:
content_markdown:
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
                  "rc": 0,
                  "mc": "string",
                  "ma": [
                    {}
                  ],
                  "result": [
                    {
                      "id": 11,                // 币种 ID
                      "currency": "usdt",       // 币种简称
                      "fullName": "usdt",       // 币种全称
                      "logo": null,             // 币种 Logo
                      "cmcLink": null,          // CMC 链接
                      "weight": 100,            // 币种权重
                      "maxPrecision": 6,        // 最大精度
                      "depositStatus": 1,       // 充值状态 (0 关闭，1 开启)
                      "withdrawStatus": 1,      // 提现状态 (0 关闭，1 开启)
                      "convertEnabled": 1,      // 小额资产兑换 (0 关闭，1 开启)
                      "transferEnabled": 1      // 转账开关 (0 关闭，1 开启)
                    }
                  ]
                }
        title: Response
        language: json
---
