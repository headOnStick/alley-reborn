# API Reference - Alley Platform

**Última atualização**: 2025-10-10

> Documentação completa dos endpoints da API do backend Alley Hooper

**Este ficheiro documenta**:
- 138 endpoints da API organizados em 19 categorias
- Métodos HTTP e paths de cada endpoint
- Estrutura da API backend que alimenta o portal
- Relação entre API e schema de dados

**Ficheiro original**: `/technical-resources/alley-hooper-api-collection.json` (Postman Collection)

**Para contexto relacionado**, ver:
- **Data Schema**: `/01-context/data-schema.md` (entidades e KPIs)
- **Portal Audit**: `/03-portal-audit/sitemap.md` (como frontend usa a API)
- **Platform Overview**: `/01-context/platform-overview.md`

---

## Visão Geral

**Total de Endpoints**: 138
**Total de Categorias**: 19

**Base URL**:
- **Development**: `http://localhost`
- **Production**: `https://api.alley-hooper.com`

**Autenticação**: Bearer Token (JWT obtido via `/api/login`)

---

## Estrutura da API

### 1. Authentication (3 endpoints)

#### Login
- **Método**: POST
- **Path**: `/api/login`
- **Descrição**: Autenticação de usuário, retorna JWT token
- **Body**: `{ "email": "...", "password": "..." }`

#### Recover Password
- **Método**: POST
- **Path**: `/api/recover`
- **Descrição**: Solicitar recuperação de senha

#### Logout
- **Método**: POST
- **Path**: `/api/logout`
- **Descrição**: Invalidar token de autenticação

---

### 2. Password Reset (2 endpoints)

#### Send Reset Link
- **Método**: POST
- **Path**: `/api/password/forgot`
- **Descrição**: Enviar link de reset de senha por email

#### Reset Password
- **Método**: POST
- **Path**: `/api/password/reset`
- **Descrição**: Efetuar reset de senha com token

---

### 3. Core Data Management (20 endpoints)

Gerenciamento das entidades principais: Posts, Comments, Authors.

#### 3.1 Posts (9 endpoints)

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Save Post | POST | `/api/post` | Salvar post do Instagram |
| Save One Post | POST | `/api/save-one-post` | Salvar um post individual |
| Save Many Posts | POST | `/api/save-many-posts` | Salvar múltiplos posts em batch |
| Check Post Exists | POST | `/api/post-exists` | Verificar se post já existe |
| Get Post | GET | `/api/get-post/:shortcode` | Obter post por shortcode |
| Get Posts | GET | `/api/get-posts` | Listar posts com filtros |
| Save Post Analysis | POST | `/api/save-post-analysis` | Salvar análise de IA do post |
| Check Has Comments | POST | `/api/has-comments` | Verificar se post tem comentários |
| Get Posts Metrics | GET | `/api/channel/posts-metrics` | Métricas agregadas de posts |

#### 3.2 Comments (4 endpoints)

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Save Comment | POST | `/api/comment` | Salvar comentário |
| Save Apify Comment | POST | `/api/save-apify-comment` | Salvar comentário via scraper Apify |
| Save Comment Analysis | POST | `/api/save-comment-analysis` | Salvar análise de IA do comentário |
| Check Comment Exists | POST | `/api/comment-exists` | Verificar se comentário já existe |

#### 3.3 Authors (7 endpoints)

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Save Author | POST | `/api/author` | Salvar autor (comentador) |
| Save Author Profile | POST | `/api/save-author-profile` | Salvar perfil do autor |
| Save Follower Profile | POST | `/api/save-follower-profile` | Salvar perfil de seguidor |
| Save Author Analysis | POST | `/api/save-author-analysis` | Salvar análise de IA do autor |
| Check Author Exists | POST | `/api/author-exists` | Verificar se autor já existe |
| Get Authors | GET | `/api/get-authors` | Listar autores com filtros |
| Get Incomplete Authors | GET | `/api/get-incomplete-authors` | Obter autores com análise incompleta |

---

### 4. Image Management (2 endpoints)

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Upload Image from URL | POST | `/api/upload-image-from-url` | Upload de imagem para análise de IA |
| Get Image by URL | GET | `/api/get-image-by-url` | Obter imagem processada |

---

### 5. Reference Tables (7 endpoints)

