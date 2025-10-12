# Análise de Página - [Nome da Página]

## Metadata
- **Nome da Página**: [Nome oficial da página no portal]
- **Rota/URL**: [/caminho/da/pagina]
- **Screenshot**: [Caminho relativo para screenshot]
- **Data de Análise**: [YYYY-MM-DD]
- **Analisado por**: [IA/Humano]
- **Versão do Portal**: [Staging/Produção]

---

## Objetivo da Página

### Propósito Aparente
[Qual parece ser o objetivo desta página baseado em conteúdo e estrutura]

### Propósito Ideal
[Qual deveria ser o objetivo baseado em necessidades de clientes identificadas]

### Usuários Alvo
[Quem é o público primário desta página]
- Persona 1: [Descrição]
- Persona 2: [Descrição]

### Momento de Uso
[Quando/em que contexto usuário acessa esta página]

---

## Screenshot e Referência Visual

**Screenshot principal**: `../screenshots/[page-name]/full-page.png`

**Screenshots adicionais** (se necessário):
- Above the fold: `../screenshots/[page-name]/above-fold.png`
- Seção específica: `../screenshots/[page-name]/section-x.png`

---

## Estrutura da Página

### Layout Geral
[Descrição da estrutura visual da página]

**Divisões principais**:
1. [Seção 1 - ex: Header com filtros]
2. [Seção 2 - ex: Grid de cards com métricas]
3. [Seção 3 - ex: Gráfico de tendência]
4. [Seção 4 - ex: Tabela de dados detalhados]

### Hierarquia Visual
[O que é mais destacado visualmente, em ordem de destaque]

**Prioridade Alta** (primeiro plano visual):
- [Elemento 1]
- [Elemento 2]

**Prioridade Média**:
- [Elemento 3]
- [Elemento 4]

**Prioridade Baixa**:
- [Elemento 5]

---

## Componentes Identificados

### Componentes UI Usados
[Lista de componentes de interface presentes na página]

1. **[Nome do Componente]** (ex: Card de Métrica)
   - **Quantidade**: [X instâncias]
   - **Localização**: [Onde aparecem]
   - **Propósito**: [Para que serve]
   - **Dados exibidos**: [Que informação mostra]

2. **[Componente 2]** (ex: Gráfico de Linha)
   - **Quantidade**: [...]
   - **Localização**: [...]
   - **Propósito**: [...]
   - **Dados exibidos**: [...]

3. **[Componente 3]**
   - [...]

### Componentes de Navegação
- **Breadcrumb**: [Sim/Não] - [Caminho mostrado]
- **Menu lateral**: [Sim/Não] - [Itens]
- **Tabs**: [Sim/Não] - [Nomes das tabs]
- **Links internos**: [Lista de links para outras páginas]

---

## KPIs e Métricas Mostrados

### Métricas Primárias
[Métricas que estão em destaque na página]

1. **[Nome da Métrica]** (ex: Taxa de Engagement)
   - **Formato de apresentação**: [Número, %, gráfico]
   - **Localização**: [Onde está na página]
   - **Contexto adicional**: [Comparação com período anterior, benchmark, etc.]
   - **Destaque visual**: [Alto/Médio/Baixo]
   - **Acionabilidade**: [O que usuário pode fazer com esta info]

2. **[Métrica 2]**
   - [...]

### Métricas Secundárias
[Métricas presentes mas não em destaque]

1. **[Nome da Métrica]**
   - **Formato**: [...]
   - **Localização**: [...]

### Métricas Ausentes (mas potencialmente relevantes)
[Métricas que deveriam estar aqui baseado em feedback de clientes]

- [Métrica 1]: [Por que deveria estar aqui]
- [Métrica 2]: [...]

---

## Formulários e Inputs

### Filtros Disponíveis
[Campos de filtro que usuário pode usar]

1. **[Nome do Filtro]** (ex: Período de Datas)
   - **Tipo**: [Dropdown/Date picker/Checkbox/etc]
   - **Opções**: [Valores disponíveis]
   - **Default**: [Valor padrão selecionado]
   - **Impacto**: [O que este filtro afeta na página]

2. **[Filtro 2]**
   - [...]

### Campos de Input
[Campos onde usuário pode inserir dados]

1. **[Nome do Campo]**
   - **Tipo**: [Text/Number/etc]
   - **Validação**: [Regras de validação visíveis]
   - **Propósito**: [Para que serve]

### Botões de Ação
[Botões que disparam ações]

1. **[Texto do Botão]** (ex: "Exportar Relatório")
   - **Ação**: [O que acontece ao clicar]
   - **Estado**: [Sempre disponível / Condicional]
   - **Feedback**: [Como usuário sabe que ação foi executada]

---

## Navegação e Fluxo

### Como Chegar a Esta Página
[Caminhos possíveis para acessar esta página]

1. [Menu principal > Item X]
2. [Dashboard > Link Y]
3. [URL direto]

### Para Onde Esta Página Leva
[Links e caminhos de saída desta página]

