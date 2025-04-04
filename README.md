# construindo-um-esquema-conceitual-para-banco-de-dados

## Projeto elaborado para mostrar de forma gráfica e visual o funcionamento de um banco de dados para uma Oficina

# 📌 Relações e Cardinalidades

|Entidade 1           |	Relacionamento   |Entidade 2      |	Cardinalidade|
|---------------------|------------------|----------------|--------------|
|Cliente	            | Possui	         |Veículo	        |1:N
|Veículo	            | Pode ter	       |Ordem de Serviço|1:N
|Ordem de Serviço     |	Contém	         |Serviço	        |N:M
|Ordem de Serviço     |	Usa	             |Peça	          |N:M
|Ordem de Serviço     |	É executada por  |Equipe	        |1:N
|Equipe	              | Possui	         |Mecânicos	      |N:M
|Tabela de Mão de Obra|	Define valor para|Serviço	        |1:N
|Cliente	            | Solicita	       |Ordem de Serviço|1:N
|Ordem de Serviço	    | Possui	         |Autorização	    |1:1

# 📝 Observações:

- No relacionamento Equipe ↔ Mecânico, a cardinalidade pode ser 1:N se um mecânico só puder pertencer a uma equipe, mas N:M se ele puder fazer parte de várias.

- A relação Ordem de Serviço ↔ Autorização pode ser modelada como 1:1, mas também pode ser um atributo dentro da entidade Ordem de Serviço.
