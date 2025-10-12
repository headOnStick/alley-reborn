# Access Credentials - Alley-Reborn Discovery

## Portal Alley (Staging Environment)

### Web Access
- **URL**: `https://stg-fe-alley-hooper.hoopers.club/login`
- **Environment**: Staging (dados reais, não produção)
- **Status**: Ativo e acessível

### Credentials

#### HTTP Basic Auth (Acesso ao domínio)
- **Username**: `alley`
- **Password**: `Hooper2025#`
- **Nota**: Requerido para acessar o domínio staging antes do login da aplicação

#### Login da Aplicação
- **Email**: `arocha@hoopers.club`
- **Password**: `arocha@hoopers.cluB`
- **Nota**: Senha tem 'B' maiúsculo no final

### Access Level
- Full access para análise e auditoria
- Não fazer modificações permanentes sem autorização
- Usar para screenshots, análise de páginas, e inventários

### Browser Requirements
- Funciona em navegadores modernos (Chrome, Firefox, Edge)
- JavaScript deve estar habilitado
- Cookies devem ser aceitos para manter sessão

---

## Segurança e Boas Práticas

### ⚠️ Proteção de Credenciais
- **NÃO compartilhar publicamente** estas credenciais
- **NÃO commitar** em repositórios públicos
- **NÃO expor** em screenshots ou documentação externa
- **Usar apenas** para fins de auditoria autorizada
- **Documentar apenas** neste ficheiro (projeto privado)

### ✅ Uso Autorizado
- Navegar livremente para análise
- Capturar screenshots de páginas
- Testar funcionalidades e fluxos
- Analisar dados apresentados no portal

### ❌ Uso Não Autorizado
- Deletar ou modificar dados de clientes
- Criar contas adicionais sem autorização
- Modificar configurações do sistema
- Exportar dados sensíveis para fora do projeto
- Compartilhar acesso com terceiros

---

## Troubleshooting

### Portal Não Acessível

**Sintoma**: Página não carrega ou erro de conexão

**Verificações**:
1. URL está correta (incluindo `https://`)
2. HTTP Basic Auth fornecido corretamente
3. Conexão à internet estável
4. Domínio não bloqueado por firewall/VPN

**Solução**:
- Tentar em browser diferente
- Limpar cache/cookies
- Verificar com arocha@hoopers.club se ambiente staging está ativo

---

### Login Falha

**Sintoma**: Credenciais rejeitadas ou erro de autenticação

**Verificações**:
1. Email correto: `arocha@hoopers.club`
2. Senha com 'B' maiúsculo: `arocha@hoopers.cluB`
3. HTTP Basic Auth já fornecido antes
4. Sessão não expirada

**Solução**:
- Verificar caps lock não está ativo
- Copiar/colar credenciais exatamente como documentado
- Fazer logout e tentar novamente
- Contactar arocha@hoopers.club se persistir

---

### Sessão Expira Frequentemente

**Sintoma**: Precisa fazer login novamente após alguns minutos

**Verificações**:
1. Cookies estão habilitados
2. Navegador não está em modo privado/incógnito
3. Não há extensões bloqueando cookies

**Solução**:
- Usar modo normal do browser (não privado)
- Aceitar cookies quando solicitado
- Manter uma tab aberta para manter sessão ativa

---

## Playwright Automation

### Configuração de Login Automatizado

**HTTP Basic Auth**:
```javascript
// NÃO funciona diretamente na URL
// Playwright MCP já trata isto automaticamente
```

**Form Login**:
```javascript
// Navegar para página de login
await page.goto('https://stg-fe-alley-hooper.hoopers.club/login');

// Preencher email
await page.getByRole('textbox', { name: 'Enter your email' })
  .fill('arocha@hoopers.club');

// Preencher senha
await page.getByRole('textbox', { name: 'Enter your password' })
  .fill('arocha@hoopers.cluB');

// Click em Sign in
await page.getByRole('button', { name: 'Sign in' }).click();

// Aguardar navegação para dashboard
await page.waitForURL('**/dashboard');
```

**Tempo de Espera Recomendado**:
- Após navegação: 5-10 segundos (para APIs carregarem)
- Após click em tab: 5 segundos (para dados carregarem)

---

## Status de Acesso

### Histórico de Uso

**2025-10-10 - Sprint 2**:
- ✅ Portal acessado com sucesso via Playwright
- ✅ Login automatizado configurado e testado
- ✅ Navegação de 6 páginas principais completa
- ✅ 25 tabs navegadas sem erros de autenticação
- ✅ 26 screenshots capturados com sucesso

### Próximos Acessos Necessários
- ⏳ Repositório Git (para análise de código frontend) - Ver `/01-context/resources.md`
- ⏳ Links Attio (para reuniões com clientes) - Ver `/01-context/resources.md`

---

## Referências Relacionadas

Para informações sobre:
- **Repositório Git, Attio, Ferramentas**: Ver `/01-context/resources.md`
- **Stakeholders e quando contactar**: Ver `/01-context/stakeholders.md`
- **Overview da plataforma**: Ver `/01-context/platform-overview.md`
- **Processos de auditoria**: Ver `/CLAUDE.md`

---

**Este ficheiro contém informações sensíveis. Acesso restrito ao projeto Alley-Reborn.**

**⚠️ CONFIDENCIAL - Não compartilhar externamente**

**Última atualização**: 2025-10-10
