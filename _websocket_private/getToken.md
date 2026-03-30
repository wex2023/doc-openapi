---
title: Get token
position_number: 4
split: '-------------------------------------'
type: post
description: /v4/ws-token
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **Notes:**

    - Limit flow rules: **1 request / 10s / apikey**

    - The accessToken is valid for **2 days**.

    - Calling this endpoint again will **reset the validity period**.

    - accessToken is equivalent to **listenKey**, used for establishing WebSocket connections.
left_code_blocks:
    -
        code_block: |-
            curl --location --request POST 'https://sapi.xt.com/v4/ws-token' \
              --header 'accept: */*' \
              --header 'Content-Type: application/json' \
              --header 'validate-algorithms: HmacSHA256' \
              --header 'validate-recvwindow: 60000' \
              --header 'validate-appkey: xxxxxxxxxx' \
              --header 'validate-timestamp: xxxxxxxxxx' \
              --header 'validate-signature: xxxxxxxxxx'
        title: Request
        language: bash
right_code_blocks:
    -
        code_block: |-
            {
                "rc": 0,
                "mc": "SUCCESS",
                "ma": [],
                "result": {
                    "accessToken": "eyJhbqGciOiJSUzI1NiJ9.eyJhY2NvdW50SWQiOiIyMTQ2Mjg1MzIyNTU5Iiwic3ViIjoibGh4dDRfMDAwMUBzbmFwbWFpbC5jYyIsInNjb3BlIjoiYXV0aCIsImlzcyI6Inh0LmNvbSIsImxhc3RBdXRoVGltZSI6MTY2MzgxMzY5MDk1NSwic2lnblR5cGUiOiJBSyIsInVzZXJOYW1lIjoibGh4dDRfMDAwMUBzbmFwbWFpbC5jYyIsImV4cCI6MTY2NjQwNTY5MCwiZGV2aWNlIjoidW5rbm93biIsInVzZXJJZCI6MjE0NjI4NTMyMjU1OX0.h3zJlJBQrK2x1HvUxsKivnn6PlSrSDXXXJ7WqHAYSrN2CG5XPTKc4zKnTVoYFbg6fTS0u1fT8wH7wXqcLWXX71vm0YuP8PCvdPAkUIq4-HyzltbPr5uDYd0UByx0FPQtq1exvsQGe7evXQuDXx3SEJXxEqUbq_DNlXPTq_JyScI",
                    "refreshToken": "eyJhbGciOiqJSUzI1NiJ9.eyJhY2NvdW50SWQiOiIyMTQ2Mjg1MzIyNTU5Iiwic3ViIjoibGh4dDRfMDAwMUBzbmFwbWFpbC5jYyIsInNjb3BlIjoicmVmcmVzaCIsImlzcyI6Inh0LmNvbSIsImxhc3RBdXRoVGltZSI6MTY2MzgxMzY5MDk1NSwic2lnblR5cGUiOiJBSyIsInVzZXJOYW1lIjoibGh4dDRfMDAwMUBzbmFwbWFpbC5jYyIsImV4cCI6MTY2NjQwNTY5MCwiZGV2aWNlIjoidW5rbm93biIsInVzZXJJZCI6MjE0NjI4NTMyMjU1OX0.Fs3YVm5YrEOzzYOSQYETSmt9iwxUHBovh2u73liv1hLUec683WGfktA_s28gMk4NCpZKFeQWFii623FvdfNoteXR0v1yZ2519uNvNndtuZICDdv3BQ4wzW1wIHZa1skxFfqvsDnGdXpjqu9UFSbtHwxprxeYfnxChNk4ssei430"
                }
            }
        title: Response
        language: json
---
