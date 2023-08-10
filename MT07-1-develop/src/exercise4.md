## GET ​/api​/v1​/Books

- URL https://fakerestapi.azurewebsites.net/api/v1/Books

- Ожидаемый результат код ответа :200, тест успешно пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: b8744e30-2ff0-417e-87d6-23f58fd06def
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 11:33:32 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
    [
    {
        "id": 1,
        "title": "Book 1",
        "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "pageCount": 100,
        "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "publishDate": "2023-06-05T11:33:33.6016859+00:00"
    },
    {
        "id": 2,
        "title": "Book 2",
        "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "pageCount": 200,
        "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "publishDate": "2023-06-04T11:33:33.6017004+00:00"
    },
    {
        "id": 3,
        "title": "Book 3",
        "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "pageCount": 300,
        "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "publishDate": "2023-06-03T11:33:33.601711+00:00"
    },
    ]
```

## POST ​/api​/v1​/Books

- URL https://fakerestapi.azurewebsites.net/api/v1/Books

- Ожидаемый результат код ответа: 201, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 1648025f-a3d5-4693-b652-7038be89fc81
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": 1,
    "title": "Book 5",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-06-05T18:58:26.012Z"
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 11:33:33 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
    [
    {
    "id": 1,
    "title": "Book 5",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-06-05T18:58:26.012Z"
    }
    ]
```
## POST ​/api​/v1​/Books с пустыми строками 

- URL https://fakerestapi.azurewebsites.net/api/v1/Books

- Ожидаемый результат код ответа :400, тест успешно пройден 

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 91d2c5a2-8e54-446c-86c5-de39b48cb087
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": ,
    "title": ,
    "description": ,
    "pageCount": ,
    "excerpt": ,
    "publishDate":
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 11:33:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-da3902d763b33a4985a68624e406f622-4e9c73a5300ac24b-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 10."
        ]
    }
}
```
## POST ​/api​/v1​/Books с некорректным JSON

- URL https://fakerestapi.azurewebsites.net/api/v1/Books

- Ожидаемый результат код ответа :400, тест успешно пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: d555c672-022e-4f95-815e-ef4d476200b9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": 0,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-06-03T11:10:20.468Z"
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 11:33:35 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-a1f49498464f9647befe0252fa272d1a-58a96e614ac02b44-00",
    "errors": {
        "$": [
            "Expected depth to be zero at the end of the JSON payload. There is an open JSON object or array that should be closed. Path: $ | LineNumber: 6 | BytePositionInLine: 42."
        ]
    }
}
```
## POST ​/api​/v1​/Books с неправильным ID

- URL https://fakerestapi.azurewebsites.net/api/v1/Books

- Ожидаемый результат код ответа :400, тест успешно пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 370d0408-6ce4-4c93-a47c-4343d6a31597
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": null,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-06-03T11:16:39.599Z"
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 14:06:24 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-5eca5b9e7622f74fb3169b5191655643-4269c7eefba69847-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 11."
        ]
    }
}
```
## GET ​/api​/v1​/Books​/{id}

- URL https://fakerestapi.azurewebsites.net/api/v1/Books/{{book_id}}

- Ожидаемый результат код ответа :200, тест успешно пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: cef16fb1-3e17-4988-a349-46ca38a08d8e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутсвует
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 14:29:03 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
{
    "id": 1,
    "title": "Book 1",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 100,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-06-05T14:29:04.4258864+00:00"
}
```
## GET ​/api​/v1​/Books​/{id} с несущетсвующим ID

- URL https://fakerestapi.azurewebsites.net/api/v1/Books/{{book_id}} 
- Ожидаемый результат код ответа :404, тест успешно пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: c5a67e83-7d63-4434-a1b1-999c1d5bae5d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутсвует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 14:29:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-7dfd363737b54142ba59d4275e32ed21-9dd27e755112d747-00"
}
```
## PUT /api​/v1​/Books​/{id}

- URL https://fakerestapi.azurewebsites.net/api/v1/Books/{{book_id}}
- Ожидаемый результат код ответа :200, тест успешно пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: f4340755-5b3e-406b-a56d-db3ca7e5194c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": 12,
    "title": "books12",
    "description": "reportoutput",
    "pageCount": 5,
    "excerpt": "string",
    "publishDate": "2023-06-02T09:15:22.557Z"
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 14:49:47 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
{
    "id": 12,
    "title": "books12",
    "description": "reportoutput",
    "pageCount": 5,
    "excerpt": "string",
    "publishDate": "2023-06-02T09:15:22.557Z"
}
```
## PUT /api​/v1​/Books​/{id} с пустыми строками

- URL https://fakerestapi.azurewebsites.net/api/v1/Books/{{bookbad_id}}
- Ожидаемый результат код ответа :400, тест успешно пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 448eeeb7-5ce7-4a53-86cb-50aefa623552
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": ,
    "title": "",
    "description": "",
    "pageCount": 0,
    "excerpt": "",
    "publishDate": "2023-06-02T09:15:22.557Z"
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 14:49:47 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-741434def08d3143b6089c8ada423411-f36db46657970342-00",
    "errors": {
        "id": [
            "The value '2525898963631' is not valid."
        ],
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```
## PUT /api​/v1​/Books​/{id} с несуществующим ID

- URL https://fakerestapi.azurewebsites.net/api/v1/Books/{{bookbad_id}}

- Ожидаемый результат код ответа :400, тест успешно пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 8af872fb-005c-42b0-b54a-55f3731286e4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": null,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-06-03T11:46:55.322Z"
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 14:49:48 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f466ab947c619946930b8c4ff39d6576-f527a1a1fe123b4b-00",
    "errors": {
        "id": [
            "The value '2525898963631' is not valid."
        ],
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 11."
        ]
    }
}
```
## PUT /api​/v1​/Books​/{id} с некорректным ID

- URL https://fakerestapi.azurewebsites.net/api/v1/Books/{{bookbad_id}}
- Ожидаемый результат код ответа :400, тест успешно пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: d733d9b4-322a-4705-bcad-14d62a03756a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": 0,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-06-03T12:07:03.662Z"
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 14:49:48 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ce9fa0997a0ac1489c1349771ddc6a66-603e889663e76f43-00",
    "errors": {
        "$": [
            "Expected depth to be zero at the end of the JSON payload. There is an open JSON object or array that should be closed. Path: $ | LineNumber: 6 | BytePositionInLine: 42."
        ],
        "id": [
            "The value '2525898963631' is not valid."
        ]
    }
}
```
## PUT /api​/v1​/Books​/{id} с отрицательным ID

- URL https://fakerestapi.azurewebsites.net/api/v1/Books/{{book_minus_id}}

- Ожидаемый результат код ответа :405, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: de5daf50-c5b8-4285-b4dc-ada6ac59af42
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": -1,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-06-03T11:46:55.322Z"
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 14:49:49 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
{
    "id": -1,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-06-03T11:46:55.322Z"
}
```
## DELETE /api​/v1​/Books​/{id} 

- URL https://fakerestapi.azurewebsites.net/api/v1/Books/{{book_id}}

- Ожидаемый результат код ответа: 200, тест успешно пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 45f02d0d-3ce2-4ee8-8534-088b04939959
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутсвует
```
- Заголовки ответа : 
```
Content-Length: 0
Date: Tue, 06 Jun 2023 14:49:49 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа 
```
Отсутсвует
```
## DELETE /api​/v1​/Books​/{id} с недопустимым значением ID 

- URL https://fakerestapi.azurewebsites.net/api/v1/Books/{{bookbad_id}}

