# 03 — JPetStore

[JPetStore](https://jpetstore.mate.academy/jpetstore/actions/Catalog.action) é uma loja de pets de demonstração (registro, login, catálogo, busca, carrinho). Foi o primeiro projeto prático: escrever casos de teste a partir de requisitos, executá-los, reportar bugs e fechar um ciclo STLC completo.

## Conteúdo

| Documento | O que tem |
|---|---|
| [test-cases-execution.md](test-cases-execution.md) | 16 casos (registro, login, busca, carrinho) com passos, resultado esperado, prioridade e status de execução |
| [stlc-cart-checklist.md](stlc-cart-checklist.md) | STLC do carrinho: checklist de 34 itens, execução, 7 bug reports e estatísticas |
| [bug-reports.md](bug-reports.md) | 5 bug reports completos (Sign-in, Help e Registration) |
| [bug-summaries.md](bug-summaries.md) | 6 bug summaries curtos (o quê / onde / quando + evidência) |

## Números

- **Casos de teste:** 16 executados em Production / Chrome / macOS — 3 passed, 11 failed, 2 blocked.
- **STLC — carrinho (26/03/2025):** 34 checks, 33 executados (97,06%), 25 passed (75,76%), 8 failed; **7 bugs** — 6 Major e 1 Moderate.
- Exemplos de bugs: campo *Quantity* aceita texto, limite de 5 unidades por produto não é aplicado, produto sem estoque pode ser comprado, coluna *Name* ausente no carrinho, campo de senha do login vem preenchido por padrão (atributo `value="j2ee"` no HTML), erro HTTP 500 no cadastro sem campos obrigatórios.

**Habilidades:** casos de teste a partir de requisitos, checklist, execução com status, bug reports (severidade × prioridade, ambiente, evidências), métricas de execução.
