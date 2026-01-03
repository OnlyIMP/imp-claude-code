---
description: Analisa todo o projeto em busca de problemas de performance e oportunidades de otimização
---

# Análise de Performance e Otimização

Leia e analise **todo o projeto** em busca de problemas de performance e oportunidades de otimização.

## Instruções:

1. **Primeiro**, mapeie a estrutura do projeto inteiro
2. **Depois**, analise cada arquivo relevante (.ts, .tsx, .js, .jsx)
3. **Liste** todos os problemas encontrados
4. **NÃO faça nenhuma alteração** - apenas liste e explique
5. **No final**, pergunte se desejo que você corrija algum item específico

## O que procurar:

### Geral
- Algoritmos que podem ser mais eficientes
- Loops desnecessários ou ineficientes
- Operações redundantes
- Operações síncronas que deveriam ser assíncronas
- Chamadas de API repetidas que poderiam ser cacheadas
- Caching que poderia ser implementado
- Memory leaks potenciais

### Next.js / React
- Componentes re-renderizando desnecessariamente
- Falta de `useMemo`, `useCallback` ou `React.memo`
- Imagens sem otimização (deveria usar `next/image`)
- Falta de lazy loading / `dynamic` import em componentes pesados
- `useEffect` com dependências incorretas

### MongoDB / Mongoose
- Queries sem índices apropriados
- Falta de `.lean()` em queries de leitura
- N+1 queries
- Projeções faltando (buscando campos desnecessários)
- Queries que poderiam ser agregadas em uma só

### Bundle Size
- Imports que podem ser mais específicos
- Bibliotecas pesadas que têm alternativas leves
- Código morto que pode ser removido

## Formato da resposta:

### 📊 Resumo Geral
- Total de arquivos analisados: X
- Problemas críticos: X
- Problemas médios: X
- Problemas leves: X
- Ganho estimado de performance: X%

### 🔴 Problemas Críticos (impacto alto)

| # | Arquivo | Linha | Problema | Impacto |
|---|---------|-------|----------|---------|
| 1 | ... | ... | ... | ... |

### 🟡 Problemas Médios

| # | Arquivo | Linha | Problema | Impacto |
|---|---------|-------|----------|---------|
| 1 | ... | ... | ... | ... |

### 🟢 Problemas Leves

| # | Arquivo | Linha | Problema | Impacto |
|---|---------|-------|----------|---------|
| 1 | ... | ... | ... | ... |

---

**Deseja que eu corrija algum problema específico? Informe o número ou "todos" para corrigir tudo.**
