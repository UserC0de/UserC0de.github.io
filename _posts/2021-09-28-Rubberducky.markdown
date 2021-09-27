---
title: "Como crear un rubberducky con un Arduino UNO"
layout: post
date: 2021-09-28 00:42
tag: jekyll
image: 
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: "This is a simple and minimalist template for Jekyll for those who likes to eat noodles."
category: project
author: Carlos
externalLink: false
---
## USB Rubber Ducky con Arduino UNO
La placa Arduino UNO, en teoría, no tiene la capacidad para actuar como un dispositivo HID, que es la función que necesitamos para poder crear con ella un USB Rubber Ducky. Sin embargo, esta placa tiene dos microcontroladores Arduino, el ATmega328 y el ATmega16u2, siendo este segundo el que nos interesa. Este microcontrolador se puede reprogramar para que funcione como un USB AVR (tal y como lo haría un Arduino Leonardo, por ejemplo), 
que es lo que nos permitiría emular un dispositivo HID y así crear nuestro propio USB Rubber Ducky.
Para conseguir esta función adicional tendremos que flashear un nuevo bootloader llamado HoodLoader2, creado por NicoHood. 
El código fuente está disponible en su propio Github.
Los pasos para flashear este bootloader empiezan por subir el sketch de instalación al Arduino con el Arduino IDE (podemos descargarlo desde aquí), de forma normal y corriente como haríamos con cualquier otro sketch programado por nososotrs mismos. 
Una vez hecho esto, necesitaremos hacer un pequeño cableado en la placa para así poder flashear el bootloader automáticamente.
El esquema de cableado que necesitamos para esto es el siguiente:
