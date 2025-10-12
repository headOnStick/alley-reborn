# Alley-Reborn Discovery Project

**Project Type**: Product Discovery & Redesign
**Status**: Sprint 2 - Portal Audit (Complete ✅) | Sprint 3 Ready
**Last Updated**: 2025-10-10 23:50

---

## Quick Navigation

### 🎯 Start Here (For AI)
1. **[/01-context/objective.md](./01-context/objective.md)** - Entenda o contexto e objetivos do projeto
2. **[TASKS.md](./TASKS.md)** - Veja qual tarefa está ativa e o progresso (50% completo)
3. **[CLAUDE.md](./CLAUDE.md)** - Instruções completas de como trabalhar neste projeto

### 📂 Project Structure

```
/Alley-Reborn/
│
├── CLAUDE.md              # Instruções de sistema para IA
├── TASKS.md               # Tracking de tarefas e progresso
├── README.md              # Este ficheiro (mapa de navegação)
│
├── 01-context/            # ✅ Contexto e informações base (COMPLETO)
│   ├── objective.md           # Objetivos e contexto do projeto
│   ├── platform-overview.md   # Overview técnico da plataforma
│   ├── data-schema.md         # Schema completo da BD (4 entidades, ~165 KPIs)
│   ├── api-reference.md       # API Reference (138 endpoints, 19 categorias)
│   ├── access-credentials.md  # Credenciais de acesso
│   ├── glossary.md            # Termos e definições
│   ├── resources.md           # Git, Attio, ferramentas técnicas
│   └── stakeholders.md        # André Rocha, comunicação
│
├── 02-meetings/           # ⏳ Reuniões com clientes (TODO)
│   ├── INDEX.md               # Lista de todas as reuniões
│   ├── insights-summary.md    # Síntese consolidada
│   └── [YYYY-MM-DD]-[tema]/   # Uma pasta por reunião
│       ├── attio-link.md
│       ├── transcript.md
│       ├── key-insights.md
│       └── action-items.md
│
├── 03-portal-audit/       # ✅ Análise do portal atual (COMPLETO)
│   ├── sitemap.md             # ✅ Mapa completo (1,546 linhas, 6 páginas, 25 tabs)
│   └── screenshots/           # ✅ 26 screenshots capturados
│
├── 04-synthesis/          # ⏳ Síntese de descobertas (TODO)
│   ├── user-needs.md          # Necessidades dos clientes
│   ├── pain-points.md         # Problemas identificados
│   ├── business-rules.md      # Regras de negócio
│   └── opportunities.md       # Oportunidades
│
├── 05-redesign-proposal/  # ⏳ Proposta de redesenho (TODO)
│   ├── product-vision.md
│   ├── page-structures/
│   ├── information-architecture.md
│   ├── roadmap.md
│   └── requirements.md
│
└── templates/             # ✅ Templates de análise (COMPLETO)
    ├── meeting-analysis/
    ├── page-analysis/
    └── gap-analysis/
```

---

## What Is This Project?

### The Platform: Alley
Alley é uma plataforma de métricas avançadas de marketing através de análise de Instagram usando AI:
- Scraping de posts
- Análise de imagens
- Análise sentimental de comentários
- Análise de perfis de comentadores
- Geração de métricas proprietárias

### The Problem
O portal está em fase alfa funcional, com todos os dados necessários, mas a estrutura de informação não está alinhada com as regras de negócio e necessidades dos clientes.

### The Goal
Redesenhar a estrutura do produto (páginas, navegação, hierarquia de informação, KPIs) baseado em:
1. Feedback real de clientes (reuniões transcritas)
2. Auditoria completa do estado atual
3. Regras de negócio identificadas

### The Approach
Discovery estruturado em 5 sprints:
1. **Setup & Context** - Criar base de documentação
2. **Portal Audit** - Inventariar estado atual completo
3. **Process Meetings** - Extrair insights de clientes
4. **Synthesis & Gap Analysis** - Cruzar dados e identificar gaps
5. **Future Proposal** - Propor redesenho

---

## Current Status

### Progress: 50% (10/20 tasks completed)

