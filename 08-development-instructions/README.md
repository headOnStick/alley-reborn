# Development Instructions - Alley Reborn

## Documentos incluídos
- `design-guidelines.md` — Orientações para designers (layout, componentes, dados permitidos).
- `api-reference-by-component.md` — Endpoints disponíveis por componente UI.
- `formula-reference.md` — Fórmulas/calculadas necessárias (data science / KPIs compostos).
- `backend-validation-checklist.md` — Itens para confirmação com engenharia de dados/backend.
- `backend-validation-status.md` — Checklist de status OK/NOK por endpoint e KPI.
- `backend-data-schema-insights.md` — Resumo da estrutura de dados confirmada e lacunas.

## Regras gerais
- Usar apenas dados existentes nas APIs levantadas (`01-context/api-reference.md`) e no data schema (`01-context/data-schema.md`).
- Quando for necessário derivar métricas, especificar a fórmula em `formula-reference.md` e a página/componente que usa.
- Qualquer nova hipótese de dado deve vir com regra de negócio clara ou ficar marcada como “a validar”.
- Manter alinhamento com a arquitetura definida: tabs principais (Brand Health, Competitive, Sponsorship, Partnerships, Engagement) e componentes descritos em `06-future-product/page-structures/dashboard.md`.

## Próximos passos
- Preencher os ficheiros com base nos endpoints actuales e layouts aprovados.
- Designers usam `design-guidelines.md` como fonte única de verdade para mockups.
- Engenharia consome `api-reference-by-component.md` + `formula-reference.md` para planear implementação.
