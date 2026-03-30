---
title: Signature generation
position_number: 5
parameters:
- name:
content:
content_markdown: >-

    Take https://sapi.wexex.io/v4/order as an example.


    The following **appKey/secret** are **for demo only** (Linux bash with `echo`, `openssl`, `curl`):


    appKey: 3976eb88-76d0-4f6e-a6b2-a57980770085


    secretKey: bc6630d0231fda5cd98794f52c4998659beda290




    Required Headers:

        validate-algorithms: HmacSHA256

        validate-appkey: 3976eb88-76d0-4f6e-a6b2-a57980770085

        validate-recvwindow: 5000

        validate-timestamp: 1641446237201

        validate-signature: 2b5eb11e18796d12d88f13dc27dbbd02c2cc51ff7059765ed9821957d82bb4d9



    Sample Request Body:

        {
          "type": "LIMIT",
          "timeInForce": "GTC",
          "side": "BUY",
          "symbol": "btc_usdt",
          "price": "39000",
          "quantity": "2"
        }



    **1. Data Part Concatenation (Y)**

        method: uppercase HTTP method, e.g. GET, POST, DELETE, PUT

        path: concrete RESTful path after filling variables, e.g. /sign/test/bb/aa

        query: sort all key=value by key (lexicographical), join with &. Example: userName=dfdfdf&password=ggg

        body:
            JSON: use the raw JSON string (no conversion/sorting)

            x-www-form-urlencoded: sort all key=value by key (lexicographical), join with &. Example: userName=dfdfdf&password=ggg

            form-data: not supported

        If multiple forms exist, concatenate in order: path -> query -> body.


    Method example:

        POST

    Path example:

        /v4/order

        The above concatenated value is recorded as path



    Parameters passed query example:

        symbol=btc_usdt

        The above concatenated value is recorded as query



    Parameters via body example:

        x-www-form-urlencoded:

            symbol=btc_usdt&side=BUY&type=LIMIT&timeInForce=GTC&quantity=1&price=0.1

            The above concatenated value is recorded as body

        json:

            {"symbol":"btc_usdt","side":"BUY","type":"LIMIT","timeInForce":"GTC","quantity":2,"price":39000}

            The above concatenated value is recorded as body



    Mixed use of query and body (divided into form and json format):

        query:
            symbol=btc_usdt&side=BUY&type=LIMIT
            The above concatenated value is recorded as query

        body:
            {"symbol":"btc_usdt","side":"BUY","type":"LIMIT"}
            The above concatenated value is recorded as body



    Finally, splice by # with leading markers:

        Y = #method#path#query#body

    Notice:

        query present, body empty: Y = #method#path#query

        query empty, body present: Y = #method#path#body

        both present: Y = #method#path#query#body




    **2. Header Part Concatenation (X)**

        Sort the following header keys in natural ascending alphabetical order, then join with &:

            validate-algorithms=HmacSHA256&validate-appkey=3976eb88-76d0-4f6e-a6b2-a57980770085&validate-recvwindow=5000&validate-timestamp=1641446237201



    **3. Generate Signature**

        Concatenate original = X + Y (no delimiter beyond the # already in Y), then compute:

        signature = org.apache.commons.codec.digest.HmacUtils.hmacSha256Hex(secretKey, original);

        Add the generated value to the request header: validate-signature: <signature>


    **4. Complete Example**

        Sample original signature message:

            validate-algorithms=HmacSHA256&validate-appkey=2063495b-85ec-41b3-a810-be84ceb78751&validate-recvwindow=60000&validate-timestamp=1666026215729#POST#/v4/order#{"symbol":"XT_USDT","side":"BUY","type":"LIMIT","timeInForce":"GTC","bizType":"SPOT","price":3,"quantity":2}

        Matters needing attention:

            Ensure Content-Type, signature original message, and final request payload are consistent.

            validate-timestamp should be milliseconds of the send time; pair with a reasonable validate-recvwindow to tolerate network jitter.

            When body is JSON, use the exact raw JSON string for signing (don't reorder keys or prettify).


left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---
