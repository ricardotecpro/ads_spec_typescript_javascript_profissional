# Mini-Projeto: Aula 12 – Buscador de Repositórios (Integração API) 📡

!!! tip "Objetivo"
    Consumir a API pública do GitHub para buscar repositórios de um usuário, aplicando tipagem de dados externos, tratamento de erros e validação com Zod.

---

## 🏗️ Requisitos do Projeto
- Usar `Axios` para realizar as chamadas HTTP.
- Definir interfaces para a resposta do GitHub.
- Validar os dados recebidos com um schema `Zod`.
- Implementar tratamento de erro para usuários não encontrados.

---

## 🛠️ Passo a Passo

### 1. Schema de Validação (Zod)
```typescript
import { z } from 'zod';

const RepoSchema = z.object({
    name: z.string(),
    description: z.string().nullable(),
    stargazers_count: z.number(),
    html_url: z.string().url()
});

type Repo = z.infer<typeof RepoSchema>;
```

### 2. Chamada de API com Axios
```typescript
async function getRepos(user: string): Promise<Repo[]> {
    const { data } = await axios.get<Repo[]>(`https://api.github.com/users/${user}/repos`);
    // Validar cada repositório da lista
    return data.map(r => RepoSchema.parse(r));
}
```

---

## ✅ Desafio Extra
- Crie uma função "Mapper" que transforme as chaves vindas do GitHub (ex: `stargazers_count`) para nomes mais amigáveis no seu código (ex: `estrelas`).
- Exiba uma mensagem de erro customizada caso a API retorne um erro 404 (Usuário não encontrado).