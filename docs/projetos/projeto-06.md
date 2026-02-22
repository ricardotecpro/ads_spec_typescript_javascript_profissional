# Mini-Projeto: Aula 06 – Repositório de Dados Genérico (Generics) 📦

!!! tip "Objetivo"
    Criar uma estrutura de dados genérica e reutilizável que possa gerenciar qualquer tipo de entidade (Usuários, Produtos, etc.) mantendo a tipagem original.

---

## 🏗️ Requisitos do Projeto
- Classe genérica `Repository<T>`.
- Restrição (`Constraints`) para garantir que as entidades possuam um `id`.
- Métodos para Adicionar, Listar, Buscar por ID e Remover.

---

## 🛠️ Passo a Passo

### 1. Interface de Entidade
```typescript
interface Entity {
    id: number | string;
}
```

### 2. Classe Repositório
```typescript
class Repository<T extends Entity> {
    private data: T[] = [];

    add(item: T): void {
        this.data.push(item);
    }

    getAll(): T[] {
        return this.data;
    }

    findById(id: number | string): T | undefined {
        return this.data.find(item => item.id === id);
    }

    remove(id: number | string): void {
        this.data = this.data.filter(item => item.id !== id);
    }
}
```

---

## ✅ Desafio Extra
- Crie uma interface `User` e uma `Product` e instancie repositórios específicos para cada uma: `const userRepo = new Repository<User>()`.
- Implemente um método `update(id, item)` que atualize os dados de uma entidade sem mudar seu `id`.