---
title: Basic Information of the Interface
position_number: 1
parameters:
- name:
content:
content_markdown: >-
    #### Base URLs


    - **USDT-M:** `https://fapi.wexex.io` (for USDT-margined futures)

    - **Coin-M:** `https://dapi.wexex.io` (for Coin-margined futures)


    #### Network Recommendation


    It is **not recommended** to access XT APIs via proxy due to **high latency and poor stability**.


    #### Request Methods


    - **GET requests:** Parameters should be passed in the **QueryString**.

    - **POST requests:** Parameters can be passed in the **RequestBody** or **QueryString**.


    When parameters are in the QueryString, include the header: `Content-Type: application/x-www-form-urlencoded`


    When parameters are in the RequestBody, include the header: `Content-Type: application/json`


    #### API Categories


    XT API endpoints are divided into **Public Interfaces** and **User Interfaces**.


    **Public Interfaces** - No authentication required. Parameters are placed in the QueryString. Usually use the GET method.


    **User Interfaces** - Require authentication via HTTP headers. Along with QueryString or RequestBody parameters, the following four headers are required:


    | Header | Description |

    | --- | --- |

    | `validate-appkey` | User API key |

    | `validate-timestamp` | Current timestamp (in milliseconds) |

    | `validate-signature` | Request signature |

    | `Content-Type` | Request content type |


    Endpoints that do **not require signature authentication** will be explicitly indicated.


    #### Authentication References


    - **How to obtain an APPKEY:** See Apply for API Key section.

    - **How to generate a signature:** See Obtain Signature section.


    #### Rate Limits


    - **Asset-related endpoints:** Up to 3 requests per second.

    - **Other endpoints:** Up to 10 requests per second per user, and 1000 requests per minute per IP.


    If the frequency limit is exceeded, the account will be locked for 10 minutes.

left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---
