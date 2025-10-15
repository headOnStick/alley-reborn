# Proposta de Redesenho - Dashboard Multi-Persona

## Metadata
- **Página**: Dashboard (Home)
- **Rota proposta**: `/dashboard`
- **Data da Proposta**: 2025-10-11
- **Versão**: 0.1
- **Status**: Draft

---

## Referências

### Análise do Estado Atual
- **Análise de página atual**: `03-portal-audit/sitemap.md` (secção “Dashboard”)
- **Gap analysis**: `05-gap-analysis/dashboard-persona-alignment.md`
- **Screenshot atual**: `03-portal-audit/screenshots/dashboard.png`

### Feedback de Clientes
**Reuniões relacionadas**:
- Hoopers x SLAM — `02-meetings/2025-10-08-hoopers-slam/key-insights.md`  
  > “Preciso de provar valor para marcas não endémicas.”  
- Hoopers <> Liga Portugal — `02-meetings/2025-10-08-liga-portugal/key-insights.md`  
  > “Quero cruzar dados de app/fantasy com social para entender a audiência.”  
- Hoopers @Meeting Room (interno) — `02-meetings/2025-10-13-internal-product/key-insights.md`  
  > “Temos de mostrar KPIs únicos por persona logo acima da dobra.”

**Necessidades atendidas**:
- Monetizar inteligência de fãs para marcas não endémicas (`04-discovery-synthesis/insights-overview.md`)
- Fornecer visão integrada da audiência (social + owned data)
- Dar suporte a decisões comerciais e community management

**Regras de negócio aplicadas**:
- Dashboards devem ser orientados a persona (CMO, Sponsorship, Community, Social)
- KPIs proprietários precisam de contexto (trend, benchmark, ação)

---

## Contexto e Justificativa

### Por Que Redesenhar Esta Página
O dashboard atual destaca métricas genéricas (followers, likes, engagement) e esconde os “insights únicos” em abas secundárias. Clientes e equipa interna não conseguem demonstrar rapidamente o valor diferenciado da Alley, reduzindo o impacto das demos e dificultando a venda para marcas não endémicas.

**Problemas principais**:
1. KPIs proprietários dispersos (marcas, emoções, segmentos) só aparecem em 2º/3º nível do produto.
2. Ausência de narrativa por persona: todos veem a mesma mistura de dados.
3. Falta de contexto (trendlines, thresholds) — difícil saber se 8% é bom ou mau.

**Impacto atual**:
- **Usuários**: não encontram rapidamente oportunidades acionáveis → navegação extensa.
- **Negócio**: demos com “wow effect” baixo, difícil fechar patrocínios/pilotos.

### Objetivos do Redesenho
**Objetivos primários**:
1. Expor KPIs proprietários acima da dobra (Métrica de sucesso: 80% dos insights “únicos” encontrados em <30s durante demos).
2. Fornecer narrativas por persona (Métrica: cada persona tem ≥1 fluxo acionável identificado nos testes com clientes piloto).

**Objetivos secundários**:
- Incluir trendlines/benchmarks automáticos (reduzir dúvidas sobre “bom vs. mau”).
- Permitir exportar segmentos/insights diretamente do dashboard.

---

## Proposta de Redesenho

### Objetivo da Página (Redesenhado)
**Para quem**: decisores de marketing, patrocínios, community e social media de organizações esportivas.  
**Para quê**: identificar, em segundos, oportunidades acionáveis (segmentos, marcas, campanhas) e saúde da audiência.  
**Quando**: início de cada sessão (pós-login) e durante demos comerciais.

### Princípios de Design Aplicados
1. **Foco em valor único**  
   - **Aplicação**: KPIs proprietários (emoções, marcas, segmentos) são hero metrics com contexto visual.

2. **Narrativa por persona**  
   - **Aplicação**: selector de persona reorganiza cards/dashboards para CMO, Sponsorship, Community ou Social; tooltips e “Next Best Action” contextualizam.

3. **Contexto antes de detalhe**  
   - **Aplicação**: cada KPI mostra trendline, comparação temporal e call-to-action (ex.: “Exportar segmento”).

4. **Progressive disclosure**  
   - **Aplicação**: drill-down mantém-se disponível via “View details” sem poluir a visão inicial.

---

## Estrutura de Informação

