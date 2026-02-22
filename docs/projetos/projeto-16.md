# Projeto Final: Aula 16 – Aplicação Fullstack e Deploy 🚀

!!! tip "Objetivo"
    O desafio final! Integrar todos os conhecimentos do curso para criar uma aplicação completa (Node + React + TS), containerizar com Docker e preparar para o Deploy.

---

## 🏗️ Requisitos do Projeto
- **Backend**: API de catálogo de produtos com Node e Express.
- **Frontend**: Dashboard para visualização e compra via React.
- **Integração**: Consumo da API própria usando Axios e Zod.
- **Docker**: Criar um `Dockerfile` funcional.
- **Build**: Scripts de build para produção ativos.

---

## 🛠️ Etapas de Execução

### 1. Desenvolvimento Integrado
- Aplique **Interfaces** e **Shared Types** entre os projetos.
- Utilize **Design Patterns** (Repository/Service) no Backend.
- Garanta **Testes Unitários** no núcleo da aplicação.

### 2. Preparação para Produção
No `package.json`:
```json
"scripts": {
  "build": "tsc",
  "start": "node dist/index.js"
}
```

### 3. Containerização (Docker)
```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build
EXPOSE 3000
CMD ["npm", "start"]
```

---

## ✅ Critérios de Sucesso
- [ ] A aplicação roda localmente via `npm run dev`.
- [ ] O build de produção é gerado sem erros de tipagem.
- [ ] A imagem Docker é construída com sucesso.
- [ ] Existe uma documentação (`README.md`) explicando como rodar o projeto.

---

## 🚀 Rumo ao Deploy!
Parabéns por chegar até aqui. Sua aplicação está pronta para o mundo real!