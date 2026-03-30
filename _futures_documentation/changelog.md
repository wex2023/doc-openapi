---
title: Changelog
position_number: 6
parameters:
- name:
content:
content_markdown: >-
    #### New API Endpoints (2025-12-05)


    A total of **14 new endpoints** have been added, covering **Biz-order** and **Biz-user** modules.


    **Biz-order:**


    | No. | API Name | Method | Path |

    | --- | --- | --- | --- |

    | 1 | Get Reverse Plan Orders | GET | `/future/trade/v1/entrust/reverse-plan-list` |

    | 2 | Get Historical Reverse Plan Orders | GET | `/future/trade/v1/entrust/reverse-plan-list-history` |

    | 3 | Get Historical TP/SL Orders | GET | `/future/trade/v1/entrust/profit-list-history` |

    | 4 | Get Historical Orders with Trades | GET | `/future/trade/v1/order/trade-history` |

    | 5 | Get All Trade Details (No Pagination) | GET | `/future/trade/v1/order/trade-list-all` |

    | 6 | Get All Orders | GET | `/future/trade/v1/order-entrust/list` |

    | 7 | Get Active Positions | GET | `/future/trade/v1/position/list/active` |

    | 8 | Get Leverage Info | GET | `/future/trade/v1/position/leverage/list` |

    | 9 | Get Historical Positions | GET | `/future/trade/v1/position/list-history` |

    | 10 | Get Cross Margin Maintenance | GET | `/future/trade/v1/position/cross-margin/{symbol}` |


    **Biz-user:**


    | No. | API Name | Method | Path |

    | --- | --- | --- | --- |

    | 11 | Get Auto-Deleveraging History | GET | `/future/user/v1/auto-deleverage/history` |

    | 12 | Get Single Coin Balance | GET | `/future/user/v1/compat/balance/{coin}` |

    | 13 | Get Take-Over Records | GET | `/future/user/v1/taker-over/list` |

    | 14 | Get Historical TP/SL Orders | GET | `/future/trade/v1/entrust/profit-list-history` |


    #### 2025-11-05


    Optimized documentation structure and added request examples. No change to API behavior or response schema.


    #### 2025-11-04


    Structure changes - Renamed most sub-item/page titles for consistency. Removed the Subscription parameters page. Moved several sub-items into General WebSocket Information.


    #### 2025-11-03


    Information architecture - Removed submodules: Rate limit rules, API library, Response format. Added submodule: Changelog. Renamed submodule: Error codes to General error codes.

left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---