**Current Sprint**: Sprint 3 - Processar Reuniões (TODO)
**Last Completed Sprint**: Sprint 2 - Auditoria do Portal ✅

**Completed** (Sprint 1 & 2):
- ✅ **Sprint 1 COMPLETO** - Setup e Contexto
  - Estrutura de pastas criada
  - 8 ficheiros de contexto em `/01-context/`
  - Templates de análise criados
  - CLAUDE.md, TASKS.md, README.md estruturados
  - **Descobertas**: `data-schema.md` + `api-reference.md` (138 endpoints)

- ✅ **Sprint 2 COMPLETO** - Auditoria do Portal
  - 6 páginas principais mapeadas
  - 25 tabs navegadas e documentadas
  - 26 screenshots capturados
  - ~165 KPIs identificados
  - sitemap.md completo (1,546 linhas)
  - Channel Detail page descoberta

**Next Steps**:
- Sprint 3: Processar reunião Hoopers x SLAM (Attio link disponível)
- Sprint 4: Gap analysis e síntese
- Sprint 5: Proposta de redesenho

---

## Key Resources

### Portal Access
- **URL**: https://stg-fe-alley-hooper.hoopers.club/login
- **Details**: Ver `/01-context/access-credentials.md`

### Meetings
- **Platform**: Attio
- **First Meeting**: https://attio.link/call/Call-Hoopers-x-SLAM-44J51ILV935ZPAgkjgYQE/transcript

### Stakeholder
- **Contact**: André Rocha (arocha@hoopers.club)
- **Details**: Ver `/01-context/stakeholders.md`

### Code Repository
- **Git**: `git@bitbucket.org:hoopersclub/fe-alley-hooper.git`
- **Details**: Ver `/01-context/resources.md`

---

## How to Use This Documentation

### For AI Agents
1. **Start every session** by reading:
   - `/01-context/objective.md` for context
   - `TASKS.md` for current task and progress
   - `CLAUDE.md` for process instructions

2. **Execute task** following processes in CLAUDE.md

3. **Document results** in appropriate directories

4. **Update TASKS.md** with progress

5. **Ask user** when information is missing (never invent)

6. **Refer to context files**:
   - `/01-context/stakeholders.md` for communication guidelines
   - `/01-context/resources.md` for technical resources
   - `/01-context/access-credentials.md` for credentials

### For Humans
This documentation is primarily designed for AI consumption, but humans can:
- Check progress in `TASKS.md`
- Understand context in `/01-context/objective.md`
- Navigate findings in respective directories
- Review AI processes in `CLAUDE.md`
- See portal audit results in `/03-portal-audit/sitemap.md`

---

## Important Principles

### 1. Never Invent Information
If something is unclear or missing, ASK the user. Do not make assumptions.

### 2. Always Document
Every analysis, insight, or discovery must be documented in the appropriate directory with proper formatting.

### 3. Maintain Traceability
Always cite sources (meetings, portal pages, code) in documentation.

### 4. Follow Structure
Use the defined directory structure and markdown formats.

### 5. Update Progress
Always update TASKS.md after completing tasks.

---

## Deliverables (End of Project)

1. **Complete Audit** of current portal
2. **Synthesis** of client feedback
3. **Gap Analysis** between current and needed
4. **Redesign Proposal** for each page
5. **Information Architecture** optimized for user workflow
6. **Implementation Roadmap** with priorities

---

## Need Help?

### Questions About the Project
- Read `/01-context/objective.md` for full context
- Check `TASKS.md` for current status (50% complete)
- Ask arocha@hoopers.club (stakeholder) - see `/01-context/stakeholders.md`

### Questions About Process
- Read `CLAUDE.md` for detailed instructions
- Check task descriptions in `TASKS.md`
- Reference templates in `/templates/`

### Questions About Structure
- This file (README.md) shows directory organization
- Each directory will have an INDEX.md with contents
- Follow examples in existing documentation

---

**Project Start Date**: 2025-10-10
**Expected Completion**: TBD
**Progress Tracking**: See TASKS.md

---

*This is a living document. It will be updated as the project progresses.*
