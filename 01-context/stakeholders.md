# Stakeholders - Alley-Reborn Discovery

## Stakeholder Principal

### André Rocha
- **Email**: `arocha@hoopers.club`
- **Papel**: Product Owner / Cliente / Decisor Final
- **Empresa**: Hoopers Club
- **Contexto**: Responsável pelo produto Alley e decisões estratégicas

---

## Responsabilidades

### André Rocha

#### Como Product Owner
- Define visão e estratégia do produto Alley
- Prioriza features e roadmap
- Valida propostas de redesenho
- Aprova decisões finais de produto

#### No Contexto Deste Projeto
- Fornecer contexto de negócio e background
- Fornecer links de reuniões com clientes (Attio)
- Fornecer acesso a recursos (portal, Git, etc.)
- Validar análises e propostas em marcos do projeto
- Aprovar decisões de redesenho antes de implementação
- Esclarecer dúvidas sobre regras de negócio

---

## Quando Contactar

### ✅ Deve Contactar (Alta Prioridade)

1. **Informação Crítica Ausente**
   - Dados necessários para avançar não estão disponíveis
   - Credenciais ou acessos em falta
   - Links de reuniões adicionais necessários

2. **Decisões de Produto**
   - Priorização entre múltiplas opções de redesenho
   - Trade-offs que impactam estratégia de negócio
   - Escolhas que afetam experiência de cliente final

3. **Validação de Marcos**
   - Conclusão de Sprint importante (ex: auditoria completa)
   - Proposta de redesenho pronta para review
   - Gap analysis completada e priorizada

4. **Ambiguidade em Regras de Negócio**
   - Feedback de clientes contraditório
   - Incerteza sobre prioridade de features
   - Dúvidas sobre target audience ou casos de uso

5. **Bloqueadores**
   - Impossibilidade de avançar sem input específico
   - Recursos técnicos inacessíveis
   - Erros ou inconsistências críticas encontradas

---

### ⚠️ Pode Contactar (Média Prioridade)

1. **Validação de Progresso**
   - Confirmar que direção da análise está correta
   - Feedback incremental sobre descobertas
   - Validação de suposições razoáveis

2. **Otimização de Processos**
   - Sugestões de melhoria no workflow
   - Identificação de eficiências possíveis
   - Ajustes de scope ou abordagem

---

### ❌ Não Contactar (Não Necessário)

1. **Detalhes Técnicos de Implementação**
   - Formatação de documentos markdown
   - Organização de ficheiros e diretórios
   - Uso de ferramentas (Playwright, WebFetch)
   - Estrutura de código frontend (analisar Git diretamente)

2. **Decisões Procedurais**
   - Como processar reuniões (seguir CLAUDE.md)
   - Como fazer screenshots (processo definido)
   - Como estruturar análises (usar templates)

3. **Informação Já Documentada**
   - Contexto já presente em `/01-context/`
   - Processos já definidos em CLAUDE.md
   - Tarefas já listadas em TASKS.md

---

## Formato de Comunicação

### ✅ Boas Práticas

**Seja Direto e Específico**:
```
❌ "Preciso de mais informação sobre o projeto"
✅ "Qual é o URL do repositório Git do backend para análise de APIs?"
```

**Contextualize a Pergunta**:
```
✅ "Estou na Task 3.1 (processar reunião Hoopers x SLAM).
    O link Attio fornecido não está acessível.
    Pode fornecer link atualizado ou credenciais adicionais?"
```

**Apresente Opções Quando Possível**:
```
✅ "Encontrei 3 abordagens para priorizar KPIs no redesenho:
    A) Por frequência de menção em reuniões
    B) Por impacto em conversão de vendas
    C) Por facilidade de implementação técnica

    Qual abordagem alinha melhor com estratégia de negócio?"
```

**Documente a Resposta**:
Após receber resposta de André:
- Registrar decisão no documento relevante
- Citar fonte: "Confirmado por arocha@hoopers.club em 2025-10-10"
- Atualizar TASKS.md se decisão afetar tarefas

---

### ❌ Más Práticas

**Perguntas Vagas**:
```
❌ "O que devo fazer agora?"
```

**Perguntas Múltiplas Não Relacionadas**:
```
❌ "Preciso de: link Git, mais reuniões, validação da análise,
    feedback sobre KPIs, e aprovação para avançar"
```
→ Separar em perguntas individuais específicas

**Perguntas Já Respondidas**:
```
❌ "Qual é o objetivo do projeto?"
→ Consultar /01-context/objective.md primeiro
```

---

## Outros Stakeholders

### Equipe de Desenvolvimento (Futura)
- **Papel**: Implementadores do redesenho proposto
- **Envolvimento**: Fase pós-discovery (após aprovação da proposta)
- **Requerimento**: Proposta deve ser clara, implementável e com requirements técnicos definidos

### Clientes de Alley (Indiretos)
- **Papel**: Usuários finais do portal
- **Envolvimento**: Via reuniões processadas (feedback registrado)
- **Representação**: André Rocha age como proxy de necessidades dos clientes

---

## Decisões Importantes (Log)

### 2025-10-10 - Início do Projeto
- **Decisor**: arocha@hoopers.club
- **Decisão**: Iniciar projeto Alley-Reborn com foco em redesenho de estrutura de informação
- **Rationale**: Portal tem capacidades técnicas funcionais mas estrutura desalinhada com necessidades
- **Impacto**: Define scope de todo o projeto (IA, não UI; estrutura, não features)

### 2025-10-10 - Sprint 2 Início
- **Decisor**: arocha@hoopers.club
- **Decisão**: Fornecer credenciais de acesso ao portal staging
- **Rationale**: Necessário para auditoria completa
- **Impacto**: Permitiu captura de 26 screenshots e documentação de 6 páginas

### [Adicionar decisões conforme surgem]

---

## Escalation Path

Se houver bloqueador crítico e André Rocha não disponível:
1. Documentar bloqueador claramente em `/TASKS.md`
2. Continuar com tarefas paralelas não bloqueadas
3. Aguardar resposta antes de prosseguir com tarefas dependentes
4. Não inventar informação ou fazer suposições críticas

---

## Disponibilidade

- **Canal**: Contexto deste projeto (sistema de IA)
- **Responsividade**: A definir (assumir resposta em horas/dias úteis)
- **Fuso Horário**: A confirmar (assumir PT - Portugal Time)

---

## Feedback Loop

### Marcos de Validação Planejados

1. **Sprint 1 Completo** (✅ Feito)
   - Status: Estrutura base criada
   - Feedback: Implícito (avançou para Sprint 2)

2. **Sprint 2 Completo** (✅ Feito - 2025-10-10)
   - Status: Auditoria do portal 100% completa
   - Feedback: Aguardando validação
   - Deliverable: sitemap.md (1,546 linhas) + 26 screenshots

3. **Sprint 3 Completo** (⏳ Pendente)
   - Deliverable: Reuniões processadas com insights
   - Validação esperada: Confirmar insights extraídos alinham com expectativas

4. **Sprint 4 Completo** (⏳ Pendente)
   - Deliverable: Gap analysis e síntese de necessidades
   - Validação esperada: Priorização de gaps alinha com estratégia

5. **Sprint 5 Completo** (⏳ Pendente)
   - Deliverable: Proposta de redesenho completa
   - Validação esperada: Aprovação para implementação

---

**Este ficheiro documenta todos os stakeholders do projeto e como/quando contactá-los. Para recursos técnicos, ver `resources.md`. Para credenciais, ver `access-credentials.md`.**

**Última atualização**: 2025-10-10