- Ожидаемый результат код ответа: 400, тест успешно пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: f0f1757f-d5f4-49d9-963b-66693c31e268
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутсвует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 14:49:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-30cddd0465fd55468c10d8af54a30f9c-174ffec4395fcd4b-00",
    "errors": {
        "id": [
            "The value '2525898963631' is not valid."
        ]
    }
}
```

## GET /api​/v1​/CoverPhotos​/{id} получение обложки по ID 
- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id}}

- Ожидаемый результат код ответа: 200, тест успешно пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 5bb44fd7-3ebb-4b61-bfdf-6281cbb8321d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутсвует
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 15:37:02 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
{
    "id": 4,
    "idBook": 4,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 4&w=250&h=350"
}
```
## GET /api​/v1​/CoverPhotos​/{id} с некорректным ID

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphotobad_id}}

- Ожидаемый результат код ответа: 400, тест успешно пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 4a2c7b8c-1f1a-415d-a29c-d1472e48a5cb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутсвует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 15:41:45 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-9c2add016102c9408c5a87cf3369e1df-7486fb7de6b5d14b-00",
    "errors": {
        "id": [
            "The value '12345678909876' is not valid."
        ]
    }
}
```
## PUT ​/api​/v1​/CoverPhotos​/{id} обновление обложки

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id}}
- Ожидаемый результат код ответа: 200, тест успешно пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 51646a05-740c-4fa0-bfea-70e0c93e96cd
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": 12,
    "idBook": 1,
    "url": "string"
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 15:41:46 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
{
    "id": 12,
    "idBook": 1,
    "url": "string"
}
```
## PUT ​/api​/v1​/CoverPhotos​/{id} с пустыми строками

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphotobad_id}}
- Ожидаемый результат код ответа: 400, тест успешно пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: a64d81ac-8909-4b8b-a463-342f38470ed5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": ,
    "idBook": ,
    "url": ""
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 15:41:46 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-dd75625a6113594d9d3c1059d9ec7102-5610d2ea8e033d47-00",
    "errors": {
        "id": [
            "The value '12345678909876' is not valid."
        ],
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```
## PUT ​/api​/v1​/CoverPhotos​/{id} с несуществующим ID

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphotobad_id}}

- Ожидаемый результат код ответа: 400, тест успешно пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: b42228ca-3e3d-49cb-b2af-d44f9a5f3d0d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": null,
    "idBook": 0,
    "url": "string"
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 15:41:47 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-19cafd5b1a4d9646a1d00bf745bf3bd4-10fe3fe0d647114f-00",
    "errors": {
        "id": [
            "The value '12345678909876' is not valid."
        ],
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 11."
        ]
    }
}
```
## PUT ​/api​/v1​/CoverPhotos​/{id} с некорректным JSON

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphotobad_id}}

- Ожидаемый результат код ответа: 400, тест успешно пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 296cf962-12b3-43fa-a55a-1180e3b15dd4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": null,
    "idBook": 0,
    "url": "string"
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 15:41:48 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e0d97bff254f2643862275e3ab18a3c3-b9eaa8986a461e41-00",
    "errors": {
        "id": [
            "The value '12345678909876' is not valid."
        ],
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 11."
        ]
    }
}
```
## PUT ​/api​/v1​/CoverPhotos​/{id} с отрицательным ID

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_minus_id}}

- Ожидаемый результат код ответа: 405, тест провален 

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 394f6a40-f236-4e23-a4d6-c31fb2ef4196
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": -1,
    "idBook": 0,
    "url": "string"
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 15:41:48 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
{
    "id": -1,
    "idBook": 0,
    "url": "string"
}
```
## DELETE ​/api​/v1​/CoverPhotos​/{id} удаление обложки 

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphoto_id}}

- Ожидаемый результат код ответа: 200, тест пройден 

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 40ecf745-d154-46fd-a2c5-ab3c00bbab7b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутсвует
```
- Заголовки ответа : 
```
Content-Length: 0
Date: Tue, 06 Jun 2023 15:41:49 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа 
```
Отсутсвует
```
## DELETE ​/api​/v1​/CoverPhotos​/{id} с недопустимым значением ID 

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{coverphotobad_id}}

- Ожидаемый результат код ответа: 400, тест пройден 

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: d9769c3d-c851-43d0-9938-598d0c1298e6
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутсвует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 15:41:49 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-a8c6c5e9c8ea5146873f521f63ceaa6f-7b1fe3cc008b7d4f-00",
    "errors": {
        "id": [
            "The value '12345678909876' is not valid."
        ]
    }
}
```

## DELETE ​/api​/v1​/Users​/{id} удаление пользователя 

- URL https://fakerestapi.azurewebsites.net/api/v1/Users/6

- Ожидаемый результат код ответа: 200, тест пройден 

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 6f3a3081-101d-407e-b6b0-fef24de76c6d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутсвует
```
- Заголовки ответа : 
```
Content-Length: 0
Date: Tue, 06 Jun 2023 16:08:22 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа 
```
Отсутсвует
```
## DELETE ​/api​/v1​/Users​/{id} с недопустимым ID

- URL https://fakerestapi.azurewebsites.net/api/v1/Users/45648324864034

- Ожидаемый результат код ответа: 400, тест пройден 

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 35369842-98dc-4b42-9772-07d05a945635
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутсвует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 16:08:23 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f082cb09ed8ab34f84fb4cc9652564af-49a9134b2baada4e-00",
    "errors": {
        "id": [
            "The value '45648324864034' is not valid."
        ]
    }
}
```

## GET ​/api​/v1​/Activities

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities

- Ожидаемый результат: код ответа 200, тест успешно пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 993ebbca-1dde-4ffc-8414-22ff497d66bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : отсутствует

- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 09:35:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
    {
        "id": 1,
        "title": "Activity 1",
        "dueDate": "2023-06-06T10:47:35.1571188+00:00",
        "completed": false
    },
    {
        "id": 2,
        "title": "Activity 2",
        "dueDate": "2023-06-06T11:47:35.1571212+00:00",
        "completed": true
    },
    {
        "id": 3,
        "title": "Activity 3",
        "dueDate": "2023-06-06T12:47:35.1571215+00:00",
        "completed": false
    },
```
## POST ​/api​/v1​/Activities

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities

- Ожидаемый результат: код ответа 201, тест успешно пройден
- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: e4805522-054f-42f1-9b49-e7fbef3c83eb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id": {{activity_id}},
 "title": "string",
 "dueDate": "2023-06-03T08:12:24.110Z",
 "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 11:24:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
{
    "id": 5,
    "title": "string",
    "dueDate": "2023-06-03T08:12:24.11Z",
    "completed": true
}
```
## POST ​/api​/v1​/Activities негативный (буквы)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Accept: text/plain
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Cache-Control: no-cache
Postman-Token: d390e364-2cda-439c-b10e-f36295e394e1
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id": null,
 "title": "string",
 "dueDate": "2023-06-03T08:12:24.110Z",
 "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:02:36 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-47a6dac543576b4f9caf884f6bac9097-10d859e6be4cf148-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 11."
        ]
    }
}
```
## POST ​/api​/v1​/Activities негативный (пустой)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities

- Ожидаемый результат : код ответа 415, тест провален

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: c5fa4702-945d-48d4-964d-b1f0dfe0c184
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:06:02 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-2237da0d949529488d6e116558dbb832-18a64685b36a4043-00"
}
```
## GET ​/api​/v1​/Activities​/{id}

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

