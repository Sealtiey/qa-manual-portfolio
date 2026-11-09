# Portfólio de QA manual — Sealtiey Menegassi

Ex-tech recruiter em transição para **QA manual**: testes de aplicações web e mobile, testes de API com Postman, consultas SQL e gestão de testes/bugs com TestRail e Jira.
Site/portfólio: **[sealtiey.github.io](https://sealtiey.github.io)**

Este repositório reúne os artefatos que produzi na formação de QA da Mate Academy — planos de teste, decomposições, casos de teste, execuções, bug reports, matrizes de rastreabilidade e técnicas de desenho de teste — convertidos para Markdown para leitura direta no GitHub. Os artefatos em si (casos, bugs, planos) estão em inglês, como foram escritos; os textos de apresentação estão em português.

## Projetos

| # | Projeto | O que tem | Habilidades demonstradas |
|---|---|---|---|
| 01 | [**Huntd** (projeto principal)](01-huntd/) | Test plan web + mobile, permission testing, RTM, test report: **155 casos** (129 web, 95% passed; 26 mobile, 100% passed) e **8 bugs no Jira** (3 high, 5 medium) | Planejamento, rastreabilidade, testes de permissão, execução e report |
| 02 | [**Conduit**](02-conduit/) | Test plan, decomposição, 120 casos no TestRail, 8 test runs com bugs vinculados ao Jira, collection Postman (44 requests / 157 checks), SQL e ambientes locais | TestRail + Jira, API testing, SQL, Docker |
| 03 | [**JPetStore**](03-jpetstore/) | 16 casos executados, ciclo STLC do carrinho (34 checks, 7 bugs), bug reports e bug summaries | Casos de teste, checklist, bug reporting, métricas de execução |
| 04 | [**Mobile**](04-mobile/) | Huntd mobile, emuladores (Android Studio / Genymotion), mockup testing, bug report curto, perguntas situacionais | Testes mobile, emuladores, bug reports com evidência |
| 05 | [**Técnicas de teste**](05-tecnicas-de-teste/) | Classes de equivalência, valores-limite, tabela de decisão, pairwise, transição de estados, tipos de teste, refinamento de requisitos, SQC | Desenho de testes (black box) e análise de requisitos |
| 06 | [**User stories — Vagas.com**](06-user-stories-vagas/) | 2 personas, 6 user stories com critérios de aceite, 23 casos de teste | Requisitos ágeis e testes a partir de critérios de aceite |
| 07 | [**DevTools e web**](07-devtools-e-web/) | Console, Network, Application, carregamento de página, cliente-servidor, bug reports estendidos | Investigação de bugs no navegador, HTTP |

## Ferramentas

- **Gestão de testes e bugs:** TestRail, Jira (stories, sprints, bugs, integração TestRail ↔ Jira)
- **API:** Postman (collections, variáveis, pre-request scripts, testes, data-driven com CSV)
- **Banco de dados:** SQL — DBeaver (SQLite), PostgreSQL via `psql`
- **Web:** Chrome DevTools (Elements, Console, Network, Application)
- **Mobile:** Android Studio (emulador), Genymotion
- **Ambientes:** Docker / Docker Compose
- **Documentação:** Google Docs/Sheets, draw.io

## Observações

- Foco: **testes manuais** (web, mobile e API). A collection do Postman usa scripts de teste do próprio Postman; não há automação de UI neste repositório.
- Links para as instâncias privadas de Jira/TestRail e para documentos do Google foram removidos; os conteúdos relevantes foram exportados e convertidos para cá.
- Tokens, senhas e dados pessoais foram substituídos por placeholders (`<token>`, `<senha>`, `test_user_NN`, `@example.com`).