1. **[Link/Botão 1]** → [Página de destino]
2. **[Link/Botão 2]** → [Página de destino]

### Posição no Fluxo de Usuário
[Onde esta página se encaixa no fluxo geral]

**Fluxo típico**:
[Página anterior] → **Esta Página** → [Página seguinte]

---

## Interações Disponíveis

### Interações Principais
[Principais ações que usuário pode fazer]

1. **[Ação 1]** (ex: Ordenar tabela por coluna)
   - **Como**: [Clique no header da coluna]
   - **Feedback visual**: [Seta indicando ordem]

2. **[Ação 2]** (ex: Hover em gráfico para ver detalhes)
   - [...]

### Interações Secundárias
- [Lista de interações menos frequentes]

---

## Performance e Usabilidade

### Velocidade de Carregamento
[Observações sobre tempo de carregamento]
- **Tempo aproximado**: [X segundos]
- **Loading states**: [Como é indicado que está carregando]

### Responsividade
- **Desktop**: [Como se comporta]
- **Tablet**: [A verificar com Playwright]
- **Mobile**: [A verificar com Playwright]

### Acessibilidade
[Observações sobre acessibilidade]
- Labels visíveis: [Sim/Não]
- Contraste adequado: [Sim/Não/Parcial]
- Navegação por teclado: [A testar]

---

## Issues Identificados

### Problemas de Usabilidade
[Dificuldades que usuário pode encontrar]

1. **[Issue 1]**
   - **Descrição**: [O que está errado]
   - **Impacto**: [Como afeta usuário]
   - **Severidade**: [Alta/Média/Baixa]
   - **Evidência**: [Screenshot ou observação]

2. **[Issue 2]**
   - [...]

### Problemas de Hierarquia de Informação
[Quando importância visual não corresponde a importância real]

1. **[Issue 1]**
   - **Problema**: [Métrica importante está escondida, ou métrica menos importante está em destaque]
   - **Deveria ser**: [Como deveria estar]

### Problemas de Clareza
[Quando informação não é clara ou é ambígua]

1. **[Issue 1]**
   - **Elemento**: [Qual elemento]
   - **Problema**: [Por que não é claro]
   - **Sugestão**: [Como melhorar]

### Dados/Funcionalidades Ausentes
[O que deveria estar aqui mas não está]

- [Item 1]: [Por que faz falta]
- [Item 2]: [...]

---

## Alinhamento com Necessidades de Clientes

### Necessidades Atendidas
[Necessidades de clientes que esta página atende]

1. **[Necessidade X]** (referência: `/02-meetings/[reuniao]/`)
   - **Como atende**: [Descrição]
   - **Qualidade**: [Bem/Parcialmente/Mal]

### Necessidades Não Atendidas
[Necessidades que esta página deveria atender mas não atende]

1. **[Necessidade Y]**
   - **Fonte**: [Link para reunião onde foi mencionada]
   - **Gap**: [O que falta]

---

## Comparação com Concorrentes (se aplicável)
[Se existem páginas similares em ferramentas concorrentes]

**Ferramenta X**:
- **O que fazem melhor**: [...]
- **O que fazemos melhor**: [...]

**Ferramenta Y**:
- [...]

---

## Oportunidades de Melhoria

### Quick Wins
[Melhorias de baixo esforço e alto impacto]

1. **[Oportunidade 1]**
   - **Mudança**: [O que mudar]
   - **Benefício**: [Impacto esperado]
   - **Esforço**: [Baixo/Médio/Alto]

### Melhorias Estruturais
[Mudanças maiores que requerem redesign]

1. **[Oportunidade 1]**
   - **Mudança**: [...]
   - **Benefício**: [...]
   - **Esforço**: [...]

---

## Dados Técnicos

### Componentes de Código (se analisado)
[Componentes React/Vue identificados no código]

- Componente principal: `[ComponentName]`
- Subcomponentes: `[List]`
- Bibliotecas usadas: [Chart.js, etc]

### APIs Chamadas
[Endpoints de API que esta página consome]

- `GET /api/[endpoint]` - [O que retorna]
- `POST /api/[endpoint]` - [Propósito]

---

## Observações Adicionais
[Notas que não se encaixam nas categorias acima]

- [Observação 1]
- [Observação 2]

---

## Próximos Passos
[O que fazer com esta análise]

- [ ] Relacionar com feedback de reunião X
- [ ] Incluir em gap analysis
- [ ] Propor redesenho em Sprint 5

---

## Rastreabilidade

**Fontes**:
- Screenshot: [Caminho]
- Código: [Repositório, arquivo, linha]
- Reuniões relacionadas: [Links]

**Referenciado em**:
- Components Matrix: `/03-portal-audit/components-matrix.md`
- KPIs Inventory: `/03-portal-audit/kpis-inventory.md`
- Gap Analysis: `/05-gap-analysis/[arquivo].md`

**Atualizado**:
- [Data] - [Quem] - [O que mudou]

---

**Template Version**: 1.0
**Última atualização do template**: 2025-10-10