- Ожидаемый результат: код ответа 200, тест пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: fc762366-f216-412b-9f8a-aa5d1d2bbe33
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 12:11:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
{
    "id": 5,
    "title": "Activity 5",
    "dueDate": "2023-06-06T17:11:54.3421821+00:00",
    "completed": false
}
```
## POST ​/api​/v1​/Activities негативный (некорректный JSON)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 162bd20d-5c8c-43e8-892b-0b5a9bdff010
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id" 0,
 "title": "string",
 "dueDate": "2023-06-03T11:15:00.428Z",
 "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:14:52 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-6e87392994c9404a911da17cd3ce6720-02cfa81bcffffd47-00",
    "errors": {
        "$": [
            "'0' is invalid after a property name. Expected a ':'. Path: $ | LineNumber: 2 | BytePositionInLine: 6."
        ]
    }
}
```
## GET ​/api​/v1​/Activities​/{id} (некорректный ID)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activitybad_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 59f61d33-34bd-43d5-b04c-d93c07515376
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:17:14 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-90fb8139c5be5042bc54a368aa4d4ffb-68a116cf13326548-00",
    "errors": {
        "id": [
            "The value '45648324864034' is not valid."
        ]
    }
}
```
## PUT ​/api​/v1​/Activities​/{id}

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

- Ожидаемый результат: код ответа 200, тест пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9ad266a3-685c-46d9-a04f-57eddf337d70
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-05T17:24:24.293Z",
    "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 12:26:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-05T17:24:24.293Z",
    "completed": true
}
```
## PUT ​/api​/v1​/Activities​/{id} (некорректный ID)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activitybad_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9912c670-689f-4fa8-acf2-7f720c472526
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id": 0,
 "title": "string",
 "dueDate": "2023-06-03T11:30:34.198Z",
 "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:29:25 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-05T17:24:24.293Z",
    "completed": true
}
```
## POST ​/api​/v1​/Activities негативный (некорректный JSON)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: a77831ef-df3a-4495-acf3-d0c847a197d3
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id" 0,
 "title": "string",
 "dueDate": "2023-06-03T11:15:00.428Z",
 "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:32:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b4057a6ca8241c4bacf4e006a1d65cf6-0b6c2f3b84435d4a-00",
    "errors": {
        "$": [
            "'0' is invalid after a property name. Expected a ':'. Path: $ | LineNumber: 2 | BytePositionInLine: 6."
        ]
    }
}
```
## PUT ​/api​/v1​/Activities​/{id} (пустые строки)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 54f34c52-de84-4a85-a6f8-5783fac48fbd
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id": 0,
 "title": "string",
 "dueDate": "2023-06-03T15:39:25.038Z",
 
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:34:19 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-4b366e6fec403d4db990d5e82de3f602-664863e5941eec4c-00",
    "errors": {
        "$": [
            "The JSON object contains a trailing comma at the end which is not supported in this mode. Change the reader options. Path: $ | LineNumber: 10 | BytePositionInLine: 0."
        ]
    }
}
```
## DELETE ​/api​/v1​/Activities​/{id}

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

- Ожидаемый результат: код ответа 200, тест пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: f6b187d8-d0e4-4d94-b316-38cbd68f1ec9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутствует
```
- Заголовки ответа :
``` 
Content-Length: 0
Date: Tue, 06 Jun 2023 12:41:47 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа: 
```
отсутствует
```
## DELETE ​/api​/v1​/Activities​/{id} (некорректный id)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activitybad_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 5fbaf016-fe93-4481-97a5-d17e7fe6d4fa
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутствует
```
- Заголовки ответа :
``` 
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:50:52 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
``` 
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-781440c1f2342a4e952709311d04c356-14ad6b9edfc3c446-00",
    "errors": {
        "id": [
            "The value '45648324864034' is not valid."
        ]
    }
}
```
## PUT ​/api​/v1​/Activities​/{id}  (отрицательный ID)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Author_minus_id}}

- Ожидаемый результат: код ответа 405, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: c03fbb52-e2bd-45c7-a8c0-f85fc6145851
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-06T10:52:24.973Z",
  "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 12:52:35 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа: 
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-06T10:52:24.973Z",
    "completed": true
}
```
## GET ​/api​/v1​/CoverPhotos​/books​/covers​/{idBook}

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{coverphoto_id}}

- Ожидаемый результат: код ответа 200, тест пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: e6c487cc-233c-4437-8869-8cc66c2dac54
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:03:52 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа: 
```
[
    {
        "id": 4,
        "idBook": 4,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 4&w=250&h=350"
    }
]
```
## GET ​/api​/v1​/CoverPhotos​/books​/covers​/{idBook} (большое число)

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{coverphotobad_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: e15181e6-364f-4c9a-b217-21171b03becb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:07:29 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа: 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-6a95faa24e2270498c453c18fbbb50d7-b9c5de1e82a04642-00",
    "errors": {
        "idBook": [
            "The value '12345678909876' is not valid."
        ]
    }
}
```
## POST ​/api​/v1​/CoverPhotos

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

- Ожидаемый результат: код ответа 201, тест пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: ef13acfd-ed3b-4b44-9c69-0df8275b6b98
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
  "id": {{coverphoto_id}},
  "idBook": 0,
  "url": "string"
}
```
- Заголовки ответа :
``` 
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:09:09 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа: 
```
{
    "id": 4,
    "idBook": 0,
    "url": "string"
}
```
## POST ​/api​/v1​/CoverPhotos негативный (буквы)

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: c1afa827-9122-4e66-892b-00418dcc8202
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса :
``` 
{
 "id": null,
 "title": "string",
 "dueDate": "2023-06-03T08:12:24.110Z",
 "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:11:29 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-87302b82664eec42b5e6f2d6826da8d4-7d76aaf656431245-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 11."
        ]
    }
}
```
## POST ​/api​/v1​/CoverPhotos негативный (пустой)

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

- Ожидаемый результат: код ответа 415, тест провален

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: e9d9be90-45d3-40fe-b651-7bb2239b935a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:12:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-543702a75f681341bdfc83e12010c1ed-3db2025131252145-00"
}
```
## POST ​/api​/v1​/CoverPhotos негативный (некорректный JSON)

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 058ba45c-18df-4e48-bada-f9013e18d967
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса :
``` 
{
  "id" 0,
  "idBook": 0,
  "url": "string"
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:17:10 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-dada4e32e56adf47a7b01637470bba0e-e1e46aafb95f4243-00",
    "errors": {
        "$": [
            "'0' is invalid after a property name. Expected a ':'. Path: $ | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```
## GET ​/api​/v1​/CoverPhotos

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

- Ожидаемый результат: код ответа 200, тест пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 68bb6568-d658-43b1-9596-91a79d95e24f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:32:26 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
[
    {
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
    },
    {
        "id": 2,
        "idBook": 2,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
    },]
```
## PUT ​/api​/v1​/Users​/{id}

- URL https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id}}

- Ожидаемый результат: код ответа 200, тест пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 5f0f482e-8663-47aa-bf35-700e90cf85b8
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id": 0,
 "userName": "string",
 "password": "string"
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:36:12 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": 0,
    "userName": "string",
    "password": "string"
}
```
## PUT ​/api​/v1​/Users​/{id} (некорректный ID)

