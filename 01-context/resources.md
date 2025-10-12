# Recursos e Ferramentas - Alley-Reborn Discovery

## Repositório de Código

### Frontend Repository
- **URL**: `git@bitbucket.org:hoopersclub/fe-alley-hooper.git`
- **Platform**: Bitbucket
- **Protocol**: SSH (requer chave SSH configurada)
- **Branch principal**: A determinar (provavelmente `main` ou `master`)

### Como Clonar
```bash
git clone git@bitbucket.org:hoopersclub/fe-alley-hooper.git
```

### Access Requirements
- Chave SSH configurada com Bitbucket
- Permissões de leitura no repositório
- Configuração Git local

### Uso no Projeto
- Análise de componentes UI
- Identificação de stack técnica
- Mapeamento de rotas e páginas
- Inventário de dependências
- Compreensão de arquitetura frontend

### Troubleshooting
**Problema**: `Permission denied` ou erro de autenticação ao clonar

**Soluções**:
1. Verificar chave SSH configurada: `ssh-add -l`
2. Testar conexão: `ssh -T git@bitbucket.org`
3. Verificar permissões no repositório
4. Contactar arocha@hoopers.club para acesso

---

## Plataforma de Reuniões

### Attio CRM
- **Nome**: Attio
- **Tipo**: Plataforma de CRM/gestão de reuniões com transcrições
- **Acesso**: Via links fornecidos pelo usuário progressivamente

### Formato de Links
```
https://attio.link/call/[Call-ID]/transcript
```

### Reuniões Disponíveis

#### 1. Hoopers x SLAM
- **Link**: `https://attio.link/call/Call-Hoopers-x-SLAM-44J51ILV935ZPAgkjgYQE/transcript`
- **Cliente**: Hoopers x SLAM
- **Status**: ⏳ Pronto para processamento (Sprint 3, Task 3.1)

#### Reuniões Adicionais
- Serão fornecidas progressivamente pelo usuário
- Aguardar novos links antes de processar
- Não assumir que há mais reuniões sem confirmação

### Como Processar (Ver CLAUDE.md para processo completo)
1. Acessar link fornecido via WebFetch tool
2. Extrair transcrição completa
3. Salvar em `/02-meetings/[YYYY-MM-DD]-[cliente-tema]/`
4. Criar ficheiros: `attio-link.md`, `transcript.md`, `key-insights.md`, `action-items.md`
5. Atualizar `/02-meetings/INDEX.md`

### Troubleshooting
**Problema**: Link não abre ou não mostra transcrição

**Soluções**:
1. Verificar link está completo e correto
2. Tentar em browser diferente (via WebFetch)
3. Verificar se link não expirou
4. Pedir novo link ao usuário

---

## Ferramentas de Automação

### Playwright (Browser Automation)
**Propósito**: Automação de browser para navegação e captura de screenshots

**Disponibilidade**: Pré-configurado via MCP (Model Context Protocol)

**Uso no Projeto**:
- Login automatizado no portal
- Navegação entre páginas e tabs
- Captura de screenshots full-page
- Análise de DOM e estrutura de páginas
- Extração de dados visuais

**Comandos Principais**:
```javascript
// Navegar
await page.goto('URL');

// Preencher formulário
await page.fill('selector', 'texto');

// Click
await page.click('selector');

// Screenshot
await page.screenshot({ fullPage: true, path: 'file.png' });

// Esperar
await page.waitForTimeout(5000); // 5 segundos
```

**Boas Práticas**:
- Esperar 5-10 segundos após navegação para dados carregarem via API
- Usar `fullPage: true` para capturar conteúdo scrollável
- Nomear screenshots de forma descritiva (ex: `channel-community.png`)

**Troubleshooting**:
**Problema**: Screenshots falham ou navegação não funciona

**Soluções**:
1. Verificar credenciais de login estão corretas
2. Aumentar tempo de espera (APIs podem demorar)
3. Verificar se sessão expirou (fazer login novamente)
4. Usar `browser_snapshot` para ver estado atual da página

---

### WebFetch (Web Content Retrieval)
**Propósito**: Acessar e extrair conteúdo de URLs externas