Tabelas de referência para taxonomias (usado em filtros e dropdowns).

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Get Player Data | GET | `/api/get-player` | Lista de jogadores |
| Get Sport Data | GET | `/api/get-sport` | Lista de esportes |
| Get Gender Data | GET | `/api/get-gender` | Lista de gêneros (3 tipos) |
| Get Age Interval Data | GET | `/api/get-age-interval` | Lista de intervalos de idade |
| Get Countries Data | GET | `/api/get-countries` | Lista de países |
| Get Industries Data | GET | `/api/get-industries` | Lista de indústrias (25 tipos) |
| Get Emotions Data | GET | `/api/get-emotions` | Lista de emoções (25 tipos) |

---

### 6. Entity Creation (3 endpoints)

Criação de entidades de referência (players, teams, brands).

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Create Player | POST | `/api/create/player` | Criar novo jogador |
| Create Team | POST | `/api/create/team` | Criar novo time |
| Create Brand | POST | `/api/create/brand` | Criar nova marca |

---

### 7. Dashboard Analytics (14 endpoints)

Endpoints usados pela página **Dashboard** (`/dashboard`).

| Endpoint | Método | Path | Uso no Portal |
|----------|--------|------|---------------|
| Get Dashboard Filters | GET | `/api/dashboard/get-filters` | Filtros do dashboard (channels, date range) |
| Get Dashboard Data | GET | `/api/dashboard/data` | Overview multi-canal |
| Get Interaction Metrics | GET | `/api/dashboard/interaction-metrics` | Métricas de interação |
| Get Sentiment Analysis | GET | `/api/dashboard/sentiment-analysis` | Sentiment breakdown |
| Get Audience Gender | GET | `/api/dashboard/audience-gender` | Demographics - Gender |
| Get Audience Age Interval | GET | `/api/dashboard/audience-age-interval` | Demographics - Age |
| Get Audience Ethnicity | GET | `/api/dashboard/audience-ethnicity` | Demographics - Ethnicity |
| Get Audience Location | GET | `/api/dashboard/audience-location` | Demographics - Location |
| Get Audience Job | GET | `/api/dashboard/audience-job` | Psychographics - Industry |
| Get Content Performance | GET | `/api/dashboard/content-performance` | Performance de conteúdo |
| Get Top Topics | GET | `/api/dashboard/top-topics` | Tópicos mais mencionados |
| Get Engagement Trend | GET | `/api/dashboard/engagement-trend` | Evolução de engagement |
| Get Discovery Funnel | GET | `/api/dashboard/discovery-funnel` | Funil de descoberta |
| Buzzer API | GET | `/api/dashboard/buzzer/data` | Alertas e notificações |

---

### 8. Instagram Dashboard (11 endpoints)

Análise específica de Instagram (não parece usado no portal atual).

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Get Instagram Filters | GET | `/api/dashboard/instagram/get-filters` | Filtros Instagram |
| Get Instagram Data | GET | `/api/dashboard/instagram/data` | Overview Instagram |
| Get Instagram KPIs | GET | `/api/dashboard/instagram/kpis` | KPIs agregados |
| Get Instagram Content Types | GET | `/api/dashboard/instagram/content-types` | Tipos de conteúdo |
| Get Instagram Top Topics | GET | `/api/dashboard/instagram/top-topics` | Tópicos principais |
| Get Instagram Emotions | GET | `/api/dashboard/instagram/emotions` | Análise emocional |
| Get Instagram Engagement Trend | GET | `/api/dashboard/instagram/engagement-trend` | Tendência de engagement |
| Get Instagram Comments | GET | `/api/dashboard/instagram/comments` | Análise de comentários |
| Get Instagram Hashtags | GET | `/api/dashboard/instagram/hashtags` | Análise de hashtags |
| Get Instagram Influencers | GET | `/api/dashboard/instagram/influencers` | Top influenciadores |
| Get Instagram Timing | GET | `/api/dashboard/instagram/timing` | Análise de timing |

---

### 9. Channel Analytics (5 endpoints)

Endpoints usados pela página **Channel Detail** (`/dashboard/channel/{id}`).