- URL https://fakerestapi.azurewebsites.net/api/v1/Users/{{Usersbad_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9126d2bd-becd-4e8e-8c06-184001869e77
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:45:00 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-a1ca159c59cbc648b94c1e70b9813b5b-e7244f50e2eaba44-00",
    "errors": {
        "id": [
            "The value '45648324864034' is not valid."
        ]
    }
}
```
## PUT ​/api​/v1​/Users​/{id} (некорректный JSON)

- URL https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 6c2eaa23-8ca8-48ae-86d0-fdca5c9e71f0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id": 0,
 "userName": ,
 "password": 
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:52:44 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ef00eacfebb3c94098e770075bbab7ef-a189e31a27361b4e-00",
    "errors": {
        "$.userName": [
            "',' is an invalid start of a value. Path: $.userName | LineNumber: 4 | BytePositionInLine: 13."
        ]
    }
}
```
## PUT ​/api​/v1​/Users​/{id} (пустые строки)

- URL https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 4ee307a9-9e7e-4ff9-99d3-bfc13ae1085b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{

 "id": 0,

 "userName": "string",

}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:56:21 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b5bb8b4298f1b74ca5e76c772247a1f4-c6bf84dd05039044-00",
    "errors": {
        "$": [
            "The JSON object contains a trailing comma at the end which is not supported in this mode. Change the reader options. Path: $ | LineNumber: 6 | BytePositionInLine: 0."
        ]
    }
}
```
## PUT ​/api​/v1​/Users​/{id}  (отрицательный ID)

- URL https://fakerestapi.azurewebsites.net/api/v1/Users/{{Author_minus_id}}

- Ожидаемый результат: код ответа 405, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: fad415a3-1052-4e99-823a-d5989a98c28d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 14:06:17 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": 0,
    "userName": "string",
    "password": "string"
}
```
## Users: (GET)получение списка пользователей

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users
- `Ожидаемый результат` Получение статус-кода 200. Тело ответа содержит список всех пользователей.
- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: fcb57d3f-c226-47e2-9bf0-08d53b43c0ba
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 15:34:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
[
{"id":1,"userName":"Пользователь 1","пароль":"Пароль1"},
{"id":2,"userName":"Пользователь 2","пароль":"Пароль2"} ,
{"id":3,"userName":"Пользователь 3","пароль":"Пароль3"},
{"id":4,"userName":"Пользователь 4","пароль":"Пароль4"} ,
{"id":5,"userName":"Пользователь 5","пароль":"Пароль5"},
{"id":6,"userName":"Пользователь 6","пароль":"Пароль6"} ,
{"id":7,"userName":"Пользователь 7","пароль":"Пароль7"},
{"id":8,"userName":"Пользователь 8","пароль":"Пароль8"} ,
{"id":9,"userName":"Пользователь 9","пароль":"Пароль9"},
{"id":10,"userName":"Пользователь 10","пароль":"Пароль10"}
]
```

## Users: (POST)добавление нового пользователя

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users
- `Ожидаемый результат` Получение статус-кода 201. Добавлен новый пользователь.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 478bc54f-e33c-484c-a995-5530cdf18602
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id":{{Author_for_put_id}},
  "userName": "User 1000",
  "password": "Password 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 15:42:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
"id":1000,
"userName":"User 1000",
"password":"Password 1000"
}
```

## Users: (POST)добавление нового пользователя (некорректный id=отрицательное значение)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users
- `Ожидаемый результат` Получение статус-кода 400. Неверный запрос. Индификатор не может быть отрицательным.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 4836b2c5-e327-4f29-91f7-ad409d61d997
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id": {{Author_minus_id}},
  "userName": "User 1000",
  "password": "Password 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 15:58:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
"id":-1,
"userName":"User 1000",
"password":"Password 1000"
}
```

##  Users: (POST)добавление нового пользователя (некорректный id=0)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users
- `Ожидаемый результат`  Получение статус-кода 400. Неверный запрос. Индификатор не может быть равен 0.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 478bc54f-e33c-484c-a995-5530cdf18602
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id": {{Author_null_id}},
  "userName": "User 1000",
  "password": "Password 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 16:04:10 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
"id":0,
"userName":"User 1000",
"password":"Password 1000"
}
```

##  Users: (POST)добавление нового пользователя (некорректный id=символы)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users
- `Ожидаемый результат`  Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 926fb3cd-8322-4893-9bbe-78a3bd08a428
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id": %%%,
  "userName": "User 1000",
  "password": "Password 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 16:12:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400 
"traceId":"00-45efa8baf9a6e241b101cb9088348ee0-83eef07491038441-00",
"errors":{"$.id":["'%' is an invalid start of a value. 
Path: $.id | LineNumber: 2 | BytePositionInLine: 8."]}
}
```
## Users: (POST)добавление нового пользователя (некорректный id=буквы)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users
- `Ожидаемый результат` Получение статус-кода 400. Неверный запрос.

- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: bf547b71-81d2-4e45-b462-c69dc3eb3388
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id": rty,
  "userName": "User 1000",
  "password": "Password 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 16:16:44 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-3217158ad075234389cbddc86c78572f-d1b442aee4dfb646-00",
"errors":{"$.id":["'r' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 8."]}
}
```
## Users: (POST)добавление нового пользователя (некорректный id=пустое значение)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users
- `Ожидаемый результат`  
Получение статус-кода 400. Неверный запрос.

- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: dc9c2dc3-ee40-4449-8fb0-3e122f3c2ce0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id":,
  "userName": "User 1000",
  "password": "Password 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 16:19:42 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-0a381b5ed644ee49ac4df26bf087b032-87f15045bea1d24f-00",
"errors":{"$.id":["',' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."]}
}
```

## Users: (POST)добавление нового пользователя (  некорректный JSON)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.

- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 7d19e10a-c0c4-4c63-b415-b3d3fef8c78b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id": 1000,
  "userName": "User 1000",
  "password": "Password 1000"
  ```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 16:21:56 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
"title":"One or more validation errors occurred.",
"status":400,
"traceId":"00-6bb9b9b4b284b14db1701ecda4dfd954-5ea12d374732754b-00",
"errors":{"$":["Expected depth to be zero at the end of the JSON payload. There is an open JSON object or array that should be closed. 
Path: $ | LineNumber: 5 | BytePositionInLine: 0."]}
}
```

##  Users: (POST) добавление нового пользователя (не заполнено тело запроса)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.

- `Заголовки запроса`
``` 
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 395887c3-6cce-426e-84bb-7a9aab6a01ae
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 16:24:26 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
"type":"https://tools.ietf.org/html/rfc7231#section-6.5.13",
"title":"Unsupported Media Type",
"status":415,
"traceId":"00-e0a5bc51f92a76449c4e962378ed595f-6e9eafcc0ca92144-00"
}
```
## Users: (POST)добавление нового пользователя(не заполнены данные имя и пароль пользователя)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.

- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9c18210b-3bf3-44b2-abae-f74d1ef6f1fd
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id": {{Author_for_put_id}},
  "userName": "",
  "password": ""
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 16:27:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
"id":1000,
"userName":"",
"password":""
}
```

## Users: (POST)добавление нового пользователя ( указаны некорректные данные имя и фамилия пользователя:цифры)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.

- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 6476fca5-a942-45dc-8f1b-c05d63954ebb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id": {{Author_for_put_id}},
  "userName": "1000",
  "password": "1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 16:30:46 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":1000,
    "userName":"1000",
    "password":"1000"
}
```
## Users: (POST)добавление нового пользователя ( указаны некорректные данные имя и фамилия пользователя: символы)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.

- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: ae67f442-bdeb-4e37-9df6-edd29d713b6a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id": {{Author_for_put_id}},
  "userName": "№№№№№№№№",
  "password": "№№№№№№№№"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 16:32:54 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":1000,
    "userName":"№№№№№№№№",
    "password":"№№№№№№№№"
}
```

