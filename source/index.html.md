---
title: Ellabib API v1.0.0
language_tabs:
  - javascript: JavaScript
toc_footers:
  - >- 
    <a href="https://github.com/vinylen2/ltu-ellabib">See Github repo</a>
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v3.6.6 -->
<h1 id="Ellabib-API">Ellabib API v1.0.0</h1>

This is the API for the Ellabib application

Base URLs:

* <a href="https://api.ellabib.se">https://api.ellabib.se</a>

<h1 id="user">User</h1>

Everything about the authenticated user

## getUser

<a id="getUserInfo"></a>

> Code samples


```javascript
$.ajax({
  url: 'http://api.ellabib.se/user/id/:id',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```


`GET /user`

*Get user info*

> Example response

```json
{
    "data": [
        {
            "id": 1,
            "firstName": "Gabriel",
            "lastName": "Wallén",
            "extId": null,
            "type": "admin",
            "displayName": "Administratör",
            "pagesRead": "235",
            "booksRead": 2,
            "classDisplayName": "1A",
            "classId": 1,
            "avatarId": 1,
            "avatarImageUrl": null,
            "avatarDisplayName": "Vanlig",
            "avatarType": "basic"
        }
    ]
}

```
<h3 id="getUser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|OK|succesful operation|Inline|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|Invalid input|None|

<h3 id="getUser-responseSchema">Response Schema</h3>

Status code 200
|Name|Type|Required|Description|
|---|---|---|---|
|id|integer|true|Unique ID for user|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
petstore_auth ( Scopes: write:pets read:pets )
</aside>


# Schemas

<h2 id="tocSorder">Order</h2>

<a id="schemaorder"></a>

```json
{
  "id": 0,
  "petId": 0,
  "quantity": 0,
  "shipDate": "2018-04-24T13:02:08Z",
  "status": "placed",
  "complete": false
}
```

### Properties

|Name|Type|Required|Description|
|---|---|---|---|
|id|integer(int64)|false|No description|
|petId|integer(int64)|false|No description|
|quantity|integer(int32)|false|No description|
|shipDate|string(date-time)|false|No description|
|status|string|false|Order Status|
|complete|boolean|false|No description|

#### Enumerated Values

|Property|Value|
|---|---|
|status|placed|
|status|approved|
|status|delivered|


<script type="application/ld+json">
{
  "@context": "http://schema.org/",
  "@type": "WebAPI",
  "description": ":dog: :cat: :rabbit: This is a sample server Petstore server.  You can find out more about Swagger at [http://swagger.io](http://swagger.io) or on [irc.freenode.net, #swagger](http://swagger.io/irc/).  For this sample, you can use the api key `special-key` to test the authorization filters.",
  "documentation": "https://mermade.github.io/shins/asyncapi.html",
  "termsOfService": "http://swagger.io/terms/",
  
  "name": "Swagger Petstore"
}
</script>

