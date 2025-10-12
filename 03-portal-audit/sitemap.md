# Sitemap - Portal Alley

## Metadata
- **Data de Análise**: 2025-10-10
- **Versão do Portal**: v0.1.27-19
- **Método**: Navegação com Playwright + Análise manual
- **Status**: Em progresso (Sprint 2)

---

## Estrutura de Navegação Principal

### Sidebar Menu (Sempre visível)

```
┌─────────────────────────┐
│ Alley Hooper Logo       │
├─────────────────────────┤
│ ● Dash                  │
│   Community             │
│   Content               │
│   Comments              │
│   Posts                 │
├─────────────────────────┤
│ [Help] [Notif] [Set] [A]│
│ v0.1.27-19              │
└─────────────────────────┘
```

**Itens do Menu**:
1. **Dash** → `/dashboard`
2. **Community** → `/analytics`
3. **Content** → `/content`
4. **Comments** → `/comments`
5. **Posts** → `/posts`

**Utilitários** (footer do sidebar):
- **Help** (botão)
- **Notifications** (botão)
- **Settings** (botão)
- **User Avatar** (botão - "A" para André Rocha)
- **Version**: v0.1.27-19

---

## Header Global (Todas as páginas)

**Componentes**:
- **Add Channel** (botão + ícone)
- **Channel Selector** (dropdown com "U" - user selecionado)

---

## Páginas Principais

### 1. Dashboard (`/dashboard`)

**URL**: `/dashboard`
**Título**: Dash

#### Estrutura da Página

##### Filtros Globais
- **Date Range Picker**: "01 Aug 2025 - 31 Aug 2025"
- **Channel Selector**: Dropdown com canais disponíveis

##### Seção: Channel Overview (Top Cards)
**Channels disponíveis**:
1. **nba**
   - 7.1K Posts
   - 90.9M Followers
   - 763.5M Likes
   - Sentiment indicators (Promoter, Detractors, Neutral)
   - Score: 6.3

2. **celtics**
   - 4.9K Posts
   - 8.3M Followers
   - 295.4M Likes
   - Score: 6.1

3. **tonywells99**
   - 0 Posts
   - 721 Followers
   - 0 Likes
   - Score: 0

##### Seção: Community

**Community Size**
- Total: 21.3M (-52.6%)
- Lista de channels com métricas

**Engagement Trends**
- Gráfico de linha (time series)
- Período: 01/08 - 30/08

**Demographics** (3 cards horizontais):

1. **Gender**
   - Male: 87.8%
   - Female: 12.2%
   - Formato: Donut chart

2. **Age Range**
   - Young Adult: 68.8%
   - Adult: 23.6%
   - Child: 4.2%
   - Teenager/Adolescent: 3.1%
   - Senior/Elderly: 0.3%
   - Formato: Donut chart

3. **Location**
   - United States: 86.8%
   - Brazil: 5.5%
   - Canada: 3.7%
   - Germany: 2.0%
   - Italy: 2.0%
   - Formato: Donut chart

**✨ Highlights**
- Card: "Comment Activity"
- AI-generated insight
- Tip suggestion
- "✨ Ask Alley" button

##### Seção: Business Profile

**Channel Selector**: "Select Channel ▼"

**Selected Channel Card** (exemplo: nba):
- Header com métricas principais (Posts, Followers, Likes)
- **Alerts & Risk Flags** (5 tipos de alerts com counters)

**Métricas Detalhadas** (grid layout):

1. **Sentiment Analysis**
   - Score médio: 6.0
   - Visual: Emoji indicators

2. **Top 5 Posts**
   - Lista de posts com métricas:
     - Caption
     - Date
     - Likes
     - Comments
     - Engagement total

3. **Main Topics**
   - Word cloud interativo
   - Top 5 topics com contadores

4. **Lifestyle**
   - 5 categorias visualizadas

5. **Time Analysis**
   - Activity Peak: 21:00
   - Best Day: Tuesday
   - Ícones visuais

6. **Top Influencers**
   - Top 5 comentadores mais ativos
   - Foto de perfil + username + count

7. **Hashtags**
   - Top hashtags usados
   - Ranking visual

**✨ Highlights**
- Card: "Peak Performance"
- AI-generated insight
- Tip suggestion
- "✨ Ask Alley" button

#### KPIs Identificados
- Community Size (21.3M)
- Gender distribution (%)
- Age range distribution (%)
- Location distribution (%)
- Sentiment Score (6.0)
- Posts metrics (likes, comments, engagement)
- Time metrics (peak hour, best day)
- Top influencers
- Top hashtags
- Alerts & Risk Flags

---

### 2. Channel Detail (`/dashboard/channel/{id}`)

**URL**: `/dashboard/channel/{id}` (ex: `/dashboard/channel/1` para NBA)
**Título**: Channel Detail
**Acesso**: Através do Dashboard ou URL direta

#### Estrutura da Página

##### Header de Canal
- **Channel Info Card**:
  - Avatar do canal (ex: nba)
  - Nome do canal (@nba)
  - Métricas permanentes:
    - 7.1K Posts
    - 90.9M Followers
    - 763.5M Likes

##### Seção: Period in Analysis
**Período**: (30 days)
**Métricas do Período**:
1. **No. Posts**: 2 (+-64.3% vs previous period)
2. **Likes**: 21.8M
3. **Comments**: 73.8K
4. **Volume Authors**: 39.3K

##### Seção: Alerts & Risk Flags
**5 tipos de alerts identificados**:
1. **Sync Score Drop** (badge "1")
   - "2 relationships with sync score drop > 40 points"
2. **Confusion Not Acknowledged** (badge "1")
   - "Post with dominant emotion 'confusion' not acknowledged by any teammate"
3. **Repeated Silence** (badge "2" - 3 instâncias)
   - "Repeated silence from player towards Brand X campaigns" (3 alerts similares)

##### Seção: Summary Cards (Grid 2x3)

**Row 1**:
1. **Authors**: 39.3k total authors
2. **Followers Engagement**: 24.06% (90.9M seguidores, 21.9M interações)
3. **Posts**: 2 total

**Row 2**:
4. **CTS**: 5.96 (Community Trust Score)
5. **Content**: Reel - 0 | Photo - 0 | Carousel - 2
6. **Dominant Emotion**: 😢 51.9% negative

#### Tabs (3 tabs totais)

##### Tab 1: Community (Demographics and top authors) ✓ ANALISADA

**Seção: Demographics** (3 donut charts):

1. **Gender**
   - Male: 87.8%
   - Female: 12.2%
   - Formato: Donut chart

2. **Location** (Top 5):
   - United States: 86.9%
   - Brazil: 4.9%
   - Canada: 3.8%
   - India: 1.8%
   - Germany: 1.3%
   - Formato: Donut chart

3. **Age Groups** (Top 5):
   - Young Adult: 68.7%
   - Adult: 23.5%
   - Child: 4.2%
   - Teenager/Adolescent: 3.3%
   - Senior/Elderly: 0.3%
   - Formato: Donut chart

**Seção: Pet Friendly**
- Dogs: 51.6%
- Cats: 48.4%