## Users: (GET c ID )получение данных о конкретном пользователе

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id}}
- `Ожидаемый результат` 
Получен статус-кода 200

- `Заголовки запроса` 
```
Request Headers
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 63a283a6-32d3-40c8-8ade-d099bf1fa0d3
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 16:35:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":6,
    "userName":"User 6",
    "password":"Password6"
}
```
## Users: (GET c ID )получение данных о конкретном пользователе (отсутствие id пользователя в базе данных) 

- `URL`  https://fakerestapi.azurewebsites.net/api/v1/Users/{{Usersbad_id}}
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.

- `Заголовки запроса`
``` 
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 82ebebfa-8052-4f1f-990d-ace35258c611
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 16:38:26 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа`
``` 
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title":"One or more validation errors occurred.",
    "status":400,
    "traceId":"00-5d54e712a2fe98438416edd9e7ddd795-8b39cb8576917540-00",
    "errors":{"id":["The value '45648324864034' is not valid."]}
}
```
## Users: (GET c ID )получение данных о конкретном пользователе (некорректный id=отрицательное значение) 

- `URL`  https://fakerestapi.azurewebsites.net/api/v1/Users/{{Author_minus_id}}
- `Ожидаемый результат` Получение статус-кода 404. Запрашиваемый ресурс не найден на сервере

- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: dfe7cc53-99b9-40bd-b5b1-babca3b0920b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 16:45:08 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title":"Not Found",
    "status":404,
    "traceId":"00-7b85cad04341c04590b86d30b53076db-b07d1e6939cfb647-00"
}
```

## Users: (GET c ID )получение данных о конкретном пользователе (некорректный id=0) 

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Users/{{Author_null_id}}
- `Ожидаемый результат` 
Получение статус-кода 404. Запрашиваемый ресурс не найден на сервере
- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: ed848af7-72a1-4f5f-9a36-f70a3bde9777
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 16:47:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title":"Not Found",
    "status":404,
    "traceId":"00-55497c65a8e9664fa49587963ac2a196-abd32e45e777614e-00"
}
```
## Authors: (GET)получение списка авторов

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors
- `Ожидаемый результат` Получен статус-кода 200

- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 98d7edf0-7c3d-4b69-82cd-2f78a44bba31
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 16:55:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{"id":1,
"idBook":1,
"firstName":"First Name 1",
"lastName":"Last Name 1"},
{"id":2,
"idBook":1,
"firstName":"First Name 2",
"lastName":"Last Name 2"},
{"id":3,
"idBook":1,
"firstName":..."Last Name 564"},
{"id":565,
"idBook":192,
"firstName":"Last Name 593"},
{"id":594,
"idBook":200,
"firstName":"First Name 594",
"lastName":"Last Name 594"}
```


## Authors: (POST)добавление нового автора

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors
- `Ожидаемый результат` Получение статус-кода 201. 
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 96dfac94-05f7-4f8f-a981-7701ce5e59c2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
 "id": {{Author_for_put_id}},
 "idBook": {{Author_for_put_id}},
 "firstName": "First Name 1000",
 "lastName": "Last Name 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 16:59:44 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
"id":1000,
"idBook":1000,
"firstName":"First Name 1000",
"lastName":"Last Name 1000"
}
```

## Authors: (POST)добавление нового автора (некорректный id=0)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.

- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: b3d2d5b4-c095-475a-8f0d-4a5dfa3ead99
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
 "id": 0,
 "idBook": 0,
 "firstName": "First Name 1000",
 "lastName": "Last Name 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 17:03:32 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":0,
    "idBook":0,
    "firstName":"First Name 1000",
    "lastName":"Last Name 1000"
}
```

## Authors: (POST)добавление нового автора (некорректный id=отрицательное значение)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: c4851f77-3430-4697-a2a8-e83325c1fe52
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
 "id": -5,
 "idBook": -5,
 "firstName": "First Name 1000",
 "lastName": "Last Name 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 17:11:33 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":-5,
    "idBook":-5,
    "firstName":"First Name 1000",
    "lastName":"Last Name 1000"
}
```
## Authors: (POST)добавление нового автора (некорректный id=символ)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса`
``` 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 148cd493-8eed-4ac6-80e1-e14f4ae90457
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
 "id": %%%,
 "idBook":%%%,
 "firstName": "First Name 1000",
 "lastName": "Last Name 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 17:12:48 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title":"One or more validation errors occurred.",
    "status":400,
    "traceId":"00-219fc3eda3d72147886356f1b5e73614-e9a3a568d2deac4a-00",
    "errors":{"$.id":["'%' is an invalid start of a value. 
    Path: $.id | LineNumber: 1 | BytePositionInLine: 7."]}
}
```
## Authors: (POST)добавление нового автора (некорректный id=пустое значение)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 069da082-c019-4589-927a-a04ba08e2155
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
 "id":,
 "idBook":,
 "firstName": "First Name 1000",
 "lastName": "Last Name 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 17:14:06 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title":"One or more validation errors occurred.",
    "status":400,
    "traceId":"00-b7b66acd48dc5242aa5db4dc8adca83b-678c4a6607ba974d-00",
    "errors":{"$.id":["',' is an invalid start of a value. 
    Path: $.id | LineNumber: 1 | BytePositionInLine: 6."]}
}
```

## Authors: (POST)добавление нового автора (некорректный id=буква)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 58a2b7f8-78f1-4508-978f-a0435e382bd5
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
 "id": yy,
 "idBook":fdd,
 "firstName": "First Name 1000",
 "lastName": "Last Name 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 17:15:28 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title":"One or more validation errors occurred.",
    "status":400,
    "traceId":"00-9b19e6d74abfae479c91257ccd3ad364-a4e7017544b2214c-00",
    "errors":{"$.id":["'y' is an invalid start of a value. 
    Path: $.id | LineNumber: 1 | BytePositionInLine: 7."]}
}
```


## Authors: (POST)добавление нового автора ( указаны некорректные данные имя и фамилия автора: цифры)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 0a6472b7-5ff9-4098-85c4-14d1f51e473c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
"id": {{Author_for_put_id}},
"idBook": {{Author_for_put_id}},
"firstName": "9999",
"lastName": "9999"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 17:36:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":1000,
    "idBook":1000,
    "firstName":"9999",
    "lastName":"9999"
}
```
## Authors: (POST)добавление нового автора ( указаны некорректные данные имя и фамилия автора: символы)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 72f75986-f3fd-4bf5-9ff5-8bc7281624c9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
 "id": {{Author_for_put_id}},
 "idBook": {{Author_for_put_id}},
 "firstName": "№№№№№№№№",
 "lastName": "№№№№№№№№"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 17:38:10 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":1000,
    "idBook":1000,
    "firstName":"№№№№№№№№","
    lastName":"№№№№№№№№"
}
```

## Authors: (POST)добавление нового автора (  некорректный JSON)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: e2edb8bf-0748-4819-bda4-abef5268dd97
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
 "id": {{Author_for_put_id}},
 "idBook": {{Author_for_put_id}},
 "firstName": "First Name 1000",
 "lastName": "Last Name 1000"
 ```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 17:40:36 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title":"One or more validation errors occurred.",
    "status":400,
    "traceId":"00-c1355b4fe8dfe24d9b28f85970edfd68-f70adeda958ac34f-00",
    "errors":{"$":["Expected depth to be zero at the end of the JSON payload. There is an open JSON object or array that should be closed. 
    Path: $ | LineNumber: 4 | BytePositionInLine: 29."]}
}
```
## Authors: (POST) добавление нового автора (не заполнено тело запроса)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 72642c13-ac8e-493c-8265-a4fd500dac1e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 17:41:37 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title":"Unsupported Media Type",
    "status":415,
    "traceId":"00-f15019aaeacf53489efe86f2bd664492-0b523ab632d0df44-00"
}
```
## Authors: (POST)добавление нового автора (не заполнены данные имя и фамилия автора)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 4f5a0044-2f95-4745-b233-0dc1a59b0361
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id":{{Author_for_put_id}},
  "idBook":{{Author_for_put_id}},
  "firstName":"",
  "lastName":""
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 17:43:12 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":1000,
    "idBook":1000,
    "firstName":"",
    "lastName":""
}
```
## Authors: (GET c ID )получение данных об авторах конкретной книги

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{Authors_id}}
- `Ожидаемый результат` Получен статус-кода 200

- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9082bbeb-4db7-4fed-b1cd-0fb830cdda34
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 17:54:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
[{
    "id":1,
    "idBook":1,
    "firstName":"First Name 1",
    "lastName":"Last Name 1"},
    {"id":2,
    "idBook":1,
    "firstName":"First Name 2",
    "lastName":"Last Name 2"},
    {"id":3,
    "idBook":1,
    "firstName":"First Name 3",
    "lastName":"Last Name 3"},
    {"id":4,
    "idBook":1,
    "firstName":"First Name 4",
    "lastName":"Last Name 4"
}]
```
## Authors: (GET c ID )получение данных о конкретном авторе

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_id}}
- `Ожидаемый результат`Получен статус-кода 200 

- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 1e348c8d-f42c-485c-9f3d-b4108ad313e4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 17:56:35 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":1,
    "idBook":1,
    "firstName":"First Name 1",
    "lastName":"Last Name 1"
}
```

## Authors: (GET c ID )получение данных об авторах конкретной книги (отсутствие id книги в базе данных)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{Authors_bad_id}}
- `Ожидаемый результат` Получение статус-кода 400. Неверный запрос.

- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: f845abe0-20c7-43cf-8995-a7af4581df19
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 17:57:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title":"One or more validation errors occurred.",
    "status":400,
    "traceId":"00-e0101e0be510874e9bd9330b8a6eebbd-9a534cccf4b52b4d-00",
    "errors":{"idBook":["The value '10000000000' is not valid."]}
}
```

## Authors: (GET c ID ) получение данных о конкретном авторе (отсутствие id автора в базе данных)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_bad_id}}
- `Ожидаемый результат` Получение статус-кода 400. Неверный запрос.

- `Заголовки запроса`
``` 
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: ccf348f3-2dce-4fca-a59c-c07a75e507f1
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 17:59:25 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title":"One or more validation errors occurred.",
    "status":400,
    "traceId":"00-4dcde00b9a473e4dbfa95fe21f6a4409-a7e1e2a8b46ac04a-00",
    "errors":{"id":["The value '10000000000' is not valid."]}
}
```


## Authors: (GET c ID )получение данных об авторах конкретной книги (некорректный id=0)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{Author_null_id}}
- `Ожидаемый результат` Получение статус-кода 400. Неверный запрос.

- `Заголовки запроса` 
```
 User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 52663e02-886c-48bb-b88b-45538c70da22
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 18:01:03 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
[]
```
## Authors: (GET c ID ) получение данных о конкретном авторе (некорректный id=0)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Author_null_id}}
- `Ожидаемый результат` Получение статус-кода 404. Запрашиваемый ресурс не найден на сервере

- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 0bc52f17-79f7-44ad-b2bf-e7fb278cfbfc
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 18:02:20 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title":"Not Found",
    "status":404,
    "traceId":"00-ad6dd99caf84ff45a241ed4bcb729cfd-570ff57e1e58524a-00"
}
```


## Authors: (GET c ID )получение данных об авторах конкретной книги (некорректный id=отрицательное значение)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{Author_minus_id}}
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.

- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 7b2fbc1c-bce3-4044-892c-a01ab6ed3217
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 18:05:20 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
[]
```

## Authors: (GET c ID ) получение данных о конкретном авторе (некорректный id=отрицательное значение)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Author_minus_id}}
- `Ожидаемый результат` 
Получение статус-кода 404. Запрашиваемый ресурс не найден на сервере

- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 187e3da9-345a-451e-ac48-89fc4d5239be
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 18:14:49 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title":"Not Found",
    "status":404,
    "traceId":"00-fb76e8134dba7a4fa5afcfe3ecef60e7-c6ef9152622a6343-00"
}
```

## Authors: (PUT)замена данных по  конкретному автору

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_id}}
- `Ожидаемый результат` 
Получен статус-кода 200
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 15440a9f-0155-461e-a40c-e11841faa64e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id":{{Authors_id}},
  "idBook":{{Authors_id}},
  "firstName": "First Name 1000",
  "lastName": "Last Name 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 18:45:59 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":1,
    "idBook":1,
    "firstName":"First Name 1000",
    "lastName":"Last Name 1000"
}
```


## Authors: (PUT)замена данных по  конкретному автору (некорректный id=0)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Author_null_id}}
- `Ожидаемый результат` 

- `Заголовки запроса`
``` 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 47e8ff2f-a85e-4483-9d2a-a28ece805c40
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id":{{Author_null_id}},
  "idBook":{{Author_null_id}},
  "firstName": "First Name 1000",
  "lastName": "Last Name 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 18:47:38 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":0,
    "idBook":0,
    "firstName":"First Name 1000",
    "lastName":"Last Name 1000"
}
```
## Authors: (PUT)замена данных по  конкретному автору (некорректный id=отрицательное значение)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Author_minus_id}}
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 3e686c4e-67d9-4376-a2a2-dd6bfab32932
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id":{{Author_minus_id}},
  "idBook":{{Author_minus_id}},
  "firstName": "First Name 1000",
  "lastName": "Last Name 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 18:51:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":-1,
    "idBook":-1,
    "firstName":"First Name 1000",
    "lastName":"Last Name 1000"
}
```

