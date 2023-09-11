---
title: Signature generation
position_number: 5
parameters:
- name:
content:
content_markdown: >-

    Take https://sapi.wexex.io/v4/order as an example.
    
    
    The following is an example appkey and secret for placing an order using a call interface implemented by echo openssl and curl tools in the linux bash environment for demonstration purposes only:
    
    
    appKey: 48f05386-4228-48e1-a69f-c9abd2d8fa52
    

    secretKey: 8fcffde41cb50b18ce9178424f38d3b688fd0f47
    




    Header part data：

        validate-algorithms: HmacSHA256
    
        validate-appkey: 48f05386-4228-48e1-a69f-c9abd2d8fa52
    
        validate-recvwindow: 5000
    
        validate-timestamp: 1692672585907
    
        validate-signature: c58a59cf674b80bd3c9182f3db4feddc87ea4f3be7762bbf4bfab39429eec7e9



    request data：

        {
          type: 'LIMIT',
          timeInForce: 'GTC',
          side: 'BUY',
          symbol: 'btc_usdt',
          bizType: 'SPOT'
          price: '39000',
          quantity: '2'
        }



    1.data part

        method: UpperCase method. eg: GET, POST, DELETE, PUT
    
        path: Concatenate all values in the order in path. The restful path in the form of /test/{var1}/{var2}/ will be spliced according to the actual parameters filled in, for example: /sign/test/bb/aa
  
        query: Sort all key=value according to the lexicographical order of the key. Example: userName=dfdfdf&password=ggg
  
        body:   
            Json: Directly by JSON string without conversion or sorting.
  
            x-www-form-urlencoded: Sort all key=values according to the lexicographical order of keys, for example: userName=dfdfdf&password=ggg
    
            form-data：This format is not currently supported.
  
        If there are multiple data forms, re-splicing is performed in the order of path, query, and body to obtain the splicing value of all data.


    Method example:
        
        POST

    Path example:

        /v4/order

        The above concatenated value is recorded as path



    Parameters passed query example:

        symbol=btc_usdt

        The above concatenated value is recorded as query



    Parameters via body example

        x-www-form-urlencoded:
      
            symbol=btc_usdt&side=BUY&bizType=SPOT&quantity=2&price=39000&type=LIMIT&timeInForce=GTC

            The above concatenated value is recorded as body

        json:
  
            {"symbol":"btc_usdt","side":"BUY","bizType":"SPOT","quantity":2,"price":39000,"type":"LIMIT","timeInForce":"GTC"}

            The above concatenated value is recorded as body



    Mixed use of query and body (divided into form and json format)

        query: 
            symbol=btc_usdt&side=BUY&type=LIMIT
            The above concatenated value is recorded as query

        body: 
            {"symbol":"btc_usdt","side":BUY,"type":"LIMIT"}
            The above concatenated value is recorded as body



    The most concatenated value of the entire data is spliced with method, path, query, and body by the # symbol to form #method, #path, #query, and #body, and the final spliced value is recorded as Y=#method#path#query#body.

    Notice：

        The query has data, but the body has no data: Y=#method#path#query

        query has no data, body has data: Y=#method#path#body

        query has data, body has data: Y=#method#path#query#body





    2.request header part
        After the keys are in natural ascending alphabetical order, use & to join them together as X. like:

            validate-algorithms=HmacSHA256&validate-appkey=48f05386-4228-48e1-a69f-c9abd2d8fa52&validate-recvwindow=5000&validate-timestamp=1692672585907



    3.generate signature
    
        Finally, the string that needs to be encrypted is recorded as original=XY
    
        Finally, encrypt the final concatenated value according to the following method to obtain a signature.
    
        signature=org.apache.commons.codec.digest.HmacUtils.hmacSha256Hex(secretkey, original);
    
        Put the generated signature singature in the request header, with validate-signature as the key and singature as the value.

    4.example

        sample of original signature message:
          
            validate-algorithms=HmacSHA256&validate-appkey=48f05386-4228-48e1-a69f-c9abd2d8fa52&validate-recvwindow=5000&validate-timestamp=1692672585907#POST#/v4/order#{"symbol":"btc_usdt","side":"BUY","bizType":"SPOT","quantity":2,"price":39000,"type":"LIMIT","timeInForce":"GTC"}

        sample request message:
  
            curl --location --request POST 'https://sapi.wexex.io/v4/order' 
            --header 'accept: */*' 
            --header 'Content-Type: application/json' 
            --header 'validate-algorithms: HmacSHA256' 
            --header 'validate-appkey: 48f05386-4228-48e1-a69f-c9abd2d8fa52' 
            --header 'validate-recvwindow: 5000' 
            --header 'validate-timestamp: 1692672585907' 
            --header 'validate-signature: c58a59cf674b80bd3c9182f3db4feddc87ea4f3be7762bbf4bfab39429eec7e9' 
            --data-raw '{"symbol":"btc_usdt","side":"BUY","bizType":"SPOT","quantity":2,"price":39000,"type":"LIMIT","timeInForce":"GTC"}'    

        matters needing attention:

            Pay attention to checking the parameter format of Content Type, signature original message and request message


left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---