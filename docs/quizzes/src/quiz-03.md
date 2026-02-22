# Quiz: Aula 03 – Tipos Avançados 🧩

1. O que representa o operador `|` no TypeScript?
   - [ ] Interseção de tipos.
   - [x] União de tipos (ou um, ou outro).
   - [ ] Divisão de tipos.
   - [ ] Comparação de igualdade.
   > Explicação: O Union Type permite que uma variável aceite múltiplos tipos diferentes.

2. O que é um "Type Alias"?
   - [ ] Um novo tipo de dado primitivo.
   - [x] Um nome personalizado para um tipo ou combinação de tipos.
   - [ ] Uma forma de ocultar dados privados.
   - [ ] Um atalho para o comando `tsc`.
   > Explicação: `type` permite criar apelidos para tipos, facilitando a reutilização e legibilidade.

3. Qual a função do operador `&` (Intersection)?
   - [ ] Escolher entre dois tipos.
   - [x] Combinar dois ou mais tipos em um único tipo que possua todas as propriedades.
   - [ ] Comparar caminhos de arquivos.
   - [ ] Atribuir um valor nulo.
   > Explicação: Interseções são muito comuns para compor objetos complexos a partir de tipos menores.

4. O que são "Literal Types"?
   - [ ] Tipos que só aceitam literatura clássica.
   - [x] Tipos que restringem uma variável a valores exatos e específicos.
   - [ ] O mesmo que o tipo `any`.
   - [ ] Variáveis que não podem ser alteradas.
   > Explicação: Você pode definir que uma string só aceite "ativo" ou "inativo", por exemplo.

5. "Narrowing" (Estreitamento) serve para quê?
    - [ ] Diminuir o tamanho do código compilado.
    - [x] Identificar o tipo exato de uma variável dentro de um bloco de código lógico.
    - [ ] Remover espaços em branco do código.
    - [ ] Limitar o número de variáveis no projeto.
    > Explicação: O narrowing permite usar métodos específicos de um tipo após verificar qual ele é.

6. Qual destes é um exemplo de "Type Guard" nativo do JavaScript?
   - [ ] `if (x == y)`
   - [x] `typeof x === "string"`
   - [ ] `x.map()`
   - [ ] `console.log(x)`
   > Explicação: Operadores como `typeof`, `instanceof` e `in` são usados pelo TS para estreitar tipos.

7. O que acontece se você tentar acessar um método de string em uma união `string | number` fora de um Type Guard?
   - [ ] O TS executa o método se for string, se não, ignora.
   - [x] O TS gera um erro informando que o método não existe no tipo `number`.
   - [ ] O código compila normalmente.
   - [ ] O programa trava.
   > Explicação: O TS só permite acessar propriedades que existam em AMBOS os tipos da união, a menos que você faça o narrowing.

8. Qual o benefício de usar uniões de literais em vez de Enums simples em alguns casos?
   - [ ] Elas ocupam mais espaço.
   - [x] São mais leves, pois desaparecem completamente no JavaScript compilado.
   - [ ] Permitem valores numéricos apenas.
   - [ ] São mais fáceis de depurar no console.
   > Explicação: Uniões de literais são apenas tipos do TS, enquanto Enums geram código JS real.

9. Como você criaria um tipo que aceita um objeto com `nome` ou um objeto com `id`?
   - [ ] Usando Interseção (`&`).
   - [x] Usando União (`|`).
   - [ ] Usando `any`.
   - [ ] Não é possível.
   > Explicação: A união permite flexibilidade entre diferentes estruturas de objeto.

10. No estudo de caso de APIs, por que tipos avançados são importantes?
    - [ ] Para economizar largura de banda.
    - [x] Para garantir que lidamos corretamente com todas as variações de resposta (sucesso, erro, vazio).
    - [ ] Para enviar dados mais rápido.
    - [ ] Para mudar o tema do VS Code.
    > Explicação: APIs são dinâmicas; tipos avançados como Union e Nullable ajudam a tratar todas as possibilidades de retorno.