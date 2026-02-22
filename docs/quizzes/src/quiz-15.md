# Quiz: Aula 15 – Clean Code e Arquitetura 📐

1. O que significa "Clean Code" (Código Limpo)?
   - [ ] Código sem comentários.
   - [x] Código escrito de forma que seja fácil de ler, entender e manter por outros desenvolvedores.
   - [ ] Código que usa muitos emojis.
   - [ ] Código que ocupa pouco espaço no disco.
   > Explicação: Um código limpo é aquele que parece ter sido escrito por alguém que se importa com quem vai ler depois.

2. No acrônimo SOLID, o que significa a letra **S**?
   - [ ] Simple Code.
   - [x] Single Responsibility Principle (Princípio da Responsabilidade Única).
   - [ ] Syntax Check.
   - [ ] Super Classes.
   > Explicação: Uma classe ou função deve ter apenas uma razão para mudar (fazer apenas uma coisa).

3. O Princípio Aberto/Fechado (Open/Closed) diz que:
   - [ ] O código deve ser aberto para o público.
   - [x] O código deve ser aberto para extensão, mas fechado para modificação direta.
   - [ ] Todas as funções devem estar fechadas em arquivos.
   - [ ] O projeto deve ser open source.
   > Explicação: Devemos ser capazes de adicionar novos comportamentos sem alterar o código que já funciona.

4. O que defende a "Segregação de Interfaces"?
   - [ ] Que não devemos usar interfaces.
   - [x] Que é melhor ter várias interfaces específicas do que uma única interface "gorda" e genérica.
   - [ ] Que as interfaces devem ficar em pastas separadas.
   - [ ] Que as interfaces devem ser privadas.
   > Explicação: Evita que as classes sejam obrigadas a implementar métodos de que não precisam.

5. O que é a Inversão de Dependência (D do SOLID)?
   - [ ] Mudar a ordem dos imports.
   - [x] Depender de abstrações (interfaces/classes abstratas) em vez de implementações concretas.
   - [ ] Deletar todas as dependências do projeto.
   - [ ] Inverter o nome das classes.
   > Explicação: Isso desconecta as camadas da aplicação, permitindo trocas fáceis de tecnologia.

6. Sobre nomenclatura: qual o melhor nome para uma variável que guarda a lista de usuários ativos?
   - [ ] `l`
   - [ ] `users`
   - [x] `activeUsers` ou `activeUserList`
   - [ ] `data123`
   > Explicação: Nomes devem ser pronunciáveis e expressar intenção clara sem necessidade de comentários.

7. Qual a regra de ouro para o tamanho das funções em Clean Code?
   - [ ] Funções devem ter pelo menos 100 linhas para serem úteis.
   - [x] Funções devem ser pequenas e fazer apenas uma coisa.
   - [ ] Funções devem ter o máximo de parâmetros possível.
   - [ ] Não existe regra para tamanho de funções.
   > Explicação: Funções pequenas são mais fáceis de testar, ler e reutilizar.

8. O que é o "Domain" (Domínio) em uma arquitetura de software?
   - [ ] O endereço do site (ex: google.com).
   - [x] Onde vivem as regras de negócio puras, independentes de banco de dados ou frameworks.
   - [ ] A pasta de imagens.
   - [ ] O servidor principal.
   > Explicação: O coração do software; deve ser a parte mais protegida e testada.

9. Por que evitar comentários óbvios no código?
   - [ ] Porque economiza digitação.
   - [x] Porque o código deve ser autoexplicativo; comentários óbvios tornam-se ruído e ficam desatualizados.
   - [ ] Porque comentários aumentam o tamanho do site.
   - [ ] Porque o computador não lê comentários.
   > Explicação: Comente o "porquê" de decisões estranhas/complexas, não o "o quê" o código faz.

10. O que significa "Boy Scout Rule" (Regra do Escoteiro) no desenvolvimento?
    - [ ] Usar uniforme para programar.
    - [x] Sempre deixar o código um pouco mais limpo do que você o encontrou.
    - [ ] Criar fogueiras no escritório.
    - [ ] Ajudar o time apenas uma vez por dia.
    > Explicação: A manutenção contínua e pequenas melhorias evitam que o projeto vire um legado impossível de manter.