# Quiz: Aula 14 – Padrões de Projeto com TypeScript 🛡️

1. O que são "Design Patterns" (Padrões de Projeto)?
   - [ ] Designs bonitos para o site.
   - [x] Soluções testadas e aprovadas para problemas comuns de design de software.
   - [ ] Atalhos de teclado no VS Code.
   - [ ] Comandos para formatar o código.
   > Explicação: Padrões ajudam a criar sistemas mais flexíveis e fáceis de manter.

2. Qual o objetivo do "Repository Pattern"?
   - [ ] Organizar as pastas do Windows.
   - [x] Isolar a lógica de acesso aos dados para que a aplicação não dependa de um banco de dados específico.
   - [ ] Salvar arquivos no GitHub.
   - [ ] Criar backups diários.
   > Explicação: Permite trocar o banco de dados (ex: SQL para Mongo) sem mexer na lógica de negócio.

3. O que faz o "Factory Pattern"?
   - [ ] Cria robôs.
   - [x] Centraliza a criação de objetos complexos em um único lugar (fábrica).
   - [ ] Deleta objetos antigos automaticamente.
   - [ ] Apenas gera listas aleatórias.
   > Explicação: Útil quando a criação de um objeto depende de muitos parâmetros ou lógicas de decisão.

4. O "Strategy Pattern" é usado para quê?
   - [ ] Planejar o projeto no calendário.
   - [x] Definir uma família de algoritmos intercambiáveis (diferentes formas de fazer a mesma coisa).
   - [ ] Atacar hackers.
   - [ ] Diminuir o custo do servidor.
   > Explicação: Exemplo: Diferentes formas de cálculo de imposto ou frete selecionáveis em tempo de execução.

5. O que é "Injeção de Dependência" (DI)?
   - [ ] Instalar vírus no computador.
   - [x] Fornecer as dependências de uma classe por fora (geralmente via construtor) em vez de criá-las internamente.
   - [ ] Mudar a versão do Node.js.
   - [ ] Injetar código no navegador.
   > Explicação: Isso torna as classes menos "presas" umas às outras, facilitando testes e manutenção.

6. Por que o TypeScript é ótimo para Design Patterns?
   - [ ] Porque ele é mais rápido.
   - [x] O uso de Interfaces permite definir contratos claros para os padrões funcionarem com segurança.
   - [ ] Ele tem ícones melhores para classes.
   - [ ] Padrões de projeto só funcionam no TypeScript.
   > Explicação: Padrões de design dependem fortemente de interfaces e polimorfismo, que o TS domina.

7. O que é o padrão "Singleton"?
   - [ ] Uma classe que só pode ter uma única instância em todo o ciclo de vida do programa.
   - [ ] Uma classe sem métodos.
   - [ ] Um arquivo com uma única linha.
   - [ ] Um comando que roda uma vez.
   > Explicação: Comumente usado para conexões de banco de dados ou gerenciamento de estado global.

8. Qual a diferença entre Service Layer e Repository?
   - [ ] Nenhuma, são o mesmo.
   - [x] O Service contém a lógica de negócio; o Repository cuida apenas de buscar/salvar dados.
   - [ ] O Repository é para frontend; o Service é para backend.
   - [ ] O Service é opcional, o Repository é obrigatório.
   > Explicação: Separar "como eu busco" de "o que eu faço com o que busquei" é crucial para Clean Code.

9. Qual o risco de não usar padrões de projeto em sistemas grandes?
   - [ ] O sistema para de funcionar.
   - [x] O código se torna um "Big Ball of Mud" (grande bola de lama), impossível de entender e modificar sem quebrar outras partes.
   - [ ] O servidor fica mais caro.
   - [ ] Nenhum risco real.
   > Explicação: Padrões dão estrutura e previsibilidade ao crescimento do software.

10. Pode-se combinar múltiplos padrões no mesmo projeto?
    - [ ] Não, eles entram em conflito.
    - [x] Sim, projetos reais costumam usar dezenas de padrões de forma complementar.
    - [ ] Sim, mas apenas no Java.
    - [ ] Sim, mas apenas dois por arquivo.
    > Explicação: Padrões como Service, Repository e Factory são frequentemente usados juntos em arquiteturas modernas.