| Endpoint | Método | Path | Uso no Portal |
|----------|--------|------|---------------|
| Get Top Posts | GET | `/api/channel/top-posts` | Channel Detail → Post tab |
| Get Top Authors | GET | `/api/channel/top-authors` | Channel Detail → Community tab |
| Get Content Types | GET | `/api/channel/content-types` | Análise de tipos de conteúdo |
| Get Last Post | GET | `/api/channel/last-post` | Último post do canal |
| Get Lifestyle Analysis | GET | `/api/channel/lifestyle` | Análise de lifestyle (psychographics) |

---

### 10. Comments Overview (3 endpoints)

Endpoints aparentemente não usados no portal atual (página dedicada a Comments não existe).

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Get Top Posts by Comments | GET | `/api/comments/overview/top-posts` | Posts com mais comentários |
| Get Sentiment Analysis | GET | `/api/comments/overview/sentiment-analysis` | Análise de sentiment |
| Get Engagement Trend | GET | `/api/comments/overview/engagement-trend` | Tendência de engagement |

---

### 11. User Management (8 endpoints)

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Get Profile (Legacy) | POST | `/api/profile` | Obter perfil do usuário (legacy) |
| Get User Profile | GET | `/api/users/me` | Obter perfil do usuário (atual) |
| Update Profile | PATCH | `/api/users/me` | Atualizar perfil |
| Upload Avatar | POST | `/api/users/me/avatar` | Upload de avatar |
| Delete Avatar | DELETE | `/api/users/me/avatar` | Deletar avatar |
| Change Password | POST | `/api/change-password` | Alterar senha |
| Delete User Account | DELETE | `/api/users/delete` | Deletar conta |
| Get User Accounts | GET | `/api/account` | Obter contas do usuário |

---

### 12. Community (2 endpoints)

Endpoints usados no portal (possivelmente Community page).

| Endpoint | Método | Path | Uso no Portal |
|----------|--------|------|---------------|
| Get My Channels | GET | `/api/community/my-channels` | Lista de canais do usuário |
| Get Social Media Reach | GET | `/api/community/social-media-reach` | Alcance em redes sociais |

---

### 13. Business Profile (2 endpoints)

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Get Business Profile Analytics | GET | `/api/business-profile/profile` | Analytics do perfil de negócio |
| Get Business Metrics | GET | `/api/business-profile/metrics` | Métricas de negócio |

---

### 14. Frontend Widgets (6 endpoints)

Sistema de widgets customizáveis (CRUD completo).

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Dynamic Widget | POST | `/api/widget/dynamic` | Widget dinâmico |
| Get All Widgets | GET | `/api/widget` | Listar widgets |
| Create Widget | POST | `/api/widget` | Criar widget |
| Get Widget | GET | `/api/widget/:id` | Obter widget por ID |
| Update Widget | PUT | `/api/widget/:id` | Atualizar widget |
| Delete Widget | DELETE | `/api/widget/:id` | Deletar widget |

---

### 15. Chat Messages (5 endpoints)

Sistema de chat/mensagens (CRUD completo).

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Get All Chat Messages | GET | `/api/chat-messages` | Listar mensagens |
| Create Chat Message | POST | `/api/chat-messages` | Criar mensagem |
| Get Chat Message | GET | `/api/chat-messages/:id` | Obter mensagem por ID |
| Update Chat Message | PUT | `/api/chat-messages/:id` | Atualizar mensagem |
| Delete Chat Message | DELETE | `/api/chat-messages/:id` | Deletar mensagem |

---

### 16. Analytics (30 endpoints)

Endpoints usados pela página **Community** (`/analytics`) - Demographics e Psychographics.

#### 16.1 Filtros
- **Get Analytics Filters**: `GET /api/analytics/get-filters`

#### 16.2 Audience Analytics (4 endpoints)

| Endpoint | Método | Path | Uso no Portal |
|----------|--------|------|---------------|
| Get Audience Age Gender | GET | `/api/analytics/audience-age-gender` | Community → Overview tab |
| Get Audience Industries | GET | `/api/analytics/audience-industries` | Community → Industry tab |
| Get Audience Emotions | GET | `/api/analytics/get-audience-emotions` | Community → Emotions tab |
| Get Audience Emotion Categories | GET | `/api/analytics/get-audience-emotion-categories` | Community → Emotions tab |

#### 16.3 Brands Tab Analytics (5 endpoints)

