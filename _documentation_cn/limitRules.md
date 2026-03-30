---
title: 频率限制规则
position_number: 3
parameters:
- name:
content:
content_markdown: |-
  某些接口会有限流控制（相应接口会有限流说明）。
  限流主要分为**网关限流**和 **WAF 限流**。

  如果接口请求触发网关限流，将返回 **429**，
  表示访问频率超过限制，**IP** 或 **apiKey** 将被封禁。

  网关限流分为：

  - **IP 限流**
  - **apiKey 限流**

  **示例说明**：

  - IP 限流：`100/s/ip` - 表示该接口**每个 IP 每秒**的请求次数限制。

  - apiKey 限流：`50/s/apiKey` - 表示该接口**每个 apiKey 每秒**的请求次数限制。
left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---
