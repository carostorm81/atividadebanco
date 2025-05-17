# atividadebanco
# 📚 Sistema de Biblioteca

Este projeto foi desenvolvido como parte da **1ª Avaliação** da disciplina de Programação com JPA, com o objetivo de implementar um sistema de biblioteca com as entidades **Aluno**, **Publicacao** e **Emprestimo**, utilizando **Java + JPA + Maven**.

---

## 🛠️ Tecnologias utilizadas

- Java 17
- Maven
- JPA (Hibernate)
- H2 Database (banco em memória para testes)
- JUnit 5

---

## 🧱 Estrutura do Projeto

- `src/main/java/com/biblioteca/model/` → Entidades JPA
- `src/main/java/com/biblioteca/dao/` → Classe DAO de Emprestimo
- `src/test/java/com/biblioteca/test/` → Testes com JUnit
- `src/main/resources/META-INF/persistence.xml` → Configuração do JPA
- `pom.xml` → Configuração de dependências Maven

---

## 📄 Entidades implementadas

### 🧑‍🎓 Aluno
- `matriculaAluno` (PK)
- `nome`

### 📘 Publicacao
- `codigoPub` (PK)
- `titulo`
- `ano`
- `autor`
- `tipo`

### 📅 Emprestimo
- `id` (PK)
- `dataEmprestimo`
- `dataDevolucao`
- `aluno` (ManyToOne)
- `publicacao` (ManyToOne)

---

## ✅ Funcionalidades

- Persistência com JPA
- CRUD completo para Emprestimos
- Testes automatizados com JUnit
- Relacionamentos entre entidades mapeados corretamente

---

## 🚀 Como executar

1. Importe o projeto no Eclipse como **Maven Project**
2. Certifique-se de que o JDK 17 está configurado
3. Rode os testes localizados em:
   - `src/test/java/com/biblioteca/test/EmprestimoDAOTest.java`

---

## 👥 Integrantes

- Nome: [ronald de jesus rodrigues]
- Matrícula: [20200795034]

---

## 📌 Observações

- As entidades seguem o modelo conceitual fornecido pela avaliação.
- O banco H2 é utilizado apenas para testes (não é necessário instalar).
- As dependências estão gerenciadas no `pom.xml`.

---

## 📂 Organização do Código

```bash
SistemaBibliotecaMaven/
├── pom.xml
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/biblioteca/
│   │   │       ├── dao/
│   │   │       └── model/
│   │   └── resources/
│   │       └── META-INF/
│   │           └── persistence.xml
│   └── test/
│       └── java/
│           └── com/biblioteca/test/
│               └── EmprestimoDAOTest.java
