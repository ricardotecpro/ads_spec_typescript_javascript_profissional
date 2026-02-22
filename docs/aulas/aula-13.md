# Aula 13 – Testes com TypeScript 🧪

!!! tip "Objetivo"
    Nesta aula, aprenderemos a garantir a qualidade e a estabilidade do nosso código usando testes automatizados. Veremos como configurar o Jest com TypeScript, criar mocks tipados e escrever testes unitários e de integração robustos.

---

## 1. Configurando o Jest com TypeScript 🛠️

O Jest é o framework de testes mais popular no ecossistema JS/TS. Para rodar testes em TS, usamos o `ts-jest`.

### Instalação
<div class="termy" data-termynal>
  <span data-ty="input">npm install -D jest ts-jest @types/jest</span>
  <span data-ty="input">npx ts-jest config:init</span>
</div>

---

## 2. Testes Unitários Tipados 🧩

Testes unitários testam a menor parte possível do código (funções, classes) de forma isolada.

```typescript
// math.ts
export const somar = (a: number, b: number) => a + b;

// math.test.ts
import { somar } from './math';

describe('Função somar', () => {
    it('deve retornar 5 ao somar 2 e 3', () => {
        const resultado: number = somar(2, 3);
        expect(resultado).toBe(5);
    });
});
```

---

## 3. Mocks Tipados com TypeScript 🎭

Mocks são usados para substituir dependências complexas (como APIs ou Banco de Dados) por versões controladas durante os testes.

```typescript
import axios from 'axios';
import { buscarUsuario } from './servico';

jest.mock('axios');
const mockedAxios = axios as jest.Mocked<typeof axios>;

it('deve buscar um usuário com sucesso', async () => {
    mockedAxios.get.mockResolvedValue({ data: { id: 1, nome: "Ricardo" } });
    const user = await buscarUsuario(1);
    expect(user.nome).toBe("Ricardo");
});
```

---

## 4. Testes de Integração 🔗

Testes de integração verificam se diferentes partes do sistema (como Rotas da API e Lógica de Negócio) funcionam bem juntas.

```typescript
import request from 'supertest';
import app from './app';

describe('API de Usuários', () => {
    it('deve criar um novo usuário', async () => {
        const res = await request(app)
            .post('/usuarios')
            .send({ nome: 'Teste', email: 'teste@exemplo.com' });
        
        expect(res.status).toBe(201);
        expect(res.body.nome).toBe('Teste');
    });
});
```

---

## 5. Visualizando o Ciclo de Testes (Mermaid)

```mermaid
graph TD;
    Red[1. Falha (Vermelho)] --> Green[2. Passa (Verde)];
    Green --> Refactor[3. Refatoração];
    Refactor --> Red;
    style Red fill:#f99,stroke:#333
    style Green fill:#9f9,stroke:#333
    style Refactor fill:#99f,stroke:#333
```

---

## 6. Exercícios Práticos 📝

1. **Básico**: Configure o Jest em um projeto TypeScript e crie um teste para uma função de multiplicão simples.
2. **Básico**: Escreva um teste que verifique se uma função que lança erro realmente o faz (use `toThrow()`).
3. **Intermediário**: Crie uma classe `Calculadora` e escreva um conjunto de testes (`describe`) para todos os seus métodos.
4. **Intermediário**: Use o `jest.spyOn()` para verificar se uma função foi chamada dentro de outra.
5. **Desafio**: Escreva um teste de integração para uma rota `GET /produtos` que deve retornar uma lista de produtos tipados.

---

## 🚀 Mini-Projeto da Aula
Crie uma **Suíte de Testes para o Repositório Genérico**.
- Recupere o código do repositório da Aula 06.
- Escreva testes unitários para os métodos `salvar`, `obterTodos` e `buscarPorId`.
- Garanta 100% de cobertura nos métodos do repositório.
- Use mocks se o repositório depender de alguma função externa de persistência.

---
**Próxima Aula**: Vamos aprender a aplicar as melhores práticas de design com [Padrões de Projeto com TypeScript](./aula-14.md)!