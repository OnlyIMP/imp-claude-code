---
description: Encontra código repetido que pode ser centralizado em um único lugar
---

# Encontrar Repetições

Leia **todo o projeto** e encontre código repetido que poderia ser centralizado para reutilização.

## Instruções:

1. **Primeiro**, mapeie a estrutura do projeto inteiro
2. **Depois**, analise cada arquivo buscando padrões repetidos
3. **Liste** todas as repetições encontradas
4. **NÃO faça nenhuma alteração** - apenas liste e sugira
5. **No final**, pergunte se desejo que você centralize algum item

## O que buscar:

### Funções Duplicadas
- Funções que fazem a mesma coisa em arquivos diferentes
- Lógica idêntica com nomes diferentes
- Funções muito similares que poderiam ser uma só com parâmetros

### Queries MongoDB/Mongoose
- Mesma query em múltiplos arquivos
- Queries similares que poderiam ser centralizadas em um service
- Padrões de populate/select repetidos

### Componentes Similares
- Componentes React muito parecidos (>70% igual)
- Componentes que só mudam props/estilos
- Lógica de componente duplicada

### Constantes Hardcoded
- URLs de API repetidas em vários arquivos
- Valores mágicos (números, strings) repetidos
- Configurações duplicadas

### Validações
- Regex de validação repetidas (email, CPF, telefone)
- Schemas de validação similares (Zod, Yup)
- Lógica de validação duplicada

### Hooks Duplicados
- useEffect com mesma lógica em componentes diferentes
- Custom hooks que fazem a mesma coisa
- Lógica de estado repetida

### Estilos
- Classes Tailwind repetidas que poderiam ser componentes
- Estilos CSS duplicados
- Variáveis de cor/espaçamento hardcoded

### Try/Catch e Error Handling
- Mesmo padrão de tratamento de erro em vários lugares
- Toast/notificações repetidas
- Lógica de loading state duplicada

## Formato da resposta:

### 📊 Resumo das Repetições
- Arquivos analisados: X
- Repetições encontradas: X
- Linhas de código que podem ser reduzidas: ~X

### 🔴 Alto Impacto (centralizar urgente)

| # | O que está repetido | Onde aparece | Sugestão |
|---|---------------------|--------------|----------|
| 1 | `formatDate()` | 5 arquivos | Criar `utils/date.ts` |
| 2 | Query de usuário | 4 arquivos | Criar `services/user.service.ts` |

**Detalhes:**

#### 1. formatDate()
```typescript
// Aparece em:
// - src/components/Card.tsx:25
// - src/pages/produto.tsx:42
// - src/pages/pedido.tsx:18

// Código repetido:
const formatDate = (date) => {
  return new Date(date).toLocaleDateString('pt-BR')
}

// Sugestão - criar utils/date.ts:
export function formatDate(date: Date | string): string {
  return new Date(date).toLocaleDateString('pt-BR')
}
```

### 🟡 Médio Impacto

| # | O que está repetido | Onde aparece | Sugestão |
|---|---------------------|--------------|----------|
| 1 | ... | ... | ... |

### 🟢 Baixo Impacto

| # | O que está repetido | Onde aparece | Sugestão |
|---|---------------------|--------------|----------|
| 1 | ... | ... | ... |

### 📁 Estrutura Sugerida

Baseado nas repetições, sugiro criar:

```
src/
├── utils/
│   ├── date.ts         # Funções de data
│   ├── format.ts       # Formatações (moeda, CPF, etc)
│   └── validators.ts   # Validações (email, CPF, etc)
├── services/
│   ├── user.service.ts    # Queries de usuário
│   └── product.service.ts # Queries de produto
├── hooks/
│   └── useDebounce.ts  # Hooks reutilizáveis
└── config/
    └── constants.ts    # URLs, valores fixos
```

---

**Deseja que eu centralize algum item? Informe:**
- Número específico (ex: "1, 3")
- "todos" para centralizar tudo
- "alto" para centralizar só os de alto impacto
