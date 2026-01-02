---
description: Otimiza o código para melhor performance
---

# Otimizar Código

Analise o código fornecido e aplique **otimizações de performance** mantendo a mesma funcionalidade.

## Áreas de otimização:

### Performance
- Reduzir complexidade de algoritmos (Big O)
- Eliminar operações redundantes
- Implementar caching onde faz sentido
- Converter operações síncronas para assíncronas quando apropriado

### Next.js / React
- Adicionar `useMemo` para cálculos pesados
- Adicionar `useCallback` para funções passadas como props
- Implementar `React.memo` em componentes que re-renderizam sem necessidade
- Usar `dynamic` import para code splitting
- Otimizar imagens com `next/image`

### MongoDB / Mongoose
- Adicionar `.lean()` em queries de leitura
- Usar projeções para buscar só campos necessários
- Sugerir índices para queries frequentes
- Substituir múltiplas queries por aggregation com `$lookup`

### Bundle Size
- Remover imports não utilizados
- Sugerir alternativas mais leves para bibliotecas pesadas
- Tree shaking de imports

## Formato da resposta:

### Código Otimizado
```typescript
// código otimizado aqui
```

### Mudanças Realizadas
Lista cada otimização feita e o motivo:

| Mudança | Antes | Depois | Ganho Esperado |
|---------|-------|--------|----------------|
| ... | ... | ... | ... |

### Métricas (se mensurável)
- Redução estimada de tempo de execução
- Redução estimada de bundle size
- Redução de chamadas ao banco

$ARGUMENTS