### Layout Proposto
```
┌──────────────────────────────────────────────┐
│ Header                                       │
│ ├ Persona Switcher (CMO | Sponsorship | …)   │
│ ├ Filtros: Canal, Segmento, Data Range        │
│ └ Contexto rápido (Total audiências, período) │
├──────────────────────────────────────────────┤
│ Hero KPIs (4 cards dinâmicos)                │
│ [Brand Health] [Emerging Brands] [Net Sentiment] [Revenue Signals] │
├──────────────────────────────────────────────┤
│ Visualização principal                       │
│ [Trendline multi-série + eventos]            │
│ [Comparação com período anterior | metas]    │
├───────────────┬──────────────────────────────┤
│ Spotlight     │ Audience & Segments          │
│ [Campanha/Brand insight]                     │
│ [Top oportunidades / alertas]                │
│              │ [Segmentos-chave]             │
│              │ [Export & Next Steps]         │
├───────────────┴──────────────────────────────┤
│ Secondary Insights                           │
│ [Content Performance snapshot]               │
│ [Community health / Growth KPIs]             │
└──────────────────────────────────────────────┘
```

### Hierarquia de Informação

**Nível 1 – Primário (above the fold)**:
- Persona selector + filtros.
- 4 Hero KPIs (Brand Health Score, Emerging Brand Momentum, Net Sentiment Trend, Revenue Opportunity Forecast).
- Visualização principal (trendline com eventos e thresholds).

**Rationale**: atende demandas de CMO/Sponsorship, prova valor único, suporta decisões imediatas.

**Nível 2 – Secundário (sem scroll adicional)**:
- Spotlight (ex.: “Nike x SLAM — Momentum -12% vs. 30d, ação sugerida”).
- Audience & Segments (top 3 segmentos com quick actions).

**Rationale**: orienta próximos passos e personaliza campanhas/ações.

**Nível 3 – Suporte (abaixo do fold/colapsável)**:
- Content Performance snapshot (melhores temas, formatos).
- Community/owned channels health (retention, growth, app/fantasy integrados).

**Rationale**: detalha insights de suporte para community/social managers sem poluir visão inicial.

---

## KPIs e Métricas

### KPIs Principais (Destaque Alto)
1. **Brand Health Score**  
   - **Por que é prioritário**: CMO quer saber se a marca está em alta/baixa pós-eventos (Liga Portugal, feedback interno).  
   - **Formato**: Card com score (0-100), trendline mini, benchmark vs. período anterior.  
   - **Ação**: “Ver eventos que impactaram” / “Exportar relatório para patrocinador”.

2. **Emerging Brand Momentum**  
   - **Justificativa**: SLAM precisa identificar marcas não endémicas com crescimento (Toyota, bancos).  
   - **Formato**: Card com top 3 marcas, % variação, botão “Ver detalhes”.  
   - **Ação**: “Gerar lista de marcas para pitch”.

3. **Net Sentiment Trend (Fans)**  
   - **Justificativa**: Community/CMO precisa ver como emoções evoluem (negativo/positivo).  
   - **Formato**: Card + sparkline + threshold (verde/amarelo/vermelho).  
   - **Ação**: “Abrir segmentos críticos” / “Avisar equipa de community”.

4. **Revenue Opportunity Forecast**  
   - **Justificativa**: Patrocínios querem potencial $$$ dos segmentos (dados internos + SLAM).  
   - **Formato**: Card hero com faixa (xx – yy €), variação MoM.  
   - **Ação**: “Exportar segmento” / “Criar campanha”.

### Métricas Secundárias
- Audience Growth vs. owned channels (app/fantasy/users).
- Campaign Impact Score (comparação de campanhas ativas).
- Engagement Efficiency (posts vs. engagement, highlight para SLAM).

### Drill-down
- Lista detalhada de marcas com correlação (positiva/negativa).
- Segmentos emergentes (car owners, finance, family) com handles.
- Timeline com eventos (jogos, campanhas, PR crises) + sentiment breakdown.

### Comparação com Estado Atual

| KPI                         | Estado Atual                         | Estado Proposto                     | Mudança                |
|----------------------------|--------------------------------------|-------------------------------------|------------------------|
| Brand Health               | Não existe                           | Hero metric com trendline           | ↑↑ maior destaque      |
| Emerging Brands            | Escondido em abas                    | Hero metric + spotlight             | ↑↑ evidência direta    |
| Net Sentiment              | Gráfico genérico                     | Card + thresholds + CTA             | ↑ clareza/ação         |
| Revenue Opportunity        | Não existe                           | Card + exportação                   | ↑ adiciona valor       |
| Followers/Likes genéricos  | Hero/primeiro plano                  | Secundário (ou removido)            | ↓ menos ruído          |
| Drill-down por post        | Em destaque                          | Aceso via “View details”            | ↓ foco em valor único  |

