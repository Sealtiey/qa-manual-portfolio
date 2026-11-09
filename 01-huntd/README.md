# 01 — Huntd (projeto principal)

[Huntd](https://huntd.tech/) é uma plataforma para contratação de desenvolvedores web3, com aplicação **web** (desktop e mobile browser) e **app mobile** (Android/iOS). Projeto final de prática: testar a versão web e a mobile a partir dos requisitos documentados e dos requisitos implícitos do produto.

## Escopo

- **Web (11 módulos):** Main Page, For Companies, For Engineers, Authentication / Registration, Candidates, Candidate Profile, Recruiter Profile, Jobs, Chats / Messages, Bonus, Footer.
- **Mobile (5 módulos, apenas o que está implementado no app):** Login / Authentication, My Chats, Profile, Preferences, Sign Out.
- Fora de escopo (definido no projeto): funcionalidades de admin e formulário de feedback.

## Abordagem

1. **[Test plan](test-plan.md)** único para web e mobile: objetivo, escopo, estratégia (funcional, UI, navegação, validação de formulários, autenticação, permissões, links), ambiente, gestão de defeitos, critérios de conclusão.
2. Decomposição por módulo → projetos separados no TestRail para web e mobile; uma story por feature no Jira.
3. **[Permission testing](permission-testing.md):** matriz de acesso por módulo para usuário deslogado, candidato e recrutador.
4. **[RTM](rtm.md):** rastreabilidade requisito técnico → módulo → casos de teste (web e mobile separadas).
5. Execução no TestRail, bugs no Jira vinculados aos resultados, e **[test report](test-report.md)** com as estatísticas.

## Números

| | Casos | Passed | Failed | Pass rate |
|---|---|---|---|---|
| Web | 129 | 123 | 6 | 95% |
| Mobile | 26 | 26 | 0 | 100% |
| **Total** | **155** | **149** | **6** | |

- **8 bugs** reportados no Jira para a aplicação web: **3 High** e **5 Medium** (nenhum Critical/Low). Nenhum defeito encontrado no mobile.
- Módulos web com falhas: Candidate Profile (3), Main Page (1), For Engineers (1), Chats / Messages (1).
- Execução: 22 a 25/09/2026.

## Documentos

| Documento | Conteúdo |
|---|---|
| [test-plan.md](test-plan.md) | Plano de teste web + mobile |
| [permission-testing.md](permission-testing.md) | Matriz de permissões (11 módulos × 3 perfis) |
| [rtm.md](rtm.md) | Requirements Traceability Matrix — web (129) e mobile (26) |
| [test-report.md](test-report.md) | Test report: execução por feature e bugs por prioridade |

**Habilidades:** planejamento de testes, análise de requisitos explícitos e implícitos, teste de permissões por perfil, rastreabilidade, TestRail, Jira, métricas de execução e report.