**Seção: Lifestyle** (Top 10):
1. Cultural/Creative: 36.2%
2. Family-Oriented: 33.3%
3. Fitness-Focused: 7.2%
4. Tech-Savvy: 5.8%
5. Eco-Friendly: 4.3%
6. Luxury-Oriented: 4.3%
7. Adventurous: 2.9%
8. Minimalist: 2.9%
9. Health-Conscious: 1.4%
10. Career-Driven: 1.4%

**Seção: Top Authors** (tabela com 5 colunas):
- Colunas: RANK, AUTHOR, LAST COMMENT, DOMINANT EMOTION, EMOTION, FREQUENCY
- Dados de top 5 comentadores mais ativos no canal
- Exemplo: #1 - @author1 - "32 min ago" - 😊 (Joy) - 92% - 52 comments

**Screenshot**: `channel-community.png`

##### Tab 2: Post (Top posts and content types) ✓ ANALISADA

**Seção: Top Posts** (tabela com 9 colunas):
- Colunas: IMAGE, DATE/TIME, POST, TYPE, DOMINANT EMOTION, GENERAL SENTIMENT, LIKES, COMMENTS, ENGAGEMENT
- Lista dos top 15 posts do canal com detalhes completos
- Exemplos:
  1. "Great seats.. better moment! ☺️" - 2023-02-12 01:50 - Photo - 😊 Positiva - Positivo - 2440.1K likes - 8.0K comments - 2.7% engagement
  2. "😱 @lakers • #NBAMediaDay" - 2024-09-30 20:11 - Photo - 😊 Positiva - Positivo - 1910.3K likes - 11.0K comments - 2.1% engagement
  3. "🤯 LeBron's reaction! 💥" - 2023-10-05 22:02 - Photo - 😊 Positiva - Positivo - 1725.0K likes - 7.5K comments - 1.9% engagement

**Seção: Content Types Breakdown** (tabela com 7 colunas):
- Colunas: CONTENT TYPE, NO. OF POSTS, FOLLOWERS ENGAGEMENT, TOTAL INTERACTIONS, DOMINANT EMOTION, AVERAGE SENTIMENT, AVERAGE CTS
- 9 categorias de conteúdo identificadas:

1. **Game Highlights & Player Performances**
   - 133 posts
   - 12.9% engagement
   - 11679.2K interactions
   - 😊 Admiração
   - Muito Positivo
   - 0.0 CTS

2. **Throwbacks & Historical Moments**
   - 29 posts
   - 4.7% engagement
   - 4263.3K interactions
   - 😐 Neutro
   - Positivo
   - 0.0 CTS

3. **Entertainment & Celebrity Appearances**
   - 27 posts
   - 3.5% engagement
   - 3140.8K interactions
   - 😐 Neutro
   - Neutro
   - 0.0 CTS

4. **Breaking News & Announcements**
   - 7 posts
   - 0.5% engagement
   - 419.4K interactions
   - 😟 Descontentamento
   - Negativo
   - 0.0 CTS

5. **Event & Game Promotions**
   - 10 posts
   - 0.4% engagement
   - 389.9K interactions
   - 😟 Descontentamento
   - Negativo
   - 0.0 CTS

6. **Merchandise & Promotions**
   - 3 posts
   - 0.4% engagement
   - 382.0K interactions
   - 😟 Descontentamento
   - Negativo
   - 0.0 CTS

7. **Fan Engagement & Memes**
   - 4 posts
   - 0.4% engagement
   - 343.1K interactions
   - 😟 Descontentamento
   - Negativo
   - 0.0 CTS

8. **Inspirational & Motivational Posts**
   - 2 posts
   - 0.3% engagement
   - 322.3K interactions
   - 😟 Descontentamento
   - Negativo
   - 0.0 CTS

9. **Stat Updates & League Standings**
   - 3 posts
   - 0.3% engagement
   - 297.7K interactions
   - 😟 Descontentamento
   - Negativo
   - 0.0 CTS

**Screenshot**: `channel-post.png`

##### Tab 3: Alerts (Alert management for channel) ✓ ANALISADA

**Seção: Alerts Table** (tabela com 7 colunas):
- Colunas: DATA/HORA, TIPO DE ALERTA, DESCRIÇÃO, SEVERIDADE, AÇÃO RECOMENDADA, ESTADO, AÇÕES

**Alerts Identificados** (3 alerts históricos):

1. **Emoção negativa em alta** (2024-05-11 09:23)
   - Descrição: "Post motivacional teve +180% de média semanal"
   - Severidade: Alta
   - Ação Recomendada: Revisar linha editorial
   - Estado: Closed

2. **Emoção negativa em alta** (2024-05-11 09:23)
   - Descrição: "Bastidores: concentração antes do jogo"
   - Severidade: Média
   - Ação Recomendada: Promover conteúdo similar
   - Estado: Done

3. **Pico de engagement** (2024-05-11 09:23)
   - Descrição: "14 perfis com padrão repetido em 1 post"
   - Severidade: Alta
   - Ação Recomendada: Ativar filtro de moderação
   - Estado: Open

**Estados de Alerts**:
- Open: Alerts ativos que precisam de ação
- Done: Alerts resolvidos com ação tomada
- Closed: Alerts fechados/arquivados

**Screenshot**: `channel-alerts.png`

#### KPIs Identificados (Channel Detail)
- Channel metrics permanentes (Posts, Followers, Likes)
- Period metrics (Posts, Likes, Comments, Volume Authors)
- Alerts & Risk Flags (5 tipos)
- Demographic distribution (Gender, Location, Age)
- Lifestyle categories (10 categorias)
- Pet Friendly distribution
- Top Authors ranking
- Top Posts ranking (15 posts)
- Content Types breakdown (9 categorias)
- CTS Score (5.96)
- Dominant Emotion (51.9% negative)
- Followers Engagement (24.06%)

#### Observações Técnicas

**APIs Identificadas**:
- `GET /api/business-profile/metrics` (period metrics)
- `GET /api/channel/top-authors` (top commenters)
- `GET /api/channel/posts-metrics` (top posts table)
- `GET /api/channel/content-types` (content categories breakdown)
- Demographics data (gender, location, age groups)
- Lifestyle data
- Pet Friendly data

**Diferença vs Dashboard**:
- Dashboard mostra overview de múltiplos canais
- Channel Detail mostra análise profunda de 1 canal específico
- Maior granularidade em demographics e content types
- Histórico de alerts específicos do canal
- Top Authors table detalhada
- Top Posts table expandida (15 vs 5)

---

### 3. Community (`/analytics`)

**URL**: `/analytics`
**Título**: Community

#### Filtros Globais
- **Date Range Picker**: "01 Aug 2025 - 31 Aug 2025"
- **Channel Filter**: "All channels"
- **Segment Filter**: "All segments" ⭐ **[Ver análise completa em `/03-portal-audit/segmentation-filters.md`]**

#### Tabs (6 tabs totais)

##### Tab 1: Interactions (Engagement metrics) ✓ ANALISADA

**Seção: Interaction Metrics** (6 cards em grid):

1. **Total Interactions**
   - Valor: 23.7M
   - Variação: +15.2% vs previous period
   - Descrição: Total interactions in period

2. **Total Likes**
   - Valor: 23.6M
   - Variação: +5.7%
   - Descrição: Accumulated likes in period

3. **Comments**
   - Valor: 80.9K
   - Variação: 0.0%
   - Descrição: Comments received

4. **Publications**
   - Valor: 2
   - Variação: -2.1%
   - Descrição: Posts published in period

