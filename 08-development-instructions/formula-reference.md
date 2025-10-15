# Formula Reference - KPIs e Métricas (Draft)

> Usar apenas quando necessário derivar métricas a partir de dados existentes. Indicar página/componente que usa cada fórmula. Se for regra de negócio, documentar claramente.

## Índice
- Brand Health Dashboard
- Competitive Insights
- Sponsorship Value
- Partnership Opportunities
- Engagement Support

---

## Brand Health Dashboard

### Brand Health Score (Hero Card)
- **Componente**: Hero Card “Brand Health Score”
- **Fórmula** (exemplo a validar):  
  `Brand Health Score = (Net Sentiment * 0.4) + (Engagement Rate * 0.3) + (Community Health Index * 0.2) + (Brand Awareness Index * 0.1)`
- **Fontes**: `sentiment.overall`, `engagement.rate`, `community.healthIndex`, `brandAwareness.index`
- **Notas**: pesos a confirmar com equipa de dados; normalizar para escala 0-100.

### Net Sentiment Trend
- **Componente**: Hero Card “Net Sentiment”; Trendline
- **Fórmula**:  
  `Net Sentiment = (% positivo) - (% negativo)`  
  `Trend = NetSentiment(today) - NetSentiment(previousPeriod)`
- **Fontes**: `sentiment.overall.positive`, `.negative`

### Community Wellbeing Index
- **Componente**: Hero Card “Community Wellbeing”
- **Fórmula** (placeholder): combinar `community.retention`, `community.activity`, `community.supportTickets`.
- **Notas**: requer definição de pesos — registar após validação.

### Crisis Alerts Threshold
- **Componente**: Alerts
- **Regra**:  
  - disparar alerta se `NetSentiment drop >= 10 pts` em <7 dias.  
  - ou se `Volume negativo` > X (definir com dados históricos).

---

## Competitive Insights

### Competitive Position Index
- **Componente**: Hero Card
- **Fórmula**:  
  `CPI = (ShareOfVoice * 0.5) + (SentimentGap * 0.3) + (EngagementGap * 0.2)`  
  onde `SentimentGap = NetSentiment(brand) - Avg(NetSentiment competitors)`
- **Nota**: ajustes conforme dados reais.

### Share of Voice
- **Componente**: Hero Card
- **Fórmula**:  
  `SoV = (Mentions brand / Total mentions market) * 100`
- **Fontes**: `competitive.mentions`, `competitive.totalMentions`.

---

## Sponsorship Value

### Revenue Opportunity Range
- **Componente**: Hero Card
- **Fórmula** (regra de negócio):  
  `Potential Revenue = AudienceSegmentSize * AvgDealValue`  
  - where `AvgDealValue` pode vir de input manual ou histórico.  
  - Range (min-max) com base em tiers (ex.: Bronze/Prata/Ouro).
- **Notas**: necessita de validação com Comercial.

### Activation Performance
- **Componente**: Hero Card
- **Fórmula**:  
  `Activation Score = (Campaign Engagement uplift %) + (Sentiment change %) + (Conversion proxies)` (normalizado).

### Sponsor Sentiment
- **Componente**: Hero Card / Spotlight
- **Fórmula**: mesma lógica de Net Sentiment mas filtrada pelo sponsor.

---

## Partnership Opportunities

### Emerging Brand Momentum
- **Componente**: Hero Card
- **Fórmula**:  
  `% change = ((Mentions brand (últimos 30d) - Media 3m) / Media 3m) * 100`
- **Fonte**: `partnerships.brandMentions`.

### Influencer Alignment Score
- **Componente**: Hero Card
- **Fórmula**:  
  `Alignment Score = (Overlap audience % + Sentiment match + Engagement match) / 3`  
  (valores normalizados).

---

## Engagement Support

### Content Efficiency
- **Componente**: Hero Card
- **Fórmula**:  
  `Content Efficiency = Total Engagement / Nº de Posts` (por período / canal).

### Audience Growth
- **Componente**: Hero Card
- **Fórmula**:  
  `% Growth = ((Followers atual - Followers período anterior) / Followers período anterior) * 100`

### Retention/Churn
- **Componente**: Hero Card
- **Fórmula**:  
  `Retention Rate = Retidos / Total`  
  `Churn Rate = Churned / Total`  
  (valores definidos conforme dados do app/fantasy).

### Heatmap Engagement
- **Componente**: Heatmap
- **Fórmula**: aglomerar `engagement.events` por dia/hora.

---

## Observações
- Todos os placeholders devem ser validados com a equipa de dados antes de implementação.
- Qualquer formula nova → atualizar este ficheiro e referenciar componente.
