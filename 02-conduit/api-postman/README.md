# Conduit — testes de API com Postman

## Collection

**[conduit-api-tests.postman_collection.json](conduit-api-tests.postman_collection.json)** — importável no Postman (formato v2.1). **44 requests** em 5 pastas, com **157 checks** (`pm.test`):

| Pasta | Requests |
|---|---|
| User | 23 |
| Articles | 12 |
| Profile | 3 |
| Tags | 1 |
| Comments | 5 |

Como a collection foi montada:

- Variáveis no nível da collection (sem depender de environment). No arquivo todas vêm vazias; usuários, tokens, slugs e IDs são gerados pelos scripts em tempo de execução.
- **Requests independentes:** funções no pre-request da collection registram usuários, criam artigos/comentários e seguem usuários quando o cenário precisa, então cada request roda sozinha.
- Testes verificam status code, tempo de resposta (< 1000 ms), estrutura e valores do corpo da resposta.
- Cenários negativos: credenciais inexistentes, campos vazios, username/email já usados, username com 41 caracteres ou começando com número, email inválido, ações sem autorização (401), em recurso de outro usuário (403) e em recurso inexistente (404).
- Há funções auxiliares para apagar os artigos criados durante os testes.

Para rodar: importar o arquivo no Postman, preencher as variáveis `url` (base da API, ex.: `https://conduit.mate.academy/api`) e `passwordConduit` (senha usada para os usuários de teste criados pelos scripts) e executar com o Collection Runner.

## Checklist de endpoints

**[endpoints-checklist.md](endpoints-checklist.md)** — os 45 cenários planejados (User 24, Articles 12, Profile 3, Tags 1, Comments 5), com endpoint e status esperado.

## Data-driven testing (CSV)

Pasta **[data-driven/](data-driven/)**: arquivos CSV usados como *data files* no Collection Runner (iterações com variáveis vindas do arquivo):

- `register_users.csv` — usuários para cadastro em massa (username, email, password).
- `postman-part-iii.csv` — username + bio esperada, para validar o perfil de cada usuário após atualizar a bio.
- `postman-part-i.csv` e `postman-part-ii.csv` — dados das partes I e II do exercício (usuários; cidades com latitude/longitude).

Bug encontrado nessa tarefa e reportado no Jira: `GET /profiles/<username>` retornava `"bio": null` para um usuário cujo CSV definia uma bio (por exemplo `"I'm a teacher"`), ou seja, a atualização de bio não estava refletida no perfil.

> Dados de teste: os nomes de usuário que pareciam nomes reais foram trocados por `test_user_NN` e os emails da parte I por endereços `@example.com`.

**Habilidades:** Postman (collections, variáveis, pre-request scripts, testes, runner, data files), cenários positivos/negativos de API, códigos de status HTTP.
