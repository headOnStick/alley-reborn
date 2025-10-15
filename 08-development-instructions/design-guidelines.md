# Design Guidelines - Alley Reborn (Draft)

> Usar apenas dados confirmados nas APIs e no data schema existente. Não introduzir KPIs novos sem regra de negócio/fórmula definida.

## 1. Estrutura Global
- Tabs principais (máx. 5): **Brand Health**, **Competitive Insights**, **Sponsorship Value**, **Partnership Opportunities**, **Engagement Support**.
- Layout KISS: acima da dobra = persona selector + 4 hero KPIs + trendline principal.
- Zona de filtros/segmentação única (topo direito), inspirada no fluxo de criação de campanhas (Meta/TikTok). Opções limitadas:
  - Canal (Instagram, app, etc.)
  - Data range (predefinições: 7d, 30d, 90d, custom)
  - Persona (CMO, Sponsorship, Community, Social)
  - Segmentos predefinidos (ex.: “Car owners”, “Financial interest”) — extraídos do endpoint `audienceSegments`.

## 2. Componentes permitidos por página

### Brand Health Dashboard
- Hero Cards (4):
  1. **Brand Health Score** (dados: `brandHealth.overallScore`, `brandHealth.trend`)
  2. **Net Sentiment** (`sentiment.overall`, `sentiment.trend`)
  3. **Community Wellbeing** (`community.healthIndex`)
  4. **Crisis Alerts** (`alerts.activeCount`, `alerts.list`)
- Trendline principal: `brandHealth.timeline` + overlay de eventos `events.timeline`.
- Spotlight cards:
  - “Top Drivers” (`brandHealth.drivers`)
  - “Emerging Risks” (`brandHealth.risks`)
- Drill-down: link para detalhes por canal (usa `brandHealth.byChannel`).

### Competitive Insights
- Hero Cards:
  1. **Competitive Position Index** (`competitive.positionIndex`)
  2. **Benchmark Sentiment** (`competitive.sentiment.compare`)
  3. **Share of Voice** (`competitive.shareOfVoice`)
  4. **Emerging Competitors** (`competitive.emerging`)
- Gráfico comparativo (bar/line) com `competitive.timeline` (multi-series).
- Tabela “Competitor Breakdown” com `competitive.byBrand`.

### Sponsorship Value
- Hero Cards:
  1. **Revenue Opportunity Estimate** (`sponsorship.revenueRange`)
  2. **Top Sponsor Impact** (`sponsorship.topSponsors`)
  3. **Activation Performance** (`sponsorship.activationScore`)
  4. **Sponsor Sentiment** (`sponsorship.sentiment`)
- Spotlight “Pitch Ready” com `sponsorship.pitchCandidates`.
- Segment list (carrossel ou tabela curta) com `audienceSegments.topByValue`.
- Exibir botões “Export pitch deck / CSV” (não mostrar dados novos).

### Partnership Opportunities
- Hero Cards:
  - **Emerging Brand Momentum** (`partnerships.emergingBrands`)
  - **New Categories Interest** (`partnerships.categories`)
  - **Influencer Alignment** (`influencers.topMatches`)
  - **Activation Gaps** (`partnerships.opportunityGaps`)
- Grid de marcas com `partnerships.brandList` (máx. 6 por view).
- Timeline “Brand Engagement vs Events” (`partnerships.timeline`).

### Engagement Support
- Hero Cards:
  - **Content Efficiency** (`engagement.contentEfficiency`)
  - **Top Formats** (`engagement.topFormats`)
  - **Audience Growth** (`audience.growth`)
  - **Retention/Churn** (`audience.retention`)
- Heatmap “Engagement by Day/Hour” (`engagement.heatmap`).
- Cards “What to do next” com `engagement.recommendations`.

## 3. Filtros & Segmentação
- Apresentar filtro como drawer ou barra lateral, com:
  - Persona (segmented control)
  - Canal
  - Data range
  - Segmentos (checkbox list, máx. 5 visíveis, multi-select)
- Mostrar contador de filtros ativos.
- Evitar combos ilimitados; manter presets geridos por produto.

## 4. Princípios visuais
- Prioridade visual: hero cards > spotlight > tabelas → cores neutras + highlight (#) para alertas.
- Indicadores de trend (↑/↓) com percentagem e cor (verde/vermelho).
- Máx. 6 componentes principais por página; extras via “View more”.
- Evitar gráficos complexos; usar line/bar/sparkline, sem 3D ou stacks confusos.
- **Campos “em desenvolvimento”**: quando for necessário mostrar dados ainda não suportados pela API/KPI, usar mock com borda tracejada cinzenta + etiqueta `Roadmap / Dados em implementação`.

## 5. Interações padrão
- Hero card → on click abre modal com detalhes + link “Ver no detalhe” (leva para subpágina).
- Spotlight segment → CTA “Exportar”/“Gerar deck” (aciona modal).
- Alerts → dropdown com lista (máx. 5), link para `alerts.list`.
- Tooltips explicam métricas (texto breve + fonte).

## 6. Restrições
- Não introduzir dados novos sem regra; se necessário, marcar “placeholder” + asterisco.
- Segmentos adicionais só se estiverem no endpoint `audienceSegments`.
- Evitar multi-step wizards na mesma página (ex.: geração de relatório deve abrir modal).

## 7. Referências para designers
- Mockups devem citar os endpoints usados (ver doc de API).
- Futuros componentes planeados (ex.: tikTok, CRM export) devem ficar etiquetados “roadmap”.
- Qualquer card/visualização sem dados confirmados deve apresentar borda tracejada + etiqueta “(roadmap)” até que o backend marque **OK** no `backend-validation-status.md`.
- Consistência com `06-future-product/page-structures/dashboard.md` é obrigatória.
