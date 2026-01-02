---
description: Executa build local e deploy para o servidor de produção
---

# Deploy para Produção

Execute o deploy completo do projeto para o servidor de produção.

## Instruções:

1. **Primeiro**, leia o arquivo CLAUDE.md do projeto para entender os comandos de deploy
2. **Execute** o build local para verificar se compila
3. **Se o build passar**, execute o deploy para o servidor
4. **Mostre** o progresso de cada etapa
5. **No final**, confirme se o deploy foi bem sucedido

## Etapas do Deploy:

### 1. Build Local
```bash
npm run build
```

Se falhar, **PARE** e mostre os erros para correção.

### 2. Sync de Arquivos (via WSL)
Envie os arquivos para o servidor excluindo:
- `node_modules`
- `.next`
- `.git`

### 3. Build e Reload no Servidor
Execute o script de deploy no servidor que faz:
- Instalação de dependências (se necessário)
- Build de produção
- Reload gracioso do PM2 (zero-downtime)

## Formato da resposta:

### 🚀 Deploy em Progresso

| Etapa | Status | Tempo |
|-------|--------|-------|
| Build local | ✅ / ❌ | Xs |
| Sync arquivos | ✅ / ❌ | Xs |
| Build servidor | ✅ / ❌ | Xs |
| PM2 reload | ✅ / ❌ | Xs |

### 📋 Detalhes

**Arquivos sincronizados:** X arquivos
**Tempo total:** X segundos

### ✅ Deploy Concluído

ou

### ❌ Deploy Falhou

**Erro:** [descrição do erro]
**Solução sugerida:** [como corrigir]

---

## Comandos de Referência (CLAUDE.md)

Os comandos específicos de deploy devem ser lidos do CLAUDE.md do projeto, que contém:
- IP do servidor
- Caminhos dos arquivos
- Script deploy.sh
- Comandos PM2

**IMPORTANTE:**
- Sempre leia o CLAUDE.md antes de executar
- Use os comandos WSL conforme documentado
- O deploy é zero-downtime (site continua funcionando durante o build)
