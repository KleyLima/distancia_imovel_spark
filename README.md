# distancia_imovel_spark
### Proposta
Dado um arquivo com a posição geográfica de diversos imóveis realizar o cálculo da distância da estação de trem/metrô
mais próxima. 

### Arquivos
Os arquivos base presentes no repositório são estacoes.csv, imoveis_20200402.gz.parquet e steps.txt, que representam os
dados das estações, imóveis e os comandos para obter o resultado, respectivamente.

### Cálculo
Visto que ambos possuem as coordenadas geográficas é possivel utilizar método de distância entre dois pontos
que basicamente é o cálculo de Pitágoras ou então a fórmula de Haversine. No caso da fórmula de Pitágoras é preciso se
atentar a conversão de graus para medida de distância. No caso é utilizado a relação para Milhas Náuticas e depois
metros.

### Teste
O fluxo pode ser facilmente visualizado no Spark-Shell usando o comando `:load steps.txt` para executar os comandos
utilizados em sequência e visualizar o DataFrame com as distâncias. Lembrando que o Spark-Shell deve ter sido chamado 
no dirétorio que contém o arquivo, caso não, substitua `steps.txt` pelo path para chegar até ele.
