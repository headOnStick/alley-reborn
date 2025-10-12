# Platform Overview - Alley

## O Que É Alley

Alley é uma plataforma SaaS de analytics avançado de Instagram que utiliza inteligência artificial para fornecer métricas de marketing que vão além das métricas superficiais oferecidas por ferramentas tradicionais.

### Proposta de Valor
**Para marcas, agências e influencers**: Entender não apenas **quantas** pessoas interagem com seu conteúdo, mas **quem** são essas pessoas (demograficamente e comportamentalmente) e **o que** estão expressando (sentimentos, intenções).

### Diferencial no Mercado
Ferramentas tradicionais (Meta Business Suite, Later, Hootsuite, etc.) fornecem:
- Número de likes
- Número de comentários
- Alcance
- Impressões
- Taxa de engagement (superficial)

**Alley fornece**:
- Perfil demográfico real da audiência engajada
- Perfil comportamental dos comentadores
- Análise sentimental profunda
- Identificação de intenções (interesse em compra, dúvidas, etc.)
- Autenticidade do engagement (detecção de bots)
- Insights visuais sobre conteúdo que funciona

---

## Arquitetura Técnica (High-Level)

### Stack do Frontend
- **Repositório**: `git@bitbucket.org:hoopersclub/fe-alley-hooper.git`
- **Framework**: A identificar durante auditoria (provavelmente React ou Vue)
- **Hospedagem**: Staging em `stg-fe-alley-hooper.hoopers.club`
- **Status**: Alfa funcional

### Backend (Inferido)
- **Scraping Engine**: Sistema de coleta de dados do Instagram
- **AI/ML Pipeline**:
  - Visão computacional para análise de imagens
  - NLP para análise de comentários e biografias
  - Modelos de classificação demográfica
- **Data Storage**: Base de dados para métricas processadas
- **API**: Expõe dados para frontend

### Fluxo de Dados
```
Instagram
    ↓ (scraping)
Backend - Coleta de Posts
    ↓
Backend - Análise AI
    ├→ Análise de Imagens
    ├→ Análise de Comentários (sentimento)
    ├→ Análise de Perfis (comentadores)
    └→ Geração de Métricas
    ↓
API
    ↓
Frontend (Portal)
    ↓
Cliente
```

---

## Capacidades Funcionais

### 1. Scraping de Conteúdo
**O que faz**:
- Coleta posts do Instagram de contas de clientes
- Captura metadados (data, hora, tipo de mídia)
- Coleta comentários associados
- Tracking contínuo de engagement

**Dados coletados**:
- Imagem/vídeo do post
- Caption
- Data/hora de publicação
- Lista de comentadores
- Texto dos comentários
- Likes, shares, saves (se disponível)

---

### 2. Análise de Imagens (Computer Vision)
**O que faz**:
- Processamento visual de imagens dos posts
- Identificação de elementos (produtos, pessoas, cenários)
- Análise de composição visual
- Classificação de tipo de conteúdo

**Output**:
- Tags visuais (ex: "produto em uso", "foto de lifestyle", "close-up")
- Elementos identificados (ex: "pessoa", "logo", "ambiente externo")
- Score de qualidade visual
- Categorização de conteúdo

**Valor para cliente**:
- Entender que tipo de conteúdo visual gera mais engagement
- Identificar padrões visuais que funcionam
- Otimizar criação de conteúdo futuro

---

### 3. Análise Sentimental de Comentários
**O que faz**:
- Processamento de linguagem natural de todos os comentários
- Classificação de sentimento (positivo, negativo, neutro)
- Identificação de temas recorrentes
- Detecção de intenções (interesse em compra, perguntas, reclamações)

**Output**:
- Score de sentimento por post
- Distribuição de sentimentos (% positivo, negativo, neutro)
- Temas mais mencionados
- Identificação de perguntas frequentes
- Detecção de potenciais crises (spike de negatividade)

**Valor para cliente**:
- Medir qualidade do engagement, não apenas quantidade
- Identificar problemas antes que escalem
- Entender o que audiência realmente pensa
- Responder a perguntas frequentes de forma proativa

