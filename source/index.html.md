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
            "roleType": "admin",
            "roleDisplayName": "Administratör",
            "pagesRead": "155",
            "booksRead": 1,
            "reviewsWritten": "1",
            "classDisplayName": "1A",
            "classId": 1,
            "avatarId": 1,
            "avatarImageUrl": "https://ellabib.se/images/avatar-1.png",
            "avatarDisplayName": "basic",
            "avatarType": "avatar-1"
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

<h1 id="classes">Classes</h1>

## getClasses

<a id="getClassesInfo"></a>

> Code samples


```javascript
$.ajax({
  url: 'http://api.ellabib.se/classes',
  method: 'get',
})
```

`GET /classes`

*Get classes info*

> Example response

```json
{
    "data": [
        {
            "pagesRead": "155",
            "displayName": "1A",
            "booksRead": 1,
            "id": 1
            },
        {
            "pagesRead": "140",
            "displayName": "2A",
            "booksRead": 1,
            "id": 2
        }
    ]
}

```
<h3 id="getClasses-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|OK|succesful operation|Inline|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|Invalid input|None|

<h3 id="getClasses-responseSchema">Response Schema</h3>

Status code 200
|Name|Type|Required|Description|
|---|---|---|---|
|id|integer|true|Unique ID for user|

<h1 id="schoolUnit">School Unit</h1>

Get data about school units


## getSchoolUnit

<a id="getSchoolUnitInfo"></a>

> Code samples


```javascript
$.ajax({
  url: 'http://api.ellabib.se/schoolunit',
  method: 'get',
})

```


`GET /schoolunit`

*Get school unit info*

> Example response

```json
{
    "data": [
        {
            "id": 1,
            "displayName": "Ellagårdsskolan",
            "pagesRead": "267",
            "booksRead": 3
        }
    ]
}
```
<h3 id="getSchoolUnit-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|OK|succesful operation|Inline|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|Invalid input|None|

<h3 id="getSchoolUnit-responseSchema">Response Schema</h3>

Status code 200
|Name|Type|Required|Description|
|---|---|---|---|
|id|integer|true|Unique ID for schoolUnit|


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

