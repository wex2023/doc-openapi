---
title: FAQ
position_number: 12
parameters:
- name:
content:
content_markdown: |-
    1. **AUTH_105**
       The server verifies the request header parameters `validate-timestamp` (`validTimeStamp`) and `validate-recvwindow` (`recvwindow`).

       The following rules must be followed:

       dealTimeStamp (server time when the request is processed, in milliseconds) - validTimeStamp < recvwindow

       Otherwise **AUTH_105** will be returned.

       To avoid this error:

       - `validate-timestamp` is recommended to use the time when the request was sent, in **milliseconds**.
       - `validate-recvwindow` should be set a little larger.


left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---
