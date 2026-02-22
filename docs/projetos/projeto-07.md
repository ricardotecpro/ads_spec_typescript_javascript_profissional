# Mini-Projeto: Aula 07 – Formulário de Perfil (Utility Types) ⚙️

!!! tip "Objetivo"
    Utilizar utilitários como `Partial`, `Readonly`, `Pick` e `Omit` para gerenciar diferentes estados de um perfil de usuário em uma aplicação.

---

## 🏗️ Requisitos do Projeto
- Interface completa de `UserProfile`.
- Criar um tipo para "Visualização Pública" (omitindo dados sensíveis).
- Criar um tipo para "Atualização de Perfil" (permitindo campos parciais).
- Garantir que o ID do usuário seja imutável.

---

## 🛠️ Passo a Passo

### 1. Modelo Base
```typescript
interface UserProfile {
    id: number;
    nome: string;
    email: string;
    telefone?: string;
    senhaHash: string;
    dataCriacao: Date;
}
```

### 2. Uso de Utility Types
```typescript
// Apenas o que o usuário pode ver de outros
type PublicProfile = Omit<UserProfile, "senhaHash" | "email">;

// O que enviamos para o banco ao atualizar (ID obrigatório, resto parcial)
type UpdatePayload = Partial<Omit<UserProfile, "id" | "dataCriacao">> & { id: number };

// Usuário imutável após carregado
type SecureUser = Readonly<UserProfile>;
```

---

## ✅ Desafio Extra
- Use `Pick` para criar um tipo `UserContact` que contenha apenas `nome` e `email`.
- Use `Record` para criar um objeto que mapeie `id` do usuário para seu `PublicProfile`.