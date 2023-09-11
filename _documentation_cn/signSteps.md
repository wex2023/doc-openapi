---
title: 签名生成
position_number: 5
parameters:
- name:
content:
content_markdown: >-

    以https://sapi.wexex.io/v4/order为例。
    
    
    以下是在linux bash环境下使用 echo openssl 和curl工具实现的一个调用接口下单的示例 appkey、secret仅供示范：
    
    
    appKey: 48f05386-4228-48e1-a69f-c9abd2d8fa52
    

    secretKey: 8fcffde41cb50b18ce9178424f38d3b688fd0f47
    




    Header部分数据：

        validate-algorithms: HmacSHA256
    
        validate-appkey: 48f05386-4228-48e1-a69f-c9abd2d8fa52
    
        validate-recvwindow: 5000
    
        validate-timestamp: 1692672585907
    
        validate-signature: c58a59cf674b80bd3c9182f3db4feddc87ea4f3be7762bbf4bfab39429eec7e9



    请求数据：

        {
          type: 'LIMIT',
          timeInForce: 'GTC',
          side: 'BUY',
          symbol: 'btc_usdt',
          bizType: 'SPOT'
          price: '39000',
          quantity: '2'
        }



    1、数据部分

        method: 大写的请求方法，例如：GET、POST、DELETE、PUT

        path: 按照path中顺序将所有value进行拼接。形如/test/{var1}/{var2}/的restful路径将按填入的实际参数后路径拼接，示例：/sign/test/bb/aa
  
        query: 按照key的字典序排序，将所有key=value进行拼接。示例：userName=dfdfdf&password=ggg
  
        body:   
            Json: 直接按JSON字符串不做转换或排序操作。
  
            x-www-form-urlencoded: 按照key的字典序排序，将所有key=value进行拼接，示例:userName=dfdfdf&password=ggg　
    
            form-data：此格式暂不支持。
  
        如果存在多种数据形式，则按照path、query、body的顺序进行再拼接，得到所有数据的拼接值。

    方法method示例：
        
        POST


    路径path示例:

        /v4/order

        上述拼接值记作为path



    参数通过query示例:

        symbol=btc_usdt

        上述值拼接记作query



    参数通过body示例

        x-www-form-urlencoded:
      
            symbol=btc_usdt&side=BUY&bizType=SPOT&quantity=2&price=39000&type=LIMIT&timeInForce=GTC

            上述值拼接记作body

        json:
  
            {"symbol":"btc_usdt","side":"BUY","bizType":"SPOT","quantity":2,"price":39000,"type":"LIMIT","timeInForce":"GTC"}

            上述值拼接记作body



    混合使用query与body(分为表单与json两种格式)

        query: 
            symbol=btc_usdt&side=BUY&type=LIMIT
            上述拼接值记作query

        body: 
            {"symbol":"btc_usdt","side":BUY,"type":"LIMIT"}
            上述拼接值记作body



    整个数据最且拼接值由#符号分别与method、path、query、body进行拼接成#method、#path、#query、#body，最终拼接值记作为Y=#method#path#query#body。

    注意：

        query有数据，body无数据：Y=#method#path#query

        query无数据，body有数据：Y=#method#path#body

        query有数据，body有数据：Y=#method#path#query#body





    2、请求头部分
        将key按照字母自然升序后，使用&方式拼接在一起，作为X。如：

            validate-algorithms=HmacSHA256&validate-appkey=48f05386-4228-48e1-a69f-c9abd2d8fa52&validate-recvwindow=5000&validate-timestamp=1692672585907



    3、生成签名
    
        最终把需要进行加密的字符串，记作为original=XY
    
        最后将最终拼接值按照如下方法进行加密得到签名。
    
        signature=org.apache.commons.codec.digest.HmacUtils.hmacSha256Hex(secretkey, original);
    
        将生成的签名singature放到请求头中，以validate-signature为Key，以singature为值。

    4、样例

        签名原始报文样例：

            validate-algorithms=HmacSHA256&validate-appkey=48f05386-4228-48e1-a69f-c9abd2d8fa52&validate-recvwindow=5000&validate-timestamp=1692672585907#POST#/v4/order#{"symbol":"btc_usdt","side":"BUY","bizType":"SPOT","quantity":2,"price":39000,"type":"LIMIT","timeInForce":"GTC"}

        请求报文样例：
      
            curl --location --request POST 'https://sapi.wexex.io/v4/order' 
            --header 'accept: */*' 
            --header 'Content-Type: application/json' 
            --header 'validate-algorithms: HmacSHA256' 
            --header 'validate-appkey: 48f05386-4228-48e1-a69f-c9abd2d8fa52' 
            --header 'validate-recvwindow: 5000' 
            --header 'validate-timestamp: 1692672585907' 
            --header 'validate-signature: c58a59cf674b80bd3c9182f3db4feddc87ea4f3be7762bbf4bfab39429eec7e9' 
            --data-raw '{"symbol":"btc_usdt","side":"BUY","bizType":"SPOT","quantity":2,"price":39000,"type":"LIMIT","timeInForce":"GTC"}'
        
        注意事项：
            注意检查 Content-Type、签名原始报文中的参数格式、请求报文中的参数格式
      
left_code_blocks:
- code_block:
  title:
  language:
right_code_blocks:
- code_block:
  title:
  language:
---