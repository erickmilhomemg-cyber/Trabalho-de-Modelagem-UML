# Trabalho-de-Modelagem-UML
Sistema de modelagem UML turma 204 informática IEMA IP balsas, Alunos: Erick Milhomem, João Gabriel soares, Samuel Alves Amorim, Thiago da Silva

README — Sistema de Biblioteca

Sobre o projeto

Este projeto apresenta a modelagem de um Sistema de Gerenciamento de Biblioteca, desenvolvido com base nos conceitos de Programação Orientada a Objetos (POO) e UML.

O sistema foi pensado para organizar as principais atividades de uma biblioteca, como cadastro de usuários, controle de livros e exemplares, realização de empréstimos, devoluções e gerenciamento de multas.

Objetivo

O principal objetivo do sistema é facilitar o controle das informações e operações realizadas em uma biblioteca.

Entre as principais funções estão:

* Cadastro de usuários e funcionários;
* Cadastro de livros e autores;
* Controle dos exemplares disponíveis;
* Registro de empréstimos e devoluções;
* Consulta de empréstimos;
* Renovação de empréstimos;
* Controle e pagamento de multas.

Classes do sistema

O sistema é composto por oito classes principais.

Pessoa

É uma classe abstrata que reúne informações comuns entre usuários e funcionários.

Atributos:

* id
* nome
* cpf
* email
* telefone

Métodos:

* getNome()
* exibirDados()

Usuário

Representa a pessoa que utiliza os serviços da biblioteca e realiza empréstimos.

Atributos:

* matricula
* dataCadastro
* status

Métodos:

* podeEmprestar()
* consultarEmprestimos()

Funcionário

Representa o funcionário responsável por registrar empréstimos e devoluções.

Atributos:

* cargo
* dataAdmissao

Métodos:

* registrarEmprestimo()
* registrarDevolucao()

Livro

Representa uma obra cadastrada no acervo da biblioteca.

Atributos:

* isbn
* titulo
* editora
* anoPublicacao

Métodos:

* adicionarAutor()
* getExemplaresDisponiveis()

Autor

Representa o autor responsável pela obra.

Atributos:

* id
* nome
* nacionalidade

Método:

* getNome()

Exemplar

Representa uma cópia física de um determinado livro.

Atributos:

* codigo
* estadoConservacao
* disponivel

Métodos:

* emprestar()
* devolver()

Empréstimo

Representa o processo de empréstimo de um exemplar para um usuário.

Atributos:

* id
* dataEmprestimo
* dataPrevistaDevolucao
* dataDevolucao
* status

Métodos:

* renovar()
* finalizar()
* calcularDiasAtraso()

Multa

Representa uma multa gerada quando um empréstimo é devolvido com atraso.

Atributos:

* id
* valor
* dataGeracao
* paga

Métodos:

* calcularValor()
* pagar()

Relacionamentos entre as classes

* Usuário e Funcionário herdam as características da classe Pessoa.
* Um Usuário pode realizar vários Empréstimos.
* Um Funcionário pode registrar vários Empréstimos.
* Um Livro pode possuir um ou mais Autores.
* Um Livro pode possuir vários Exemplares.
* Um Empréstimo está relacionado a um Exemplar.
* Um Empréstimo pode gerar uma Multa quando ocorre atraso.

Conceitos utilizados

Durante a modelagem foram utilizados conceitos importantes da Programação Orientada a Objetos, como:

* Classes e objetos;
* Abstração;
* Herança;
* Encapsulamento;
* Associação;
* Composição;
* Multiplicidade.

Diagrama de classes

O diagrama representa visualmente a estrutura do sistema e mostra como as classes estão relacionadas entre si. A classe Pessoa serve como base para Usuário e Funcionário, enquanto Livro, Autor, Exemplar, Empréstimo e Multa representam as principais entidades envolvidas no funcionamento da biblioteca.

Integrantes

Projeto: Sistema de Gerenciamento de Biblioteca

Disciplina: Programação Orientada a Objetos / Análise de Sistemas

Finalidade

Este projeto foi desenvolvido para fins acadêmicos, com o objetivo de aplicar na prática os conceitos de modelagem de sistemas e Programação Orientada a Objetos.
