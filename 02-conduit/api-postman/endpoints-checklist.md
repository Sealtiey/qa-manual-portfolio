# Conduit API — checklist de endpoints

Lista de cenários de API planejados e cobertos na collection do Postman (todos marcados como cobertos na planilha original). Base: API do Conduit (`/api`). Conteúdo original em inglês.

| # | Action | Endpoint | Expected status |
|---|---|---|---|
| **User** |  |  |  |
| 1 | Successful sign in | POST /users/login | 200 |
| 2 | Sign in with non-existing credential | 〃 | 422 |
| 3 | Sign in with empty email | 〃 | 422 |
| 4 | Sign in with empty password | 〃 | 422 |
| 5 | Successful sign up | POST /users | 200 |
| 6 | Sign up with taken username | 〃 | 422 |
| 7 | Sign up with taken email | 〃 | 422 |
| 8 | Sign up with username starting from number | 〃 | 422 |
| 9 | Sign up with username with 41 symbols | 〃 | 422 |
| 10 | Sign up with username with spaces | 〃 | 422 |
| 11 | Sign up with empty username | 〃 | 422 |
| 12 | Sign up with empty email | 〃 | 422 |
| 13 | Sign up with email without @ | 〃 | 422 |
| 14 | Sign up with email without . | 〃 | 422 |
| 15 | Sign up with email without name part | 〃 | 422 |
| 16 | Sign up with email with more than 254 symbols | 〃 | 422 |
| 17 | Sign up with empty password | 〃 | 422 |
| 18 | Get info about user | GET /user | 200 |
| 19 | Update info about user: image | PUT /user | 200 |
| 20 | Update info about user: bio | 〃 | 200 |
| 21 | Update info about user: username | 〃 | 200 |
| 22 | Update info about user: email | 〃 | 200 |
| 23 | Update info about user: password | 〃 | 200 |
| 24 | Update info about user without authorization | 〃 | 401 |
| **Articles** |  |  |  |
| 1 | Create an article | POST /articles | 200 |
| 2 | Update an article | PUT /articles/:slug | 200 |
| 3 | Delete an article | DELETE /articles/:slug | 204 |
| 4 | Get an article | GET /articles/:slug | 200 |
| 5 | Get articles | GET /articles | 200 |
| 6 | Get articles from Your feed | GET /articles/feed?limit=10&offset=0 | 200 |
| 7 | Get articles from Global feed | GET /articles?limit=10&offset=0 | 200 |
| 8 | Get articles by tag | GET /articles?limit=10&tag=:tag:&offset=0 | 200 |
| 9 | Create an article without authorization | POST /articles | 401 |
| 10 | Delete an article without authorization | DELETE /articles/:slug | 401 |
| 11 | Delete an article of another user | DELETE /articles/:slug | 403 |
| 12 | Delete non-existing article | DELETE /articles/:slug | 404 |
| **Profile** |  |  |  |
| 1 | Get info about profile | GET /profiles/:profile | 200 |
| 2 | Follow the user | POST /profiles/:username:/follow | 200 |
| 3 | Unfollow the user | DELETE /profiles/:username:/follow | 200 |
| **Tags** |  |  |  |
| 1 | Get tags | GET /tags | 200 |
| **Comments** |  |  |  |
| 1 | Get comments | GET /articles/:slug:/comments | 200 |
| 2 | Post a comment | POST /articles/:slug:/comments | 200 |
| 3 | Delete a comment | DELETE /articles/:slug:/comments/:id: | 204 |
| 4 | Delete a comment of another user | DELETE /articles/:slug:/comments/:id: | 403 |
| 5 | Delete a comment without authorization | DELETE /articles/:slug:/comments/:id: | 401 |

`〃` = mesmo endpoint da linha anterior.
