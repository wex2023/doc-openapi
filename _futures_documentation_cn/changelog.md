---
title: 更新日志
position_number: 6
parameters:
- name:
content:
content_markdown: >-
    #### 新增接口清单（2025-12-05）


    本次更新共新增 **14 个接口**，涵盖 **Biz-order** 与 **Biz-user** 两大模块。


    **Biz-order：**


    | 序号 | 接口名称 | 请求类型 | 路径 |

    | --- | --- | --- | --- |

    | 1 | 查询计划反手 | GET | `/future/trade/v1/entrust/reverse-plan-list` |

    | 2 | 查询历史计划反手 | GET | `/future/trade/v1/entrust/reverse-plan-list-history` |

    | 3 | 查询历史止盈止损委托 | GET | `/future/trade/v1/entrust/profit-list-history` |

    | 4 | 查询有成交的历史订单 | GET | `/future/trade/v1/order/trade-history` |

    | 5 | 查询不分页的成交明细 | GET | `/future/trade/v1/order/trade-list-all` |

    | 6 | 查询全部委托 | GET | `/future/trade/v1/order-entrust/list` |

    | 7 | 获取当前持仓信息 | GET | `/future/trade/v1/position/list/active` |

    | 8 | 获取杠杆信息 | GET | `/future/trade/v1/position/leverage/list` |

    | 9 | 查询历史仓位 | GET | `/future/trade/v1/position/list-history` |

    | 10 | 查询全仓维持保证金 | GET | `/future/trade/v1/position/cross-margin/{symbol}` |


    **Biz-user：**


    | 序号 | 接口名称 | 请求类型 | 路径 |

    | --- | --- | --- | --- |

    | 11 | 查询自动减仓历史 | GET | `/future/user/v1/auto-deleverage/history` |

    | 12 | 查询单币种资产 | GET | `/future/user/v1/compat/balance/{coin}` |

    | 13 | 查询接管记录 | GET | `/future/user/v1/taker-over/list` |

    | 14 | 查询历史止盈止损委托 | GET | `/future/trade/v1/entrust/profit-list-history` |


    #### 2025-11-05


    优化文档结构，补充了请求示例（curl）。保留原有参数与响应说明，无业务逻辑变更。


    #### 2025-11-04


    结构调整 - 修改了大部分子项的名称，统一命名风格。删除订阅参数页面。将部分子项移动到通用 WebSocket 信息。


    #### 2025-11-03


    信息架构 - 删除子模块：频率限制规则、API 库、返回格式。新增子模块：更新日志。子模块重命名：错误码 → 通用错误码。

left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---
