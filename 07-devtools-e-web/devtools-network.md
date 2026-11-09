# DevTools — Network

Identificação, na aba *Network*, de uma requisição bem-sucedida, uma com problema de backend (5xx) e uma com problema de frontend (4xx). Conteúdo original em inglês.

| Request | Request name | Request method | Request URL | Status code |
|---|---|---|---|---|
| Successful request | comments | GET | https://conduit.mate.academy/_next/data/QM9lXs-Ci0evin7H8A5Bk/index.json | 200 OK |
| Request with a backend problem | 500 | GET | https://mock.httpstatus.io/500 | 500 Internal Server Error |
| Request with a frontend problem | dummy?data=someData | GET | https://example.com/dummy?data=someData | 404 Not Found |