## Authors: (PUT)замена данных по  конкретному автору(отсутствие id автора в базе данных)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_bad_id}}
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 77a9177a-53d9-4069-80b5-5b74c4fbf321
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id":{{Authors_bad_id}},
  "idBook":{{Authors_bad_id}}
  "firstName": "First Name 1000",
  "lastName": "Last Name 1000"
}
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 18:53:17 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title":"One or more validation errors occurred.",
    "status":400,
    "traceId":"00-a9278af22013be419d6c8c6459f1202c-b8fd9aea4973bb4e-00",
    "errors":{"id":["The value '10000000000' is not valid."],
    "$.id":["The JSON value could not be converted to System.Int32. 
    Path: $.id | LineNumber: 1 | BytePositionInLine: 18."]}
}
```
## Authors: (PUT)замена данных по  конкретному автору (  некорректный JSON)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_id}}
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 28b18dbe-8ce0-4dda-8b6a-5a3fb775b89e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
  "id":{{Authors_id}},
  "idBook":{{Authors_id}}
  "firstName": "First Name 1000",
  "lastName": "Last Name 1000"
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 18:54:25 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title":"One or more validation errors occurred.",
    "status":400,
    "traceId":"00-d405888a95ba9a469ced6a422b757759-d305e9bac905ba4b-00",
    "errors":{"$":["'\"' is invalid after a value. Expected either ',', '}', or ']'. Path: $ | LineNumber: 3 | BytePositionInLine: 2."]}
}
```


## Authors: (PUT)замена данных по  конкретному автору (не заполнено тело запроса)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_id}}
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9583e303-463f-4d49-bf32-2388d35dccc3
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 18:55:32 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- `Тело ответа` 
```
{
    "type":"https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title":"Unsupported Media Type",
    "status":415,
    "traceId":"00-feb6d477b75de64e9906464b1c493b74-7dea6dabf13a414d-00"
}
```
## Authors: (PUT)замена данных по  конкретному автору (не заполнены данные имя и фамилия автора)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_id}}
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 83d72fd0-cf5b-4519-bb3c-e127ed07cd96
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
   "id": {{Authors_id}},
  "idBook": {{Authors_id}},
  "firstName": "",
   "lastName": ""
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 18:58:45 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
"id":1,
"idBook":1,
"firstName":"",
"lastName":""
}
```

## Authors: (PUT)замена данных по  конкретному автору ( указаны некорректные данные имя и фамилия автора: символы)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_id}}
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: da53a4bf-23d5-428d-bc9a-80a12e9c7f34
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
   "id": {{Authors_id}},
  "idBook": {{Authors_id}},
  "firstName": "№№№№№№№№",
   "lastName": "№№№№№№№№"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 18:59:40 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":1,"idBook":1,
    "firstName":"№№№№№№№№",
    "lastName":"№№№№№№№№"
}
```
## Authors: (PUT)замена данных по  конкретному автору ( указаны некорректные данные имя и фамилия автора: цифры)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_id}}
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: c996f21c-ba5a-4de1-a823-417dcec83106
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Тело запроса` 
```
{
   "id": {{Authors_id}},
  "idBook": {{Authors_id}},
  "firstName": "99999",
   "lastName": "99999"
}
```
- `Заголовки ответа`
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 19:00:37 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- `Тело ответа` 
```
{
    "id":1,
    "idBook":1,
    "firstName":"99999",
    "lastName":"99999"
}
```
## Authors: (DELETE )удаление данных о конкретном авторе

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_id}}
- `Ожидаемый результат` 
Получен статус-кода 200
- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 7ecb3ba7-16ef-4842-b45f-2c3c9f57c550
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Length: 0
Date: Tue, 06 Jun 2023 19:05:01 GMT
Server: Kestrel
api-supported-versions: 1.0
```
## Authors: (DELETE )удаление данных о конкретном авторе   (некорректный id=0)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Author_null_id}}
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 544c5441-1479-4943-b0dd-859158508d50
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Length: 0
Date: Tue, 06 Jun 2023 19:09:07 GMT
Server: Kestrel
api-supported-versions: 1.0
 ```

## Authors: (DELETE )удаление данных о конкретном авторе   (некорректный id=отрицательное число)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Author_minus_id}}
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 54ef54b2-6c0c-4747-b2d2-d811d9dcabc9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Length: 0
Date: Tue, 06 Jun 2023 19:09:41 GMT
Server: Kestrel
api-supported-versions: 1.0
```

## Authors: (DELETE )удаление данных о конкретном авторе   (отсутствие id автора в базе данных)

- `URL` https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_bad_id}}
- `Ожидаемый результат` 
Получение статус-кода 400. Неверный запрос.
- `Заголовки запроса` 
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: ed1922f6-ab38-4a28-8e0b-0e8d5f590a6e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- `Заголовки ответа`
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 19:10:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
## GET ​/api​/v1​/Activities

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities

- Ожидаемый результат: код ответа 200, тест успешно пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 993ebbca-1dde-4ffc-8414-22ff497d66bf
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 09:35:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
    {
        "id": 1,
        "title": "Activity 1",
        "dueDate": "2023-06-06T10:47:35.1571188+00:00",
        "completed": false
    },
    {
        "id": 2,
        "title": "Activity 2",
        "dueDate": "2023-06-06T11:47:35.1571212+00:00",
        "completed": true
    },
    {
        "id": 3,
        "title": "Activity 3",
        "dueDate": "2023-06-06T12:47:35.1571215+00:00",
        "completed": false
    },]
```
## POST ​/api​/v1​/Activities

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities

- Ожидаемый результат: код ответа 201, тест успешно пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: e4805522-054f-42f1-9b49-e7fbef3c83eb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id": {{activity_id}},
 "title": "string",
 "dueDate": "2023-06-03T08:12:24.110Z",
 "completed": true
}
```

- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 11:24:18 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
{
    "id": 5,
    "title": "string",
    "dueDate": "2023-06-03T08:12:24.11Z",
    "completed": true
}
```
## POST ​/api​/v1​/Activities негативный (буквы)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Accept: text/plain
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Cache-Control: no-cache
Postman-Token: d390e364-2cda-439c-b10e-f36295e394e1
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id": null,
 "title": "string",
 "dueDate": "2023-06-03T08:12:24.110Z",
 "completed": true
}
```

- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:02:36 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-47a6dac543576b4f9caf884f6bac9097-10d859e6be4cf148-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 11."
        ]
    }
}
```
## POST ​/api​/v1​/Activities негативный (пустой)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities

- Ожидаемый результат : код ответа 415, тест провален

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: c5fa4702-945d-48d4-964d-b1f0dfe0c184
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса :
```
 отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:06:02 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-2237da0d949529488d6e116558dbb832-18a64685b36a4043-00"
}
```
## GET ​/api​/v1​/Activities​/{id}

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

- Ожидаемый результат: код ответа 200, тест пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: fc762366-f216-412b-9f8a-aa5d1d2bbe33
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа :
``` 
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 12:11:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
{
    "id": 5,
    "title": "Activity 5",
    "dueDate": "2023-06-06T17:11:54.3421821+00:00",
    "completed": false
}
```
## POST ​/api​/v1​/Activities негативный (некорректный JSON)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 162bd20d-5c8c-43e8-892b-0b5a9bdff010
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id" 0,
 "title": "string",
 "dueDate": "2023-06-03T11:15:00.428Z",
 "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:14:52 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-6e87392994c9404a911da17cd3ce6720-02cfa81bcffffd47-00",
    "errors": {
        "$": [
            "'0' is invalid after a property name. Expected a ':'. Path: $ | LineNumber: 2 | BytePositionInLine: 6."
        ]
    }
}
```
## GET ​/api​/v1​/Activities​/{id} (некорректный ID)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activitybad_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 59f61d33-34bd-43d5-b04c-d93c07515376
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:17:14 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-90fb8139c5be5042bc54a368aa4d4ffb-68a116cf13326548-00",
    "errors": {
        "id": [
            "The value '45648324864034' is not valid."
        ]
    }
}
```
## PUT ​/api​/v1​/Activities​/{id}

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

- Ожидаемый результат: код ответа 200, тест пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9ad266a3-685c-46d9-a04f-57eddf337d70
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-05T17:24:24.293Z",
    "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 12:26:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа 
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-05T17:24:24.293Z",
    "completed": true
}
```
## PUT ​/api​/v1​/Activities​/{id} (некорректный ID)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activitybad_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9912c670-689f-4fa8-acf2-7f720c472526
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса :
``` 
{
 "id": 0,
 "title": "string",
 "dueDate": "2023-06-03T11:30:34.198Z",
 "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:29:25 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-05T17:24:24.293Z",
    "completed": true
}
```
## POST ​/api​/v1​/Activities негативный (некорректный JSON)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: a77831ef-df3a-4495-acf3-d0c847a197d3
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id" 0,
 "title": "string",
 "dueDate": "2023-06-03T11:15:00.428Z",
 "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:32:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b4057a6ca8241c4bacf4e006a1d65cf6-0b6c2f3b84435d4a-00",
    "errors": {
        "$": [
            "'0' is invalid after a property name. Expected a ':'. Path: $ | LineNumber: 2 | BytePositionInLine: 6."
        ]
    }
}
```
## PUT ​/api​/v1​/Activities​/{id} (пустые строки)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 54f34c52-de84-4a85-a6f8-5783fac48fbd
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса :
``` 
{
 "id": 0,
 "title": "string",
 "dueDate": "2023-06-03T15:39:25.038Z",
 
}
```
- Заголовки ответа :
``` 
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:34:19 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-4b366e6fec403d4db990d5e82de3f602-664863e5941eec4c-00",
    "errors": {
        "$": [
            "The JSON object contains a trailing comma at the end which is not supported in this mode. Change the reader options. Path: $ | LineNumber: 10 | BytePositionInLine: 0."
        ]
    }
}
```
## DELETE ​/api​/v1​/Activities​/{id}

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

- Ожидаемый результат: код ответа 200, тест пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: f6b187d8-d0e4-4d94-b316-38cbd68f1ec9
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутствует
```
- Заголовки ответа : 
```
Content-Length: 0
Date: Tue, 06 Jun 2023 12:41:47 GMT
Server: Kestrel
api-supported-versions: 1.0
```
- Тело ответа: 
```
отсутствует
```
## DELETE ​/api​/v1​/Activities​/{id} (некорректный id)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activitybad_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 5fbaf016-fe93-4481-97a5-d17e7fe6d4fa
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
Отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 12:50:52 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа: 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-781440c1f2342a4e952709311d04c356-14ad6b9edfc3c446-00",
    "errors": {
        "id": [
            "The value '45648324864034' is not valid."
        ]
    }
}
```
## PUT ​/api​/v1​/Activities​/{id}  (отрицательный ID)

- URL https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Author_minus_id}}

- Ожидаемый результат: код ответа 405, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: c03fbb52-e2bd-45c7-a8c0-f85fc6145851
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-06T10:52:24.973Z",
  "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 12:52:35 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа: 
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-06T10:52:24.973Z",
    "completed": true
}
```
## GET ​/api​/v1​/CoverPhotos​/books​/covers​/{idBook}

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{coverphoto_id}}

