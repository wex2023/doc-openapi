---
title: Frequency Limiting Rules
position_number: 3
parameters:
- name:
content:
content_markdown: |-
  Some interfaces will have limited flow control (the corresponding interface will have a limited flow description).
  The flow limit is mainly divided into **gateway flow limit** and **WAF flow limit**.

  If the interface request triggers the gateway flow limit, **429** will be returned,
  indicating that the access frequency exceeds the limit, and the **IP** or **apiKey** will be blocked.

  Gateway flow limiting is divided into:

  - **IP flow limiting**
  - **apiKey flow limiting**

  **Example descriptions**:

  - IP flow limit: `100/s/ip` - indicates the limit of the number of requests **per second per IP** for this interface.

  - apiKey flow limit: `50/s/apiKey` - indicates the limit of the number of requests **per second per apiKey** for this interface.
left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---
