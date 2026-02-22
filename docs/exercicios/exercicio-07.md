# Exercícios: Aula 07 – Utility Types e Manipulação de Tipos ⚙️

### 🟢 Nível: Básico
1.  **Partial**: Use o utilitário `Partial` em uma interface `Usuario` para criar uma variável que tenha apenas o nome.
2.  **Readonly**: Crie uma versão `Readonly` de um objeto `Carro` e tente alterar uma propriedade.

### 🟡 Nível: Intermediário
3.  **Pick e Omit**: A partir de uma interface `Funcionario`, use `Pick` para criar um tipo com apenas `nome` e `cargo`, e `Omit` para criar um tipo que não tenha o `salario`.
4.  **Record**: Use o `Record` para mapear códigos de erro (números) para mensagens de erro (strings).

### 🔴 Nível: Desafio
5.  **Mapeamento de API**: Crie um tipo que represente a resposta de uma "atualização de perfil", onde todos os campos do usuário original são opcionais, exceto o `id`, que deve ser obrigatório.