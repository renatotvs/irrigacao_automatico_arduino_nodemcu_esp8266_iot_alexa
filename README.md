# Descrição do Projeto

Projeto de irrigação automático IOT com Arduino NodeMCU ESP8266 com suporte Alexa

#### Componentes utilizados

+ Placa Arduino NodeMCU ESP8266
+ Base Shield NodeMCU V3
+ Arduino NodeMCU V3 com ESP8266
+ Placa Base para NodeMCU V3 Loli
+ Display LCD - I2C
+ Sensor de Umidade
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

+ LiquidCrystal_I2C - para uso do displayLCD
+ ESP8266WiFi - Configurações da rede wi-fi

#### Suporte Alexa

+ Fauxmo - biblioteca de suporte para alexa

#### Esquema de ligação

![Esquema-regador-plantas-automatico-arduino-nodeMcu-esp8266-iot-alexa drawio](https://user-images.githubusercontent.com/42357180/157962078-32cefca9-b91f-4a1e-9d09-8f1fb5d1eeff.png)


#### Codigo - explicações


+ **Configurações da rede wi-fi**

```
//Configração do WiFi
const char* ssid = "nome da rede wi-fi";  // SSID Wifi
const char* password = "pwd";  // Senha Wifi
```





