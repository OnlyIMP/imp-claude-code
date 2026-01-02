---
description: Analisa e corrige problemas de lint no código
---

# Lint e Correções

Analise o código fornecido aplicando regras de **ESLint**, **Prettier** e **boas práticas de TypeScript**.

## O que verificar:

### ESLint
- Variáveis não utilizadas
- Imports não utilizados
- Console.log esquecidos
- Funções async sem await
- Promises não tratadas
- Comparações com == ao invés de ===
- Hooks fora de ordem ou condicionais

### Prettier / Formatação
- Indentação inconsistente
- Ponto e vírgula faltando ou sobrando
- Aspas simples vs duplas (manter consistência)
- Trailing commas
- Largura de linha (max 80-100 chars)

### TypeScript
- Tipos implícitos que deveriam ser explícitos
- Uso de `any`
- Assertions desnecessárias
- Tipos que poderiam ser mais específicos
- Null checks faltando

### React / Next.js
- Keys faltando em listas
- Dependências de useEffect incorretas
- useState com tipo inferido errado
- Props sem tipagem

## Formato da resposta:

### Problemas Encontrados

| Linha | Problema | Severidade | Regra |
|-------|----------|------------|-------|
| 10 | Variável não utilizada | warning | no-unused-vars |
| 23 | Console.log | error | no-console |
| ... | ... | ... | ... |

### Código Corrigido

```typescript
// código com todas as correções aplicadas
```

### Resumo
- ✅ X problemas corrigidos
- ⚠️ X avisos
- ❌ X erros

$ARGUMENTS
