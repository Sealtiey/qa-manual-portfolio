# Arquitetura cliente-servidor — requisições da API do Conduit

Análise de 5 requisições reais feitas pela interface do Conduit, capturadas no DevTools (aba *Network*): descrição, URL, método, path, headers, corpo da requisição e da resposta, e status code. Conteúdo original em inglês.

> Tokens de autenticação foram substituídos por `<token>`. A senha da conta de teste foi substituída por `<senha>`.

## Resumo

| # | Requisição | Método registrado | Path | Status |
|---|---|---|---|---|
| 1 | Registration | POST | `/api/users` | 200 |
| 2 | Create Article | GET | `/api/articles/new-article-title-om7hkr` | 200 |
| 3 | Update Article | GET | `/api/articles/article-title-t7rlvf` | 200 |
| 4 | Delete Article | DELETE | `/api/articles/article-title-t7rlvf` | 204 |
| 5 | Get profile information | GET | `/api/profiles/usersalty` | 304 |

## Request #1: Registration

This request is needed to register a new user.

| Propriedade | Valor |
|---|---|
| Request URL | `https://conduit.mate.academy/api/users` |
| Method | POST |
| Path | `/api/users` |
| Authorization | — |
| Content-Type (request) | application/json |
| Status code | 200 |
| Content-Type (response) | application/json; charset=utf-8 |

**Request body / payload (como exibido no DevTools):**

```
user
: 
{username: "usersalty", email: "user@gmail.com", password: "<senha>"}
email
: 
"user@gmail.com"
password
: 
"<senha>"
username
: 
"usersalty"
```

**Response body:**

```json
{
    "user": {
        "username": "usersalty",
        "email": "user@gmail.com",
        "token": "<token>",
        "bio": null,
        "image": null
    }
}
```

## Request #2: Create Article

This request is needed to create a new article.

| Propriedade | Valor |
|---|---|
| Request URL | `https://conduit.mate.academy/api/articles/article-title-t7rlvf` |
| Method | GET |
| Path | `/api/articles/new-article-title-om7hkr` |
| Authorization | `Token <token>` |
| Content-Type (request) | — |
| Status code | 200 |
| Content-Type (response) | application/json; charset=utf-8 |

**Request body / payload (como exibido no DevTools):**

```
author
: 
{username: "usersalty", bio: null, image: "/images/smiley-cyrus.jpg", following: false}
body
: 
"Article body"
createdAt
: 
"2026-07-22T14:53:15.777Z"
description
: 
"Article topic"
favorited
: 
false
favoritesCount
: 
0
slug
: 
"article-title-t7rlvf"
tagList
: 
[]
title
: 
"Article Title"
updatedAt
: 
"2026-07-22T14:53:15.777Z"
```

**Response body:**

```json
{
    "article": {
        "slug": "article-title-t7rlvf",
        "title": "Article Title",
        "description": "Article topic",
        "body": "Article body",
        "createdAt": "2026-07-22T14:53:15.777Z",
        "updatedAt": "2026-07-22T14:53:15.777Z",
        "tagList": [],
        "favorited": false,
        "favoritesCount": 0,
        "author": {
            "username": "usersalty",
            "bio": null,
            "image": "/images/smiley-cyrus.jpg",
            "following": false
        }
    }
}
```

## Request #3: Update Article

This request is necessary to update an article.

| Propriedade | Valor |
|---|---|
| Request URL | `https://conduit.mate.academy/api/articles/article-title-t7rlvf` |
| Method | GET |
| Path | `/api/articles/article-title-t7rlvf` |
| Authorization | `Token <token>` |
| Content-Type (request) | application/json |
| Status code | 200 |
| Content-Type (response) | application/json; charset=utf-8 |

**Request body / payload (como exibido no DevTools):**

```
article
: 
{title: "New Article Title", description: "Article topic", body: "Article body", tagList: []}
body
: 
"Article body"
description
: 
"Article topic"
tagList
: 
[]
title
: 
"New Article Title"
```

**Response body:**

```json
{
    "article": {
        "slug": "article-title-t7rlvf",
        "title": "New Article Title",
        "description": "Article topic",
        "body": "Article body",
        "createdAt": "2026-07-22T14:53:15.777Z",
        "updatedAt": "2026-07-22T14:58:52.191Z",
        "tagList": [],
        "favorited": false,
        "favoritesCount": 0,
        "author": {
            "username": "usersalty",
            "bio": null,
            "image": "/images/smiley-cyrus.jpg",
            "following": false
        }
    }
}
```

## Request #4: Delete Article

This request is required to delete an article.

| Propriedade | Valor |
|---|---|
| Request URL | `https://conduit.mate.academy/api/articles/article-title-t7rlvf` |
| Method | DELETE |
| Path | `/api/articles/article-title-t7rlvf` |
| Authorization | `Token <token>` |
| Content-Type (request) | — |
| Status code | 204 |
| Content-Type (response) | — |

## Request #5: Get profile information

This request is required to access the user page.

| Propriedade | Valor |
|---|---|
| Request URL | `https://conduit.mate.academy/api/profiles/usersalty` |
| Method | GET |
| Path | `/api/profiles/usersalty` |
| Authorization | `Token <token>` |
| Content-Type (request) | — |
| Status code | 304 |
| Content-Type (response) | — |

**Request body / payload (como exibido no DevTools):**

```
profile
: 
{username: "usersalty", bio: null, image: "/images/smiley-cyrus.jpg", following: false}
bio
: 
null
following
: 
false
image
: 
"/images/smiley-cyrus.jpg"
username
: 
"usersalty"
```

**Response body:**

```json
{
    "profile": {
        "username": "usersalty",
        "bio": null,
        "image": "/images/smiley-cyrus.jpg",
        "following": false
    }
}
```
