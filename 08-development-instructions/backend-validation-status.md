# Backend & KPI Validation Status (2024-10-13)

## Dashboard Endpoints Existentes
- [OK] `/api/dashboard/get-filters` — Tabelas de referência completas (género, idade, etnia, lifestyle, status, indústria, continente, players, teams); confirmar apenas serialização final.
- [OK] `/api/dashboard/sentiment-analysis` — 17 260 posts com sentimento (avg 6.45, 1.38M comentários) suportam trend/delta; manter uso de cache Redis.
- [OK] `/api/dashboard/engagement-trend` — Agregações diárias recentes com milhões de interações; pronto para trend e overlay futuro.
- [OK] `/api/dashboard/audience-*` — Autores com atributos demográficos/segmentação suficientes (industry, status, pet, localização) → payloads completos dentro dos limites configurados.
- [OK] `/api/dashboard/content-performance` — Volume (3.3B likes / 15.3M comentários) garante métricas de eficiência e alcance; aplicar filtros de canal conforme necessário.
- [OK] `/api/dashboard/buzzer/data` — Configurações `buzzer_api_key` e `buzzer_app_identifier` ativas para contas 1/9; validar resposta do serviço externo em staging.

## Analytics, Instagram e Segmentação
- [OK] `/api/analytics/get-brand-*`, `/api/analytics/get-top-items` — `brands`, `posts_analysis_brand`, categorias populadas; apto para momentum/afinidades.
- [NOK] `/api/dashboard/instagram/*` — Tabelas `instagram_*` vazias; necessário pipeline de ingestão ou ocultar módulo.
- [NOK] Segmentação & Exports — Inexistem `/audienceSegments/*`, `/exports/*`; criar tabela de presets e endpoints antes de expor UX.

## Endpoints Planeados (Draft API Reference)
- [NOK] Brand Health (`/brandHealth/*`, `/events/timeline`, `/alerts/active`) — Rotas/datasets consolidados ausentes; preencher `alerts` e construir serviço agregador.
- [NOK] Competitive (`/competitive/*`) — Falta implementação; usar `posts_analysis_brand`+sentimento para gerar SoV/Gap ao criar endpoints.
- [NOK] Sponsorship (`/sponsorship/*`, `/audienceSegments/topValue`) — Sem dados de revenue/activation; modelar esquema comercial antes de ativar.
- [NOK] Partnership (`/partnerships/*`, `/influencers/matches`) — Requer vistas temporais e motor de matching; apenas mentions brutas disponíveis hoje.
- [NOK] Engagement Support dedicados (`/engagement/*`, `/audience/growth`, `/audience/retention`, `/engagement/recommendations`) — Aproveitar `DashboardService`, mas falta histórico (`channel_history` vazio) e endpoints específicos.

## Fórmulas & KPIs
- [NOK] Brand Health Score — Ausência de `community.healthIndex` e `brandAwareness`; definir métricas/fonte antes de calcular.
- [OK] Net Sentiment Trend — `avg_sentiment_value` + contagens positiva/negativa suportam cálculo conforme serviço atual.
- [NOK] Community Wellbeing — Sem dados de retention/support; ajustar definição ou recolher métricas adicionais.
- [NOK] Crisis Alerts — Tabela `alerts` vazia; sincronizar com Buzzer ou gerar alertas internos.
- [OK] Competitive Position / Share of Voice — `posts_analysis_brand` fornece base; falta apenas endpoint consolidado.
- [NOK] Revenue Opportunity Range — Não existe `AvgDealValue` nem segmentos monetizáveis; criar integrações comerciais.
- [NOK] Activation Performance — Ausência de métricas de uplift/conversão; necessário tracking de campanhas.
- [NOK] Sponsor Sentiment — Apenas 22 posts com `sponsors` preenchido; expandir tagging automático antes de usar KPI.
- [OK] Emerging Brand Momentum — Combinar mentions por marca (30d vs média 3m) viável com dados existentes.
- [NOK] Influencer Alignment — `author_followers` (709 registos) insuficiente para overlap robusto; ampliar scraping ou ajustar scoring.
- [OK] Content Efficiency — Likes/comentários e contagem de posts disponíveis; KPI utilizável já via content-performance.
- [NOK] Audience Growth — `channel_history` vazio; ativar job de captura diária para habilitar cálculo.
- [NOK] Retention/Churn — Não existem colunas de retained/churned; definir fonte (app/CRM) antes de expor.
- [OK] Heatmap Engagement — `posts.post_date` + métricas permitem agregação dia/hora.
