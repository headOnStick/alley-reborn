# API Reference by Component (Draft)

> Usar apenas endpoints já documentados em `01-context/api-reference.md`. Ajustar nomenclaturas conforme a API real.

## Brand Health Dashboard
| Componente | Endpoint (nome) |
|------------|-----------------|
| Hero Card - Brand Health Score | `GET /brandHealth/overview` |
| Hero Card - Net Sentiment | `GET /sentiment/overview` |
| Hero Card - Community Wellbeing | `GET /community/health` |
| Hero Card - Crisis Alerts | `GET /alerts/active` |
| Trendline (score + eventos) | `GET /brandHealth/timeline`, `GET /events/timeline` |
| Drivers & Risks | `GET /brandHealth/drivers`, `GET /brandHealth/risks` |
| Breakdown por canal | `GET /brandHealth/byChannel` |

## Competitive Insights
| Componente | Endpoint |
|------------|----------|
| Competitive Position Index | `GET /competitive/position` |
| Benchmark Sentiment | `GET /competitive/sentiment` |
| Share of Voice | `GET /competitive/sov` |
| Emerging Competitors | `GET /competitive/emerging` |
| Timeline Comparativo | `GET /competitive/timeline` |
| Tabela por Competitor | `GET /competitive/byBrand` |

## Sponsorship Value
| Componente | Endpoint |
|------------|----------|
| Revenue Opportunity | `GET /sponsorship/revenue` |
| Top Sponsor Impact | `GET /sponsorship/top` |
| Activation Performance | `GET /sponsorship/activationScore` |
| Sponsor Sentiment | `GET /sponsorship/sentiment` |
| Pitch Candidates | `GET /sponsorship/pitchCandidates` |
| Audience Segments (valor) | `GET /audienceSegments/topValue` |

## Partnership Opportunities
| Componente | Endpoint |
|------------|----------|
| Emerging Brand Momentum | `GET /partnerships/emerging` |
| Category Interest | `GET /partnerships/categories` |
| Influencer Alignment | `GET /influencers/matches` |
| Opportunity Gaps | `GET /partnerships/gaps` |
| Brand Grid | `GET /partnerships/brands` |
| Timeline (brand engagement) | `GET /partnerships/timeline` |

## Engagement Support
| Componente | Endpoint |
|------------|----------|
| Content Efficiency | `GET /engagement/contentEfficiency` |
| Top Formats | `GET /engagement/topFormats` |
| Audience Growth | `GET /audience/growth` |
| Retention/Churn | `GET /audience/retention` |
| Heatmap (day/hour) | `GET /engagement/heatmap` |
| Recommendations | `GET /engagement/recommendations` |

## Segmentação / Filtros
| Componente | Endpoint |
|------------|----------|
| Segmentos predefinidos | `GET /audienceSegments/list` |
| Detalhe segmento | `GET /audienceSegments/{segmentId}` |
| Configuração de filtros (persona, canal, data) | `GET /filters/presets` (se existir) |

## Alertas & Exports
| Componente | Endpoint |
|------------|----------|
| Alerts list | `GET /alerts/list` |
| Export segment/pitch | `POST /exports/segment`, `POST /exports/pitch` |

> Confirmar a existência real dos endpoints na referência oficial; ajustar nomes conforme necessário.
