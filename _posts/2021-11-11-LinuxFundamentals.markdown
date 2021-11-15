---
title: "TryHackMe | Linux Fundamentals - Parte 1 (ESPAÑOL)"
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

<h3 style="color: #a6d608;"><i>Responda las siguiente preguntas</i></h3>
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
<br>
Por ejemplo, Ubuntu y Debian son algunas de las distribuciones más comunes de Linux porque es muy extensible. Es decir, puede ejecutar Ubuntu como un servidor (como sitios web y aplicaciones web) o como un escritorio completo. Para esta serie, usaremos Ubuntu. 
> ***Ubuntu Server puede ejecutarse en sistemas con solo 512 MB de RAM***

<h3 style="color: #a6d608;"><i>Responda las siguiente preguntas</i></h3>
**[Pregunta]**<br>
 Investigación: ¿En qué año fue el primer lanzamiento de un sistema operativo Linux?

> **1991**

---

## Task 3: Interacting With Your First Linux Machine (In-Browser)
Esta sala tiene una Ubuntu Linux con máquina la que puede interactuar dentro de su navegador mientras sigue el material de esta sala. 
Contiene toda la información de la máquina implementada en la habitación, incluida la dirección IP y el temporizador de vencimiento, junto con los botones para administrar la máquina. Recuerde " Terminar " una máquina una vez que haya terminado con la habitación.<br>

<h3 style="color: #a6d608;"><i>Responda las siguiente preguntas</i></h3>
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

<h3 style="color: #a6d608;"><i>Responda las siguiente preguntas</i></h3>
**[Pregunta]**<br>
Si quisiéramos generar el texto " TryHackMe ", ¿cuál sería nuestro comando?
> **echo TryHackMe**


**[Pregunta 2]**<br>
¿Cuál es el nombre de usuario de la persona con la que inició sesión en su implementada Linux máquina ?
> **tryhackme**

---

## Task 5: Interacting With the Filesystem! 
Hasta ahora solo hemos cubierto los " echo " y " whoami comandos ". No es tan útil cuando considera las cosas que tenemos que hacer, incluida la navegación por el sistema de archivos, leer y escribir en él también.<br>
<br>
En esta tarea, aprenderemos los comandos para poder hacer precisamente eso. Al igual que en la tarea anterior, mostraré los comandos en la tabla en el siguiente encabezado y mostraré ejemplos de estos comandos que se utilizan.

