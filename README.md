# Relógio com LED
Dev's: Andre Ribeiro, Carlos Trevisan, Felipe Bis, Ian Degaspari

## Descrição

Um relógio com 86 leds, onde as cores são baseadas no horário durante o dia.

## Funcionamento

A comunicação com os leds é feita a partir de um ESP32. Utiliza-se o ESP32 para se conectar com a internt e poder capturar a hora, minutos, e segundos em tempo real com base no WI-FI.

O Relógio possui 86 leds onde a representação da hora e dos minutos é feita com fileiras de 4 leds formando dois digitos, conforme a imagem abaixo:

![alt text](https://cdn.discordapp.com/attachments/459524958452973590/803775160854380564/gugu.png)

Já os minutos e segundos são representados por duas fileiras de 15 leds, portando, cada led representa 4 minutos, com isso é feito um esquema de cores para representar os 4 minutos completo, se o do minutos, ou segundo estiver da cor da hora, esse minuto/segundo está completo totalizando 4 minutos, caso contrário, ele representa 1, 2, ou 3 mintuos/segundos.

Ao longo do dia a cor do relógio vai mudando, a noite a paleta de cor se aproxima do azul/roxo, onde 00h temos o roxo, durante o dia as cores se aproximam do amarelo/vermelho, onde o vermelho estará presente as 12h.
