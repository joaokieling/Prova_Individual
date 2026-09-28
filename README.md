Sistema de Academia

O que é este projeto?

O Sistema de Academia é um projeto feito em PHP que representa o funcionamento básico de uma academia. Ele foi desenvolvido para colocar em prática os conceitos de Programação Orientada a Objetos, sem uso de frameworks ou banco de dados.

Qual problema ele procura representar?

O sistema representa situações comuns de uma academia, como alunos fazendo matrícula, escolhendo planos, realizando pagamentos e tendo treinos com diferentes exercícios.

A ideia é organizar essas informações através de classes e objetos, deixando cada parte do sistema responsável por uma função específica.

Como ele foi desenvolvido?

O projeto foi desenvolvido em PHP utilizando classes para representar as partes principais de uma academia.

Cada classe possui suas próprias informações e métodos. O arquivo index.php é usado para criar os objetos e demonstrar como eles funcionam juntos.

A estrutura funciona basicamente assim:

Pessoa -> informações básicas de uma pessoa
Aluno -> representa um aluno (herda de Pessoa)
Professor -> representa um professor (herda de Pessoa)
Plano -> representa um plano da academia
Matricula -> relaciona um aluno com um plano
Treino -> representa um treino
Exercicio -> representa os exercícios de um treino
Pagamento -> representa um pagamento

Principais funcionalidades

- Criar e exibir alunos
- Criar professores
- Criar planos
- Fazer matrículas
- Alterar o plano de uma matrícula
- Cancelar uma matrícula
- Criar treinos
- Adicionar exercícios aos treinos
- Registrar e realizar pagamentos

Tecnologias utilizadas

- PHP -> linguagem utilizada para desenvolver o sistema
- Git -> utilizado para controlar as versões do projeto
- GitHub -> utilizado para armazenar e compartilhar o projeto

Conceitos de Programação Orientada a Objetos

- Classes e objetos -> cada parte importante da academia é representada por uma classe e seus objetos
- Encapsulamento -> os dados das classes são protegidos e acessados através de métodos
- Herança -> Aluno e Professor utilizam características que vêm da classe Pessoa
- Construtores -> utilizados para criar os objetos já com suas informações
- Métodos -> representam ações que os objetos podem realizar, como realizar um pagamento ou cancelar uma matrícula
- Relacionamento entre objetos -> diferentes classes trabalham juntas. Por exemplo, uma Matricula possui um Aluno e um Plano, enquanto um Treino possui um Professor e vários Exercicios
- Polimorfismo -> os métodos exibirDados() e apresentar() são sobrescritos nas subclasses

Estrutura do projeto

- Pessoa.php -> informações básicas de uma pessoa
- Aluno.php -> representa um aluno
- Professor.php -> representa um professor
- Plano.php -> representa um plano
- Matricula.php -> representa uma matrícula
- Exercicio.php -> representa um exercício
- Treino.php -> representa um treino
- Pagamento.php -> representa um pagamento
- index.php -> executa e demonstra o funcionamento do sistema

Dicionário de classes

Pessoa
Classe base com os atributos nome, cpf e email. Possui os getters e os métodos exibirDados() e apresentar().

Aluno (herda de Pessoa)
Adiciona os atributos matricula e ativo. Possui o método desativar() e sobrescreve exibirDados().

Professor (herda de Pessoa)
Adiciona os atributos especialidade e cref. Sobrescreve exibirDados() e apresentar().

Plano
Possui nome, valorMensal e duracaoMeses. Tem o método calcularValorTotal(), que multiplica o valor mensal pela duração.

Matricula
Possui numero, aluno, plano, dataMatricula e ativa. Tem os métodos alterarPlano() e cancelar(). Ao cancelar, também desativa o aluno.

Exercicio
Possui nome, series e repeticoes. Tem o método exibirDados().

Treino
Possui nome, professor e um array de exercicios. Tem os métodos adicionarExercicio() e exibirTreino().

Pagamento
Possui codigo, matricula, valor, data e pago. Tem os métodos realizarPagamento(), isPago() e exibirDados().

Relacionamentos entre as classes

- Aluno e Professor herdam de Pessoa
- Matricula possui um Aluno e um Plano
- Treino possui um Professor e vários Exercicios
- Pagamento possui uma Matricula

Como executar o projeto

1. Tenha o PHP 8 ou superior instalado.
2. No terminal, dentro da pasta do projeto, execute:

   php -S localhost:8000

3. Acesse no navegador:

   http://localhost:8000/index.php

Autor

João Vitor Trevisan Kieling
Projeto Evolutivo Individual - Programação Orientada a Objetos