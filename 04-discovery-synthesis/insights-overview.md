# Discovery Insights Overview

> Fonte viva para consolidar necessidades, dores e oportunidades identificadas nas reuniões de discovery. Atualizar sempre que um novo encontro for processado em `/02-meetings/`.

---

## 1. Snapshot por Reunião

| Data | Cliente | Tema central | Necessidades chave | Próximos passos | Artefactos |
| --- | --- | --- | --- | --- | --- |
| 2025-10-08 | SLAM | Fan intelligence para monetizar audiência | Provar valor a marcas não endémicas; atualizar perfis reais de seguidores; suportar decisões editoriais/merch | Preparar demo presencial NYC + one-pager | [Pasta](../02-meetings/2025-10-08-hoopers-slam/) |
| 2025-10-08 | Liga Portugal | Fan experience & ticketing orientados a dados | Integrar dados de app/fantasy/redes sociais; métricas comerciais acionáveis; benchmarking com outras ligas | Enviar deck + agendar demo com Diogo Lourenço & João Cardoso | [Pasta](../02-meetings/2025-10-08-liga-portugal/) |
| 2025-10-13 | Hoopers (interno) | Reposicionamento do produto Alley | Destacar KPIs únicos, criar dashboards por persona, clarificar storytelling comercial | Redesenhar UI/UX; preparar one-pagers/roteiros por persona; avaliar contratação de Product/UX | [Pasta](../02-meetings/2025-10-13-internal-product/) |

> **Como usar**: adicionar uma linha por reunião processada. Priorizar colunas “Necessidades chave” e “Próximos passos” com notas concisas (1–2 frases).

---

## 2. Backlog de Necessidades (Cross-Clientes)

| Categoria | Descrição | Origem (Reunião/linha) | Evidência | Impacto estimado |
| --- | --- | --- | --- | --- |
| Monetização com marcas não endémicas | Necessidade de quantificar interesses (automóvel, finanças, etc.) para propostas comerciais | SLAM (`insights-overview` linha 1) | `02-meetings/2025-10-08-hoopers-slam/key-insights.md` | Alta (impacta 80–90% dos deals SLAM) |
| Fan intelligence integrada | Desejo de cruzar dados proprietários (app, fantasy, ticketing) com social analytics | Liga Portugal (`insights-overview` linha 2) | `02-meetings/2025-10-08-liga-portugal/key-insights.md` | Alta (directamente ligado a fan experience & bilhética) |
| Storytelling por persona | Demos e dashboards precisam falar diretamente com CMO, community, sponsorship e social media managers | Hoopers interno (`insights-overview` linha 3) | `02-meetings/2025-10-13-internal-product/key-insights.md` | Alta (essencial para conversão comercial) |
| KPIs contextualizados | Necessidade de thresholds, trendlines e benchmarks para tornar insights acionáveis | Hoopers interno (`insights-overview` linha 3) | `02-meetings/2025-10-13-internal-product/key-insights.md` | Alta (melhora confiança no produto) |

> **Nota**: duplicar linhas quando a mesma necessidade surge em vários clientes; usar a coluna “Origem” para manter rastreabilidade.

---

## 3. Oportunidades de Produto

| Tema | Ideia | Clientes interessados | Dependências | Status |
| --- | --- | --- | --- | --- |
| Benchmarking entre ligas | Dashboard que compara KPIs (engagement, sentiment, horários) entre Liga e concorrentes | Liga Portugal | Consolidar inventário de KPIs (`/03-portal-audit`) | Em descoberta |
| Segmentação de propostas comerciais | Biblioteca de filtros (carros, finanças, lifestyle) para exportar insights | SLAM, potencialmente Liga | Definir taxonomias → depende de análise do data schema | Em descoberta |
| Dashboards por persona | Layouts específicos (CMO, Community, Sponsorship, Social) destacando KPIs exclusivos | Hoopers interno; aplicável a todos os clientes | Reorganizar sitemap + priorizar KPIs únicos | Em desenho |

---

## 4. Ações Pendentes (Follow-ups)

| Responsável | Ação | Clientes | Status | Fonte |
| --- | --- | --- | --- | --- |
| Equipa Hoopers | Enviar one-pager + agendar demo NYC | SLAM | Pendente | `02-meetings/2025-10-08-hoopers-slam/action-items.md` |
| Equipa Hoopers | Agendar demo com Diogo Lourenço & João Cardoso | Liga Portugal | Pendente | `02-meetings/2025-10-08-liga-portugal/action-items.md` |
| Produto Hoopers | Reestruturar tabs + dashboards por persona antes das demos de novembro | Interno | Em progresso | `02-meetings/2025-10-13-internal-product/action-items.md` |

---

## 5. Processo de Atualização

1. **Processar reunião** em `/02-meetings/` (pasta + ficheiros).
2. **Adicionar linha** à tabela “Snapshot por Reunião”.
3. **Avaliar se surgiram novas necessidades**; se sim, copiar para “Backlog de Necessidades” com referência de origem.
4. **Atualizar oportunidades** ou ações pendentes conforme aplicável.
5. **Referenciar sempre os ficheiros de origem** (`key-insights.md`, `action-items.md`) para rastreabilidade.

> Dica: use esta página como base para Sprint 4 (síntese) e Sprint 5 (roadmap). As colunas de impacto/dependências tornam mais fácil priorizar gaps e requisitos.
