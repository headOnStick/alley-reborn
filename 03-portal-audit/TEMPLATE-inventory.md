# [Tipo de Inventário] - Portal Alley

## Metadata
- **Tipo de Inventário**: [Components / KPIs / Forms / etc]
- **Data de Criação**: [YYYY-MM-DD]
- **Última Atualização**: [YYYY-MM-DD]
- **Total de Itens**: [X]
- **Status**: [Completo / Em progresso]

---

## Resumo Executivo
[Breve overview do que este inventário contém e principais insights]

**Principais descobertas**:
- [Insight 1]
- [Insight 2]
- [Insight 3]

---

## Metodologia
[Como este inventário foi criado]

**Fontes**:
- Análise de páginas em `/03-portal-audit/pages-inventory/`
- Análise de código em repositório Git
- Navegação manual do portal

**Período de análise**: [Datas]

---

# OPÇÃO A: Inventário de Componentes

## Componentes Identificados

### [Nome do Componente 1]

#### Descrição
[O que é este componente e para que serve]

#### Variantes
[Se há variações deste componente]
- Variante 1: [Descrição]
- Variante 2: [Descrição]

#### Onde é Usado
[Lista de páginas que usam este componente]
| Página | Quantidade | Propósito na Página | Screenshot |
|--------|------------|---------------------|------------|
| Dashboard | 4 | Cards de métricas principais | [link] |
| Profile Analysis | 2 | Métricas de audiência | [link] |
| [Page] | X | [Purpose] | [link] |

**Total de usos**: [X instâncias no portal]

#### Props/Configurações Comuns
[Parâmetros que este componente aceita]
- `title`: [Tipo] - [Descrição]
- `value`: [Tipo] - [Descrição]
- `icon`: [Tipo] - [Descrição]

#### Dependências
[Bibliotecas ou outros componentes que este depende]
- [Biblioteca X]
- [Componente Y]

#### Observações
- [Nota sobre uso, problemas, oportunidades]

---

### [Componente 2]
[Repetir estrutura acima]

---

## Matriz de Uso de Componentes

[Tabela consolidada mostrando quais componentes são usados em quais páginas]

| Componente / Página | Dashboard | Profile | Posts | Analytics | Settings |
|---------------------|-----------|---------|-------|-----------|----------|
| MetricCard          | ✓ (4x)    | ✓ (2x)  | -     | ✓ (6x)    | -        |
| LineChart           | ✓ (1x)    | -       | ✓ (3x)| ✓ (2x)    | -        |
| DataTable           | -         | ✓ (1x)  | ✓ (1x)| ✓ (1x)    | -        |
| [Component]         | [X]       | [X]     | [X]   | [X]       | [X]      |

**Legenda**:
- ✓ (Nx) = Usado N vezes na página
- - = Não usado

---

## Análise de Padrões

### Componentes Mais Usados
1. **[Component 1]**: [X usos] - [Por que é popular]
2. **[Component 2]**: [Y usos] - [...]

### Componentes Menos Usados
1. **[Component X]**: [1 uso] - [Por que é raro / Deveria ser removido?]

### Inconsistências Identificadas
- [Mesmo propósito, componentes diferentes em páginas diferentes]
- [Variações de estilo sem justificativa]

### Oportunidades
- [Componente que poderia ser reutilizado em mais lugares]
- [Necessidade de novo componente para padrão recorrente]

---

# OPÇÃO B: Inventário de KPIs

## KPIs Identificados

### [Nome do KPI 1]

#### Descrição
[O que mede este KPI e por que é importante]

#### Cálculo/Fonte
[Como é calculado ou de onde vem o dado]
- **Fórmula**: [Se aplicável]
- **Fonte de dados**: [API endpoint, tabela de BD, etc]

#### Onde Aparece
| Página | Formato | Destaque | Screenshot |
|--------|---------|----------|------------|
| Dashboard | Card com número grande | Alto | [link] |
| [Page] | Linha em tabela | Baixo | [link] |

**Total de aparições**: [X vezes no portal]

#### Contexto Adicional Mostrado
[Informação adicional apresentada junto com o KPI]
- Comparação com período anterior: [Sim/Não]
- Benchmark ou meta: [Sim/Não]
- Tendência (gráfico sparkline): [Sim/Não]
- Explicação/tooltip: [Sim/Não]

#### Relacionado a Necessidades de Clientes
[Reuniões onde este KPI foi mencionado como importante]
- Reunião: [Link] - Cliente disse: > "[Quote]"

#### Prioridade Sugerida
[Alta/Média/Baixa baseado em frequência de uso + feedback de clientes]

#### Observações
- [Notas sobre este KPI]

---

### [KPI 2]
[Repetir estrutura acima]

---

## Categorização de KPIs

### Por Categoria de Métricas

#### Engagement Metrics
- [KPI 1]: [Breve descrição]
- [KPI 2]: [...]

