# Backend Data Schema Insights (2024-10-13)

## Core Entidades
- Accounts/Users: `accounts` liga-se a `users` via `users_accounts` (com `is_owner`); `account_configs` + `config_definitions` guardam settings (ex.: `buzzer_api_key` para contas 1 e 9).
- Channels/Autores: `channel` associa-se a contas (`accounts_channels`) e autores (`channel_author`); `channel_history` existe mas está vazio — requer job diário antes de usar métricas históricas.
- Autores: `authors` contém atributos demográficos e de lifestyle (gender, idade, etnia, indústria, status, pet friendly, localização). Soma de seguidores ≈ 7.1B, com 4 330 players e 825 teams referenciáveis.

## Conteúdo & Interações
- Posts: 58 871 registos em `posts` com likes, comentários, métricas de sentimento (`avg_sentiment_value`, contagens positivas/negativas), `media_type_id` e `sponsors` (apenas 22 posts com lista não vazia).
- Comentários: `comments` (4.61M) ligados a `posts` e `authors`, com timestamps e FK opcionais.
- Análises: `comments_analysis` (1.60M) + satélites (`comment_analysis_emotion`, `_player`, `_team`) fornecem sentimento/toxicidade/emoções; `posts_analysis` + `_brand/_team/_player/_call_to_action` mapeiam entidades e call-to-actions (1 101 ligações a marcas).
- Hashtags: `posts_hashtag` com índices por hashtag e ligações a posts/comentários.

## Segmentação & Referências
- Dimensões confirmadas: `genders`, `age_intervals`, `ethnicities`, `lifestyles`, `status_class`, `industries`, `continents`, `countries`, `states`, `cities`, `languages`, `emotions`, `call_to_action`, `media_types`.
- `authors` referenciam essas dimensões, alimentando filtros existentes (`/api/dashboard/get-filters` e `/api/analytics/get-filters`).
- `user_filters` (JSON) permite presets de filtros por utilizador.

## Lacunas de Dados
- Instagram: `instagram_accounts` e tabelas relacionadas estão vazias — endpoints Instagram retornam vazio até ingestão.
- Alertas/Growth: `alerts` e `channel_history` sem registos; impossibilita calcular alertas internos e crescimento/retention.
- Segmentos/Exports: não existem tabelas para `audienceSegments` ou exports (confirmado via consultas); é necessário novo esquema para suportar `/audienceSegments/*` e `/exports/*`.
- Métricas de negócio: não há colunas para awareness, retention, revenue ou activation — KPIs planeados dependem de fontes externas ou novo armazenamento.

## Ações Recomendadas
- Implementar ETL para `channel_history` (followers, engagement diário) e popular `alerts` com dados do Buzzer ou motor interno.
- Desenhar tabelas `audience_segments` e `report_exports` com metadata suficiente (ID, nome, regra, tamanho estimado, timestamps).
- Priorizar pipeline de ingestão Instagram (contas, posts, métricas por media) antes de expor endpoints no produto.
- Definir esquema comercial/CRM para revenue opportunity, activation performance e sponsor sentiment antes de marcar KPIs como OK.
