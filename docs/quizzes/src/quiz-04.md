# Quiz: Aula 04 – Interfaces e Modelagem de Domínio 🏗️

1. Qual a palavra-chave usada para definir um contrato de objeto?
   - [ ] type contract
   - [x] interface
   - [ ] declare
   - [ ] model
   > Explicação: No TS, `interface` é a forma padrão de definir a estrutura de objetos e contratos na POO.

2. Como você indica que uma propriedade é opcional?
   - [ ] Usando `nullable`
   - [ ] Usando `optional`
   - [x] Usando um ponto de interrogação (`?`) após o nome da propriedade.
   - [ ] Não existe propriedade opcional em interfaces.
   > Explicação: Propriedades marcadas com `?` podem ou não ser incluídas no objeto.

3. O que faz o modificador `readonly`?
   - [ ] Torna a propriedade invisível.
   - [x] Impede que o valor da propriedade seja alterado após a criação do objeto.
   - [ ] Torna a propriedade obrigatória.
   - [ ] Converte a propriedade para string.
   > Explicação: `readonly` garante imutabilidade para propriedades específicas de um objeto.

4. Como uma interface pode herdar propriedades de outra?
   - [ ] Usando `implements`
   - [x] Usando `extends`
   - [ ] Usando `inherits`
   - [ ] Usando `merge`
   > Explicação: `extends` permite compor interfaces, criando hierarquias de contratos.

5. Qual a diferença entre `interface` e `type` quanto ao "Declaration Merging"?
   - [ ] Nenhuma, ambos se fundem.
   - [x] Interfaces com o mesmo nome se fundem; tipos com mesmo nome geram erro.
   - [ ] Tipos se fundem; interfaces não.
   - [ ] O TS não permite nomes repetidos em nenhum caso.
   > Explicação: O merging automático de interfaces é útil para estender bibliotecas de terceiros.

6. Quando uma classe quer seguir as regras de uma interface, ela usa:
   - [ ] extends
   - [x] implements
   - [ ] follows
   - [ ] uses
   > Explicação: `implements` força a classe a fornecer implementações para todos os membros da interface.

7. Posso usar `interface` para definir o tipo de uma função?
   - [ ] Não, apenas `type` pode fazer isso.
   - [x] Sim, usando uma sintaxe de chamada de assinatura.
   - [ ] Apenas se a função estiver dentro de um objeto.
   - [ ] Sim, mas a função não pode ter parâmetros.
   > Explicação: Interfaces no TS são versáteis e podem descrever quase qualquer coisa, inclusive funções.

8. Qual a recomendação oficial do TS sobre o uso de Interface vs Type?
   - [ ] Use sempre Type.
   - [x] Prefira Interface para objetos e POO até que precise de lógicas específicas do Type.
   - [ ] A escolha é puramente estética.
   - [ ] Interfaces serão removidas em versões futuras.
   > Explicação: Interfaces tendem a ter um desempenho de compilação ligeiramente melhor e são o padrão para POO.

9. O que é "Modelagem de Domínio"?
   - [ ] Desenhar logos para o site.
   - [x] Representar as regras e entidades do negócio através de tipos e interfaces.
   - [ ] Comprar domínios de internet (.com, .com.br).
   - [ ] Criar modelos 3D para o projeto.
   > Explicação: Modelar o domínio significa traduzir as necessidades reais do negócio em código seguro.

10. Pode uma interface estender múltiplas outras interfaces ao mesmo tempo?
    - [ ] Não, herança múltipla não é permitida.
    - [x] Sim, basta separar as interfaces por vírgula no `extends`.
    - [ ] Sim, mas apenas se elas não tiverem propriedades repetidas.
    - [ ] Sim, mas apenas na versão corporativa do TS.
    > Explicação: O TS permite a composição flexível de múltiplos contratos em uma única interface.