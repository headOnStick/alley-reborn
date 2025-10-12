# Objetivo do Projeto Alley-Reborn

**Última atualização**: 2025-10-10

---

## Contexto

**Alley** é uma plataforma SaaS de analytics para Instagram que usa IA (scraping, computer vision, NLP, sentiment analysis) para fornecer insights sobre audiências, conteúdo e engagement. O portal web serve clientes B2B (agências, marcas) para monitorização de canais de Instagram.

**Problema identificado**: O portal tem **capacidades técnicas funcionais** mas a **estrutura de informação está desalinhada com necessidades reais de clientes**, dificultando descoberta de insights críticos e tomada de decisão.

**Estado atual (2025-10-10)**:
- ✅ Sprint 1 (Setup) - Completo
- ✅ Sprint 2 (Auditoria Portal) - Completo (6 páginas, 25 tabs, 26 screenshots, ~165 KPIs documentados)
- ⏳ Sprint 3 (Processar Reuniões) - Pendente
- ⏳ Sprint 4 (Gap Analysis & Síntese) - Pendente
- ⏳ Sprint 5 (Proposta de Redesenho) - Pendente

---

## Objetivo Principal

**Redesenhar a Arquitetura de Informação (IA) do portal Alley** para alinhar estrutura, navegação e apresentação de dados com necessidades reais de clientes, maximizando descoberta de insights e eficiência de decisões.

### O que **É** este projeto:
- ✅ Redesenho de Arquitetura de Informação (IA)
- ✅ Reorganização de estrutura de dados e navegação
- ✅ Priorização de KPIs e métricas por relevância de negócio
- ✅ Discovery baseado em feedback de clientes reais
- ✅ Proposta implementável para equipa de desenvolvimento

### O que **NÃO é** este projeto:
- ❌ Redesenho visual/UI (mantém design system atual)
- ❌ Implementação técnica (apenas proposta)
- ❌ Desenvolvimento de novas features funcionais
- ❌ Alteração de capacidades de backend/APIs

---

## Deliverables Finais

### 1. Documentação de Discovery
- **Auditoria Completa do Portal** (`/03-portal-audit/`)
  - Sitemap técnico com 100% de páginas, tabs, KPIs documentados
  - Screenshots de todas as views
  - Inventário de métricas e funcionalidades

- **Análise de Reuniões com Clientes** (`/02-meetings/`)
  - Transcrições processadas
  - Key insights extraídos
  - Necessidades e pain points identificados

### 2. Gap Analysis (`/04-synthesis/`)
- Comparação: "O que o portal oferece" vs "O que clientes precisam"
- Priorização de gaps por impacto e frequência
- Identificação de informação crítica escondida ou ausente

### 3. Proposta de Redesenho (`/05-redesign-proposal/`)
- Nova estrutura de informação justificada
- Wireframes de navegação (não UI detalhado)
- Mapeamento de KPIs priorizados por contexto
- Requirements técnicos para implementação
- Plano de transição e migration path

---

## Critérios de Sucesso

### Para Clientes (Usuários Finais):
1. **Time-to-insight reduzido**: Informação crítica acessível em ≤3 clicks
2. **Descoberta intuitiva**: Não é necessário "saber onde procurar"
3. **Contexto adequado**: KPIs apresentados quando são relevantes
4. **Redução de noise**: Métricas secundárias não obscurecem insights principais

### Para o Negócio:
1. **Alinhamento com feedback real**: Proposta baseada em necessidades documentadas
2. **Implementável**: Requirements claros e factíveis com stack atual
3. **Escalável**: Estrutura suporta adição futura de canais/features
4. **Mensurável**: KPIs de sucesso definidos para validar pós-implementação

### Para a Equipa de Desenvolvimento:
1. **Clareza técnica**: O que mudar, onde, e porquê
2. **Não-disruptivo**: Aproveita componentes e APIs existentes
3. **Faseável**: Pode ser implementado incrementalmente

---

## Princípios de Design (IA)

1. **User-Centered**: Decisões baseadas em necessidades reais de clientes, não em estrutura técnica
2. **Context-Aware**: Informação apresentada no contexto de uso (não dumps de dados)
3. **Progressive Disclosure**: Começar com overview, permitir drill-down para detalhes
4. **Consistency**: Padrões de navegação e apresentação consistentes entre páginas
5. **Scannability**: Facilitar scan visual rápido para identificar padrões e anomalias