---

## Componentes UI Sugeridos

### Componentes Principais
1. **Persona Switcher (Segmented Control)**  
   - **Propósito**: Alterna layout/KPIs para CMO, Sponsorship, Community, Social.  
   - **Dados**: altera cards prioritários e quick actions.  
   - **Quantidade**: 1 (global).  
   - **Localização**: Header.  
   - **Existe hoje?**: Não → criar componente.

2. **Hero Metric Card v2**  
   - **Propósito**: Destacar KPI com trend e CTA.  
   - **Dados**: Score/percentual + variação + ícone.  
   - **Quantidade**: 4 (dinâmicos por persona).  
   - **Localização**: Primeira linha.  
   - **Existe hoje?**: Sim (cards), mas precisa adaptar (trendline, thresholds, CTA).

3. **Trendline + Event Overlay**  
   - **Propósito**: Exibir evolução do KPI vs. eventos.  
   - **Dados**: Sentiment/Brand health vs. tempo, eventos (campanhas, jogos).  
   - **Quantidade**: 1 principal.  
   - **Localização**: Centro (baixo dos hero cards).  
   - **Existe hoje?**: Gráfico básico -> adaptar.

4. **Segment Spotlight**  
   - **Propósito**: Destacar segmento/marca com insight e ação.  
   - **Dados**: Nome, variação, impacto, CTA (exportar).  
   - **Quantidade**: 1 (rotativo).  
   - **Localização**: Coluna esquerda (second row).  
   - **Existe hoje?**: Não → criar.

5. **Audience Segments Panel**  
   - **Propósito**: Mostrar top segmentos com quick actions (ver detalhes/exportar).  
   - **Dados**: Segmento, tamanho, valor potencial, sentimento.  
   - **Quantidade**: 1 painel.  
   - **Localização**: Coluna direita (second row).  
   - **Existe hoje?**: Parcial (tabelas) → adaptar.

### Componentes de Suporte
- **Content Snapshot cards** (resumo de temas/performance).
- **Community Health gauge** (retention, churn, owned channels).
- **Alerts/Next Best Actions list** (integra com notifications).

### Novos Componentes Necessários
1. **Persona Switcher**  
   - **Por que**: garante narrativa específica por perfil.  
   - **Especificação**: segmented control, default CMO, persiste preferência.  
   - **Prioridade**: Alta.

2. **Segment Spotlight**  
   - **Por que**: traduz insights em ações claras (pitch, campanha).  
   - **Especificação**: card largo com insight, variação, CTA duplo.  
   - **Prioridade**: Alta.

3. **Quick Exports Drawer**  
   - **Por que**: facilitar export de segmentos/relatórios sem mudar de página.  
   - **Especificação**: drawer modal com formatos (CSV, PPT, integração CRM).  
   - **Prioridade**: Média.

---

## Navegação e Fluxo

### Como Chegar a Esta Página
**Primário**: Sidebar principal > “Dashboard” (default pós-login).  
**Secundário**: Link “Voltar ao overview” em todas as abas internas (Community, Content, etc.).

### Interações Principais
1. Selecionar persona → hero KPIs e painéis ajustam automaticamente.  
2. User clica em hero card > abre modal com detalhamento + ações (ver eventos, exportar).  
3. Segment Spotlight CTA “Gerar pitch deck” → utiliza Quick Exports Drawer.  
4. Audience Panel “Ver detalhes” → leva para aba segmentação (com filtros aplicados).  
5. Alerts list → linka diretamente para componentes relevantes (ex.: “Influencer X trending” → abre drill-down).

### Fluxo Pós-Ação
Exemplo (Sponsorship persona):
1. Seleciona persona “Sponsorship”.  
2. Vê “Emerging Brand Momentum” negativo para Nike.  
3. Click CTA “Explorar eventos” → trendline com overlay de campanhas.  
4. Gera relatório para equipa comercial via Quick Export.  
5. Marca follow-up em CRM (integração futura).

---

## Conteúdo e Mensagens

### Mensagens-Chave (Above the fold)
- “Brand health está +8% vs. último mês — principal driver: campanha #PlayGreen”.
- “Emerging Brands: Reebok (+23%), Toyota (+18%), Novo Banco (+12%).”
- “Net sentiment caiu 5 pts após jogo 10/10 — veja eventos críticos.”
- “Revenue Opportunity: €2,4M–€3,1M (Segmento: “Basketball Dads with EV interest”).”

