# Descrição do Projeto

Projeto de irrigação automático IOT com Arduino NodeMCU ESP8266 com suporte Alexa.

## Funcionalidades:

+ **1) irrigação automática:** o mecanismo de medição do solo é feito de uma em uma hora. Quando o sensor calcula estar abaixo de 70% de umidade é acionado o processo de irrigação. O tempo definido de irrigação foi de 30 segundos. O Tempo é tratado de acordo com a necessidade do solo e fluxo controlado de água. Esse controle pode ser feito atravéz de cotejadores que podem ser definidos para cada planta. 

**Exemplo:** Uma determinada planta em um vaso maior você pode aumentar o fluxo de água no cotejador e em outra planta com vaso menor você pode definir um fluxo menor de água.

O objetivo da irrigação automática é garantir que o solo seja sempre regado de acordo com as condições de umidade do solo, garantindo uma vida mais saudável as plantas. Nesse projeto destacamos a importância de manter a umidade entre 70 a 80%. Definimos que o corte será abaixo de 70%.

+ **2) Irrigação manual:** (Poderá ser feito via navegador web pela rede wi-fi ou pelo dispositivo alexa)

Usar alexa nesse projeto é dar como opcional a funcionalidade de irrigação manual que pode ser acionada dizendo "Alexa, ligar irrigação" e "Alexa, desligar irrigação" ou por outras chamadas personalizadas.

#### Componentes utilizados para montar o circuito eletrônico

+ Placa Arduino NodeMCU V3 ESP8266
+ Base Shield NodeMCU V3
+ Display LCD - I2C
+ Sensor de Umidade do solo
+ Válvula elétrica solenoide 12V
+ Relê 5v (responsável por acionar a válvula elétrica)
+ Terminal femea (para ligar nos polos da solenóide)
+ Fonte de alimentação 12V 1A
+ Conector Adaptador Borne X Plug P4 Fêmea (faz a ligação da fonte e o regulador de tensão)
+ Regulador De Tensão 5v LM7805
+ Capacitor para saída de 5v
+ Capacitor para entrada de 12v
+ Dissipador para o regulador de tensão
+ Pasta Térmica
+ Caixa de Passagem tampa transparente (estrutura para armazenar o circuito eletrônico)

#### Materiais utilizados para irrigação das plantas

+ Kit Irrigação Completo Gotejamento P Horta Ou Vasos

![image](https://user-images.githubusercontent.com/42357180/158000720-b31f9958-adb0-4090-bfbb-46adf0b63f92.png)


#### Bibliotecas principais Utilizadas

+ LiquidCrystal_I2C e Wire - para uso do displayLCD
+ ESP8266WiFi - Configurações da rede wi-fi
+ ESP8266WebServer - configura um servidor web

#### Suporte Alexa

+ FauxmoESP - biblioteca de suporte para alexa

Explicação da biblioteca FauxmoESP: 

#### Esquema básico de ligação

![Esquema-regador-plantas-automatico-arduino-nodeMcu-esp8266-iot-alexa drawio](https://user-images.githubusercontent.com/42357180/157962078-32cefca9-b91f-4a1e-9d09-8f1fb5d1eeff.png)


#### Codigo - explicações

+ Nome do dispositivo para detecção na Alexa:

```
#define LAMP_1 "IRRIGAÇÃO"
```

**Obs:** Na Alexa o dispositivo será detectado como lampada como o nome de IRRIGAÇÃO.

+ **Configurações da rede wi-fi**

```
//Configração do WiFi
const char* ssid = "nome da rede wi-fi";  // SSID Wifi
const char* password = "pwd";  // Senha Wifi
```


### Protótipo do projeto em funcionamento

![20220309_141822](https://user-images.githubusercontent.com/42357180/157976663-1d519da9-b9b1-4abc-a54d-e595b4c1e4bb.jpg)

![20220309_141934](https://user-images.githubusercontent.com/42357180/157976722-456cf787-df0f-46d4-bd9d-581f263302f7.jpg)

![20220310_131016](https://user-images.githubusercontent.com/42357180/157976806-e7ce7529-72fe-475f-8ac4-2bd532b1aa8f.jpg)

![20220310_141008](https://user-images.githubusercontent.com/42357180/157977163-7c974a28-4fef-4853-baf9-494d0854d86a.jpg)