---

## Fases do Projeto (High-Level)

### Fase 1: Auditoria e Discovery ✅
**Objetivo**: Entender "O que existe" (portal atual) e "O que é necessário" (feedback de clientes)

**Sprints**:
- ✅ Sprint 1 - Setup e Contexto (estrutura de documentação)
- ✅ Sprint 2 - Auditoria Técnica do Portal (sitemap, screenshots, inventário)
- ⏳ Sprint 3 - Processar Reuniões com Clientes (transcrições → insights)

### Fase 2: Análise e Síntese ⏳
**Objetivo**: Identificar gaps e priorizar necessidades

**Sprint**:
- ⏳ Sprint 4 - Gap Analysis, Síntese de Necessidades, Análise de Código Frontend

### Fase 3: Proposta de Redesenho ⏳
**Objetivo**: Criar proposta implementável de nova IA

**Sprint**:
- ⏳ Sprint 5 - Proposta de Redesenho (wireframes, requirements, plano)

---

## Stakeholders

### Product Owner
- **André Rocha** (`arocha@hoopers.club`)
- Decisor final, validação de marcos, fornece contexto de negócio
- **Ver**: `/01-context/stakeholders.md` para detalhes de comunicação

### Clientes (Indiretos)
- Usuários finais do portal (agências, marcas)
- Representados via reuniões processadas e feedback de André

### Equipa de Desenvolvimento (Futura)
- Implementadores da proposta após aprovação
- Requer proposta clara, implementável, com requirements técnicos

---

## Métricas de Progresso

**Discovery Phase**:
- ✅ Páginas auditadas: 6/6 (100%)
- ✅ Tabs mapeadas: 25/25 (100%)
- ✅ Screenshots: 26/26 (100%)
- ✅ KPIs documentados: ~165 KPIs inventariados
- ⏳ Reuniões processadas: 0/1+ (Hoopers x SLAM disponível)

**Analysis Phase**:
- ⏳ Gap analysis completa: 0%
- ⏳ Necessidades sintetizadas: 0%
- ⏳ Código frontend analisado: 0% (Git repo disponível)

**Proposal Phase**:
- ⏳ Nova IA proposta: 0%
- ⏳ Wireframes criados: 0%
- ⏳ Requirements técnicos definidos: 0%

---

## Recursos Disponíveis

Para informação detalhada sobre recursos técnicos, ver:
- **Credenciais de Acesso**: `/01-context/access-credentials.md`
- **Recursos Técnicos (Git, Attio, Ferramentas)**: `/01-context/resources.md`
- **Stakeholders e Comunicação**: `/01-context/stakeholders.md`
- **Glossário de Termos**: `/01-context/glossary.md`
- **Overview da Plataforma**: `/01-context/platform-overview.md`
- **Data Schema (Base de Dados)**: `/01-context/data-schema.md`
- **API Reference (138 endpoints)**: `/01-context/api-reference.md`

Para tarefas detalhadas e progresso operacional:
- **Tarefas e Status**: `/TASKS.md`
- **Instruções do Sistema**: `/CLAUDE.md`

---

## Referências Rápidas

### Estrutura de Documentação
```
/Alley-Reborn/
├── /01-context/          # Contexto e recursos (este ficheiro)
├── /02-meetings/         # Reuniões com clientes processadas
├── /03-portal-audit/     # Auditoria completa do portal (✅ completo)
├── /04-synthesis/        # Gap analysis e síntese
├── /05-redesign-proposal/# Proposta final de redesenho
└── /templates/           # Templates de análise
```

### Páginas do Portal Mapeadas (Sprint 2)
1. Dashboard (`/dashboard`) - Overview multi-canal
2. Channel Detail (`/dashboard/channel/{id}`) - 3 tabs (Community, Post, Alerts)
3. Community (`/analytics`) - 6 tabs de análise de audiência
4. Channel (`/channel`) - 4 tabs de análise de canal
5. Posts (`/posts`) - 3 tabs de análise de conteúdo
6. Alerts (`/alerts`) - Configuração de alertas e notificações

**Ver**: `/03-portal-audit/sitemap.md` para documentação detalhada (1,546 linhas)

---

**Este ficheiro define o objetivo, contexto, deliverables e princípios do projeto. Para tarefas operacionais, ver `/TASKS.md`. Para recursos técnicos, ver ficheiros em `/01-context/`.**
