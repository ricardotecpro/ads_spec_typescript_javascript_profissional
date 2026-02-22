# Quiz: Aula 06 – Generics (Programação Genérica) 📦

1. Para que servem os Generics no TypeScript?
   - [ ] Gerar números aleatórios.
   - [x] Criar componentes reutilizáveis que trabalham com diversos tipos mantendo a segurança.
   - [ ] Remover a necessidade de declarar variáveis.
   - [ ] Compilar o código mais rápido.
   > Explicação: Generics permitem que o "contrato" de tipo seja definido no momento do uso, e não na criação.

2. Qual caractere é comumente usado para representar um tipo genérico?
   - [ ] $
   - [ ] @
   - [x] < T >
   - [ ] { P }
   > Explicação: Embora qualquer nome possa ser usado, `<T>` (de Type) é a convenção universal.

3. Qual a principal vantagem de Generics sobre o uso de `any`?
   - [ ] Generics são mais fáceis de digitar.
   - [x] Generics preservam a informação do tipo original, evitando erros de runtime.
   - [ ] `any` é mais rápido que Generics.
   - [ ] Não há diferença real.
   > Explicação: Com `any`, perdemos o autocompletar e a segurança; com Generics, o TS "lembra" do tipo que foi passado.

4. O que é uma "Generic Constraint" (Restrição)?
   - [ ] Uma regra que impede o uso de Generics.
   - [x] O uso de `extends` para limitar quais tipos podem ser passados ao componente genérico.
   - [ ] Um erro que acontece quando o código é muito grande.
   - [ ] Uma forma de ocultar tipos complexos.
   > Explicação: Constraints permitem garantir que o tipo passado possua certas propriedades (como `.length` ou `.id`).

5. Posso usar Generics em interfaces?
   - [ ] Não, apenas em funções e classes.
   - [x] Sim, é muito comum para definir respostas de APIs ou estruturas de dados.
   - [ ] Sim, mas apenas com o tipo string.
   - [ ] Sim, mas apenas se a interface for vazia.
   > Explicação: Interfaces genéricas como `Response<T>` facilitam a modelagem de dados consistentes.

6. O que significa `<T extends string>`?
   - [ ] Que T deve herdar de uma classe chamada string.
   - [x] Que o tipo genérico T deve ser obrigatoriamente compatível com uma string.
   - [ ] Que string passa a ser um tipo genérico.
   - [ ] Nada, a sintaxe está errada.
   > Explicação: Restringe o Generic a aceitar apenas strings ou tipos que se comportem como strings.

7. Qual o resultado de `retornarItem<number>(10)` se a função for genérica?
   - [ ] "10" (string)
   - [x] 10 (number)
   - [ ] any
   - [ ] Um erro de compilação.
   > Explicação: A função retorna exatamente o valor mantendo o tipo especificado ou inferido.

8. Onde a "Programação Genérica" é mais utilizada?
   - [ ] Apenas em calculadoras.
   - [x] Em coleções (Arrays, Sets), Repositórios de dados e Wrappers de API.
   - [ ] Em arquivos de configuração apenas.
   - [ ] Nunca deve ser usada em projetos reais.
   > Explicação: Ferramentas de banco de dados e frameworks front/back dependem fortemente de Generics.

9. O TypeScript pode inferir o tipo genérico sozinho?
   - [ ] Não, é sempre obrigatório escrever `<Tipo>`.
   - [x] Sim, a partir do valor passado como argumento para a função ou construtor.
   - [ ] Sim, mas apenas para o tipo boolean.
   - [ ] Sim, mas apenas no modo estrito.
   > Explicação: A inferência de argumentos de tipo torna o uso de Generics menos "verboso".

10. Generics aumentam o tamanho do código JavaScript final?
    - [ ] Sim, muito.
    - [x] Não, eles são removidos completamente durante a compilação.
    - [ ] Sim, mas apenas se usarmos classes.
    - [ ] Apenas se usarmos constraints.
    > Explicação: Assim como a maioria das funcionalidades do TS, Generics são ferramentas de "tempo de design/compilação".