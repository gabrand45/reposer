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
