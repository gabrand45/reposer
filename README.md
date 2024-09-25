# reposer


## Exercício 1
```sql
-- criando a primeira tabela de clientes
create table clientes (
idCliente int primary key auto_increment,
nomeCliente varchar(100), 
emailCliente varchar(150),
dataNascimento date,
telefoneCliente varchar(14)
);
-- atributos adicionados
```


## Exercício 2
```sql
-- criando tabela de produtos do exercício 2
create table produtos (
idProdutos int primary key,
nomeProduto varchar(100) not null unique,
precoProduto decimal(8,2)
);
```


## Exercício 3
```sql
-- Criando tabela de fatura e utilizando Timestamp
create table faturas (
idFatura int primary key,
dataCriacao timestamp default current_timestamp,
valorFatura decimal(10,2)
);
-- timestamp é data com minutos
```

## Exercício 4
```sql
create database cai;
use cai;

-- criando tabela funcionarios
create table funcionarios (
ID int primary key, 
nome varchar(50), 
sobrenome varchar(50), 
salário double
);
-- adicionando dataNascimento na tabela funcionarios
alter table funcionarios add dataNascimento date;
-- criando tabela departamento
create table departamento (
id int primary key,
nome varchar(50)
);
-- adicionando IDDepartamento na tabela funcionarios
alter table funcionarios add IDDepartamento int;
-- criando tabela projetos
create table projetos (
id int primary key,
NomeProjeto varchar(150)
);
-- renomenado coluna sobrenome para apelido na tabela funcionarios
alter table funcionarios rename column sobrenome to apelido;
-- criando tabla cliente
create table cliente (
id int primary key,
nomeCliente varchar(50)
);
-- adicionando idCliente a tabela projetos
alter table projetos add idCliente int;
-- criando tabela endereços
create table endereços (
rua varchar(50),
cidade varchar(100),
cep int(8)
);
-- adicionando id a tabela endereços
alter table endereços add id int primary key;
-- adicionando idEndereço na tabela funcionarios
alter table funcionarios add idEndereço int(50);
-- renomenado a coluna nomeCliente para nomeEmpresa na tabela cliente
alter table cliente rename column nomeCliente to nomeEmpresa;
-- criando tabela pedidos
create table pedidos (
id_pedidos int primary key,
dataPedido date
);
-- adicionando idClientes a tabela pedidos
alter table pedidos add idClientes int;
-- criando tabela itensPedidos
create table itensPedidos (
id_itensPedidos int primary key
);
-- trocando o nome de "nomeProduto" para "descricaoProduto" na tabela produtos
alter table Produtos rename column nomeProduto to descricaoProduto;
-- criado tabela estoques
create table estoques (
id_estoques int primary key,
quantidade int
);
-- adicionando coluna idprodutos em estoques
alter table estoques add idProdutos int;
-- criando tabela vendas
create table vendas (
id_vendas int primary key,
dataVenda date
);
-- adionando uma coluna em vendas chamada idcliente
alter table vendas add idCliente int;
-- criando tabela produtos
create table produtos (
nomeProduto varchar(50),
quantidadeProduto int,
valorProduto double
);
```