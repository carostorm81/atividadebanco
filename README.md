## Desenvolvimento de um Sistema de Biblioteca com H2 Database e JPA

Inicialmente, um banco de dados para um sistema de biblioteca foi modelado e criado utilizando o H2 Database. Este banco de dados compreende as tabelas `ALUNO`, `EMPRESTIMO` e `PUBLICACAO`. Posteriormente, foram definidas as relações entre essas tabelas através da implementação de chaves estrangeiras, garantindo a integridade referencial dos dados.

O mapeamento dessas tabelas para entidades Java foi realizado de forma automatizada através do gerador de entidades de persistência integrado ao NetBeans, utilizando a conexão com o driver do H2 Database e especificando o caminho do arquivo do banco de dados local. Essa ferramenta facilita a criação das classes de entidade, estabelecendo a correspondência entre as tabelas do banco de dados e os atributos das classes Java.

## A Classe DAO Genérica

Para padronizar o acesso aos dados, foi implementada uma classe `DAO` genérica. Essa classe tem como responsabilidade a gestão de qualquer entidade persistente do sistema, utilizando as funcionalidades fornecidas pelas classes do pacote `javax.persistence`. Além disso, a `DAO` base implementa os métodos fundamentais de CRUD (`findAll`, `insert`, `update` e `delete`), oferecendo uma interface comum para a manipulação dos dados no banco.

## A Classe EmpréstimoDAO Específica

A classe `EmpréstimoDAO` estende a classe `DAO`, especializando as operações de acesso aos dados da entidade `Empréstimo`. Os métodos CRUD herdados são sobrescritos para, possivelmente, adicionar lógica específica a essa entidade. Destaca-se o uso da API Criteria para a construção de consultas dinâmicas e flexíveis ao banco de dados, bem como a utilização da classe `Transaction` para controlar as operações de inserção, atualização e exclusão de registros, garantindo a atomicidade das transações.

## Problema na Execução dos Testes da EmpréstimoDAO

A classe `AtivDAO` foi designada como a classe principal do projeto, com o objetivo de executar os testes da classe `EmpréstimoDAO`. No entanto, um erro crítico impede a execução desses testes: o compilador não está conseguindo localizar o método `main` dentro da classe `AtivDAO`. A ausência desse método essencial impede que a aplicação seja iniciada e, consequentemente, que os testes sejam realizados.

## Discentes:
Elton Carlos Viana Pantoja
