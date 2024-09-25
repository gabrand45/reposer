# reposer

-- criando tabela
create table clientes (
idCliente int primary key,
nomeCliente varchar(100), 
emailCliente varchar(150),
dataNascimento date,
telefoneCliente varchar(14)
);
-- atributos adicionados

create table produtos (
idProdutos int primary key,
nomeProduto varchar(100),
precoProduto decimal(8,2)
);

create table faturas (
idFatura int primary key,
dataCriacao timestamp default current_timestamp,
valorFatura decimal(10,2)
);

-- timestamp é data com minutos