# desafio_dio3
Desafio dio 3

# Projeto de Banco de Dados: Oficina Mecânica

## Descrição

Este projeto consiste na criação de um banco de dados para o gerenciamento de uma oficina mecânica. O objetivo é modelar e implementar um sistema que permita o cadastro de clientes, veículos, mecânicos, serviços e ordens de serviço, além de possibilitar a realização de consultas e relatórios para auxiliar na gestão da oficina.

## Funcionalidades

* Cadastro de clientes, veículos, mecânicos e serviços.
* Registro de ordens de serviço, associando clientes, veículos, mecânicos e serviços.
* Consultas SQL para recuperar informações sobre clientes, veículos, serviços e ordens de serviço.
* Geração de relatórios com informações relevantes para a gestão da oficina.

## Esquema Lógico

O esquema lógico do banco de dados foi modelado utilizando o modelo relacional, com as seguintes tabelas:

* **Clientes:** (ID_Cliente (PK), Nome, Endereco, Telefone)
* **Veiculos:** (ID_Veiculo (PK), ID_Cliente (FK), Modelo, Marca, Ano)
* **Mecanicos:** (ID_Mecanico (PK), Nome, Especialidade)
* **Servicos:** (ID_Servico (PK), Descricao, Preco)
* **Ordens_Servico:** (ID_Ordem (PK), ID_Cliente (FK), ID_Veiculo (FK), Data_Entrada, Data_Saida)
* **Servicos_Ordem:** (ID_Ordem (FK), ID_Servico (FK), ID_Mecanico (FK), Horas_Trabalhadas, PRIMARY KEY(ID_Ordem, ID_Servico))

## Tecnologias Utilizadas

* [Nome do SGBD utilizado] (ex: MySQL, PostgreSQL)
* SQL

## Como Executar

1.  Clone este repositório: `git clone https://github.com/dolthub/dolt`
2.  Importe o script SQL (`script.sql`) para o seu SGBD.
3.  Insira dados de exemplo utilizando o arquivo `dados.sql` (opcional).
4.  Execute as consultas SQL presentes no arquivo `consultas.sql` para interagir com o banco de dados.

## Consultas SQL

O arquivo `consultas.sql` contém exemplos de consultas SQL que demonstram as funcionalidades do banco de dados, incluindo:

* Recuperações simples com SELECT Statement
* Filtros com WHERE Statement
* Expressões para gerar atributos derivados
* Ordenações dos dados com ORDER BY
* Condições de filtros aos grupos – HAVING Statement
* Junções entre tabelas para fornecer uma perspectiva mais complexa dos dados

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests para melhorar este projeto.

## Autor

* [Seu Nome]

## Licença

Este projeto está sob a licença [Nome da Licença].