### Interactuar con el sistema de archivos
Como dije anteriormente, ser capaz de navegar por la máquina en la que está conectado sin depender de un entorno de escritorio es bastante importante. Después de todo, ¿de qué sirve iniciar sesión si no podemos ir a ninguna parte?
![image](https://user-images.githubusercontent.com/43649283/141395115-e81af62e-b92d-459c-85e1-5f818fcb1da1.png)

---

### Listado de archivos en nuestro directorio actual (ls)
Antes de que podamos hacer algo, como averiguar el contenido de cualquier archivo o carpeta, necesitamos saber qué existe en primer lugar. Esto se puede hacer usando el comando "ls" (abreviatura de listado)
![image](https://user-images.githubusercontent.com/43649283/141395193-65b23ac3-a7fd-411b-a203-c09de8f98c9f.png)<br>
En la captura de pantalla anterior, podemos ver que existen los siguientes directorios / carpetas: 

* Archivos importantes
* Mis documentos
* Notas
* Imágenes

> Consejo profesional: Puede enumerar el contenido de un directorio sin tener que navegar hasta él usando ls y el nombre del directorio. Es decir `ls Pictures`

---

### Cambiando nuestro directorio actual (cd)
Ahora que sabemos qué carpetas existen, necesitamos usar el " cd comando " (abreviatura de c hange d irectory) para cambiar a ese directorio. Digamos que si quisiera abrir el directorio "Imágenes", haría " cd Imágenes ". Donde nuevamente, queremos averiguar el contenido de este directorio "Imágenes" y para hacerlo, usaríamos " ls " nuevamente:
![image](https://user-images.githubusercontent.com/43649283/141395593-2ff51dba-0421-495e-828a-d5ed4605a085.png)
En este caso, ¡parece que hay 4 imágenes de perros!

---

### Salida del contenido de un archivo (cat)
Si bien saber sobre la existencia de archivos es genial, no es tan útil a menos que podamos ver su contenido.<br>
Pasaremos a discutir algunas de las herramientas disponibles para nosotros que nos permiten transferir archivos de una máquina a otra en una sala posterior.<br>
Pero por ahora, vamos a hablar de simplemente ver el contenido de los archivos de texto usando un comando llamado " cat".<br>
<br>
"Cat" es la abreviatura de concatenación y es una manera fantástica de generar el contenido de los archivos (¡no solo archivos de texto!).<br>
En la captura de pantalla a continuación, puede ver cómo combiné el uso de "ls" para enumerar los archivos dentro de un directorio llamado "Documentos": <br>
![image](https://user-images.githubusercontent.com/43649283/141395688-344708c4-5f4a-4342-84f0-eb71f87838e6.png)
Hemos aplicado algunos conocimientos de antes en esta tarea para hacer lo siguiente:

1. Se usó " **ls** " para informarnos qué archivos están disponibles en la carpeta "Documentos" de esta máquina. En este caso, se llama "todo.txt".
2. Luego hemos usado `cat todo.txt` para concatenar / generar el contenido de este archivo "todo.txt", donde el contenido es "¡Aquí hay algo importante que debo hacer más tarde!"

> **Consejo profesional:** puedes usar catpara generar el contenido de un archivo dentro de directorios sin tener que navegar hasta él usando cat y el nombre del directorio. Es decir **`cat /home/ubuntu/Documents/todo.txt`**

A veces, cosas como nombres de usuario, contraseñas (sí, realmente ...), banderas o ajustes de configuración se almacenan en archivos donde se puede usar "cat" para recuperarlos.

### Descubriendo la ruta completa a nuestro directorio de trabajo actual (pwd) 
Notará que a medida que avanza en la navegación de su máquina Linux, el nombre del directorio en el que está trabajando actualmente aparecerá en su terminal.<br>
Es fácil perder la pista de dónde estamos exactamente en el sistema de archivos, por eso quiero presentar " pwd ". Esto significa ***print working directory***.<br>
Usando la máquina de ejemplo de antes, estamos actualmente en la carpeta "Documentos", pero ¿dónde está exactamente en el sistema de archivos de la máquina Linux? Podemos averiguarlo usando este comando "pwd" como en la siguiente captura de pantalla:
![image](https://user-images.githubusercontent.com/43649283/141517690-27a1e13f-2a7b-4caf-ae8d-55f28b8b3a16.png)
Analicemos esto:
1. Ya sabemos que estamos en "Documentos" gracias a nuestro terminal, pero en este momento, no tenemos idea de dónde está almacenado "Documentos" para que podamos volver a él fácilmente en el futuro.
2. He utilizado el **"pwd"** (*print working directory*) de comandos para encontrar la ruta completa del archivo de esta carpeta "**Documentos**".
3. Linux nos dice amablemente que este directorio "Documentos" está almacenado en "**/home/ubuntu/Documents**" en la máquina - ¡es bueno saberlo!
4. Ahora en el futuro, si nos encontramos en una ubicación diferente, podemos usar **`cd /home/ubuntu/Documents`** para cambiar nuestro directorio de trabajo a este directorio "Documentos".

<h3 style="color: #a6d608;"><i>Responda las siguiente preguntas</i></h3>
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

---

## Task 6: Searching for Files 
Aunque no lo parece hasta ahora, una de las características redentoras de Linux es realmente lo eficiente que puede ser con él. Dicho esto, solo puede ser tan eficiente como esté familiarizado con él, por supuesto. A medida que interactúa con sistemas operativos como Ubuntu a lo largo del tiempo, los comandos esenciales como los que ya hemos cubierto comenzarán a convertirse en memoria muscular.<br>
<br>
Una forma fantástica de demostrar cuán eficiente puede ser con sistemas como este es usar un conjunto de comandos para buscar rápidamente archivos en todo el sistema al que nuestro usuario tiene acceso. No es necesario usarlo constantemente **cd** y **ls** para averiguar qué es dónde. En su lugar, podemos usar comandos como **find** para automatizar cosas como esta para nosotros!
> Aquí es donde Linux comienza a ser un poco más intimidante para acercarse, pero lo analizaremos y le ayudaremos a hacerlo.


### Usando find
El comando de búsqueda es fantástico en el sentido de que se puede usar de manera muy simple o bastante compleja, dependiendo de lo que desee hacer exactamente. De hecho, tanto es así, tenemos una sala completa dedicada a usar y practicar el búsqueda comando de . Sin embargo, vamos a ceñirnos primero a los fundamentos.<br>
Tome el fragmento a continuación, podemos ver una lista de directorios disponibles para nosotros: 
![image](https://user-images.githubusercontent.com/43649283/141525626-a07d3c5e-4427-4496-bc22-55dd9ea7471e.png)

1. Desktop
2. Documents
3. Pictures
4. folder1

Ahora, por supuesto, los directorios pueden contener incluso más directorios dentro de sí mismos. Se convierte en un dolor de cabeza cuando tenemos que revisar cada uno de ellos solo para intentar buscar archivos específicos. Nosotros podemos usar **find** para hacer esto por nosotros!<br>
Comencemos de manera simple y asumamos que ya sabemos el nombre del archivo que estamos buscando, ¡pero no podemos recordar dónde está exactamente! En este caso, buscamos "**passwords.txt**"
![image](https://user-images.githubusercontent.com/43649283/141525899-e2e341dc-d95f-496d-88e6-2264849a16c5.png)

**"Find"** ha logrado encontrar el archivo - resulta que está ubicado en la carpeta1 /passwords.txt - dulce. Pero digamos que no conocemos el nombre del archivo o queremos buscar todos los archivos que tengan una extensión como ".txt". Encuentra ¡hagámoslo nosotros también!<br>
<br>
Simplemente podemos usar lo que se conoce como comodín (\*) para buscar cualquier cosa que tenga .txt al final. En nuestro caso, queremos encontrar todos los archivos .txt que se encuentran en nuestro directorio actual. Construiremos un comando como **`find -name \*.txt`**. Donde "Find" ha podido encontrar cada archivo .txt y luego nos ha dado la ubicación de cada uno:
![image](https://user-images.githubusercontent.com/43649283/141526045-708e270e-86df-4898-8e79-1e940a65a7fe.png)
Find ha logrado encontrar :
1. "passwords.txt" ubicado dentro de "folder1" 
2. "todo.txt" ubicado dentro de "Documentos"

Eso no fue tan difícil, ¡eh! 

---

### Usando Grep 
Otra gran utilidad que es muy buena para aprender es el uso de "**grep**". El comando "**grep**" nos permite buscar en el contenido de los archivos los valores específicos que estamos buscando.<br>
Tomemos, por ejemplo, el registro de acceso de un servidor web. En este caso, el access.log de un servidor web tiene 244 entradas.
![image](https://user-images.githubusercontent.com/43649283/141698672-bea21835-75d1-4bbd-a816-81da029a9111.png)
Usando un comando como **cat** no lo va a cortar muy bien aquí. Digamos, por ejemplo, si quisiéramos buscar en este archivo de registro para ver las cosas que visitó un determinado usuario / dirección IP. Mirar 244 entradas no es tan eficiente considerando que queremos encontrar un valor específico.<br>
<br>
Nosotros podemos usar **grep** para buscar en todo el contenido de este archivo cualquier entrada del valor que estamos buscando. Siguiendo con el ejemplo del registro de acceso de un servidor web, queremos ver todo lo que ha visitado la dirección IP **"81.143.211.90"** (tenga en cuenta que esto es ficticio)
![image](https://user-images.githubusercontent.com/43649283/141698781-ef14c61d-d606-4114-b4bf-0ea890459749.png)
"Grep" ha buscado en este archivo y nos ha mostrado cualquier entrada de lo que hemos proporcionado y que está contenido en este archivo de registro para la IP. 

<h3 style="color: #a6d608;"><i>Responda las siguiente preguntas</i></h3>
**[Pregunta]**<br>
Utilice grep en "access.log" para encontrar la bandera que tiene el prefijo "THM". ¿Cuál es la bandera?
> **THM{\*\*\*\*\*\*}**

**[Pregunta 2]**<br>
¡Y todavía no he encontrado lo que estoy buscando!
> *No answer needed*

---

## Task 7: Introducción a los operadores de shell
Los operadores de Linux son una forma fantástica de mejorar sus conocimientos sobre el trabajo con Linux. Hay algunos operadores importantes que vale la pena mencionar. Cubriremos los conceptos básicos y los dividiremos en trozos del tamaño de un bocado.<br>
En una descripción general, mostraré los siguientes operadores:
![image](https://user-images.githubusercontent.com/43649283/141699246-28de998a-d4d6-480f-b692-89e0bd38c839.png)
Cubriremos estos con un poco más de detalle.

### Operador "&"
Este operador nos permite ejecutar comandos en segundo plano. Por ejemplo, digamos que queremos copiar un archivo grande. Obviamente, esto llevará bastante tiempo y no nos permitirá hacer nada más hasta que el archivo se copie correctamente.<br>
<br>
El operador de shell "&" nos permite ejecutar un comando y hacer que se ejecute en segundo plano (como esta copia de archivo) ¡permitiéndonos hacer otras cosas! 

---

### Operador "&&" 
Este operador de shell es un poco engañoso en el sentido de lo familiar que es para su socio "&". A diferencia del operador "&", podemos usar "&&" para hacer una lista de comandos para ejecutar, por ejemplo "**command1 && command2**". Sin embargo, vale la pena señalar que **command2** solo se ejecutará si **command1** fue exitoso. 

---

### Operador ">"
Este operador es lo que se conoce como redirector de salida. Lo que esto significa esencialmente es que tomamos la salida de un comando que ejecutamos y enviamos esa salida a otro lugar.<br>
<br>
Un gran ejemplo de esto es redirigir la salida del **echo** comando que aprendimos en la Task 4. Por supuesto, ejecutar algo como "**echo howdy**" devolverá "howdy" a nuestra terminal, eso no es muy útil. Lo que podemos hacer en su lugar, es redirigir "howdy" a algo como un nuevo archivo.<br>
<br>
Digamos que queremos crear un archivo llamado "**welcome**" con el mensaje "**hey**". Podemos correr ***echo hey > welcome*** donde queremos que se cree el archivo con el contenido "hey" así:
![image](https://user-images.githubusercontent.com/43649283/141700114-99a620cd-60f9-4052-8c4a-3a03b53acccb.png)
![image](https://user-images.githubusercontent.com/43649283/141700123-69013ccd-12d2-4013-beb1-55a83c0c2960.png)
> *Nota: Si el archivo, es decir, "welcome" ya existe, el contenido se **sobrescribirá**.* 

---

## Operador ">>"
Este operador también es un redirector de salida como en el operador anterior (**>**) Nosotros discutimos. Sin embargo, lo que hace que este operador sea diferente es que en lugar de sobrescribir cualquier contenido dentro de un archivo, por ejemplo, simplemente pone la salida al final.<br>
<br>
Siguiendo con nuestro ejemplo anterior donde tenemos el archivo "welcome" que tiene el contenido de "hey". Si tuviera que usar echo para agregar "hello" al archivo usando el operador "**>**", el archivo ahora solo tendrá "hello" y no "hey".<br>
<br>
El operador **>>** permite agregar la salida al final del archivo, **en lugar de eemplazar el contenido de esta manera**:
![image](https://user-images.githubusercontent.com/43649283/141700297-9a5d17d5-36bb-4e10-b1af-80041f774553.png)
![image](https://user-images.githubusercontent.com/43649283/141700308-da9a4bae-500f-4c4f-9aa6-78547a1c7925.png)

<h3 style="color: #a6d608;"><i>Responda las siguiente preguntas</i></h3>
**[Pregunta]**<br>
Si quisiéramos ejecutar un comando en segundo plano, ¿Qué operador querríamos usar?
> **&**

**[Pregunta 2]**<br>
Si quisiera reemplazar el contenido de un archivo llamado "passwords" con la palabra "password123", ¿cuál sería el comando? 
> **`echo password123 > passwords`**

**[Pregunta 3]**<br>
Ahora, si quisiera agregar "tryhackme" a este archivo llamado "passwords" pero también mantener "passwords123", ¿cuál sería mi comando?
> **`echo tryhackme >> passwords`**

**[Pregunta 4]**<br>
Ahora use la máquina Linux implementada para ponerlos en práctica
> *No answer needed*

---
## Task 8: Conclusiones y resúmenes
¡Buen trabajo para llegar a esta etapa! Cubrimos bastante para sus primeras interacciones con Linux. Sin embargo, estas son las funciones / más esenciales que utilizará cada vez que interactúe con una máquina Linux.<br>
<br>
Espero que esta sala no haya sido demasiado abrumadora para que la enciendas. Como mencioné anteriormente, se familiarizará con estas cosas muy rápidamente debido a la frecuencia con la que las usará.<br>
Para recapitular rápidamente, hemos cubierto lo siguiente:
1. Comprender por qué Linux es tan común hoy en día 
2. ¡Interactuando con su primera máquina Linux!
3. Ejecutó algunos de los comandos más fundamentales
4. ¡Recibí una introducción a la navegación por el sistema de archivos y cómo podemos usar comandos como find y grep para hacer que la búsqueda de datos sea aún más eficiente! 
5. Mejore sus comandos aprendiendo sobre algunos de los operadores de shell importantes. 

---

## Task 9: Conceptos básicos y Linux parte 2
¡Visite la segunda parte de la serie de fundamentos de Linux [aquí!](https://tryhackme.com/room/linuxfundamentalspart2)

<pre><code>┌──(kali㉿kali)-[~/ctf/thm/alfred]
└─$ nmap $ip -Pn
Host discovery disabled (-Pn). All addresses will be marked 'up' and scan times will be slower.
Starting Nmap 7.91 ( https://nmap.org ) at 2021-07-09 10:06 EDT
Nmap scan report for 10.10.145.45
Host is up (0.19s latency).

PORT     STATE SERVICE
80/tcp   open  http  
3389/tcp open  ms-wbt-server
8080/tcp open  http
</code></pre><p>Now we will do comprehensive scans on three ports we found from quick scan.</p>
