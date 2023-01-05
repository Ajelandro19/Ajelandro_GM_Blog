---
title: "ESP32"
date: 2023-01-05T13:21:46-05:00
draft: false
---
# Primeros pasos 

Seguramente recientemente adquiriste o piensas adquirir una ESP32 y no sabes por donde empezar. En este post te voy a mostrar como instalar el entorno de desarrollo y como hacer tu primer programa.

## ¿Qué es una ESP32?

## ¿Cómo programarla desde el Arduino IDE?
 El primer paso es abrir el IDE de Arduino, posteriormente ir a la opción de preferencias dentro de la pestaña *Archivo* y agregar la siguiente URL en la sección de "Gestor de URLs Adicionales para Tarjetas":
 > https://dl.espressif.com/dl/package_esp32_index.json

 En la pestaña *Herramientas* seleccionar la opción de *Placa* y luego *Gestor de Tarjetas*. Buscar la opción de *ESP32* y luego instalarla.
![Gestor de tarjetas](../../images/GestortarjetaESP32.png)
 Una vez instalado, seleccionar la opción de *ESP32 Dev Module* en la pestaña de *Placa* dentro de la pestaña *Herramientas*.
 
![Seleccionar tarjeta](../../images/ESP32Dev.png)


## Primer programa
Para hacer nuestro primer programa, vamos a encender y apagar un led interno de la placa. Para esto escribimos el siguiente código en el IDE de Arduino:
```c
void setup() {
  pinMode(2, OUTPUT);
}
void loop() {
  digitalWrite(2, HIGH);
  delay(1000);
  digitalWrite(2, LOW);
  delay(1000);
}   
```
Luego de compilar, conectamos nuestra placa a la computadora y seleccionamos el puerto en el que se encuentra conectada. En caso de no saber el puerto al que se encuentra, abrir el administrador de dispositivos y buscar *USB-SERIAL CH340*.
![Puerto de la tarjeta](../../images/COM.png)

Finalmente, presionamos el botón de *Subir* y el programa se cargará en la placa.

En caso de que no se cargue el programa, verificar que la placa esté conectada correctamente y que el puerto seleccionado sea el correcto.

Nota: Para algunos modelos de ESP32, es necesario mantener el boton de *Boot* presionado mientras se carga el programa.
