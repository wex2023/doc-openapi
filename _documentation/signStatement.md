---
title: Signature Instructions
position_number: 4
parameters:
- name:
content:
content_markdown: >-
    Since WEX needs to provide some open interfaces for third-party platforms, the issue of **data security** needs to be considered.


    Such as:

    - Whether the data has been tampered with

    - Whether the data is outdated

    - Whether the data can be submitted repeatedly

    - The access frequency of the interface


    Among these, **whether data has been tampered with is the most important issue**.


    **Steps:**


    1. **Appkey & Secretkey** Apply for `appkey` and `secretkey` in the user center first, each user's keys are different.


    2. **Timestamp** Add `timestamp`.
    Its value should be the **unix timestamp (milliseconds)** of the time when the request is sent.
    The time of the data is calculated based on this value.


    3. **Signature** Add `signature`, its value is obtained by the signature algorithm rule.


    4. **RecvWindow** Add `recvwindow` (defines the valid time of the request).
    Valid time is fixed at a certain value.
    When a request is received, the server checks if: serverTime - timestamp < recvwindow.
    Any request older than **5000 ms** is invalid.
    If the client's timestamp is more than **1 second ahead of server time**, the request is invalid.
    **Note:** Online conditions are not always 100% reliable. That's why we provide the `recvWindow` parameter.
    For high-frequency trading, adjust `recvWindow` to meet timeliness needs.
    RecvWindow longer than **5 seconds** is **not recommended**.


    5. **Algorithm** Add `algorithms` (signature method).
    Recommended: `HmacSHA256`.
    Supported algorithms: HmacMD5, HmacSHA1, HmacSHA224, **HmacSHA256 (recommended)**, HmacSHA384, HmacSHA512
examples:
  -
    name: validate-appkey
    mandatory: true
    example: dbefbc809e3e83c283a984c3a1459732ea7db1360ca80c5c2c8867408d28cc83
    description:
  -
    name: validate-timestamp
    mandatory: true
    example: 1641446237201
    description:
  -
    name: validate-signature
    mandatory: true
    example: 0a7d0b5e802eb5e52ac0cfcd6311b0faba6e2503a9a8d1e2364b38617877574d
    description:
  -
    name: validate-recvwindow
    mandatory: true
    example: 5000 (millisecond)
    description:
  -
    name: validate-algorithms
    mandatory: true
    example: HmacSHA256
    description: HmacMD5, HmacSHA1, HmacSHA224, HmacSHA256, HmacSHA384, HmacSHA512. Default is HmacSHA256
  -
    name: validate-signversion
    mandatory: false
    example: 1.0
    description: Reserved, signed version number

left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---