5. **Engagement Rate**
   - Valor: 23.9%
   - Descrição: Average follower engagement

6. **Followers**
   - Valor: 99.2M
   - Variação: 0.0%
   - Descrição: Total followers

**Seção: Top Authors**
- Lista de top 5 comentadores mais ativos
- Por cada autor:
  - Ranking (#1, #2, etc)
  - Foto de perfil
  - Nome + @username
  - Número de comments
  - Main Emotion (Joy, N/A, etc)
  - Nível de atividade (alta)

**Seção: Top Performing Posts**
- Lista de top 5 posts por engagement
- Por cada post:
  - Ranking (#1, #2, etc)
  - Caption do post
  - Views (N/A para alguns)
  - Likes
  - Comments
  - Engagement %

##### Tab 2: Audience (Demographics and segments) ✓ ANALISADA

**Seção: Audience Overview** (4 cards):
1. **Total Followers**: 99.2M (+2.3%)
2. **Profiles Analyzed**: 6.2K (100%)
3. **Active Channels**: 3
4. **Male Dominance**: 87.3%

**Seção: Audience Demographics**:
- **Gender Distribution**: Male 87.3%, Female 12.7%
- **Age Distribution**: Young Adult 55.3%, Unknown 20.3%, Adult 18.9%, Child 2.9%, Teen 2.3%
- **Geographic Location**: US 80.3%, Brazil 5.2%, Canada 3.5%, Germany 1.7%
- **Ethnicity**: African 56%, Caucasian 29.7%, Latino 7.6%, Asian 3.8%

**Seção: Detailed Segmentation**:
- **Lifestyles**: Cultural/Creative 66.7%, Family-Oriented 33.3%
- **Industries**: Arts/Entertainment 63.8%, Medical/Health 7.7%, Business/Finance 5.4%

**Screenshot**: `community-audience.png`

##### Tab 3: Sentiments (Emotional analysis) ✓ ANALISADA

**Seção: Overview** (3 cards):
1. **Average CTS Score**: 6.0/10 (Community Trust Score)
2. **Comments Analyzed**: 393 (complete profiles)
3. **Trend**: → Stable

**Seção: Sentiment Distribution**:
- **Positive Sentiment**: 20.6%
- **Neutral Sentiment**: 27.5%
- **Negative Sentiment**: 51.9%

**Seção: Detailed Emotional Analysis**:
- Happiness & Enthusiasm: 58.1%
- Anger & Conflict: 20.4%
- Sadness & Discouragement: 14.2%
- Indecision & Reflection: 6.8%
- Social Connection: 0.6%

**Seção: Top Posts by Sentiment** (3 posts com breakdown de sentiment)

**Seção: Spam and Toxicity Detection**:
- Total Comments: 65.4K
- Spam Filtered: 15
- Spam Rate: 0.0%
- Toxicity Rate: 0.0%

**Screenshot**: `community-sentiments.png`

##### Tab 4: Content (Performance by type) ✓ ANALISADA

**Seção: Content Types** (9 categorias):
1. Game Highlights & Player Performances - 149 posts (56%) - Engagement: 12.3%, Views: 12.2M
2. Throwbacks & Historical Moments - 39 posts (15%) - Engagement: 4.8%, Views: 4.8M
3. Entertainment & Celebrity Appearances - 37 posts (14%) - Engagement: 3.6%, Views: 3.5M
4. Breaking News & Announcements - 16 posts (6%)
5. Fan Engagement & Memes - 7 posts (3%)
6. Event & Game Promotions - 10 posts (4%)
7. Merchandise & Promotions - 3 posts (1%)
8. Inspirational & Motivational Posts - 2 posts (1%)
9. Stat Updates & League Standings - 3 posts (1%)

**Seção: Performance Metrics**:
- Total Views: 10.8M
- Average Engagement per Post: 1.4M

**Seção: Top 5 Performing Content** (posts com likes, comments, engagement %)

**Seção: Most Used Hashtags**:
- #lgk - 50% (1 use)
- #shameonyoujb - 50% (1 use)

**Seção: Brand Mentions**:
- Nike: 142 mentions (+15%, Positive)
- Gatorade: 89 mentions (+8%, Positive)
- NBA: 234 mentions (+12%, Positive)
- ESPN: 67 mentions (+3%, Neutral)

**Screenshot**: `community-content.png`

##### Tab 5: Geography (Regional distribution) ✓ ANALISADA

⚠️ **Nota**: Este tab mostra "Coming Soon: Complete Geographic Analysis" - dados são sample/parciais.

**Seção: Geographic Distribution**:
- Interactive World Map (Under development)
- **Top Countries by Audience**: Unknown 97.7%, United States 1.5%, Brazil 0.1%, Canada 0.1%
- Total countries represented: 81
- Total followers: 0.0M

**Seção: Countries with Largest Audience** (Top 10 com métricas de engagement)

**Seção: Top Cities**:
- Unknown/Unknown: 41.2K
- New York City, US: 74
- Los Angeles, US: 35
- Chicago, US: 28
- Houston, US: 23
- Boston, US: 18
- Miami, US: 16
- Atlanta, US: 15

**Seção: Language Distribution**:
- English: 99.5% (391 comments)
- Spanish: 0.3% (1 comment)
- Italian: 0.3% (1 comment)

**Seção: Engagement by Time Zone**:
- GMT+0 (Lisboa): 8.3% - Peak: 20:00-22:00
- GMT-3 (São Paulo): 7.9% - Peak: 19:00-21:00
- GMT+1 (Luanda): 8.7% - Peak: 21:00-23:00
- GMT+2 (Maputo): 6.4% - Peak: 18:00-20:00

**Screenshot**: `community-geography.png`

##### Tab 6: Brands (Items and brands detected) ✓ ANALISADA

**Seção: Brands by Categories** (gráfico de barras):
- Sports: ~36 brands
- Fashion & Apparel: ~27 brands
- Food & Beverages: ~5 brands
- Electronics: ~3 brands

**Seção: Detected Item Categories** (6 categorias):
1. Clothing: 60 detections (39.7%) - Top: Jacket
2. Other: 58 detections (38.4%) - Top: Brand Logo
3. Footwear: 21 detections (13.9%) - Top: Sneakers
4. Electronics: 7 detections (4.6%) - Top: Smartphone
5. Accessories: 3 detections (2%) - Top: Belt
6. Jewelry: 2 detections (1.3%) - Top: Ring

**Seção: Top 10 Detected Items**:
1. Jacket - 42 detections
2. Brand Logo - 21 detections
3. Sneakers - 20 detections
4. Cap - 17 detections
5. T-shirt - 15 detections
6. Hat - 7 detections
7. Smartphone - 4 detections
8. Car - 4 detections
9. Headphones - 3 detections
10. Shirt - 3 detections

**Seção: Brand Affinity** (Top 10):
1. Nike - Sports, 143 mentions (96% very positive)
2. Adidas - Sports, 36 mentions (40% positive)
3. Jordan - Sports, 19 mentions (36% very positive)
4. Supreme - Fashion & Apparel, 13 mentions (29% positive)
5. Champion - Sports, 12 mentions (28% positive)
6. Gucci - Fashion & Apparel, 12 mentions (28% positive)
7. Under Armour - Sports, 12 mentions (28% positive)
8. Polo - Fashion & Apparel, 10 mentions (27% positive)
9. Ralph Lauren - Fashion & Apparel, 9 mentions (27% positive)
10. Puma - Sports, 8 mentions (26% positive)

**Seção: Brand Categories** (4 categorias):
1. Sports - 234 mentions (Avg: positive)
2. Fashion & Apparel - 113 mentions (Avg: positive)
3. Food & Beverages - 13 mentions (Avg: positive)
4. Electronics - 10 mentions (Avg: positive)

**Screenshot**: `community-brands.png`

#### KPIs Identificados (tab Interactions)
- Total Interactions (23.7M)
- Total Likes (23.6M)
- Comments (80.9K)
- Publications (2)
- Engagement Rate (23.9%)
- Followers (99.2M)
- Top Authors (ranking)
- Top Performing Posts (ranking)

---

### 3. Content (`/content`)

**URL**: `/content`
**Título**: Content

#### Filtros Globais
- **Date Range Picker**: "01 Aug 2025 - 31 Aug 2025"
- **Channel Filter**: "All channels"
- **Segment Filter**: "All segments"

#### Tabs (7 tabs totais)

##### Tab 1: Overview (Content performance) ✓ ANALISADA

**Seção: Performance Metrics** (4 cards):
1. **Total Posts**: 268 (-60.8% vs previous)
2. **Total Reach**: 0 (0% vs previous)
3. **Average Engagement**: 86,268.8% (+25.3% vs previous)
4. **Saves per Post**: 0 (0% vs previous)

**Seção: Evolution Over Time** (gráfico com 4 opções):
- Interactions / Comments / Likes / Engagement

**Seção: Distribution by Content Type**:
- Carousel: 177 posts (66%)
- Reel: 65 posts (24.3%)
- Photo: 26 posts (9.7%)
- Video: 0 posts (0%)

**Seção: Top 4 Performing Posts** (com detalhes expandíveis):
1. "@usabasketball trick shots..." - 547.9K likes, 753 comments (62 days ago)
2. "Tatum, Steph and LeBron pregame rituals..." - 541.4K likes, 681 comments (69 days ago)
3. "Steph joining Bucks postgame huddle..." - 539.1K likes, 890 comments (47 days ago)
4. "TOP 100 PLAYS OF 2024-25..." - 515.3K likes, 1,413 comments (40 days ago)

**Seção: Engagement Breakdown**:
- Likes: 23,041,933 (90.6%)
- Comments: 78,113 (0.3%)
- Shares: 1,387,203 (5.5%)
- Saves: 924,802 (3.6%)

**Screenshot**: `content-overview.png`

##### Tab 2: Topics (Themes and subjects) ✓ ANALISADA

**Seção: Topic Metrics** (3 cards):
1. **Total Topics**: 47
2. **Dominant Topic**: Game Highlights (28.5%)
3. **Topic Diversity**: High - 3.2/5

**Seção: Top Topics Evolution** (gráfico de linha):
- Tracking top topics over time (Aug 01-31)
- Game Highlights dominant throughout period

**Seção: Top Themes** (Top 10 com percentagens):
1. Game Highlights - 28.5%
2. Game Recaps - 14.9%
3. Awards & Recognition - 10.6%
4. League News - 8.5%
5. Inspirational Content - 6.4%
6. Trade Rumors - 6.4%
7. Historical Moments - 6.4%
8. Player Stats - 4.3%
9. Throwback Content - 4.3%
10. Celebrity Appearances - 4.3%

**Seção: Rising Topics** (Trending):
- Analytics & Stats: +45% growth
- Trade Speculation: +38% growth
- Behind the Scenes: +22% growth

**Seção: Trending Topics**:
1. NBA Draft Talk - 12 posts (4.5%), Highest engagement: 89.4K
2. Olympics Basketball - 8 posts (3.0%), Highest engagement: 72.1K
3. Training Camp Updates - 6 posts (2.2%), Highest engagement: 45.3K

**Seção: Topics by Sentiment**:
- Positive Topics: Game Highlights, Awards & Recognition
- Neutral Topics: League News, Player Stats
- Negative Topics: Trade Rumors, Controversial Plays

**Screenshot**: `content-topics.png`

##### Tab 3: Hashtags (Tags and mentions) ✓ ANALISADA

**Seção: Hashtag Metrics** (4 cards):
1. **Total Unique Hashtags**: 9
2. **Most Used**: #NBABDAY (8 posts)
3. **Average per Post**: 2.3
4. **Hashtag Reach**: 12.4M

**Seção: Most Used Hashtags**:
1. #NBABDAY - 8 posts, 547.9K likes
2. #NBAAllStar - 5 posts, 298.4K likes
3. #Playoffs2024 - 4 posts, 187.2K likes
4. #TeamUSA - 3 posts, 142.8K likes
5. #DunkContest - 2 posts, 95.6K likes
6. #RisingStars - 2 posts, 78.3K likes
7. #TradeDeadline - 1 post, 45.2K likes
8. #SummerLeague - 1 post, 32.1K likes
9. #G League - 1 post, 28.9K likes

**Seção: Hashtag Performance**:
- Best Performing: #NBABDAY (68.5K avg engagement)
- Most Consistent: #NBAAllStar (59.7K avg engagement)
- Fastest Growing: #TeamUSA (+187% growth)

**Seção: Emerging Hashtags** (New this period):
- #Olympics2024 - 3 posts, 89.4K likes
- #ParisGames - 2 posts, 67.2K likes

**Seção: Hashtag Trends** (gráfico):
- Usage over time showing seasonal patterns
- Peak usage during major events (All-Star, Playoffs)

**Screenshot**: `content-hashtags.png`

##### Tab 4: Visual (Visual analysis) ✓ ANALISADA

⚠️ **Nota**: Este tab mostra "Coming Soon: Visual Analysis" - dados são sample/parciais.

**Seção: Visual Overview** (3 cards):
1. **Images Analyzed**: 268
2. **Dominant Color**: Blue (#1D428A) - 42%
3. **Average Brightness**: 65%

**Seção: Color Palette Distribution**:
- Blue Tones: 42% (NBA brand colors)
- Red Tones: 28% (team colors)
- Black/Gray: 18% (neutral backgrounds)
- Yellow/Gold: 12% (accent colors)

**Seção: Composition Analysis**:
- Action Shots: 45% (players in motion)
- Portrait/Close-ups: 28% (player faces)
- Wide Shots: 18% (arena/crowd)
- Graphics/Text: 9% (stats, announcements)

**Seção: Image Quality Metrics**:
- High Resolution (>1080p): 89%
- Medium Resolution: 8%
- Low Resolution: 3%
- Average Aspect Ratio: 4:5 (Instagram optimized)

**Seção: Face Detection**:
- Posts with Faces: 78%
- Multiple Faces: 42%
- Average Faces per Post: 2.3

**Screenshot**: `content-visual.png`

##### Tab 5: Timing (Frequency and schedules) ✓ ANALISADA

**Seção: Publishing Metrics** (4 cards):
1. **Posts per Week**: 61.6
2. **Best Time to Post**: 14:00-16:00
3. **Best Day**: Sunday
4. **Posting Consistency**: 87%

**Seção: Posting Frequency** (gráfico de barras por dia da semana):
1. Sunday - 45 posts (16.8%)
2. Monday - 42 posts (15.7%)
3. Tuesday - 40 posts (14.9%)
4. Wednesday - 38 posts (14.2%)
5. Thursday - 36 posts (13.4%)
6. Friday - 35 posts (13.1%)
7. Saturday - 32 posts (11.9%)

**Seção: Best Times to Post** (hourly breakdown):
- Peak 1: 14:00-16:00 (highest engagement: 94.2K avg)
- Peak 2: 19:00-21:00 (second highest: 87.6K avg)
- Peak 3: 22:00-00:00 (third highest: 78.4K avg)
- Lowest: 04:00-06:00 (12.3K avg)

**Seção: Publishing Calendar** (heatmap):
- Darker cells indicate higher engagement
- Pattern shows weekday afternoons + weekend evenings perform best

**Seção: Engagement by Time** (line chart):
- Shows correlation between posting time and engagement
- Afternoon/evening posts consistently outperform morning posts

**Seção: Posting Patterns**:
- Average Time Between Posts: 2.8 hours
- Most Active Period: Weekends 14:00-22:00
- Recommended Schedule: 8-10 posts/day focusing on peak hours

**Screenshot**: `content-timing.png`

##### Tab 6: Sentiments (Emotion analysis) ✓ ANALISADA

**Seção: Sentiment Metrics** (4 cards):
1. **Dominant Emotion**: Annoyance (0.4%)
2. **Positive Sentiment**: 95.1%
3. **Negative Sentiment**: 2%
4. **Neutral Sentiment**: 2.9%

**Seção: Emotional Analysis** (11 emotions com percentagens):
1. Annoyance: 0.4%
2. Anticipation: 0.4%
3. Approval: 0.4%
4. Desire: 0.4%
5. Excitement: 0.4%
6. Joy & Excitement: 0.4%
7. Amusement: 0.4%
8. Anger & Conflict: 0.4%
9. Confusion: 0.4%
10. Disapproval: 0.4%
11. Sadness & Discouragement: 0.4%

**Seção: Sentiments by Post** (Top 5 positive posts):
1. "USA Basketball trick shots..." - 98.2% positive
2. "Steph Curry Olympics celebration..." - 97.8% positive
3. "LeBron James pregame ritual..." - 97.1% positive
4. "Kevin Durant clutch moment..." - 96.5% positive
5. "Giannis Antetokounmpo dunk..." - 95.9% positive

**Seção: Sentiment Trend** (gráfico de linha):
- Overall positive sentiment stable at ~95% throughout period
- Minor dips during controversial content (trade news, referee calls)

**Seção: CTS Score Distribution** (Community Trust Score):
- Posts with CTS >8.0: 45%
- Posts with CTS 6.0-8.0: 42%
- Posts with CTS <6.0: 13%

**Screenshot**: `content-sentiments.png`

##### Tab 7: Competitive (Benchmark and comparison) ✓ ANALISADA

⚠️ **Nota**: Este tab mostra "Coming Soon: Competitive Analysis" - dados são sample/parciais.

**Seção: Competitive Metrics** (4 cards):
1. **Market Position**: 2nd place
2. **Engagement Share**: 23.4%
3. **Growth vs Competitors**: +15.6%
4. **Voice Share**: 18.9%

**Seção: Channel Performance Comparison** (Top 5 competitors):
1. NBA - 2nd position, 268 posts, 23.6M likes, +5.7%
2. ESPN - 1st position, 342 posts, 28.4M likes, +8.2%
3. Bleacher Report - 3rd position, 198 posts, 18.7M likes, -2.4%
4. House of Highlights - 4th position, 156 posts, 15.2M likes, -4.8%
5. Yahoo Sports - 5th position, 134 posts, 12.1M likes, -6.2%

**Seção: Competitive Advantages** (vs ESPN):
- Engagement Rate: +8.2% (NBA ahead)
- Avg Likes per Post: -14.7% (ESPN ahead)
- Comment Rate: +22% (NBA ahead)

**Seção: Market Share**:
- ESPN: 28.7%
- NBA (current): 23.4%
- Bleacher Report: 18.9%
- Others: 29.0%

**Seção: Content Strategy Comparison**:
- NBA Focus: Game Highlights, Behind-the-Scenes
- ESPN Focus: Breaking News, Analysis
- Bleacher Report Focus: Highlights, Memes
- House of Highlights Focus: Top Plays, Viral Moments

**Screenshot**: `content-competitive.png`

#### KPIs Identificados (tab Overview)
- Total Posts (268)
- Total Reach (0)
- Average Engagement (86,268.8%)
- Saves per Post (0)
- Content Type Distribution (Carousel, Reel, Photo, Video)
- Engagement Breakdown (Likes, Comments, Shares, Saves)

---

### 4. Comments (`/comments`)

**URL**: `/comments`
**Título**: Comments

#### Filtros Globais
- **Date Range Picker**: "01 Aug 2025 - 31 Aug 2025"
- **Channel Filter**: "All channels"
- **Segment Filter**: "All segments"

#### Tabs (6 tabs totais)

##### Tab 1: Overview (Conversation health) ✓ ANALISADA

**Seção: Conversation Volume** (4 cards):
1. **Total Comments**: 65.4K (+42.5%)
2. **Comments per Post**: 244.0
3. **Growth**: +19.5K (+42.5%)
4. **Active Commenters**: 41.8K unique authors

**Seção: Comment Growth Trend**:
- Gráfico de linha mostrando volume ao longo do tempo (20-30 de agosto)

**Seção: Conversation Quality** (3 cards):
1. **Average Length**: 48 chars (+9.8%)
2. **Conversation Depth**: 1.3 replies per comment (-0.1%)
3. **Response Rate**: 19.7% (+5.4%)

**Seção: Conversation Health** (3 cards):
1. **Positive Sentiment**: 20.6% (-13.5%)
2. **Health Score**: 100.0/100
3. **Spam + Toxicity**: 0.0%

**Seção: Quality Breakdown**:
- 103 posts (0%)
- 3.7K posts (6%)
- 24.6K posts (38%)
- 5.6K posts (9%)

**Seção: Comments that Generated Most Conversation** (Top 3):
1. "Rockets-Lakers" - 908,709 replies, 70% engagement
2. "Wolves-Nuggets" - 908,709 replies, 70% engagement
3. "Mavs-Warriors" - 908,708 replies, 70% engagement

**Seção: Posts with Most Comments** (Top 4):
1. "Plenty of buckets..." - 2.8K comments, 46.2K likes, CTS 7.5%, 72% positive
2. "Avengers assembled..." - 2.1K comments, 410.5K likes, CTS 7.8%, 72% positive
3. "Remembering Kobe..." - 2.1K comments, 454.8K likes, CTS 8.1%, 72% positive
4. "Kevin Hart..." - 1.9K comments, 262.2K likes, CTS 8.4%, 72% positive

**Screenshot**: `comments-overview.png`

##### Tab 2: Topics (Discussed themes) ✓ ANALISADA

**Seção: Topic Overview** (3 cards):
1. **Discussion Categories**: 9 topics
2. **Most Discussed**: Game Highlights (56% - 31.8K comments)
3. **Question Frequency**: 12.3%

**Seção: Top Discussion Topics** (9 categorias com percentagens e counts):
1. Game Highlights - 56% (31.8K comments)
2. Player Performance - 15.2% (8.6K comments)
3. Trade & Roster Moves - 8.9% (5.1K comments)
4. Team Rivalries - 7.3% (4.1K comments)
5. League News - 4.8% (2.7K comments)
6. Historical Comparisons - 3.2% (1.8K comments)
7. Game Predictions - 2.1% (1.2K comments)
8. Referee Decisions - 1.5% (0.9K comments)
9. Off-Court News - 1.0% (0.6K comments)

**Seção: Sentiment by Topic**:
- Game Highlights: 72% positive, 18% neutral, 10% negative
- Player Performance: 65% positive, 20% neutral, 15% negative
- Trade & Roster Moves: 42% positive, 28% neutral, 30% negative
- Team Rivalries: 58% positive, 22% neutral, 20% negative

**Seção: Emerging Topics** (New conversations):
- Olympics Basketball: 2.8K comments (4.3% of total)
- Draft Prospects: 1.9K comments (2.9% of total)
- Coaching Changes: 1.2K comments (1.8% of total)

**Seção: Topics Evolution** (gráfico de linha):
- Shows how discussion topics shift over time
- Game Highlights remain consistently dominant

**Screenshot**: `comments-topics.png`

##### Tab 3: Sentiments (Emotion analysis) ✓ ANALISADA

**Seção: Sentiment Metrics** (4 cards):
1. **Q3 Positive Comments**: 20.6%
2. **CTS Score**: 6.0/10 (Community Trust Score)
3. **Q3 Negative Comments**: 51.9%
4. **Q3 Neutral Comments**: 27.5%

**Seção: Emotional Analysis** (11 emotions com contadores):
1. Joy & Excitement - 13.5K comments (20.6%)
2. Annoyance - 8.9K comments (13.6%)
3. Anger & Conflict - 7.2K comments (11.0%)
4. Approval - 6.5K comments (9.9%)
5. Neutral - 5.8K comments (8.9%)
6. Admiration - 4.3K comments (6.6%)
7. Amusement - 3.7K comments (5.7%)
8. Disappointment - 3.2K comments (4.9%)
9. Curiosity - 2.8K comments (4.3%)
10. Excitement - 2.4K comments (3.7%)
11. Sadness & Discouragement - 1.9K comments (2.9%)

**Seção: CTS Score Distribution**:
- Dominant: 20.6% (positive comments)
- Passive: 51.9% (negative comments)
- Neutral: 27.5% (neutral comments)

**Seção: Top 50 Emotions in Comments** (word cloud):
- Visualização de palavras mais frequentes em comentários
- Maior destaque: "Great", "Love", "Best", "Amazing"

**Seção: What Triggers Emotions** (emotional triggers):
- Positive: Game-winning shots, Player achievements, Team victories
- Negative: Controversial calls, Trade news, Injuries
- Neutral: Stats updates, Game schedules

**Screenshot**: `comments-sentiments.png`

##### Tab 4: Language (Expressions and languages) ✓ ANALISADA

⚠️ **Nota**: Este tab mostra "Coming Soon: Language Analysis" - dados são sample/parciais.

**Seção: Language Overview** (4 cards):
1. **Languages Detected**: 12
2. **Primary Language**: Portuguese (68.4%)
3. **Avg Words per Comment**: 12.3
4. **Slang Usage**: 23.7%

**Seção: Language Distribution** (12 línguas):
1. Portuguese - 68.4% (44.7K comments)
2. English - 18.9% (12.4K comments)
3. Spanish - 5.2% (3.4K comments)
4. French - 2.8% (1.8K comments)
5. Italian - 1.7% (1.1K comments)
6. German - 1.2% (0.8K comments)
7. Dutch - 0.6% (0.4K comments)
8. Russian - 0.4% (0.3K comments)
9. Chinese - 0.3% (0.2K comments)
10. Japanese - 0.2% (0.1K comments)
11. Korean - 0.2% (0.1K comments)
12. Arabic - 0.1% (0.1K comments)

**Seção: Most Used Expressions by Language**:
- Portuguese: "top demais", "que jogo", "melhor do mundo"
- English: "let's go", "goat", "straight fire"
- Spanish: "qué jugador", "increíble", "el mejor"

**Seção: Slang and Internet Language**:
- Emojis per comment: 1.8 avg
- Abbreviations: 15.2% of comments
- All caps usage: 8.7% of comments

**Screenshot**: `comments-language.png`

##### Tab 5: Moderation (Toxicity and spam) ✓ ANALISADA

**Seção: Moderation Metrics** (4 cards):
1. **Spam Rate**: 0.0% (0 comments filtered)
2. **Bot Rate**: 51.2% (33.5K accounts identified)
3. **Toxicity Rate**: 0.0% (0 toxic comments)
4. **Clean Comments**: 48.7% (31.8K safe comments)

**Seção: Evolution of Spam, Bots and Toxicity** (gráfico de linha):
- Shows volume of clean comments vs. spam/toxic over time
- Period: Aug 01-31, 2025
- Clean comments consistently high throughout period

**Seção: Detected Spam Types**:
1. Promotional Spam - 5 comments (55.6%)
   - Example: "BANDLAB MUSIC 2 OUT ON ALL PLATFORMS LINK IN BIO"

**Seção: Bot Detection Patterns**:
1. Rapid Fire (High Risk) - 2 accounts (100%)
   - Description: Multiple comments posted in rapid succession (>5 comments/minute)

**Seção: Flagged Comments (Spam & Bots)** (Top 10 de 33.5K flagged):
- All flagged comments are from accounts created <3 days ago
- Detection reasons: new_account, rapid_fire, promotional_content
- Actions taken: flagged_for_review, account_monitoring

**Seção: Toxic Content Types**:
1. Hate Speech - 13 comments
   - Severity: Critical
   - Action: Removed
   - 100% of total toxic content

**Seção: Moderation Effectiveness** (4 métricas):
1. **Detection Accuracy**: 100.0% (Excellent)
2. **Average Response Time**: 56,467.9 min (Poor - ~39 days)
3. **False Positives**: 0.0% (Excellent)
4. **Recurrence**: 25.0% (Acceptable)

**Seção: Spam and Bot Origins**:
- No origin data available (API returned 500 error)

**Seção: Moderation Recommendations**:
- No recommendations available (API returned 500 error)

**Screenshot**: `comments-moderation.png`

##### Tab 6: Influence (Networks and influencers) ✓ ANALISADA

**Seção: Influence Metrics** (4 cards):
1. **Active Influencers**: 690 users with high engagement
2. **Total Reach**: 746.2M combined followers
3. **Influence Rate**: 2.1% (influencer comments)
4. **Active Communities**: - (no data)

**Seção: Influence and Engagement Evolution** (gráfico de linha):
- Tracks Active Influencers, Total Reach, Engagement Rate over time
- Period: Aug 01-31, 2025

**Seção: Top Influencers** (Top 3):
1. @blacktiger_hayati (Analyst) - Score 22
   - 14.0K followers
   - 37 comments
   - 0 replies
   - 10.6% engagement

2. @virginia_angela71 (Influencer) - Score 20
   - 16.0K followers
   - 38 comments
   - 0 replies
   - 10.6% engagement

3. @mxrantswrld (Influencer) - Score 12
   - 14.3K followers
   - 39 comments
   - 0 replies
   - 32.5% engagement

**Seção: Rising Influencers** (4 novos influencers):
1. @future_mvp - +284% growth, 12.4K followers, 18.3% engagement, 14d active
2. @clutch_takes - +198% growth, 8.9K followers, 15.7% engagement, 21d active
3. @hoop_insights - +167% growth, 7.2K followers, 14.2% engagement, 18d active
4. @nba_pulse - +142% growth, 6.1K followers, 12.8% engagement, 28d active

**Seção: Active Communities** (4 comunidades):
1. Lakers Nation - 18.4K members (Positive), 94% activity, 2.3K posts, 12.8K comments, Top 3
2. Warriors Fans - 15.2K members (Positive), 87% activity, 1.9K posts, 10.2K comments, Top 4
3. NBA Analytics - 12.7K members (Neutral), 78% activity, 1.4K posts, 8.9K comments, Top 2
4. Basketball Memes - 9.8K members (Positive), 92% activity, 2.8K posts, 15.4K comments, Top 5

**Seção: Influence Patterns** (5 tipos):
1. Conversation Starters - 247 users (29%) - Create threads with 50+ replies
2. Amplifiers - 189 users (22%) - Repost and increase reach
3. Analysts - 156 users (18%) - Long and detailed comments
4. Engagers - 142 users (17%) - Reply to many comments
5. Curators - 113 users (14%) - Share relevant content

**Seção: Conversations Started by Influencers** (Top 3):
1. @hoopsfanatic - "MVP Race Analysis" (2h ago) - 284 replies, 1.2K likes, 24.8K reach (Positive)
2. @nbastats_pro - "Defensive Stats Breakdown" (5h ago) - 197 replies, 892 likes, 18.4K reach (Neutral)
3. @lakers_nation - "Trade Deadline Predictions" (8h ago) - 312 replies, 1.8K likes, 32.1K reach (Neutral)

**Seção: Influencer Impact** (4 métricas):
1. **Conversations Started**: 1.2K (+42% vs average) - Threads created by influencers
2. **Average Reach**: 18.4K (8.2x vs average) - People reached per post
3. **Response Rate**: 68% (+34% vs average) - Comments that receive replies
4. **Conversation Quality**: 8.7/10 (+2.3 pts vs average) - Depth and engagement score

**Screenshot**: `comments-influence.png`

#### KPIs Identificados (tab Overview)
- Total Comments (65.4K)
- Comments per Post (244.0)
- Growth (+19.5K, +42.5%)
- Active Commenters (41.8K)
- Average Length (48 chars)
- Conversation Depth (1.3)
- Response Rate (19.7%)
- Positive Sentiment (20.6%)
- Health Score (100/100)
- Spam + Toxicity (0.0%)

---

### 5. Posts (`/posts`)

**URL**: `/posts`
**Título**: Posts Hub
**Subtítulo**: "Daily operational management of content and community"

#### Filtros Globais
- **Date Range Picker**: "01 Aug 2025 - 31 Aug 2025"
- **Channel Filter**: "All channels"
- **Segment Filter**: "All segments"

#### Tabs (3 tabs totais)

##### Tab 1: Posts (Daily posts feed) ✓ ANALISADA

**Seção: Daily Metrics** (4 cards - presente em todas as tabs):
1. **Posts Published**: 268 (in selected period)
2. **Total Comments**: 78.1K (all posts)
3. **Active Alerts**: 5 (Critical + Warnings)
4. **Community Health**: 100.0/10 (Neutra)

**Controles da Página**:
- Auto-refresh checkbox
- Refresh button
- View toggle: FEED / GRID
- Filter dropdown: All posts / Critical only / Warnings only / OK only

**Estrutura**: Feed operacional de posts com informações detalhadas (similar ao Instagram feed)
- Cada post mostra: imagem, caption, data, likes, comments, engagement metrics
- Posts organizados cronologicamente (mais recentes primeiro)
- Infinite scroll para carregar mais posts

**Screenshot**: `posts-posts.png`

##### Tab 2: Comments (Comments activity) ✓ ANALISADA

**Seção: Daily Metrics** (mesmas 4 cards do Tab 1)

**Seção: Comment Statistics** (4 cards):
1. **Comments Today**: 0 (-100.0% vs ontem)
2. **Response Rate**: 68% (+5.2% - Posts com resposta)
3. **Average Time**: 4.2 min (-1.8 min vs período anterior)
4. **Unique Commenters**: 41,773 (+27.3% vs período anterior)

**Seção: Recent Comments** (feed de comentários em tempo real):
- Lista dos comentários mais recentes com:
  - Avatar do usuário
  - @username
  - Timestamp (ex: "agora", "2h ago")
  - Texto do comentário
  - Post associado (snippet do caption)
  - Contagem de likes (❤️ 0)

**Exemplos de comentários recentes**:
- @eastsideebbie32: "Forget Ayesha my boy …….i got some hoes on go !😂"
- @realdp____: "Y'all Want Giannis Though"
- @silentjoker6658: "it is so incredible 😍😍"
- @daniel.shippy: "That last shot u didn't have to see to know it went in!"
- @quindiica: "No curry just likes cooking lmao"

**Screenshot**: `posts-comments.png`

##### Tab 3: Alerts (Alerts and moderation) ✓ ANALISADA

**Seção: Daily Metrics** (mesmas 4 cards dos tabs anteriores)

**Filtros de Alerts**:
- **Type**: All / Toxicity / Spam / Bot / Sentiment / Engagement
- **Severity**: All / High / Medium / Low
- **Status**: All / Open / Resolved

**Seção: Alerts Table** (tabela com colunas):
- DATA/HORA
- TIPO DE ALERTA
- DESCRIÇÃO
- SEVERIDADE
- AÇÃO RECOMENDADA
- ESTADO
- AÇÕES (Ver Post, Resolver)

**Tipos de Alerts Identificados**:
1. **Engagement Alerts** (maioria):
   - "Engagement X% abaixo da média esperada"
   - Severidade: High (>50%), Medium (30-50%), Low (<30%)
   - Ação recomendada: "Promote similar content"

2. **Bot Detection Alerts**:
   - "X contas de bot detectadas nos comentários"
   - Severidade: Medium (2-3 bots), Low (1 bot)
   - Ação recomendada: "Block suspicious accounts"

**Exemplos de Alerts** (ordenados por data/hora, mais recentes primeiro):
- Post #54418 (2025-08-30 23:05): Engagement 60% abaixo - High - Open
- Post #54438 (2025-08-30 22:00): Engagement 33% abaixo - Medium - Open
- Post #54425 (2025-08-30 20:00): 3 contas de bot detectadas - Medium - Open
- Post #54423 (2025-08-30 19:00): Engagement 22% abaixo - Low - Open
- Post #54431 (2025-08-30 18:00): Engagement 87% abaixo - High - Open

**Total de Alerts no período**: ~50+ alerts listados (todos status "Open")

**Screenshot**: `posts-alerts.png`

#### KPIs Identificados (tab Posts)
- Feed de posts operacional
- Controles de refresh e view modes
- Filtros por criticidade

---

## Rotas Adicionais Identificadas

### Autenticação
- `/login` - Página de login
- `/register` - Página de registro (link visível no login)
- `/forgot-password` - Recuperação de senha

### Legais
- `/terms-and-conditions` - Termos e condições
- `/privacy-policy` - Política de privacidade

---

## Padrões de Componentes Identificados

### Componentes de Navegação
- **Sidebar** (fixa, sempre visível)
- **Header** (com Add Channel + User selector)
- **Breadcrumbs**: Não identificados ainda
- **Tabs**: Usados em Community (6 tabs)

### Componentes de Dados
- **Metric Card** (valor + variação % + descrição)
- **Donut Chart** (gender, age, location)
- **Line Chart** (engagement trends)
- **Word Cloud** (main topics)
- **User List** (top authors, top influencers)
- **Post Card** (top posts)
- **Highlight Card** (AI-generated insights com "Ask Alley")
- **Alert Badge** (risk flags)

### Componentes de Input
- **Date Range Picker**
- **Dropdown** (channels, segments)
- **Button** (diversos tipos)

### Componentes Visuais
- **Avatar** (user photos)
- **Icons** (diversos, necessário inventariar)
- **Badges** (counters em alerts)
- **Tags** (para categorização)

---

## Filtros Globais Identificados

### Comuns a múltiplas páginas
1. **Date Range Picker**
   - Default: Últimos 30 dias (01 Aug - 31 Aug 2025)
   - Formato: "DD MMM YYYY - DD MMM YYYY"

2. **Channel Selector**
   - Opções: Individual channels ou "All channels"
   - Channels disponíveis: nba, celtics, tonywells99

3. **Segment Selector** (Community page)
   - Opções: "All segments" + segmentos definidos
   - Status: Não explorado ainda

---

## Observações Técnicas

### APIs Identificadas (via console logs)

**Dashboard**:
- `GET /api/dashboard/engagement-trend`
- `GET /api/dashboard/audience-gender`
- `GET /api/dashboard/audience-age-interval`
- `GET /api/dashboard/audience-location`
- `GET /api/dashboard/sentiment-analysis`
- `GET /api/dashboard/top-topics`
- `GET /api/dashboard/instagram/influencers`
- `GET /api/dashboard/instagram/hashtags`
- `GET /api/dashboard/instagram/timing`
- `GET /api/analytics/get-audience-age-gender`
- `GET /api/analytics/get-audience-industries`
- `GET /api/channel/lifestyle`
- `GET /api/channel/posts-metrics`
- `GET /api/community/my-channels`
- `GET /api/community/social-media-reach`

**Community (Analytics)**:
- `GET /api/analytics/get-filters`
- `GET /api/business-profile/metrics`
- `GET /api/channel/top-authors`
- `GET /api/channel/posts-metrics`

### Loading States
- Mensagens "No data available" / "Sem dados disponíveis" / "Nenhum post disponível"
- Dados carregam de forma assíncrona
- **Tempo recomendado de espera**: 15 segundos por página/tab

### Multi-idioma
- Interface principalmente em inglês
- Alguns elementos em português ("Sem dados disponíveis")
- **Observação**: Inconsistência de idioma a ser investigada

---

## Próximos Passos (Auditoria)

### Páginas a Mapear
- [x] Dashboard ✓ COMPLETO
- [x] Channel Detail ✓ COMPLETO (3/3 tabs) **[NOVA - Descoberta em 2025-10-10]**
- [x] Community ✓ COMPLETO (6/6 tabs)
- [x] Content ✓ COMPLETO (7/7 tabs)
- [x] Comments ✓ COMPLETO (6/6 tabs)
- [x] Posts ✓ COMPLETO (3/3 tabs)

### Tabs Mapeadas (Total: 25 tabs)
- [x] Channel Detail: 3 tabs (Community, Post, Alerts) **[NOVA]**
- [x] Community: 6 tabs (Interactions, Audience, Sentiments, Content, Geography, Brands)
- [x] Content: 7 tabs (Overview, Topics, Hashtags, Visual, Timing, Sentiments, Competitive)
- [x] Comments: 6 tabs (Overview, Topics, Sentiments, Language, Moderation, Influence)
- [x] Posts: 3 tabs (Posts, Comments, Alerts)

### Screenshots Capturados (Total: 27 screenshots)
- [x] dashboard.png
- [x] channel-community.png **[NOVO]**
- [x] channel-post.png **[NOVO]**
- [x] channel-alerts.png **[NOVO]**
- [x] community-interactions.png
- [x] community-audience.png
- [x] community-sentiments.png
- [x] community-content.png
- [x] community-geography.png
- [x] community-brands.png
- [x] filter-location-section.png **[NOVO - Filtros de Segmentação]**
- [x] content-overview.png
- [x] content-topics.png
- [x] content-hashtags.png
- [x] content-visual.png
- [x] content-timing.png
- [x] content-sentiments.png
- [x] content-competitive.png
- [x] comments-overview.png
- [x] comments-topics.png
- [x] comments-sentiments.png
- [x] comments-language.png
- [x] comments-moderation.png
- [x] comments-influence.png
- [x] posts-posts.png
- [x] posts-comments.png
- [x] posts-alerts.png

### Análises Pendentes (Sprint 3)
- [ ] Inventário completo de componentes UI
- [ ] Inventário completo de KPIs consolidados
- [ ] Análise de fluxos de usuário
- [ ] Documentação de padrões de design
- [ ] Análise de código Git para componentes React/Vue
- [ ] Documentação de integrações e APIs
- [ ] Análise de performance e otimizações

---

## Estatísticas Finais

**Páginas principais mapeadas**: 6/6 (100%)
- Dashboard ✓ COMPLETO
- Channel Detail ✓ COMPLETO (3 tabs) **[NOVA - Descoberta 2025-10-10]**
- Community ✓ COMPLETO (6 tabs)
- Content ✓ COMPLETO (7 tabs)
- Comments ✓ COMPLETO (6 tabs)
- Posts ✓ COMPLETO (3 tabs)

**Total de tabs mapeadas**: 25 tabs
- Channel Detail: 3 tabs **[NOVA]**
- Community: 6 tabs
- Content: 7 tabs
- Comments: 6 tabs
- Posts: 3 tabs

**KPIs únicos identificados**: ~165+ métricas individuais (acrescentadas ~15 métricas do Channel Detail)

**Tipos de componentes identificados**: ~20+ tipos

**Endpoints de API identificados**: ~34+ endpoints (+ 4 novos do Channel Detail)

**Screenshots capturados**: 26 arquivos PNG (+ 3 novos: channel-community, channel-post, channel-alerts)

**Tabs com dados "Coming Soon"**: 3 (Content Visual, Content Competitive, Comments Language)

**Tabs com erros de API**: 1 (Comments Moderation - endpoints de origins e recommendations com 500)

---

**Status geral**: ✅ **Auditoria de Navegação 100% completa** (Sprint 2 + Descoberta adicional)

**Próxima ação**: Sprint 3 - Análise de código, componentização e documentação técnica

**Tempo total de execução**: ~3.5 horas de navegação sistemática + extração de dados

**Última atualização**: 2025-10-10 (Sprint 2 concluído + Channel Detail page descoberta e documentada)

**Nota importante**: Durante a continuação da sessão, foi descoberta uma página adicional não identificada inicialmente:
- **Channel Detail Page** (`/dashboard/channel/{id}`) com 3 tabs completas
- Esta página oferece análise profunda de um canal individual vs. overview multi-canal do Dashboard
- Todos os 3 screenshots capturados e documentação completa no sitemap
- Sprint 2 agora está 100% completo com esta página adicional incluída
