# Quiz: Aula 13 – Testes com TypeScript 🧪

1. Qual o framework de testes mais popular no ecossistema JS/TS?
   - [ ] Mocha
   - [ ] Jasmine
   - [x] Jest
   - [ ] PyTest
   > Explicação: Jest é o padrão da indústria devido à sua facilidade de configuração e funcionalidades integradas.

2. Por que precisamos do `ts-jest`?
   - [ ] Para rodar testes mais rápido.
   - [x] Para permitir que o Jest entenda e compile arquivos TypeScript durante os testes.
   - [ ] Para desenhar diagramas de teste.
   - [ ] Para instalar o TypeScript.
   > Explicação: O Jest nativamente só entende JS; o `ts-jest` faz a ponte para o TS.

3. O que define um "Teste Unitário"?
   - [ ] Testar se o banco de dados está ligado.
   - [x] Testar uma pequena parte isolada do código (função ou classe) sem dependências externas reais.
   - [ ] Testar a interface gráfica (UI) apenas.
   - [ ] Testar a conexão de rede.
   > Explicação: O foco é a lógica interna daquela "unidade" específica.

4. O que faz o bloco `describe` no Jest?
   - [ ] Executa uma função.
   - [x] Agrupa um conjunto de testes relacionados (uma suíte de testes).
   - [ ] Deleta os testes antigos.
   - [ ] Descreve o projeto para o usuário final.
   > Explicação: Organiza os testes por categoria ou funcionalidade.

5. Qual a função do método `expect()`?
   - [ ] Espera a internet carregar.
   - [x] Define o valor que estamos testando para compará-lo com um resultado esperado.
   - [ ] Faz a função rodar de novo.
   - [ ] Cria uma nova variável.
   > Explicação: É onde as asserções (verificações) do teste começam.

6. O que é um "Mock" em testes?
   - [ ] Uma piada sobre o código.
   - [x] Um objeto simulado que substitui uma dependência real (como uma API ou banco) para controlar o comportamento no teste.
   - [ ] Um erro de compilação.
   - [ ] Uma versão oficial do código.
   > Explicação: Mocks permitem testar a lógica sem precisar de infraestrutura real e lenta.

7. No TypeScript, por que usamos `jest.Mocked<typeof modulo>`?
   - [ ] Para deletar o módulo.
   - [x] Para que o TypeScript saiba que aquele módulo foi mockado e permita acessar métodos de simulação (como `.mockResolvedValue`).
   - [ ] Para tornar o módulo privado.
   - [ ] Para converter o módulo em string.
   > Explicação: Garante que o TS não reclame quando tentarmos usar funções de mock em variáveis tipadas.

8. O que é "Cobertura de Testes" (Coverage)?
   - [ ] O número de arquivos do projeto.
   - [x] A porcentagem do código que é executada durante os testes.
   - [ ] O tamanho total do projeto em MB.
   - [ ] O número de desenvolvedores no time.
   > Explicação: Ajuda a identificar partes do código que ainda não foram verificadas pelos testes.

9. Diferença entre `it` e `test` no Jest:
   - [ ] `it` é para backend e `test` para frontend.
   - [x] Nenhuma, são sinônimos gramaticais apenas.
   - [ ] `test` é mais rápido que `it`.
   - [ ] `it` foi removido na versão 20.
   > Explicação: Você pode usar qualquer um conforme sua preferência de leitura (Ex: "it should...", "test that...").

10. Qual a vantagem de usar TDD (Test Driven Development)?
    - [ ] Fazer o código mais rápido na primeira vez.
    - [x] Garantir que o código atenda aos requisitos desde o início e facilitar refatorações seguras no futuro.
    - [ ] Eliminar a necessidade de documentação.
    - [ ] Diminuir o salário do QA.
    > Explicação: Escrever testes antes do código obriga o desenvolvedor a pensar no design e nos contratos da aplicação.