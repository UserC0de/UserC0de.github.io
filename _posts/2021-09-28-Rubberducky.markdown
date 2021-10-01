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
Entonces empecé a investigar y justamente **[S4vitar](https://www.youtube.com/channel/UCNHWpNqiM8yOQcHXtsluD7Q)** subió un vídeo de como convertir el arduino uno en un rubberducky, parece que los planetas se alienaron porque la verdad es que no se. 
## Tabla de contenido
* [Introducción al USB RubberDucky](#introdución-al-usb-rubberducky)
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
Por rubber ducky se conoce a un dispositivo USB que contiene información "maliciosa" la cual podría infectar tu PC una vez que lo conectas a ella. Esta información podría ser un keylogger, un encriptador de información o cualquier otra herramienta para apropiarse de tu **información** o negarte el uso a ella.

<div class="usb">
  <img src="/assets/images/rubberducky1.jpg"
      align="right"
</div>

Al momento de conectar este USB, es reconocido con un dispositivo HID, haciéndose pasar por un teclado normal (para no levantar sospechas y evitar que sea bloqueado por antivirus o firewall) y ejecuta las teclas indicadas en su código.