| Endpoint | Método | Path | Uso no Portal |
|----------|--------|------|---------------|
| Get Item Categories | GET | `/api/analytics/get-item-categories` | Community → Brands tab (items detectados) |
| Get Top Items | GET | `/api/analytics/get-top-items` | Community → Brands tab |
| Get Brand Affinity | GET | `/api/analytics/get-brand-affinity` | Community → Brands tab |
| Get Brand Categories | GET | `/api/analytics/get-brand-categories` | Community → Brands tab |
| Get Brand Graph | GET | `/api/analytics/get-brand-graph` | Community → Brands tab (visualização) |

#### 16.4 Reference Data (20 endpoints)

Taxonomias para filtros e dropdowns:
- Gender, Age Intervals, Sport, State, City
- Post Categories, Media Type
- Brand, Item, Celebrity
- Ethnicity, Lifestyle, Status Class, Industry
- Location, Country, Continent
- Player, Team

---

### 17. Content Topics (12 endpoints)

Endpoints usados pela página **Channel** (`/channel`) - Análise de conteúdo.

| Endpoint | Método | Path | Uso no Portal |
|----------|--------|------|---------------|
| Get Topic Distribution | GET | `/api/content/get-topic-distribution` | Channel → Topics tab |
| Get Top Hashtags | GET | `/api/content/get-hashtag-top` | Channel → Hashtags tab |
| Get Emerging Hashtags | GET | `/api/content/get-hashtag-emerging` | Channel → Hashtags tab |
| Get Hashtag Metrics | GET | `/api/content/get-hashtag-metrics` | Channel → Hashtags tab |
| Get Hashtag Combinations | GET | `/api/content/get-hashtag-combinations` | Channel → Hashtags tab |
| Get Hashtag Evolution | GET | `/api/content/get-hashtag-evolution` | Channel → Hashtags tab |
| Get Timing Metrics | GET | `/api/content/get-timing-metrics` | Channel → Timing tab |
| Get Timing Times | GET | `/api/content/get-timing-times` | Channel → Timing tab |
| Get Timing Performance | GET | `/api/content/get-timing-performance` | Channel → Timing tab |
| Get Timing Frequency | GET | `/api/content/get-timing-frequency` | Channel → Timing tab |
| Get Timing Lifespan | GET | `/api/content/get-timing-lifespan` | Channel → Timing tab |
| Get Topics Evolution | GET | `/api/content/get-topics-evolution` | Channel → Topics tab |

---

### 18. System (2 endpoints)

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Ping | POST | `/api/ping` | Health check |
| Version | GET | `/api/version` | Versão da API |

---

### 19. Webhooks (1 endpoint)

| Endpoint | Método | Path | Descrição |
|----------|--------|------|-----------|
| Bitbucket Webhook | POST | `/api/bitbucket-webhook` | Webhook de deploy automático |

---

## Mapeamento: API → Portal

### Dashboard (`/dashboard`)
**Endpoints usados**:
- `/api/dashboard/get-filters`
- `/api/dashboard/data`
- `/api/dashboard/interaction-metrics`
- `/api/dashboard/sentiment-analysis`
- `/api/dashboard/audience-*` (gender, age, ethnicity, location, job)
- `/api/dashboard/content-performance`
- `/api/dashboard/top-topics`
- `/api/dashboard/engagement-trend`

### Channel Detail (`/dashboard/channel/{id}`)
**Endpoints usados**:
- `/api/channel/top-posts` (Post tab)
- `/api/channel/top-authors` (Community tab)
- `/api/channel/content-types`
- Possivelmente `/api/dashboard/audience-*` para demographics

### Community (`/analytics`)
**Endpoints usados**:
- `/api/analytics/get-filters`
- `/api/analytics/audience-age-gender` (Overview tab)
- `/api/analytics/audience-industries` (Industry tab)
- `/api/analytics/get-audience-emotions` (Emotions tab)
- `/api/analytics/get-item-categories` (Brands tab)
- `/api/analytics/get-top-items` (Brands tab)
- `/api/analytics/get-brand-*` (Brands tab)

### Channel (`/channel`)
**Endpoints usados**:
- `/api/content/get-topic-distribution` (Topics tab)
- `/api/content/get-hashtag-*` (Hashtags tab - 6 endpoints)
- `/api/content/get-timing-*` (Timing tab - 5 endpoints)

