# Mini-Projeto: Aula 04 – Sistema de Gerenciamento de Tarefas (Interfaces) ✅

!!! tip "Objetivo"
    Modelar um sistema de tarefas (To-Do) corporativo usando `interfaces`, propriedades opcionais e herança de interfaces.

---

## 🏗️ Requisitos do Projeto
- Interface para `Usuario`.
- Interface para `Tarefa` com campos opcionais.
- Interface para `Projeto` que agrupa várias tarefas.
- Garantir imutabilidade em campos críticos com `readonly`.

---

## 🛠️ Passo a Passo

### 1. Definição das Interfaces
```typescript
interface IUser {
    readonly id: number;
    nome: string;
    email: string;
}

interface ITask {
    titulo: string;
    descricao?: string;
    concluida: boolean;
    responsavel: IUser;
}

interface IProject {
    nome: string;
    tarefas: ITask[];
}
```

### 2. Implementação
Crie uma função que receba um `IProject` e retorne apenas as tarefas concluídas.
```typescript
const meuProjeto: IProject = {
    nome: "Refatoração TS",
    tarefas: [
        { titulo: "Setup", concluida: true, responsavel: { id: 1, nome: "R", email: "r@b.com" } },
        { titulo: "Build", concluida: false, responsavel: { id: 1, nome: "R", email: "r@b.com" } }
    ]
};

function listarConcluidas(projeto: IProject): ITask[] {
    return projeto.tarefas.filter(t => t.concluida);
}
```

---

## ✅ Desafio Extra
- Crie uma interface `ITaskUrgente` que estende `ITask` e adiciona um campo `prazo: Date`.
- Use `Declaration Merging` para adicionar uma propriedade `avatar` na interface `IUser`.