---

### 4. Análise de Perfis de Comentadores

#### 4.1 Análise de Foto de Perfil
**O que faz**:
- Visão computacional na foto de perfil de cada comentador
- Inferência demográfica (idade aproximada, gênero aparente)
- Classificação de tipo de conta (pessoal, empresa, influencer, genérica)

**Output**:
- Perfil demográfico agregado da audiência
- Distribuição de idade
- Distribuição de gênero
- Percentagem de contas reais vs possivelmente fake

**Limitações**:
- Inferência probabilística, não certeza absoluta
- Depende da qualidade da foto de perfil
- Considerações de privacidade e ética

#### 4.2 Análise de Biografia
**O que faz**:
- Processamento de texto da biografia
- Extração de interesses mencionados
- Identificação de localização (quando mencionada)
- Classificação de perfil comportamental

**Output**:
- Interesses comuns da audiência
- Localizações geográficas
- Perfis comportamentais (ex: "entusiasta de fitness", "empreendedor", "mãe/pai")
- Profissões/áreas de atuação

**Valor para cliente**:
- Entender **quem** realmente interage com conteúdo
- Validar se audiência corresponde a target desejado
- Identificar micro-segmentos valiosos
- Otimizar targeting de conteúdo e ads

---

### 5. Métricas Proprietárias

#### Score de Qualidade de Engagement
Métrica composta que pondera:
- Sentimento dos comentários
- Autenticidade das contas
- Relevância dos comentadores (perfil alinhado com target)
- Profundidade do engagement (comentários longos vs "🔥")

#### Segmentação de Audiência
Agrupamento automático de comentadores em segmentos:
- Por demografia
- Por interesses
- Por comportamento
- Por autenticidade

#### Métricas de Autenticidade
- Detecção de bots (contas fake)
- Score de autenticidade por post
- Identificação de engagement artificial vs orgânico

#### Performance Visual
- Correlação entre elementos visuais e engagement
- Score de performance por tipo de conteúdo
- Recomendações de otimização visual

---

## Casos de Uso

### Para Marcas (e-commerce, produtos, serviços)
**Problema**: "Tenho 10k likes mas não sei se essas pessoas vão comprar"
**Solução Alley**:
- Perfil demográfico dos engajados
- Detecção de intenção de compra em comentários
- Validação se audiência corresponde a target
- ROI de conteúdo (qual conteúdo atrai potenciais clientes)

### Para Agências de Marketing
**Problema**: "Preciso provar valor de campanhas além de métricas de vaidade"
**Solução Alley**:
- Qualidade de engagement, não apenas quantidade
- Análise sentimental para medir impacto de campanha
- Segmentação de audiência alcançada
- Reports com insights acionáveis para clientes

### Para Influencers
**Problema**: "Preciso mostrar que minha audiência tem valor para marcas"
**Solução Alley**:
- Perfil detalhado da audiência (não só números)
- Autenticidade do engagement (não bots)
- Poder de influência real (sentimento, intenções)
- Micro-segmentos valiosos dentro da audiência

### Para E-commerce
**Problema**: "Não sei quem são meus clientes no Instagram"
**Solução Alley**:
- Perfil comportamental de quem comenta
- Identificação de early adopters vs late majority
- Detecção de perguntas sobre produtos
- Análise de satisfação pós-compra (via comentários)

---

## Estado Atual da Plataforma

### O Que Está Funcionando
- ✅ Scraping de posts do Instagram operacional
- ✅ Análise AI de imagens processando corretamente
- ✅ Análise sentimental de comentários ativa
- ✅ Análise de perfis (foto + bio) implementada
- ✅ Dados sendo coletados e armazenados
- ✅ Frontend renderizando dados
- ✅ Sistema end-to-end funcional

### O Que Não Está Funcionando (Product-Level)
- ❌ Estrutura de informação desalinhada com necessidades
- ❌ KPIs não priorizados corretamente
- ❌ Navegação não otimizada para fluxo de trabalho
- ❌ Excesso de informação sem hierarquia clara
- ❌ Difícil extrair insights acionáveis rapidamente
- ❌ Não está pronto para vendas comerciais