#### Sentiment Metrics
- [KPI 3]: [...]

#### Audience Demographics
- [KPI 4]: [...]

#### Content Performance
- [KPI 5]: [...]

### Por Nível de Detalhe

#### KPIs de Alto Nível (Summary)
[Métricas agregadas para overview rápido]
- [Lista]

#### KPIs Detalhados (Drill-down)
[Métricas granulares para análise profunda]
- [Lista]

---

## Análise de Cobertura

### KPIs Mencionados por Clientes
[Do processamento de reuniões]
| KPI | Mencionado em | Status no Portal |
|-----|---------------|------------------|
| [KPI X] | Reunião A, B | Existe, bem posicionado |
| [KPI Y] | Reunião C | Existe mas escondido |
| [KPI Z] | Reunião A | Não existe |

### Gaps Identificados
[KPIs que clientes querem mas não existem ou não estão visíveis]
1. **[KPI Missing]**: Mencionado em [X reuniões], não existe no portal
2. **[KPI Hidden]**: Existe mas difícil de encontrar

---

# OPÇÃO C: Inventário de Formulários

## Formulários Identificados

### [Nome do Formulário/Filtro 1]

#### Localização
- **Página**: [Nome da página]
- **Posição**: [Header/Sidebar/Modal/etc]

#### Campos
| Campo | Tipo | Required | Default | Validação |
|-------|------|----------|---------|-----------|
| Start Date | Date Picker | Sim | -30 dias | Must be before End Date |
| End Date | Date Picker | Sim | Hoje | - |
| Account | Dropdown | Não | Todas | - |
| [Field] | [Type] | [Yes/No] | [Value] | [Rules] |

#### Propósito
[O que este formulário faz]

#### Ação ao Submeter
[O que acontece quando usuário submete]

#### Validações e Feedback
[Como usuário sabe se input é válido/inválido]

#### UX Issues
[Problemas de usabilidade identificados]
- [Issue 1]

---

### [Formulário 2]
[Repetir estrutura]

---

## Padrões de Input

### Campos Mais Comuns
[Inputs que aparecem em múltiplos formulários]

1. **Date Range Picker**: [X ocorrências]
   - Páginas: [Lista]
   - Implementações: [Consistente? Variações?]

2. **Account Selector**: [Y ocorrências]
   - [...]

### Inconsistências
[Mesmo tipo de input implementado de formas diferentes]
- [Descrição da inconsistência]

---

# OPÇÃO D: Inventário de Navegação

## Estrutura de Navegação

### Menu Principal
```
├── Dashboard
├── Posts
│   ├── All Posts
│   ├── Top Performing
│   └── Recent
├── Audience
│   ├── Overview
│   ├── Demographics
│   └── Interests
├── [Section]
│   ├── [Subsection]
│   └── [Subsection]
└── Settings
```

### Navegação Secundária
[Breadcrumbs, tabs, links contextuais]

---

## Análise de Fluxos

### Fluxos Principais Identificados
[Caminhos comuns que usuário percorre]

**Fluxo 1**: [Nome do fluxo]
1. [Página inicial] →
2. [Ação/Navegação] →
3. [Página destino]

**Observações**:
- [Fricções neste fluxo]
- [Oportunidades de otimização]

---

# SEÇÃO COMUM A TODOS OS INVENTÁRIOS

## Estatísticas Gerais

### Por Frequência de Uso
[Top itens mais usados no portal]
| Item | Ocorrências | % do Total |
|------|-------------|------------|
| [Item 1] | X | Y% |
| [Item 2] | X | Y% |

### Por Página
[Densidade de uso por página]
| Página | Total de [Items] | Complexidade |
|--------|------------------|--------------|
| Dashboard | 15 | Alta |
| [Page] | X | [Low/Med/High] |

---

## Recomendações

### Consolidação
[Itens que poderiam ser consolidados para reduzir complexidade]
- [Recomendação 1]

### Padronização
[Onde implementar padrões consistentes]
- [Recomendação 2]

### Priorização
[O que merece mais destaque baseado em análise]
- [Recomendação 3]

### Remoção
[Candidatos para remoção por baixo uso ou redundância]
- [Item para considerar remover]

---

## Próximos Passos
[O que fazer com este inventário]

- [ ] Cruzar com feedback de reuniões
- [ ] Incluir em gap analysis
- [ ] Usar para proposta de redesenho

---

## Rastreabilidade

**Baseado em**:
- Análises de páginas: `/03-portal-audit/pages-inventory/`
- Código fonte: [Repositório]
- Screenshots: `/03-portal-audit/screenshots/`

**Referenciado em**:
- Gap Analysis: [Link]
- Proposta de redesenho: [Link]

**Atualizado**:
- [Data] - [Mudança]

---

**Template Version**: 1.0
**Última atualização do template**: 2025-10-10
