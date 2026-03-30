---
title: 常见问题
position_number: 12
parameters:
- name:
content:
content_markdown: |-
    1. **AUTH_105**
       服务器会验证请求头参数 `validate-timestamp` (`validTimeStamp`) 和 `validate-recvwindow` (`recvwindow`)。

       必须遵循以下规则：

       dealTimeStamp（服务器处理请求的时间，毫秒） - validTimeStamp < recvwindow

       否则将返回 **AUTH_105**。

       为避免此错误：

       - `validate-timestamp` 建议使用发送请求时的时间，单位为**毫秒**。
       - `validate-recvwindow` 应设置得稍大一些。


left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---