### Next Best Actions (Persona-specific)
- **CMO**: “Enviar resumo executivo para board”, “Ver campanhas com maior lift”.  
- **Sponsorship**: “Gerar pitch deck para Toyota”, “Comparar sponsors emergentes”.  
- **Community**: “Abrir segmento Haters+Discord 4AM”, “Agendar Q&A com influencers”.  
- **Social**: “Ativar plano de posts com humor (sentiment ↑)”, “Identificar top 10 conteúdos UGC”.

### Microcopy / Tooltips
- Hero cards exibem “vs. período anterior”, “benchmark vs. mercado” (quando disponível).  
- Tooltips explicam metodologia (ex.: “Brand Health combina sentiment + engagement + reach ponderado”).  
- Alerts explicam regra de disparo (“Alerta gerado após queda >10 pts no sponsor sentiment em 7 dias”).

---

## Integrações e Dados

### Fontes Necessárias
- Dados sociais existentes (Instagram, Twitter, TikTok — roadmap).  
- Owned data: app/fantasy/ticketing (Liga Portugal).  
- CRM/marketing automation (para export e quick actions).  
- Event tracking (campanhas, jogos, PR).

### Requisitos Técnicos
- Endpoint consolidado para hero KPIs com filtros (tempo, canal, persona).  
- Endpoint para segmentos (filtros + export).  
- Cálculo de Brand Health & Revenue Forecast (definir fórmulas com Product/Data).  
- Logging de ações (qual CTA foi executado).

### Dependências
- Tasks pendentes do Sprint 2 (inventário KPIs/forms) para garantir dados completos.  
- Priorização de implementação com equipa de Engenharia (André Rocha).  
- Integração com Quick Export / CRM (roadmap).

---

## Métricas de Sucesso do Redesenho
- Tempo médio para o utilizador encontrar “insight único” < 30s (testes de usabilidade).  
- Número de demos que usam dashboards personalizados (meta ≥ 90%).  
- Taxa de conversão de piloto após demos (baseline TBD).  
- Feedback NPS das personas internas (CMO, Sponsorship, Community, Social).  
- Aumento do uso de exportações de segmentos vs. baseline.

---

## Roadmap de Implementação
1. **Discovery detalhado (Semana 1-2)**  
   - Workshop Produto/Comercial para priorizar KPIs por persona.  
   - Definir fórmulas de Brand Health & Revenue Forecast com equipa de dados.

2. **Design & protótipo (Semana 2-3)**  
   - Criar wireframes (low/high fidelity) → validar com clientes piloto (Liga, SLAM).  
   - Iterar microcopy/tooltips/ações.

3. **Implementação faseada (Semana 4-6)**  
   - Fase 1: Persona switcher + hero cards + trendline + spotlight.  
   - Fase 2: Audience panel + quick exports + alerts.  
   - Fase 3: Integrações avançadas (CRM, event overlays, benchmarks externos).

4. **Teste & rollout (Semana 7)**  
   - Testes internos (QA + demo scripts).  
   - Beta com clientes piloto.  
   - Rollout geral + acompanhamento de métricas.

5. **Iteração contínua (Pós-lançamento)**  
   - Ajustar KPIs conforme feedback.  
   - Expandir para novos canais (TikTok, Discord).

---

## Próximas Ações
- [ ] Agendar workshop Produto/Comercial (responsável: André Costa + Ricardo).
- [ ] Validar fórmulas de KPIs com André Rocha (dados/engenharia).
- [ ] Produzir protótipo inicial em Figma (precisa design/UX).  
- [ ] Agendar sessões de feedback com Liga Portugal e SLAM.  
- [ ] Atualizar `TASKS.md` (Sprint 4) com milestones de redesign.

---

## Rastreabilidade
- **Baseado em**: `03-portal-audit/sitemap.md`, `05-gap-analysis/dashboard-persona-alignment.md`, `02-meetings/...` (SLAM, Liga, interna), `04-discovery-synthesis/insights-overview.md`.  
- **Alimenta**: `05-gap-analysis/` (fechamento), roadmap técnico (Engineering), demos (NYC/Liga Summit).  
- **Validado por**: a validar com André Costa & Ricardo Presa após protótipo.  
- **Atualizado**: 2025-10-11 — 1ª versão (Draft).
