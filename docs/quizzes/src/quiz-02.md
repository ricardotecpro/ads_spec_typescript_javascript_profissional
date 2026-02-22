# Quiz: Aula 02 – Tipos Fundamentais e Inferência 🛠️

1. Qual destes NÃO é um tipo primitivo no TypeScript?
   - [ ] string
   - [ ] boolean
   - [x] tuple
   - [ ] number
   > Explicação: Tipos primitivos são os básicos herdados do JS. Tupla é uma estrutura de dados de array com tipos fixos.

2. Como o TypeScript infere o tipo de `let x = 10;`?
   - [ ] Como `any`.
   - [x] Como `number`.
   - [ ] Como `string`.
   - [ ] Ele não infere, gera erro.
   > Explicação: O TS observa o valor inicial atribuído à variável para determinar seu tipo automaticamente.

3. O que define uma Tupla no TypeScript?
   - [ ] Um array que aceita qualquer tipo.
   - [x] Um array com número fixo de elementos e tipos conhecidos em posições específicas.
   - [ ] Um objeto com chaves numéricas.
   - [ ] Uma lista encadeada.
   > Explicação: Diferente de um array comum, na tupla a ordem e o tipo de cada elemento importam.

4. Por que usar `enum` em vez de simples constantes de string?
   - [ ] Porque ocupa menos memória.
   - [x] Para melhorar a legibilidade e evitar erros de digitação em valores fixos.
   - [ ] Porque é obrigatório em todas as classes.
   - [ ] Para permitir que o usuário mude o tipo da variável.
   > Explicação: Enums criam um conjunto de nomes amigáveis para valores constantes, facilitando a manutenção.

5. Qual a principal diferença entre `any` e `unknown`?
   - [ ] Nenhuma, ambos são iguais.
   - [ ] `any` é mais seguro que `unknown`.
   - [x] `unknown` obriga você a verificar o tipo antes de realizar operações, enquanto `any` permite tudo.
   - [ ] `any` só aceita números e `unknown` só aceita strings.
   > Explicação: `unknown` é a "versão segura" do `any`, forçando o desenvolvedor a usar Type Guards.

6. Quando uma função deve ter o tipo de retorno `void`?
   - [ ] Quando ela retorna uma string vazia.
   - [x] Quando ela não retorna nenhum valor deliberadamente.
   - [ ] Quando ela nunca termina sua execução.
   - [ ] Quando ela retorna `null`.
   > Explicação: `void` indica a ausência de retorno em uma função.

7. O tipo `never` é usado para quê?
   - [ ] Variáveis que podem ser nulas.
   - [x] Funções que nunca retornam (lançam exceção ou loop infinito).
   - [ ] Funções que retornam um booleano falso.
   - [ ] Variáveis que ainda não foram inicializadas.
   > Explicação: `never` representa um estado que tecnicamente não deveria ocorrer ou que nunca chega ao fim.

8. Como declarar explicitamente um array de strings?
   - [ ] `let nomes: string`
   - [x] `let nomes: string[]` ou `let nomes: Array<string>`
   - [ ] `let nomes: [string]`
   - [ ] `let nomes: list(string)`
   > Explicação: As duas sintaxes são válidas e representam uma lista de elementos do mesmo tipo.

9. O que acontece se você tentar atribuir um número a uma variável inferida como string?
   - [ ] O TS converte o número para string automaticamente.
   - [ ] O código roda, mas dá erro no navegador.
   - [x] O compilador gera um erro de tipo imediatamente.
   - [ ] Nada acontece.
   > Explicação: O sistema de tipos estáticos impede atribuições incompatíveis para garantir a consistência dos dados.

10. Qual a vantagem de usar Tipagem Explícita?
    - [ ] Deixar o código mais curto.
    - [x] Documentar a intenção do código e evitar ambiguidades em lógica complexa.
    - [ ] Fazer o código compilar mais rápido.
    - [ ] Permitir o uso de variáveis sem valor inicial.
    > Explicação: Embora a inferência seja útil, a tipagem explícita em contratos (como funções e objetos) melhora a manutenção do projeto.