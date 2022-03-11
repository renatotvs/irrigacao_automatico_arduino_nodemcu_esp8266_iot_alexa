# Descrição do Projeto

Projeto de irrigação automático IOT com Arduino NodeMCU ESP8266 com suporte Alexa.

## Funcionalidades:

+ **1) irrigação automática:** é feito medição no solo de uma em uma hora com o sensor de umidade. Quando o sensor medir abaixo de 70% de umidade é onde é feito a irrigação. Após a irrigação será feito na próxima hora uma nova verificação do solo.

O ideal que o solo esteja regado e mantido em uma umidade entre 70 a 80%. Nesse projeto definimos que o corte será abaixo de 70%.

+ **2) Irrigação manual:** (Poderá ser feito via navegador pela rede wi-fi ou pela alexa remotamente)

O objetvo de usar alexa nesse projeto é dar como opcional a funcionalidade de irrigação manual que pode ser acionada dizendo "Alexa, ligar irrigação" e "Alexa, desligar irrigação" ou por outras chamadas personalizadas.


#### Componentes utilizados

+ Placa Arduino NodeMCU V3 ESP8266
+ Base Shield NodeMCU V3
+ Display LCD - I2C
+ Sensor de Umidade do solo
+ Relê 5v
+ Válvula elétrica solenoide 12V
+ Terminal femea (para ligar nos polos da solenóide)
+ Fonte de alimentação 12V 1A
+ Plug P4 (para ligar fonte e arduino)
+ Regulador De Tensão 5v LM7805
+ Capacitor para saída de 5v
+ Capacitor para entrada de 12v
+ Dissipador para o regulador de tensão
+ Pasta Térmica

#### Bibliotecas principais Utilizadas

+ LiquidCrystal_I2C e Wire - para uso do displayLCD
+ ESP8266WiFi - Configurações da rede wi-fi
+ ESP8266WebServer - configura um servidor web

#### Suporte Alexa

+ FauxmoESP - biblioteca de suporte para alexa

Explicação da biblioteca FauxmoESP: 

#### Esquema de ligação

![Esquema-regador-plantas-automatico-arduino-nodeMcu-esp8266-iot-alexa drawio](https://user-images.githubusercontent.com/42357180/157962078-32cefca9-b91f-4a1e-9d09-8f1fb5d1eeff.png)


#### Codigo - explicações

+ Nome do dispositivo para detecção na Alexa:

```
#define LAMP_1 "IRRIGAÇÃO"
```

**Obs:** Na Alexa o dispositivo será detectado como lampada.

+ **Configurações da rede wi-fi**

```
//Configração do WiFi
const char* ssid = "nome da rede wi-fi";  // SSID Wifi
const char* password = "pwd";  // Senha Wifi
```