**Disponibilidade**: Ferramenta disponível no ambiente

**Uso no Projeto**:
- Acessar links Attio para transcrições de reuniões
- Ler documentação externa quando necessário
- Extrair conteúdo web para análise

**Formato**:
```
WebFetch(url, prompt)
- url: URL completa a acessar
- prompt: Instrução de o que extrair da página
```

**Exemplo**:
```
url: "https://attio.link/call/Call-ID/transcript"
prompt: "Extrair a transcrição completa da reunião em formato markdown limpo"
```

---

### File System Tools
**Propósito**: Criar, ler, editar ficheiros e diretórios

**Ferramentas Disponíveis**:
- **Read**: Ler ficheiros existentes
- **Write**: Criar novos ficheiros ou sobrescrever
- **Edit**: Editar partes específicas de ficheiros existentes
- **Glob**: Buscar ficheiros por padrão
- **Grep**: Buscar conteúdo dentro de ficheiros

**Uso no Projeto**:
- Criar toda a estrutura de documentação
- Atualizar ficheiros de análise
- Organizar screenshots e inventários
- Manter TASKS.md e índices atualizados

---

## Ambiente de Trabalho

### Portal Alley (Staging)
- **URL**: `https://stg-fe-alley-hooper.hoopers.club/login`
- **Credenciais**: Ver `/01-context/access-credentials.md`
- **Environment**: Staging (dados reais, não produção)
- **Acesso**: Completo para análise e auditoria
- **Restrições**: Não modificar ou deletar dados

### Sistema de Documentação
- **Formato**: Markdown (.md)
- **Estrutura**: Ver `/Alley-Reborn/` (diretórios numerados)
- **Versionamento**: Git (assumido)
- **Navegação**: Links relativos entre documentos

---

## Checklist de Recursos Disponíveis

Antes de iniciar cada sprint, verificar:

### Sprint 1 (Setup)
- [✅] Estrutura de diretórios criada
- [✅] CLAUDE.md, TASKS.md, OBJECTIVE.md criados
- [✅] Ficheiros de contexto em `/01-context/` preenchidos

### Sprint 2 (Auditoria do Portal)
- [✅] Portal acessível com credenciais
- [✅] Login funcional
- [✅] Playwright configurado e testado
- [✅] Screenshots capturados (26 total)
- [✅] Sitemap.md completo

### Sprint 3 (Processar Reuniões)
- [ ] Link Attio da primeira reunião testado
- [ ] WebFetch funcional para extração
- [ ] Template de análise de reunião preparado
- [ ] Estrutura `/02-meetings/` pronta

### Sprint 4 (Síntese)
- [ ] Todas as reuniões processadas
- [ ] Auditoria do portal completa
- [ ] Código frontend analisado (Git clonado)

### Sprint 5 (Proposta)
- [ ] Gap analysis completa
- [ ] Feedback de stakeholder obtido
- [ ] Templates de proposta preparados

---

## Log de Uso de Recursos

### 2025-10-10 (Sessão 1)
- ✅ Estrutura de documentação criada
- ✅ Ficheiros de contexto preenchidos
- ✅ CLAUDE.md e TASKS.md definidos

### 2025-10-10 (Sessão 2 - Sprint 2)
- ✅ Portal acessado via Playwright
- ✅ Login automatizado configurado
- ✅ Navegação sistemática de 6 páginas
- ✅ 25 tabs navegadas
- ✅ 26 screenshots capturados
- ✅ Sitemap.md completo (1,546 linhas)
- ✅ Channel Detail page descoberta e documentada

### Próximos Recursos Necessários
- ⏳ Acesso ao repositório Git (Sprint 2 Tasks 2.3-2.6 ou Sprint 4)
- ⏳ Links Attio adicionais (Sprint 3)
- ⏳ Feedback de stakeholder (Sprint 4-5)

---

**Este ficheiro documenta todos os recursos técnicos disponíveis para o projeto. Para credenciais, ver `access-credentials.md`. Para stakeholders, ver `stakeholders.md`.**

**Última atualização**: 2025-10-10
