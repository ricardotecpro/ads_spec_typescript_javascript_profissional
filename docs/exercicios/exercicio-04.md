# Exercícios: Aula 04 – Interfaces e Modelagem de Domínio 🏗️

### 🟢 Nível: Básico
1.  **Interface Simples**: Crie uma interface `Usuario` com `nome`, `idade` e uma propriedade opcional `site`.
2.  **Extensão**: Crie uma interface `Admin` que estenda `Usuario` e adicione a propriedade `nivel` (número).

### 🟡 Nível: Intermediário
3.  **Readonly**: Crie uma interface `Configuracao` onde todas as propriedades sejam `readonly`. Tente alterar uma após a criação.
4.  **Interface de Função**: Defina uma interface para uma função que receba dois números e retorne um booleano.

### 🔴 Nível: Desafio
5.  **Modelagem de Sistema**: Modele as interfaces para um sistema de "Pedidos de Ecommerce". Deve haver um `Cliente`, um `Produto` e um `Pedido` (que contém uma lista de produtos e o cliente).