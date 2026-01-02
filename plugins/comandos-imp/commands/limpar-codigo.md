---
description: Refatora e limpa o código seguindo boas práticas
---

# Limpar Código

Refatore o código fornecido aplicando **clean code** e **boas práticas** sem alterar a funcionalidade.

## O que fazer:

### Nomenclatura
- Renomear variáveis/funções com nomes descritivos
- Usar convenções consistentes (camelCase para variáveis, PascalCase para componentes)
- Remover abreviações confusas

### Estrutura
- Extrair funções muito longas em funções menores
- Remover código duplicado (DRY)
- Remover código morto/comentado
- Organizar imports (externos primeiro, depois internos)

### TypeScript
- Adicionar tipos onde estiver faltando
- Remover `any` desnecessários
- Criar interfaces/types para objetos complexos
- Usar enums para valores fixos

### React / Next.js
- Separar lógica de UI (custom hooks)
- Componentizar elementos repetidos
- Ordenar hooks no topo do componente
- Props destructuring consistente

### Legibilidade
- Adicionar espaçamento adequado
- Simplificar condicionais complexas
- Usar early returns para reduzir aninhamento
- Adicionar comentários APENAS onde realmente necessário

## Formato da resposta:

### Código Refatorado
```typescript
// código limpo aqui
```

### Mudanças Realizadas
- [ ] Lista cada mudança feita
- [ ] Explique brevemente o motivo

### Arquivos Sugeridos (se aplicável)
Se fizer sentido dividir em múltiplos arquivos, sugira a estrutura:
```
/components
  /NomeComponente
    index.tsx
    useNomeComponente.ts  (hook)
    types.ts              (tipos)
```

$ARGUMENTS
