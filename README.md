# Banco-de-dados
Este repositório tem como intuito o "depósito" de todos os bancos utilizados durante minhas aulas de Banco de Dados, bem como os comandos trabalhados dentro destes bancos e pequenas descrições de seus usos.

# Criando-o-primeiro-banco-de-dados

-- Criação do banco de dados
CREATE DATABASE Biblioteca;

-- Selecionar o banco de dados criado
USE Biblioteca;

-- Criação da tabela Livros
CREATE TABLE Livros (
    Id INT PRIMARY KEY AUTO_INCREMENT,
    Titulo VARCHAR(100) NOT NULL,
    Autor VARCHAR(100) NOT NULL,
    AnoPublicacao INT,
    ISBN VARCHAR(20),
    Quantidade INT DEFAULT 0
);

-- Inserir dados na tabela Livros
INSERT INTO Livros (Titulo, Autor, AnoPublicacao, ISBN, Quantidade)
VALUES
    ('Dom Casmurro', 'Machado de Assis', 1899, 'ABC123', 5),
    ('O Hobbit', 'J.R.R. Tolkien', 1937, 'DEF456', 3),
    ('1984', 'George Orwell', 1949, 'GHI789', 7);

-- Consulta para verificar os dados inseridos
SELECT * FROM Livros;
