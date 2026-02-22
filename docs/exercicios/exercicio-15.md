# Exercícios: Aula 15 – Clean Code e Arquitetura 📐

### 🟢 Nível: Básico
1.  **Nomes Semânticos**: Refatore uma função com nomes genéricos (ex: `a`, `b`, `fn1`) para nomes que expliquem sua função.
2.  **Função de Responsabilidade Única**: Quebre uma função que faz duas coisas (ex: valida e salva no banco) em duas funções separadas.

### 🟡 Nível: Intermediário
3.  **Inversão de Dependência**: Refatore uma classe que instancia diretamente um serviço para que ela receba o serviço no construtor.
4.  **Segregação de Interface**: Quebre uma interface "gorda" que tem 10 métodos em três interfaces menores e mais específicas.

### 🔴 Nível: Desafio
5.  **Domain Entities**: Crie uma Entidade de Domínio para um "Pedido" que contenha uma lógica interna para calcular o total sem depender de serviços externos.