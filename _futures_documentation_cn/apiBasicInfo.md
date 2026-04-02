---
title: 接口基础信息
position_number: 1
parameters:
- name:
content:
content_markdown: >-
    #### 基础地址


    - **USDT-M:** `https://fapi.wexex.io` （适用于 U 本位合约）

    - **Coin-M:** `https://dapi.wexex.io` （适用于币本位合约）


    #### 网络建议


    由于高延迟和稳定性差的原因，**不建议通过代理访问 XT API**。


    #### 请求方式


    - **GET 请求：** 参数放在 **QueryString** 中。

    - **POST 请求：** 参数可以放在 **RequestBody** 或 **QueryString** 中。


    当参数放在 QueryString 中时，必须在 HTTP Header 中添加：`Content-Type: application/x-www-form-urlencoded`


    当参数放在 RequestBody 中时，必须在 HTTP Header 中添加：`Content-Type: application/json`


    #### 接口分类


    XT API 接口分为 **公共接口** 和 **用户接口**。


    **公共接口** - 无需身份认证。参数直接放入 QueryString 中。通常使用 GET 方法。


    **用户接口** - 需要在 Header 中传入认证参数。除了 QueryString 或 RequestBody 参数外，至少需要以下四个 Header：


    | Header | 说明 |

    | --- | --- |

    | `validate-appkey` | 用户公钥 |

    | `validate-timestamp` | 当前时间戳（毫秒） |

    | `validate-signature` | 请求签名 |

    | `Content-Type` | 请求类型 |


    不需要签名的接口将在文档中额外说明。


    #### 认证说明


    - **如何获取 APPKEY：** 请参阅"申请 API Key"章节。

    - **如何获取签名：** 请参阅"获取签名"章节。


    #### 限流规则


    - **资产类接口：** 每秒最多 3 次请求。

    - **其他接口：** 单个用户每秒最多 10 次请求，单个 IP 每分钟最多 1000 次。


    超过限制后账户将被锁定 10 分钟。

left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---
