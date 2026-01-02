---
description: Analisa o código em busca de problemas de performance
---

# Análise de Performance

Analise o código fornecido ou o arquivo atual em busca de **problemas de performance**.

## O que procurar:

### Geral
- Loops desnecessários ou ineficientes
- Operações síncronas que deveriam ser assíncronas
- Chamadas de API repetidas que poderiam ser cacheadas
- Memory leaks potenciais
- Imports desnecessários aumentando bundle size

### Next.js / React
- Componentes re-renderizando desnecessariamente
- Falta de `useMemo`, `useCallback` ou `React.memo` onde necessário
- Imagens sem otimização (usar `next/image`)
- Falta de lazy loading em componentes pesados
- `useEffect` com dependências incorretas causando loops

### MongoDB
- Queries sem índices apropriados
- Falta de `.lean()` quando não precisa de métodos do Mongoose
- N+1 queries (múltiplas queries quando uma com `$lookup` resolveria)
- Projeções faltando (buscando campos desnecessários)

### TypeScript
- Uso excessivo de `any` que poderia ser tipado
- Type assertions desnecessárias

## Formato da resposta:

Para cada problema encontrado, forneça:

1. **Localização**: Arquivo e linha
2. **Problema**: O que está errado
3. **Impacto**: Qual o custo de performance (baixo/médio/alto)
4. **Solução**: Código corrigido

Se nenhum problema for encontrado, confirme que o código está otimizado.

$ARGUMENTS
