---
title: Create Track
position_number: 13
type: post
description: /future/trade/v1/entrust/create-track
parameters:
    -
        name: callback
        type: string
        mandatory: true
        default:
        description: Callback type configuration
        ranges: FIXED;PROPORTION
    -
        name: callbackVal
        type: number
        mandatory: true
        default:
        description: "Callback value (must be > 0)"
        ranges: ">0"
    -
        name: orderSide
        type: string
        mandatory: true
        default:
        description: Order side
        ranges: BUY;SELL
    -
        name: origQty
        type: number
        mandatory: true
        default:
        description: Original quantity (contracts)
        ranges:
    -
        name: positionSide
        type: string
        mandatory: true
        default:
        description: Position side
        ranges: BOTH;LONG;SHORT
    -
        name: positionType
        type: string
        mandatory: true
        default:
        description: Position type
        ranges: CROSSED;ISOLATED
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair
        ranges:
    -
        name: triggerPriceType
        type: string
        mandatory: true
        default:
        description: Trigger price type
        ranges: INDEX_PRICE;MARK_PRICE;LATEST_PRICE
    -
        name: activationPrice
        type: number
        mandatory: false
        default:
        description: Activation price
        ranges:
    -
        name: clientMedia
        type: string
        mandatory: false
        default:
        description: Client media
        ranges:
    -
        name: clientMediaChannel
        type: string
        mandatory: false
        default:
        description: Client media channel
        ranges:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: Client order ID
        ranges:
    -
        name: expireTime
        type: integer
        mandatory: false
        default:
        description: Expiration time
        ranges:
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_symbol | Trading pair does not exist |

    | symbol_is_not_trading | Trading pair is not available for trading |

    | symbol_not_support_openapi | The trading pair does not support placing orders via OpenAPI |

    | deposit_coupon_exists | The coupon has been claimed or already bound |

    | exist_bonus_positon_not_create_reverse_position | Reverse position cannot be created |

    | invalid_params | Invalid or missing parameters |

    | invalid_exceed_max_rate_limit | Callback ratio exceeds maximum limit |

    | invalid_below_min_rate_limit | Callback ratio below minimum limit |

    | invalid_exceed_max_price_limit | Callback ratio exceeds latest transaction price limit |

    | invalid_exceed_min_price_limit | Callback ratio below latest transaction price limit |

    | invalid_activation_price | Invalid activation price |

    | invalid_quantity_scale | Quantity must be an integer |

    | user_can_not_trade | Account prohibited from trading |

    | sub_account_not_trade | Sub-account cannot trade |

    | user_can_not_open_position | Account restricted from opening positions |

    | symbol_is_not_open_position | The trading pair is not open for new positions |

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
