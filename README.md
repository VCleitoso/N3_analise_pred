# N3_analise_pred
O que foi feito:

Simplesmente um dropna para retirada de dados nulos, não foram muitos e não parecem impactar tanto nos resultados.
A maior parte dos dados nulos era do ano de 2004, provavelmente por falta de monitoração, ou seja, o dropna não afeta a predição de valores acima de 2004.
O database então foi convertido em um init.sql, que é adicionado à um container mysql
A tabela no container é utlizada nas predições.

O arquivo N3.ipynb começa pedindo para o usuário escolher o endereço ip que está hospedando o docker, alṕem de dar instruções sobre como subir o docker
Em seguida, ele nos mostra gráficos de consumo e tipo de consumo, para ter umam melhor ideia da evolução do consumo de energia elétrica e quais as áreas mais consumistas.

Em seguida, são realizadas predições, usando as colunas 'ano', 'mes', 'sigla_uf_encoded', 'tipo_consumo_encoded', 'numero_consumidores', para prever o consumo de energia elétrica.

Foram usados os métodos de regressão linear, random forest e duas redes neurais.
Destas, os resultados mais favoráveis são encontrados na random forest.

É então gerado um html com os resultados, que é hospedado na rede local.