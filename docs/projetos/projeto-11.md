# Mini-Projeto: Aula 11 – Dashboard de Usuários (Frontend React) ⚛️

!!! tip "Objetivo"
    Desenvolver uma interface simples em React com TypeScript para listar e adicionar usuários, focando na tipagem de Props, Hooks e Eventos.

---

## 🏗️ Requisitos do Projeto
- Componente `UserCard` tipado.
- Formulário para adicionar novos usuários.
- Uso de `useState` com interface genérica.
- Tipagem de eventos de clique e mudança de input.

---

## 🛠️ Passo a Passo

### 1. Definição da Interface
```typescript
interface User {
    id: number;
    nome: string;
    cargo: string;
}
```

### 2. Componente de Lista
```tsx
const UserList = () => {
    const [users, setUsers] = useState<User[]>([]);

    const addUser = (nome: string) => {
        const newUser = { id: Date.now(), nome, cargo: "Dev" };
        setUsers([...users, newUser]);
    };

    return (
        <div>
            {users.map(u => <UserCard key={u.id} user={u} />)}
            <Form onAdd={addUser} />
        </div>
    );
};
```

---

## ✅ Desafio Extra
- Crie um `Context API` para gerenciar o tema da aplicação (Light/Dark) e garanta que o provedor e o hook `useTheme` estejam 100% tipados.
- Tipar o evento do formulário para evitar o recarregamento da página (`e.preventDefault()`).