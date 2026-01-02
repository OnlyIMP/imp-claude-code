---
description: Planeja a implementação de uma nova feature
argument-hint: [descrição da feature]
---

# Planejar Feature

Crie um **plano detalhado de implementação** para a feature descrita.

## Instruções:

1. **Primeiro**, leia o projeto atual para entender a estrutura existente
2. **Depois**, crie o plano adaptado ao projeto
3. **NÃO implemente nada** - apenas planeje
4. **No final**, pergunte se desejo que você comece a implementar

## Estrutura do plano:

### 1. Resumo da Feature
- O que é
- Qual problema resolve
- Quem vai usar

### 2. Análise do Projeto Atual
- Como essa feature se encaixa no projeto existente
- O que já existe que pode ser reaproveitado
- O que precisa ser criado do zero

### 3. Requisitos Técnicos

#### Frontend (se aplicável)
- Componentes necessários
- Estados a gerenciar
- Rotas novas

#### Backend (se aplicável)
- Endpoints de API necessários
- Validações
- Autenticação/autorização

#### Banco de Dados (se aplicável)
- Collections/schemas novos ou alterações
- Índices necessários

### 4. Arquivos a Criar/Modificar

```
📁 Arquivos NOVOS a criar:
├── /app ou /pages
│   └── ...
├── /components
│   └── ...
└── /api
    └── ...

📝 Arquivos EXISTENTES a modificar:
├── ...
└── ...
```

### 5. Etapas de Implementação

Divida em tarefas pequenas e ordenadas:

| # | Etapa | Descrição | Tempo estimado |
|---|-------|-----------|----------------|
| 1 | ... | ... | ~X min |
| 2 | ... | ... | ~X min |

### 6. Dependências

- Pacotes npm necessários (se houver novos)
- Serviços externos (APIs, etc)
- Variáveis de ambiente novas (.env)

### 7. Considerações

- **Segurança**: Pontos de atenção
- **Performance**: Possíveis gargalos
- **Edge cases**: Casos especiais a tratar

### 8. Estimativa Total

| Fase | Tempo |
|------|-------|
| Setup inicial | X min |
| Backend | X min |
| Frontend | X min |
| Testes | X min |
| **Total** | **X horas** |

---

**Deseja que eu comece a implementar? Se sim, por qual etapa?**

---

Feature a planejar: $ARGUMENTS
