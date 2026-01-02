---
description: Analisa todo o projeto buscando problemas de código, lint, formatação e organização
---

# Limpar Código

Leia **todo o projeto** e liste todos os problemas de código, lint, formatação, TypeScript e organização.

## Instruções:

1. **Primeiro**, mapeie a estrutura do projeto inteiro
2. **Depois**, analise cada arquivo (.ts, .tsx, .js, .jsx)
3. **Liste** todos os problemas encontrados
4. **NÃO faça nenhuma alteração** - apenas liste
5. **No final**, pergunte se desejo que você corrija algum item

## O que verificar:

### Código Não Usado
- Variáveis não utilizadas
- Imports não utilizados
- Funções que nunca são chamadas
- Arquivos que não são importados
- Código comentado que deveria ser removido

### ESLint
- Console.log esquecidos
- Funções async sem await
- Promises não tratadas
- Comparações com == ao invés de ===
- Hooks fora de ordem ou em condicionais

### Formatação
- Indentação inconsistente
- Ponto e vírgula faltando ou sobrando
- Aspas simples vs duplas (inconsistência)
- Linhas muito longas (> 100 chars)

### TypeScript
- Tipos implícitos que deveriam ser explícitos
- Uso de `any`
- Assertions desnecessárias
- Null checks faltando
- Tipos que poderiam ser mais específicos

### React / Next.js
- Keys faltando em listas/maps
- Dependências de useEffect incorretas
- Props sem tipagem

### Organização
- Arquivos muito grandes que deveriam ser divididos
- Funções muito longas (mais de 50 linhas)
- Código duplicado que deveria ser extraído
- Nomenclatura ruim (data, temp, x, y)
- Funções com muitos parâmetros (mais de 4)

## Formato da resposta:

### 📊 Resumo Geral
- Arquivos analisados: X
- Total de problemas: X
- Erros: X
- Avisos: X

### 🔴 Erros (devem ser corrigidos)

| # | Arquivo | Linha | Problema | Tipo |
|---|---------|-------|----------|------|
| 1 | ... | ... | ... | ... |

### 🟡 Avisos (recomendado corrigir)

| # | Arquivo | Linha | Problema | Tipo |
|---|---------|-------|----------|------|
| 1 | ... | ... | ... | ... |

### 🔵 Formatação e Organização

| # | Arquivo | Linha | Problema |
|---|---------|-------|----------|
| 1 | ... | ... | ... |

### 📋 Resumo por Arquivo

| Arquivo | Erros | Avisos | Formatação |
|---------|-------|--------|------------|
| ... | X | X | X |

---

**Deseja que eu corrija algum problema? Informe:**
- Número específico (ex: "1, 5, 7")
- "todos" para corrigir tudo
- Nome do arquivo para corrigir um arquivo inteiro
