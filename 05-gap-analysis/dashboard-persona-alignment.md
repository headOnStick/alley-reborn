# Gap Analysis - Dashboard & Persona Alignment

## Metadata
- **Foco da Análise**: Dashboard raiz do Alley (visão multi-persona)
- **Data de Análise**: 2025-10-11
- **Analisado por**: IA (Codex Assist)
- **Prioridade Geral**: Alta

---

## Contexto
Das auditorias do portal (`03-portal-audit/sitemap.md`) e das reuniões recentes (SLAM, Liga Portugal, alinhamento interno), surgiu um padrão: o dashboard atual mostra métricas genéricas (engagement) enquanto os KPIs diferenciadores (emoções, marcas, segmentos) ficam espalhados em níveis profundos. Clientes e equipa interna pedem uma narrativa clara por persona antes das demos de novembro.

**Relacionado a**:
- Análise de página: `03-portal-audit/sitemap.md`
- Reuniões: `02-meetings/2025-10-08-hoopers-slam/key-insights.md`, `02-meetings/2025-10-08-liga-portugal/key-insights.md`, `02-meetings/2025-10-13-internal-product/key-insights.md`
- Necessidades de clientes: `04-discovery-synthesis/insights-overview.md`

---

## Estado Atual

### O Que Existe Hoje
- Dashboard principal mistura cards de engagement e contadores genéricos sem contexto.
- KPIs proprietários (emoções, marcas, segmentos) estão em subníveis (2º/3º nível) e exigem múltiplos cliques e scroll extensivo.
- Não há thresholds (bom/mau), nem comparações temporais claras (MoM/YoY).
- Único layout para todos os perfis (CMO, sponsorship, community, social).

**Funcionalidades presentes**:
- Cards de overview (followers, likes, sentiment genérico) agrupados por canal.
- Gráficos lineares simples (engagement trends) sem interpretação.
- Links para tabs secundárias (Community, Content, Comments, Posts).

**KPIs mostrados**:
- Seguidores, likes, posts (valores absolutos).
- Score genérico de sentiment (única referência de emoção).

**Estrutura de informação**:
- Sidebar → Dashboard → cards horizontais + widgets empilhados.
- KPIs únicos (marcas, emoções detalhadas, segmentos) apenas em páginas filhas (`/analytics`, `/content`, `/comments`).

**Screenshot/Referência**: `03-portal-audit/screenshots/dashboard.png`

### Como Está Sendo Usado
- Usado de forma genérica para overview em demos iniciais.
- Equipa interna reporta dificuldade em “vender” valor porque o dashboard não mostra os insights diferenciadores (`02-meetings/2025-10-13-internal-product/transcript.md`).
- Clientes (SLAM, Liga) procuram indicadores acionáveis (segmentos, marcas, emoções) e não os veem rapidamente.

**Frequência de acesso**: Alta (primeira página após login).
**Tempo médio na página**: n/d (suposição de uso superficial em demos).
**Ações comuns**: Scroll rápido, clique em tabs secundárias para encontrar dados relevantes.

---

## Estado Desejado

### O Que Clientes Precisam

**Necessidades identificadas**:
1. **KPIs acionáveis na primeira dobra**
   - **Fonte**: `02-meetings/2025-10-08-hoopers-slam/key-insights.md`
   - **Por que é importante**: ajuda o CMO a provar valor a marcas não endémicas.
   - **Impacto de não atender**: perder oportunidade de demonstrar ROI único.

2. **Narrativas por persona (CMO, Sponsorship, Community, Social)**
   - **Fonte**: `02-meetings/2025-10-13-internal-product/key-insights.md`
   - **Importância**: cada comprador quer ver use cases específicos.
   - **Impacto**: demos menos eficazes; mensagem diluída.

3. **Trendlines e benchmarks**
   - **Fonte**: feedback interno + clientes (`02-meetings/2025-10-13-internal-product/transcript.md`)
   - **Importância**: interpretar se 8% engagement é bom ou mau.
   - **Impacto**: números desconectados; decisões subjetivas.

**Fluxo de trabalho ideal**:
1. CMO abre dashboard e vê KPIs únicos (emoções, brands, segmentos) com comparações temporais.
2. Seleciona persona (ou dashboard predefinido) e recebe narrativa/insights correspondentes.
3. Exporta segmentos ou gera report para campanhas/pitches sem sair da página inicial.

### Regras de Negócio Aplicáveis
1. **Personas definem o storytelling**
   - **Fonte**: sessão interna – `02-meetings/2025-10-13-internal-product/transcript.md`
   - **Implicação**: dashboards configuráveis ou predefinidos por buyer.

2. **KPIs únicos devem estar acima da dobra**
   - **Fonte**: reuniões com SLAM e Liga (`key-insights`)
   - **Implicação**: reorganizar layout e priorizar dados proprietários.

---

## Análise de Gap

### Gap 1: Dashboard genérico sem foco em valor único

#### Categoria
Funcionalidade mal implementada / Navegação inadequada

#### Descrição do Gap