### Posts (`/posts`)
**Endpoints usados**:
- `/api/get-posts` (listagem)
- `/api/channel/posts-metrics` (métricas)
- Possivelmente `/api/channel/top-posts`

### Alerts (`/alerts`)
**Endpoints usados**:
- `/api/dashboard/buzzer/data` (possivelmente)
- Endpoint específico não identificado

---

## Endpoints Não Usados no Portal Atual

### 1. Instagram Dashboard (11 endpoints)
Categoria inteira `/api/dashboard/instagram/*` não parece estar em uso no portal staging atual.

**Possíveis razões**:
- Feature desativada
- Em desenvolvimento
- Apenas em produção

### 2. Comments Overview (3 endpoints)
Categoria `/api/comments/overview/*` não tem página correspondente no portal.

**Implicação**: Dados de comments existem mas não têm visualização dedicada.

### 3. Business Profile (2 endpoints)
Categoria `/api/business-profile/*` não identificada no portal.

### 4. Chat Messages & Widgets
Possivelmente features internas ou admin-only.

---

## Análise de Cobertura

### KPIs no Schema vs API Disponível

**✅ Bem Coberto**:
- Demographics (gender, age, ethnicity, location) - múltiplos endpoints
- Post performance (likes, comments, engagement) - endpoints dedicados
- Channel overview - endpoints específicos

**⚠️ Cobertura Parcial**:
- **Emotional Analysis** - Apenas 2 endpoints (`get-audience-emotions`, `get-audience-emotion-categories`)
  - Schema tem 25 emoções específicas
  - API parece retornar apenas categorias agregadas
- **Entity Recognition** - Endpoints de players/teams existem mas uso não claro
- **Brand & Item Detection** - 5 endpoints mas integração com portal limitada

**❌ Possivelmente Ausente**:
- **Call to Action detection** - Nenhum endpoint identificado
- **Post Categories** (9 tipos) - Endpoint existe (`get-post-categories`) mas uso não claro
- **Content Moderation** (spam, toxicity) - Nenhum endpoint identificado
- **Following List Analysis** - Nenhum endpoint identificado

---

## Oportunidades Identificadas

### Para Sprint 4 (Gap Analysis)

1. **API Existente mas Sub-Usada**:
   - Instagram Dashboard (11 endpoints) não usado
   - Comments Overview (3 endpoints) não usado
   - Brand Analytics (5 endpoints) pouco integrados

2. **Features Possíveis com API Atual**:
   - Página dedicada a análise de comentários
   - Dashboard alternativo Instagram-focused
   - Drill-down de brands e items detectados

3. **Gaps na API**:
   - Nenhum endpoint para Call to Action detection
   - Nenhum endpoint para Content Moderation
   - Nenhum endpoint para Following List Analysis
   - Nenhum endpoint para Emotional Volatility Index

4. **Inconsistências**:
   - Schema documenta 165 KPIs
   - API tem 138 endpoints (alguns retornam múltiplos KPIs)
   - Portal mostra ~50-60 KPIs
   - **Pergunta**: Quais dados existem na BD mas não têm endpoint?

---

## Próximos Passos

### Sprint 3
Processar reuniões para identificar quais endpoints/KPIs são realmente importantes para clientes.

### Sprint 4
- Cruzar este ficheiro com `/01-context/data-schema.md`
- Identificar dados na BD sem endpoint
- Identificar endpoints sem uso no portal
- Priorizar gaps por valor de negócio

### Sprint 5
Propor redesenho que:
- Aproveite endpoints sub-usados (Instagram Dashboard, Comments Overview)
- Crie páginas para endpoints órfãos
- Priorize KPIs com base em feedback de clientes

---

## REFERÊNCIAS CRUZADAS

**Para entender os dados**:
- `/01-context/data-schema.md` - Schema da base de dados

**Para entender o portal**:
- `/03-portal-audit/sitemap.md` - Como frontend consome a API

**Para código fonte**:
- Ver `/01-context/resources.md` para Git do frontend
- Backend repository: TBD

---

**Este ficheiro é referência crucial para entender capabilities técnicas da plataforma. Consultar quando analisar funcionalidades do portal ou propor novos features.**

**Postman Collection completa**: `/technical-resources/alley-hooper-api-collection.json`
