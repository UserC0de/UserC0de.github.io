---
title: "Linux Fundamentals - Parte 1"
layout: post
date: 2021-11-11 19:38
tag: linux, kernel, commands, hacking, Se tensó
image: /assets/images/LinuxFundamentals1/linuxfundamental.png
headerImage: true
walkthroughs: true
hidden: false
description: "Como crear un rubberducky con un Arduino UNO"
category: project
author: Carlos
externalLink: false
---
## Task 1: Introdution
Bienvenido a la primera parte de la serie de salas "Conceptos básicos de Linux". Lo más probable es que esté utilizando una máquina con Windows o Mac, ambos son diferentes en el diseño visual y en su funcionamiento. Al igual que Windows, iOS y MacOS, Linux es solo otro sistema operativo y uno de los más populares del mundo que alimenta autos inteligentes, dispositivos Android, supercomputadoras, electrodomésticos, servidores empresariales y más.

¡Cubriremos parte de la historia detrás de Linux y luego, finalmente, comenzaremos su viaje de ser un asistente de Linux! Esta habitación te tendrá:

   1. Ejecutando sus primeros comandos en una interactiva Linux máquina en su navegador
   2. Enseñarle algunos comandos esenciales que se utilizan para interactuar con el sistema de archivos.
   3. Presentarle cómo trabajan los usuarios y grupos en Linux (y lo que esto significa para nosotros como probadores de penetración)

**[Pregunta]**
Let's get started!
> *No answer needed*

---
    
## Task 2: A Bit of Background on Linux 
### ¿Dónde se utiliza Linux?

Es justo decir que **Linux** es mucho más intimidante de abordar que los sistemas operativos (SO) como Windows. Ambas variantes tienen sus propias ventajas y desventajas. Por ejemplo, Linux es considerablemente más liviano y te sorprendería saber que es muy probable que hayas usado Linux de una forma u otra todos los días. Linux impulsa cosas como:

* Sitios web que visita
* Paneles de control / entretenimiento para el automóvil
* Sistemas de punto de venta (PoS) como cajas registradoras y cajas registradoras en tiendas
* Infraestructuras críticas como controladores de semáforos o sensores industriales

---

### Sobre Linux

El nombre " Linux " es en realidad un término general para varios sistemas operativos basados en UNIX (otro sistema operativo). Gracias a que UNIX es de código abierto, las variantes de Linux vienen en todas las formas y tamaños, las más adecuadas para el uso del sistema.

Por ejemplo, Ubuntu y Debian son algunas de las distribuciones más comunes de Linux porque es muy extensible. Es decir, puede ejecutar Ubuntu como un servidor (como sitios web y aplicaciones web) o como un escritorio completo. Para esta serie, usaremos Ubuntu. 
> ***Ubuntu Server puede ejecutarse en sistemas con solo 512 MB de RAM***

**[Pregunta]**<br>
 Investigación: ¿En qué año fue el primer lanzamiento de un sistema operativo Linux?

> *1991*

---

## Task 3: Interacting With Your First Linux Machine (In-Browser)
Esta sala tiene una Ubuntu Linux con máquina la que puede interactuar dentro de su navegador mientras sigue el material de esta sala. 
Contiene toda la información de la máquina implementada en la habitación, incluida la dirección IP y el temporizador de vencimiento, junto con los botones para administrar la máquina. Recuerde " Terminar " una máquina una vez que haya terminado con la habitación.<br>

**[Pregunta]**<br>
 ¡Implementé mi primera máquina Linux!
> *No answer needed*

---
## Task 4: Running Your First few Commands 
Como discutimos anteriormente, un gran punto de venta del uso de sistemas operativos como Ubuntu es lo livianos que pueden ser. Esto, por supuesto, no viene sin sus desventajas, donde, por ejemplo, a menudo no hay una GUI (interfaz gráfica de usuario) o lo que también se conoce como un entorno de escritorio que podamos utilizar para interactuar con la máquina (a menos que haya sido instalado). Una gran parte de la interacción con estos sistemas se realiza mediante el "Terminal".
<br>
La "Terminal" está basada puramente en texto y es intimidante al principio. Sin embargo, si analizamos algunos de los comandos, después de un tiempo, ¡rápidamente se familiarizará con el uso de la terminal! 
![image](https://user-images.githubusercontent.com/43649283/141393431-c4c7441f-cbd0-4303-8824-a3b4be29e222.png)
¡Necesitamos poder realizar funciones básicas como navegar a archivos, generar su contenido y crear archivos! Los comandos para hacerlo se explican por sí mismos (una vez que sepa cuáles son, por supuesto ...)<br>

Comencemos con dos de los primeros comandos que he desglosado en la siguiente tabla:
![image](https://user-images.githubusercontent.com/43649283/141393746-86e2a13b-81c2-4405-9d71-c680c45917e8.png)
> Consulte los fragmentos a continuación para ver un ejemplo de cada comando que se utiliza ...

**[Pregunta]**<br>
Si quisiéramos generar el texto " TryHackMe ", ¿cuál sería nuestro comando?
> **echo TryHackMe**


**[Pregunta 2]**<br>
¿Cuál es el nombre de usuario de la persona con la que inició sesión en su implementada Linux máquina ?
> **tryhackme**

---
## Task 5: Interacting With the Filesystem! 
Hasta ahora solo hemos cubierto los " echo " y " whoami comandos ". No es tan útil cuando considera las cosas que tenemos que hacer, incluida la navegación por el sistema de archivos, leer y escribir en él también.<br>

En esta tarea, aprenderemos los comandos para poder hacer precisamente eso. Al igual que en la tarea anterior, mostraré los comandos en la tabla en el siguiente encabezado y mostraré ejemplos de estos comandos que se utilizan.

## Interactuar con el sistema de archivos
Como dije anteriormente, ser capaz de navegar por la máquina en la que está conectado sin depender de un entorno de escritorio es bastante importante. Después de todo, ¿de qué sirve iniciar sesión si no podemos ir a ninguna parte?
![image](https://user-images.githubusercontent.com/43649283/141395115-e81af62e-b92d-459c-85e1-5f818fcb1da1.png)

## Listado de archivos en nuestro directorio actual (ls)
Antes de que podamos hacer algo, como averiguar el contenido de cualquier archivo o carpeta, necesitamos saber qué existe en primer lugar. Esto se puede hacer usando el comando "ls" (abreviatura de listado)
![image](https://user-images.githubusercontent.com/43649283/141395193-65b23ac3-a7fd-411b-a203-c09de8f98c9f.png)<br>
En la captura de pantalla anterior, podemos ver que existen los siguientes directorios / carpetas: 

* Archivos importantes
* Mis documentos
* Notas
* Imágenes


