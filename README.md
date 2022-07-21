### Kafka Learning


## Dinamica e Funcionamento

Producer - Quem produz o evento
Consumer - Consumidor da Mensagem

Em vez de conversarem diretamente, o Kafka fica no meio do caminho.

Kafka é um conjunto de maquinas, um Cluster.

Os nós do Kafka sao os Brokers, maquinas que processam e armazenam as mensagens. 

## Tópicos

Tópico é o canal de comunicacao responsavel por receber e disponiblizar os dados enviados para o kafka.

Esse topico pode ser lido por quantos sistemas precisarem. Diferente do RabbitMq

Topico é como se fosse um LOG. 

Quando um topico recebe uma mensagem ele vai armazenando uma atras da outra. E ela ganha como se fosse um ID (offset) - Posicao de cada mensagem.

Topico
0 1 2 3 4 5 6 7 N
^
First Record

O kafka permite reprocessar as mensagens.

## Anatomia de um registro

Offset 0 -> - Headers
            - Key (Agrupamento de mensagens que garante a ordem da entrega)
            - Value (Payload)
            - Timestamp

## Partições

Cada tópico pode ter uma ou mais partições, para garantir a resiliencia e distribuição dos seus dados. 

Topico recebe uma mensagem ele vai para uma partição (gaveta)


