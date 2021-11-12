---
title: "TryHackMe | Linux Fundamentals - Parte 1"
layout: post
date: 2021-11-11 19:38
tag: linux, kernel, commands, hacking, Se tensó
image: /assets/images/LinuxFundamentals1/linuxfundamental.png
headerImage: true
walkthroughs: true
hidden: true
description: "THM Linux Fundamentals - Parte 1 en español"
category: walkthroughs
author: userc0de
externalLink: false
---
## Task 1: Introdution
Bienvenido a la primera parte de la serie de salas "Conceptos básicos de Linux". Lo más probable es que esté utilizando una máquina con Windows o Mac, ambos son diferentes en el diseño visual y en su funcionamiento. Al igual que Windows, iOS y MacOS, Linux es solo otro sistema operativo y uno de los más populares del mundo que alimenta autos inteligentes, dispositivos Android, supercomputadoras, electrodomésticos, servidores empresariales y más.

¡Cubriremos parte de la historia detrás de Linux y luego, finalmente, comenzaremos su viaje de ser un asistente de Linux! Esta habitación te tendrá:

   1. Ejecutando sus primeros comandos en una interactiva Linux máquina en su navegador
   2. Enseñarle algunos comandos esenciales que se utilizan para interactuar con el sistema de archivos.
   3. Presentarle cómo trabajan los usuarios y grupos en Linux (y lo que esto significa para nosotros como probadores de penetración)

**[Pregunta]**<br>
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

> **1991**

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

### Interactuar con el sistema de archivos
Como dije anteriormente, ser capaz de navegar por la máquina en la que está conectado sin depender de un entorno de escritorio es bastante importante. Después de todo, ¿de qué sirve iniciar sesión si no podemos ir a ninguna parte?
![image](https://user-images.githubusercontent.com/43649283/141395115-e81af62e-b92d-459c-85e1-5f818fcb1da1.png)

### Listado de archivos en nuestro directorio actual (ls)
Antes de que podamos hacer algo, como averiguar el contenido de cualquier archivo o carpeta, necesitamos saber qué existe en primer lugar. Esto se puede hacer usando el comando "ls" (abreviatura de listado)
![image](https://user-images.githubusercontent.com/43649283/141395193-65b23ac3-a7fd-411b-a203-c09de8f98c9f.png)<br>
En la captura de pantalla anterior, podemos ver que existen los siguientes directorios / carpetas: 

* Archivos importantes
* Mis documentos
* Notas
* Imágenes

> Consejo profesional: Puede enumerar el contenido de un directorio sin tener que navegar hasta él usando ls y el nombre del directorio. Es decir `ls Pictures`

### Cambiando nuestro directorio actual (cd)
Ahora que sabemos qué carpetas existen, necesitamos usar el " cd comando " (abreviatura de c hange d irectory) para cambiar a ese directorio. Digamos que si quisiera abrir el directorio "Imágenes", haría " cd Imágenes ". Donde nuevamente, queremos averiguar el contenido de este directorio "Imágenes" y para hacerlo, usaríamos " ls " nuevamente:
![image](https://user-images.githubusercontent.com/43649283/141395593-2ff51dba-0421-495e-828a-d5ed4605a085.png)
En este caso, ¡parece que hay 4 imágenes de perros!

### Salida del contenido de un archivo (cat)
Si bien saber sobre la existencia de archivos es genial, no es tan útil a menos que podamos ver su contenido.<br>
Pasaremos a discutir algunas de las herramientas disponibles para nosotros que nos permiten transferir archivos de una máquina a otra en una sala posterior.<br>
Pero por ahora, vamos a hablar de simplemente ver el contenido de los archivos de texto usando un comando llamado " cat".<br>
"Cat" es la abreviatura de concatenación y es una manera fantástica de generar el contenido de los archivos (¡no solo archivos de texto!).<br>
En la captura de pantalla a continuación, puede ver cómo combiné el uso de "ls" para enumerar los archivos dentro de un directorio llamado "Documentos": <br>
![image](https://user-images.githubusercontent.com/43649283/141395688-344708c4-5f4a-4342-84f0-eb71f87838e6.png)
Hemos aplicado algunos conocimientos de antes en esta tarea para hacer lo siguiente:

1. Se usó " **ls** " para informarnos qué archivos están disponibles en la carpeta "Documentos" de esta máquina. En este caso, se llama "todo.txt".
2. Luego hemos usado `cat todo.txt` para concatenar / generar el contenido de este archivo "todo.txt", donde el contenido es "¡Aquí hay algo importante que debo hacer más tarde!"

> **Consejo profesional:** puedes usar catpara generar el contenido de un archivo dentro de directorios sin tener que navegar hasta él usando cat y el nombre del directorio. Es decir `cat /home/ubuntu/Documents/todo.txt`

A veces, cosas como nombres de usuario, contraseñas (sí, realmente ...), banderas o ajustes de configuración se almacenan en archivos donde se puede usar "cat" para recuperarlos.

### Descubriendo la ruta completa a nuestro directorio de trabajo actual (pwd) 
Notará que a medida que avanza en la navegación de su máquina Linux, el nombre del directorio en el que está trabajando actualmente aparecerá en su terminal.<br>
Es fácil perder la pista de dónde estamos exactamente en el sistema de archivos, por eso quiero presentar " pwd ". Esto significa p rint w RABAJAR d irectorio.<br>
Usando la máquina de ejemplo de antes, estamos actualmente en la carpeta "Documentos", pero ¿dónde está exactamente en el sistema de archivos de la máquina Linux? Podemos averiguarlo usando este comando "pwd" como en la siguiente captura de pantalla:
![image](https://user-images.githubusercontent.com/43649283/141517690-27a1e13f-2a7b-4caf-ae8d-55f28b8b3a16.png)
Analicemos esto:
1. Ya sabemos que estamos en "Documentos" gracias a nuestro terminal, pero en este momento, no tenemos idea de dónde está almacenado "Documentos" para que podamos volver a él fácilmente en el futuro.
2. He utilizado el **"pwd"** (*print working directory*) de comandos para encontrar la ruta completa del archivo de esta carpeta "**Documentos**".
3. Linux nos dice amablemente que este directorio "Documentos" está almacenado en "**/home/ubuntu/Documents**" en la máquina - ¡es bueno saberlo!
4. Ahora en el futuro, si nos encontramos en una ubicación diferente, podemos usar **`cd /home/ubuntu/Documents`** para cambiar nuestro directorio de trabajo a este directorio "Documentos".

**[Pregunta]**<br>
En la máquina Linux que implementa, ¿cuántas carpetas hay?
> **4**

**[Pregunta 2]**<br>
¿Qué directorio contiene un archivo?
> **folder4**

**[Pregunta 3]**<br>
¿Cuál es el contenido de este archivo?
> **Hello World**

**[Pregunta 4]**<br>
Utilice el comando **cd** para navegar hasta este archivo y averiguar el nuevo directorio de trabajo actual. ¿Cual es la ruta?
> `/home/tryhackme/folder4`



