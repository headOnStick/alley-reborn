# Backend Validation Checklist – Alley Reborn

> Objetivo: validar se os endpoints e dados disponíveis suportam o redesign proposto.  
> Entrega esperada: backend confirma cada item com **OK** ou indica planos/impedimentos.

## Estrutura
1. Endpoints existentes – confirmar disponibilidade e payload.
2. Endpoints novos – necessidade de implementação.
3. Fórmulas/KPIs compostos – confirmar dados de origem e cálculos.
4. Segmentação & exports – capacidades de filters/export.

---

## 1. Endpoints existentes (confirmar payload)
| Item | Endpoint | Uso | OK? | Notas |
|------|----------|-----|-----|-------|
| Dashboard filters | `GET /api/dashboard/get-filters` | Persona/filtros base | [ ] | Ver se inclui canais, datas; precisamos acrescentar persona/segmento? |
| Sentiment overview | `GET /api/dashboard/sentiment-analysis` | Net sentiment (Hero + trend) | [ ] | Confirmar payload e possibilidade de trend comparativo |
| Engagement trend | `GET /api/dashboard/engagement-trend` | Trendline principal | [ ] | Permite overlay com eventos? (caso não, ver item 2) |
| Audience demographics | `/api/dashboard/audience-*` | Painel Audience (secundário) | [ ] | Dados válidos para Community persona? |
| Content performance | `GET /api/dashboard/content-performance` | Content Efficiency (secundário) | [ ] | Devolve total engagement & posts? |
| Buzzer alerts | `GET /api/dashboard/buzzer/data` | Crisis alerts | [ ] | Confirma estrutura (title, severity, timestamp)? |
| Brands/Items | `/api/analytics/get-brand-*`, `/get-top-items` | Partnerships: brand momentum | [ ] | Payload inclui contagem temporal? (se não, ver item 2) |
| Instagram endpoints | `/api/dashboard/instagram/*` | Dados adicionais (opcional) | [ ] | Decidir se vamos usar; se sim, confirmar payload |

---

## 2. Endpoints novos / a desenvolver
| Necessidade | Descrição | Ação |
|-------------|-----------|------|
| Brand Health overview | Endpoint consolidado com score + drivers + risks | [ ] criar endpoint |
| Community wellbeing index | Estrutura (retention, CTS, engagement) | [ ] definir métricas e endpoint |
| Events overlay | Endpoint para listar eventos (campanhas/jogos) com timestamps | [ ] criar endpoint ou reutilizar fonte |
| Competitive benchmarks | Share of voice, sentiment gap, position index por concorrente | [ ] definir modelo de dados + endpoint |
| Sponsorship monetization | Revenue opportunity, activation performance, sponsor sentiment | [ ] especificar cálculos/dados + endpoint |
| Partnership momentum | Emerging brands, category interest (variação temporal) | [ ] definir estrutura |
| Audience segments list | Endpoint para listar segmentos predefinidos (car owners, etc.) com IDs | [ ] criar endpoint |
| Exports | Endpoints para gerar CSV/PDF (segment, pitch deck) | [ ] definir e implementar |

---

## 3. Fórmulas / KPIs compostos
| KPI | Dados necessários | Situação | OK? | Notas |
|-----|-------------------|----------|-----|-------|
| Brand Health Score | Sentiment, engagement, retention, awareness | [ ] confirmar fontes e pesos | [ ] | Sem awareness no schema – definir regra |
| Net Sentiment Trend | Sentiment positive/negative por período | Disponível | [ ] | Confirmar se API devolve períodos necessários |
| Community Wellbeing | Retention, CTS, support metrics | Parcial | [ ] | Definir formula com dados existentes |
| Competitive Position | Mentions por brand, sentiment gap | Não disponível | [ ] | Necessário criar dataset |
| Revenue Opportunity | Segment size, avg deal value | N/A | [ ] | Requires business input e storage |
| Activation Performance | Campanhas, uplift metrics | N/A | [ ] | Ver dados existentes / criar modelo |
| Emerging Brand Momentum | Mentions por período (brand detection) | Parcial | [ ] | Confirmar se detectamos marcas com timestamp |
| Influencer Alignment | Overlap audience, sentiment match | Parcial | [ ] | Confirmar dados de influenciadores (Community) |
| Content Efficiency | Engagement + posts count | Disponível | [ ] | Ver se endpoint fornece contagens |
| Retention/Churn | Audience retention data | Disponível | [ ] | Confirmar colunas usable |

---

## 4. Segmentação & Filtros
| Item | Descrição | Ação |
|------|-----------|------|
| Segment presets | Lista de segmentos (ex.: car owners, finance interest) com regras de agregação | [ ] definir e criar endpoint |
| Filter combinations | Validar limites (persona, canal, data, segmento) | [ ] confirmar viabilidade |
| Export actions | `POST /exports/*` para CSV/PDF com segmentos | [ ] implementar |

---

## Próximos passos
1. Backend preencher colunas “OK?” / “Notas” e devolver com feedback.  
2. Em paralelo, definir requisitos detalhados para endpoints novos (payloads, exemplos).  
3. Após validação, atualizar `api-reference-by-component.md` e `formula-reference.md` com status “OK/Em Desenvolvimento”.  
4. Designers só usam KPIs marcados como OK; restantes ficam etiquetados como “(em desenvolvimento)”.  
5. Atualizar `TASKS.md` e roadmap técnico conforme confirmarmos disponibilidade.