**Estado Atual**:
- Cards e gráficos focam em métricas genéricas de engagement.
- Ausência de thresholds e de storytelling por persona.
- KPIs diferenciadores espalhados em páginas secundárias.

**Estado Desejado**:
- Dashboard apresenta, na primeira dobra, os principais KPIs proprietários (emoções, marcas, segmentos, saúde da marca, oportunidades de patrocínio).
- Layout segmentado ou configurável por persona.
- Trendlines e comparações automáticas, com indicadores vermelho/verde.

**Diferença**:
- Falta de clareza quanto ao valor único do produto; necessidade de reorganização estrutural e visual.

#### Impacto

**Severidade**: Alta

**Afeta**:
- CMOs, Sponsorship Managers, Community Managers, Social Media Managers.
- Demos comerciais (NYC, Liga Portugal Summit).

**Consequências**:
- **Usuário**: dificuldade em extrair insights acionáveis rapidamente; confiança reduzida.
- **Negócio**: perda de “wow effect” em pitches; risco de churn no piloto; mensagens menos convincentes para marcas não endémicas.

#### Evidências

**Feedback de clientes**:
> “Preciso de quantificar interesses automóvel/financeiro para a proposta” – SLAM  
> “Quero entender fãs por app/fantasy com social data” – Liga Portugal
– Ver `02-meetings/2025-10-08-hoopers-slam/key-insights.md`, `02-meetings/2025-10-08-liga-portugal/key-insights.md`.

**Observação na análise**:
- KPIs únicos estão em 2º/3º nível (`03-portal-audit/sitemap.md`); screenshot `dashboard.png`.

#### Causa Raiz

Possíveis causas:
- [x] Prioridade histórica em métricas genéricas (herdado de MVP).
- [x] Falta de Product/UX dedicado.
- [ ] Limitação técnica de APIs.
- [ ] Decisão explícita de negócio.

---

## Recomendações

### Solução Proposta
1. **Reestruturar dashboards**:
   - Criar tabs raiz: Brand Health, Competitive Insight, Sponsorship Value, Partnership Opportunities, Engagement Support (reforçado na sessão interna).
   - Dashboard principal mostra KPIs únicos por persona (configurações predefinidas ou selector rápido).
   - Introduzir trendlines, thresholds e comparações automáticas.

2. **Narrativa por Persona**:
   - One-pager/dashboards específicos para CMO, Sponsorship, Community, Social (alinhado com ações em `02-meetings/2025-10-13-internal-product/action-items.md`).

3. **Exportação/Segmentação rápida**:
   - Botões para gerar segmentos/reports diretamente do dashboard inicial (apoia demandas de SLAM e Liga).

### Benefícios Esperados
- Demonstração clara de valor único já na primeira interação.
- Melhor alinhamento com dores dos clientes (monetização, fan intelligence, patrocínios).
- Suporte direto às demos de novembro (NYC, Liga Summit) e a pilotos futuros.

### Riscos
- **Implementação parcial**: apenas reorganizar layout sem ajustar dados → risco de parecer “mais do mesmo”.

### Dependências
- Necessidade de Product Designer/PM (ação já listada nas reuniões internas).
- Inventário de KPIs e dados (ligação com tarefas pendentes do Sprint 2 e 4).

### Ações Recomendadas
- [ ] Definir narrativa e KPIs-chave por persona (Produto + Comercial).
- [ ] Desenhar protótipos de dashboard reestruturado com UX dedicado.
- [ ] Validar com clientes piloto (Liga Portugal, SLAM) antes das demos.
- [ ] Implementar trendlines/benchmarks e exportação de segmentos nas APIs.

### Métricas de Sucesso
- % de demos em que o dashboard gera “insight único” nos primeiros 3 minutos (feedback qualitativo).
- Taxa de conversão de piloto após demos (baseline atual: n/d).
- Tempo médio para identificar oportunidades de patrocínio dentro da plataforma (reduzir).

---

## Próximos Passos
- [ ] Agendar workshop Produto/Comercial para priorizar KPIs por persona.
- [ ] Criar protótipos (Figma) do novo dashboard (responsável: Produto/UX).
- [ ] Calendarizar piloto com Liga Portugal e SLAM para validar narrativa.
- [ ] Sincronizar com Sprint 4 tasks para conectar insights → gap → proposta (ver `TASKS.md`).

---

## Rastreabilidade

**Baseado em**:
- `/03-portal-audit/sitemap.md`
- `/02-meetings/2025-10-08-hoopers-slam/key-insights.md`
- `/02-meetings/2025-10-08-liga-portugal/key-insights.md`
- `/02-meetings/2025-10-13-internal-product/key-insights.md`
- `/04-discovery-synthesis/insights-overview.md`

**Alimenta**:
- `/05-gap-analysis/` (roadmap de gaps)
- `/06-future-product/page-structures/` (design futuro)
- `/06-future-product/information-architecture.md`

**Validado por**:
- A validar com André Costa (CEO) e Ricardo Presa (Diretor de Vendas) após protótipo inicial.

**Atualizado**:
- 2025-10-11 — Criação da análise inicial (IA Codex)
