## DIO - Desafio: Bootcamp Heineken - Inteligência Artificial Aplicada a Dados com Copilot
# Projeto de Banco de Dados para Oficina Mecânica
O sistema permite que clientes cadastrem seus veículos, agendem revisões ou consertos e acompanhem o andamento dos serviços realizados. Cada veículo é atendido por uma equipe especializada de mecânicos, que executa os serviços necessários e utiliza peças específicas conforme os requisitos de cada ordem de serviço.
## Objetivo
Este projeto consiste na criação de um modelo conceitual de banco de dados para um sistema de controle e gerenciamento de execução de ordens de serviço (OS) em uma oficina mecânica. O esquema foi desenvolvido com base em uma narrativa fornecida.

## Narrativa do Projeto
A narrativa descreve o seguinte cenário:
- Clientes levam os veículos à oficina mecânica para consertos ou revisões periódicas.
- Cada veículo é designado a uma equipe de mecânicos, que identifica os serviços a serem executados e preenche uma Ordem de Serviço (OS) com data de entrega.
- O valor de cada serviço é calculado com base em uma tabela de referência de mão de obra.
- O valor de cada peça utilizada também compõe o valor total da OS.
- O cliente autoriza a execução dos serviços.
- A mesma equipe avalia e executa os serviços.
- Mecânicos possuem código, nome, endereço e especialidade.
- Cada OS possui:
    -  Número.
    -  Data de emissão.
    -  Valor total.
    -  Status (Pendente, Em andamento, Concluída).
    -  Data para conclusão dos trabalhos.
- Uma OS pode ser composta por vários serviços, e um mesmo serviço pode estar contido em mais de uma OS.
- Uma OS pode ter vários tipos de peça, e uma peça pode estar presente em mais de uma OS.

## Passos Realizados
- Identificação das entidades principais: Cliente, Veículo, Equipe, Mecânico, Ordem de Serviço (OS), Serviço e Peça.
- Definição dos relacionamentos entre as entidades.
- Identificação dos atributos essenciais para cada entidade.
   -  Att: Em Angola, o Bilhete de Identidade (BI) é o documento de identificação oficial dos cidadãos, usando esse contexto vamos adaptar o modelo para utilizar o BI como identificador único dos clientes e mecânicos, em vez do CPF.
     
![Oficina](https://github.com/user-attachments/assets/aefe7adc-362d-4e6f-a4fb-52b03af07420)

## Regras de Negócio
Foram definidas as seguintes regras de negócio:
- O valor total da OS é calculado somando o valor dos serviços e das peças utilizadas.
- Os status possíveis da OS são: Pendente, Em andamento, Concluída.
- Sempre que uma peça é utilizada em uma OS, a quantidade em estoque deve ser atualizada.
- A execução dos serviços só pode ocorrer após a autorização do cliente.