- Ожидаемый результат: код ответа 200, тест пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: e6c487cc-233c-4437-8869-8cc66c2dac54
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа :
``` 
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:03:52 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа: 
```
[
    {
        "id": 4,
        "idBook": 4,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 4&w=250&h=350"
    }
]
```
## GET ​/api​/v1​/CoverPhotos​/books​/covers​/{idBook} (большое число)

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{coverphotobad_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: e15181e6-364f-4c9a-b217-21171b03becb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:07:29 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа: 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-6a95faa24e2270498c453c18fbbb50d7-b9c5de1e82a04642-00",
    "errors": {
        "idBook": [
            "The value '12345678909876' is not valid."
        ]
    }
}
```
## POST ​/api​/v1​/CoverPhotos

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

- Ожидаемый результат: код ответа 201, тест пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: ef13acfd-ed3b-4b44-9c69-0df8275b6b98
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
  "id": {{coverphoto_id}},
  "idBook": 0,
  "url": "string"
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:09:09 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа: 
```
{
    "id": 4,
    "idBook": 0,
    "url": "string"
}
```
## POST ​/api​/v1​/CoverPhotos негативный (буквы)

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: c1afa827-9122-4e66-892b-00418dcc8202
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id": null,
 "title": "string",
 "dueDate": "2023-06-03T08:12:24.110Z",
 "completed": true
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:11:29 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-87302b82664eec42b5e6f2d6826da8d4-7d76aaf656431245-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 2 | BytePositionInLine: 11."
        ]
    }
}
```
## POST ​/api​/v1​/CoverPhotos негативный (пустой)

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

- Ожидаемый результат: код ответа 415, тест провален

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: e9d9be90-45d3-40fe-b651-7bb2239b935a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:12:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-543702a75f681341bdfc83e12010c1ed-3db2025131252145-00"
}
```
## POST ​/api​/v1​/CoverPhotos негативный (некорректный JSON)

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 058ba45c-18df-4e48-bada-f9013e18d967
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
  "id" 0,
  "idBook": 0,
  "url": "string"
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:17:10 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-dada4e32e56adf47a7b01637470bba0e-e1e46aafb95f4243-00",
    "errors": {
        "$": [
            "'0' is invalid after a property name. Expected a ':'. Path: $ | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
```
## GET ​/api​/v1​/CoverPhotos

- URL https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

- Ожидаемый результат: код ответа 200, тест пройден

- Заголовки запроса :
```
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 68bb6568-d658-43b1-9596-91a79d95e24f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
отсутствует
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:32:26 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
[
    {
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
    },
    {
        "id": 2,
        "idBook": 2,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
    },]
```	
## PUT ​/api​/v1​/Users​/{id}

- URL https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id}}

- Ожидаемый результат: код ответа 200, тест пройден

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 5f0f482e-8663-47aa-bf35-700e90cf85b8
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id": 0,
 "userName": "string",
 "password": "string"
}
```
- Заголовки ответа : 
```
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 13:36:12 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": 0,
    "userName": "string",
    "password": "string"
}
```
## PUT ​/api​/v1​/Users​/{id} (некорректный ID)

- URL https://fakerestapi.azurewebsites.net/api/v1/Users/{{Usersbad_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 9126d2bd-becd-4e8e-8c06-184001869e77
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:45:00 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-a1ca159c59cbc648b94c1e70b9813b5b-e7244f50e2eaba44-00",
    "errors": {
        "id": [
            "The value '45648324864034' is not valid."
        ]
    }
}
```
## PUT ​/api​/v1​/Users​/{id} (некорректный JSON)

- URL https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 6c2eaa23-8ca8-48ae-86d0-fdca5c9e71f0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
 "id": 0,
 "userName": ,
 "password": 
}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:52:44 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-ef00eacfebb3c94098e770075bbab7ef-a189e31a27361b4e-00",
    "errors": {
        "$.userName": [
            "',' is an invalid start of a value. Path: $.userName | LineNumber: 4 | BytePositionInLine: 13."
        ]
    }
}
```
## PUT ​/api​/v1​/Users​/{id} (пустые строки)

- URL https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id}}

- Ожидаемый результат: код ответа 400, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: 4ee307a9-9e7e-4ff9-99d3-bfc13ae1085b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{

 "id": 0,

 "userName": "string",

}
```
- Заголовки ответа : 
```
Content-Type: application/problem+json; charset=utf-8
Date: Tue, 06 Jun 2023 13:56:21 GMT
Server: Kestrel
Transfer-Encoding: chunked
```
- Тело ответа:
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b5bb8b4298f1b74ca5e76c772247a1f4-c6bf84dd05039044-00",
    "errors": {
        "$": [
            "The JSON object contains a trailing comma at the end which is not supported in this mode. Change the reader options. Path: $ | LineNumber: 6 | BytePositionInLine: 0."
        ]
    }
}
```
## PUT ​/api​/v1​/Users​/{id}  (отрицательный ID)

- URL https://fakerestapi.azurewebsites.net/api/v1/Users/{{Author_minus_id}}

- Ожидаемый результат: код ответа 405, тест провален

- Заголовки запроса :
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Postman-Token: fad415a3-1052-4e99-823a-d5989a98c28d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
- Тело запроса : 
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Заголовки ответа :
``` 
Content-Type: application/json; charset=utf-8; v=1.0
Date: Tue, 06 Jun 2023 14:06:17 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
```
- Тело ответа:
```
{
    "id": 0,
    "userName": "string",
    "password": "string"
}
```