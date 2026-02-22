# Mini-Projeto: Aula 10 – API de Tarefas (Backend com Node.js) 🟢

!!! tip "Objetivo"
    Construir uma API REST funcional para gerenciamento de tarefas utilizando Node.js, Express e TypeScript, focando na tipagem de Request/Response e uso de DTOs.

---

## 🏗️ Requisitos do Projeto
- Criar rotas para: Listar, Criar e Deletar tarefas.
- Tipar rigorosamente o corpo da requisição (`JSON Body`).
- Implementar um middleware simples de log.
- Usar uma estrutura de "Base de Dados" em memória (Array tipado).

---

## 🛠️ Passo a Passo

### 1. Servidor Básico
```typescript
import express, { Request, Response } from 'express';

const app = express();
app.use(express.json());

interface Tarefa {
    id: number;
    titulo: string;
    feita: boolean;
}

const db: Tarefa[] = [];
```

### 2. Rotas Tipadas
```typescript
app.get('/tarefas', (req: Request, res: Response) => {
    res.json(db);
});

app.post('/tarefas', (req: Request<{}, {}, Omit<Tarefa, 'id'>>, res: Response) => {
    const nova: Tarefa = { id: Date.now(), ...req.body };
    db.push(nova);
    res.status(201).json(nova);
});
```

---

## ✅ Desafio Extra
- Crie um middleware que verifique se o campo `titulo` está presente no corpo da requisição antes de passar para a rota de criação.
- Implemente a rota `DELETE /tarefas/:id` tratando o parâmetro `id` de forma tipada.