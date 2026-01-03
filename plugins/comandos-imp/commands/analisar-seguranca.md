---
description: Analisa o projeto em busca de falhas de segurança e vulnerabilidades
---

# Análise de Segurança

Leia **todo o projeto** e encontre falhas de segurança, vulnerabilidades e dados sensíveis expostos.

## Instruções:

1. **Primeiro**, mapeie a estrutura do projeto inteiro
2. **Depois**, analise cada arquivo buscando vulnerabilidades
3. **Liste** todas as falhas encontradas por severidade
4. **NÃO faça nenhuma alteração** - apenas liste e explique
5. **No final**, pergunte se desejo que você corrija algum item

## O que buscar:

### Dados Sensíveis Expostos
- API keys, tokens, senhas hardcoded no código
- Secrets em arquivos que não estão no .gitignore
- Dados sensíveis sendo enviados para o frontend (senhas, tokens internos)
- Console.log com dados sensíveis
- Variáveis de ambiente expostas no client-side

### Autenticação e Autorização
- Rotas sem verificação de autenticação
- Falta de verificação de permissões (qualquer usuário acessa qualquer coisa)
- Tokens JWT sem validação adequada
- Sessões que não expiram
- Senhas sem hash ou com hash fraco

### Injeção e XSS
- SQL/NoSQL Injection (queries com input do usuário sem sanitização)
- XSS (Cross-Site Scripting) - HTML/JS não escapado
- Command Injection (exec, spawn com input do usuário)
- Path Traversal (acesso a arquivos com input do usuário)

### Requisições e APIs
- CORS muito permissivo (Access-Control-Allow-Origin: *)
- Endpoints sem rate limiting
- Dados sensíveis na URL (tokens, senhas em query params)
- Falta de validação de input no backend
- Respostas de erro expondo stack trace ou info interna

### MongoDB / Mongoose
- Queries sem sanitização ($where, $regex com input do usuário)
- Falta de validação de ObjectId
- Projeção expondo campos sensíveis (senha, tokens)
- Operadores perigosos vindos do frontend

### Upload de Arquivos
- Sem validação de tipo de arquivo
- Sem limite de tamanho
- Arquivos salvos com nome original (path traversal)
- Execução de arquivos uploadados

### Next.js / React Específico
- getServerSideProps expondo dados sensíveis
- API Routes sem autenticação
- Variáveis NEXT_PUBLIC_ com dados sensíveis
- dangerouslySetInnerHTML sem sanitização
- Links externos sem rel="noopener noreferrer"

### Headers de Segurança
- Falta de Content-Security-Policy
- Falta de X-Frame-Options
- Falta de X-Content-Type-Options
- Falta de Strict-Transport-Security

### Dependências
- Pacotes com vulnerabilidades conhecidas
- Dependências desatualizadas com CVEs

## Formato da resposta:

### 📊 Resumo de Segurança
- Arquivos analisados: X
- Vulnerabilidades críticas: X
- Vulnerabilidades médias: X
- Vulnerabilidades baixas: X
- **Nível de risco geral:** 🔴 Alto / 🟡 Médio / 🟢 Baixo

### 🔴 Vulnerabilidades Críticas (corrigir URGENTE)

| # | Arquivo | Linha | Vulnerabilidade | Risco |
|---|---------|-------|-----------------|-------|
| 1 | ... | ... | ... | ... |

**Detalhes:**

#### 1. [Nome da vulnerabilidade]
```typescript
// Código vulnerável em src/api/users.ts:25
const user = await User.findOne({ email: req.body.email })
// Problema: Input não sanitizado, possível NoSQL injection
```

**Como explorar:** Um atacante poderia enviar `{"email": {"$gt": ""}}` e obter dados de outros usuários.

**Como corrigir:**
```typescript
// Validar e sanitizar input
const email = String(req.body.email).toLowerCase().trim()
const user = await User.findOne({ email })
```

### 🟡 Vulnerabilidades Médias

| # | Arquivo | Linha | Vulnerabilidade | Risco |
|---|---------|-------|-----------------|-------|
| 1 | ... | ... | ... | ... |

### 🟢 Vulnerabilidades Baixas

| # | Arquivo | Linha | Vulnerabilidade | Risco |
|---|---------|-------|-----------------|-------|
| 1 | ... | ... | ... | ... |

### 🔒 Recomendações Gerais

1. **Implementar:** [lista do que falta]
2. **Atualizar:** [dependências vulneráveis]
3. **Configurar:** [headers, CORS, etc]

### 📋 Checklist de Segurança

- [ ] Todas as rotas autenticadas estão protegidas
- [ ] Inputs são validados no backend
- [ ] Dados sensíveis não vazam para o frontend
- [ ] CORS está configurado corretamente
- [ ] Rate limiting implementado
- [ ] Headers de segurança configurados
- [ ] Dependências atualizadas

---

**Deseja que eu corrija alguma vulnerabilidade? Informe:**
- Número específico (ex: "1, 3")
- "criticas" para corrigir só as críticas
- "todas" para corrigir tudo
