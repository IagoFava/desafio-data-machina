# desafio-data-machina

Iago Fava da Costa

Desafio Data Machina

_________________________________________________________________________
O script criado para o desafio 1 é uma aplicação direta do conceito de Standard Normal Distribution que pode ser conferido em:
https://onlinestatbook.com/2/normal_distribution/standard_normal.html#:~:text=A%20normal%20distribution%20with%20a,called%20a%20standard%20normal%20distribution.&text=Since%20the%20distribution%20has%20a,(or%20above)%20the%20mean.
_________________________________________________________________________
Já o script usado na resolução do desafio 2.1 e 2.2 seguem as seguintes etapas:
	- Chamada de bibliotecas
	- Definição da função que calcula a distância e o tempo de viagem entre duas cidades,
		usando uma API do Google cloud chamada Distance Matrix.
	- Aplicação de um input-exemplo para o desafio 2.1, com uma viagem de carro de Catanduva para São José do Rio Preto.
		Hora de partida: momento que o código é rodado.
	- Input-exemplo para 2.2
		Hora de partida (não aceita input no passado): 24/03/2021, 21h
		Arquivo .xlsx contendo "Nome" | "Valor" | "Cidade" | "Data Lim"
	- Definição de uma função baseada no problema do caixeiro viajante
		Diferentemente do original, o algoritmo tenta maximizar o valor (lucro);
		O lucro é uma variável dependete da hora que cada viagem é feita;
		O algoritmo faz todas as permutações de ordem de trajeto possíveis, guardando o melhor resultado até o momento.
		No fim, ele faz print da melhor ordem de entrega e qual o valor do lucro.
	- Chamada da função do caixeiro viajante adaptada.

_________________________________________________________________________
Limitações:
	- Para o desafio 2.2, o script admite que o arquivo de input já está tratado (sem espaços e dentro do ASCII)
		A primeira cidade no arquivo deve ser Sao+Paulo
	- O algoritmo é pouco eficiente em processamento com muitas cidades;
		O tempo rodando o código aumenta de forma fatorial
	- O programa admite apenas uma entrega por cidade.

_________________________________________________________________________
Propostas de melhorias:
	- Considerar a carga horária do funcionário entregador
		A cada 8 horas de trajeto, seriam adicionadas 16 horas de descanso
	- Usar um algoritmo de melhor desempenho e modificá-lo para as necessidades do desafio 2.2
	- Fazer o tratamento do arquivo .xlsx dentro do próprio código
	- Adicionar Sao+Paulo no próprio script, sem necessidade de vir do input
	- Somar lucro diversas entradas de um
_________________________________________________________________________
Considerações finais:

O programa cria uma rota otimizada a partir do lucro, mas a validação é difícil de ser feita.
Foram encontradas dificuldades ao longo do processo:
	- Adaptação minha para o uso API de Distance Matrix. Em especial, ativar permissões no Google Cloud
	- Encontrar um código do problema do caixeiro viajante que fosse customizável para minhas necessidades
	- Customizar o dito código
	- Lidar com DateTime
	- Para o desafio 1, houve confusão sobre o conceito de normalização
	- 


_________________________________________________________________________
A API usada pode ser consultada em:
https://developers.google.com/maps/documentation/distance-matrix/overview#distance-matrix-advanced

O custo de uso da API:
https://developers.google.com/maps/documentation/distance-matrix/usage-and-billing
