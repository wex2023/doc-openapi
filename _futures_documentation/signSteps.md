---
title: Obtain Signature
position_number: 3
parameters:
- name:
content:
content_markdown: >-
    #### Generate Signature


    Note: `${?}` and `$?` refer to variable substitution.


    To generate a signature (`signature`), use the **SECRET KEY** obtained with your API Key to encrypt the `unencrypted_string`.


    #### Rules


    - **If HTTP request parameters are in QueryString:** `unencrypted_string = ${fixed_header}#${end_point}#${query_string}` When multiple key-value pairs exist in `query_string`, sort the keys **alphabetically** and concatenate with `&`, for example: `keya=value&keyb=value&keyc=value`


    - **If HTTP request parameters are in RequestBody:** `unencrypted_string = ${fixed_header}#${end_point}#${request_body}`


    #### fixed_header Format


    `fixed_header = "validate-appkey=${your_appkey}&validate-timestamp=${current_timestamp}"`


    Each part of `unencrypted_string` is joined with `#`.


    #### Example Breakdown


    Suppose current timestamp = ***** and your APPKEY = ++++++


    `fixed_header="validate-appkey=++++++&validate-timestamp=*****"`

    `end_point="/future/user/v1/balance/detail"`

    `query_string="coin=btc"`


    Then: `unencrypted_string="validate-appkey=++++++&validate-timestamp=*****#/future/user/v1/balance/detail#coin=btc"`


    #### Generate the Signature


    After obtaining the unencrypted_string, you can use the encryption algorithm along with the SECRETKEY to obtain the signature SIGNATURE for the unencrypted_string.


    After generating the signature, include `SIGNATURE` in the HTTP request header as the value of `validate-signature`.

left_code_blocks:
- code_block: |-
    # Generate signature example
    SIGNATURE=$(echo -n "$unencrypted_string" | \
      openssl dgst -sha256 -hmac "$SECRETKEY" | \
      awk '{print $2}')
    echo $SIGNATURE
  title: Shell
  language: bash
right_code_blocks:
- code_block:
  title:
  language:
---