**Diagnóstico**: Problema de **product design** (estrutura de informação), não de **engenharia** (capacidades técnicas).

---

## Jornada do Usuário (Idealizada)

### 1. Onboarding
Cliente conecta conta de Instagram → Alley começa scraping

### 2. Data Collection
Sistema coleta posts e comentários (contínuo)

### 3. Processing
AI analisa imagens, comentários e perfis

### 4. Insights
Cliente acessa portal e vê:
- Dashboard com KPIs principais
- Análise de posts individuais
- Perfil da audiência
- Tendências ao longo do tempo
- Recomendações acionáveis

### 5. Action
Cliente ajusta estratégia de conteúdo baseado em insights

### 6. Loop
Continuamente monitorar performance e refinar

---

## Tecnologias e Ferramentas (A Confirmar Durante Auditoria)

### Frontend (Provável)
- **Framework**: React ou Vue.js
- **State Management**: Redux, Vuex, ou Context API
- **Charts/Visualizations**: D3.js, Chart.js, ou similar
- **UI Framework**: Material-UI, Ant Design, ou custom

### Backend (Inferido)
- **Scraping**: Puppeteer, Selenium, ou similar
- **AI/ML**: TensorFlow, PyTorch, ou serviços cloud (AWS Rekognition, Google Vision)
- **NLP**: spaCy, NLTK, ou APIs de sentiment analysis
- **API**: Node.js, Python (Flask/FastAPI), ou similar

### Infrastructure
- **Hosting**: Cloud (AWS, GCP, Azure, ou similar)
- **Database**: PostgreSQL, MongoDB, ou similar
- **Storage**: S3 ou equivalente para imagens
- **CDN**: Para servir assets do portal

---

## Limitações Conhecidas

### Técnicas
- Dependente de acesso ao Instagram (mudanças na API podem impactar)
- Qualidade de análise AI depende de qualidade de dados de entrada
- Inferências demográficas são probabilísticas, não absolutas

### De Negócio
- Compliance com termos de serviço do Instagram
- Privacidade e GDPR (análise de perfis públicos)
- Escalabilidade (quanto custa processar milhões de comentários)

### De Produto (Atuais - A Resolver)
- Estrutura de informação não alinhada com uso real
- Curva de aprendizado alta para novos usuários
- Dificulta demo comercial efetiva

---

## Perguntas em Aberto (A Esclarecer)

### Técnicas
- [ ] Qual é o framework frontend exato? (React, Vue, Angular, etc.)
- [ ] Quais bibliotecas de componentes são usadas?
- [ ] Há design system ou styleguide?
- [ ] Como é feita autenticação/autorização?
- [ ] Há diferentes níveis de acesso (admin, cliente, viewer)?

### De Produto
- [ ] Quais são as personas de usuário definidas?
- [ ] Há fluxos de usuário documentados?
- [ ] Qual é o pricing model planejado?
- [ ] Há planos/tiers diferentes?
- [ ] Qual é o modelo de onboarding?

### De Dados
- [ ] Que volume de dados é processado atualmente?
- [ ] Qual é a latência de atualização (real-time, hourly, daily)?
- [ ] Há histórico de dados (quantos meses atrás)?
- [ ] Como são tratados dados de contas privadas?

---

## Glossário Rápido (Ver `/01-context/glossary.md` para lista completa)

- **Engagement**: Interação com conteúdo (likes, comments, shares, saves)
- **Sentiment**: Classificação emocional de texto (positivo, negativo, neutro)
- **Comentador**: Usuário que deixa comentário em post
- **Score**: Métrica numérica calculada (ex: score de qualidade)
- **Segmento**: Grupo de usuários com características similares
- **KPI**: Key Performance Indicator (métrica principal)

---

**Este documento fornece overview técnico e funcional da plataforma. Para objetivos do projeto de discovery, ver `/01-context/objective.md`.**

**Última atualização**: 2025-10-10
