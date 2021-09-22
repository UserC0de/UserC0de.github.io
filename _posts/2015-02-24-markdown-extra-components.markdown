---
title: "Red team vs Blue team"
layout: post
date: 2021-09-22 22:26
image: /assets/images/markdown.jpg
headerImage: false
tag:
- Hacking Ethical
- Teams
- Blue
- Red
- Cybersecurity
category: blog
author: Carlos Montero
description: Diferentes equipos sobre la seguridad de la información
---

Estos equipos juegan un papel importante en la defensa contra ataques cibernéticos avanzados que amenazan las comunicaciones empresariales, los datos sensibles de los clientes o los secretos comerciales.

##Qué es un Red Team
Un equipo rojo está formado por profesionales de la seguridad que actúan como amenazas que intentan superar controles de seguridad cibernética. Estos equipos suelen estar formados por hackers éticos independientes que evalúan la seguridad del sistema de manera objetiva.

Utilizan todas las técnicas disponibles para encontrar puntos débiles en personas, procesos y tecnología para obtener acceso no autorizado a los activos. Como resultado de estos ataques simulados, los equipos rojos hacen recomendaciones y planes sobre cómo fortalecer la postura de seguridad de una organización.

##Cómo funciona un Red Team
Te sorprendería saber que los equipos rojos pasan más tiempo planeando un ataque que realizándolos. En efecto, los equipos rojos despliegan una serie de métodos para obtener acceso a una red. Por ejemplo, los ataques de ingeniería social se basan en el reconocimiento y la investigación para realizar campañas de spear phishing dirigidas.

Asimismo, antes de realizar una prueba de penetración, se utilizan rastreadores de paquetes y analizadores de protocolos para explorar la red y recopilar la mayor cantidad de información posible sobre el sistema.

La información típica recogida durante esta fase incluye:

   * Descubrir los sistemas operativos en uso (Windows, MacOS o Linux).
   * Identificar la marca y el modelo del equipo de red (servidores, cortafuegos, conmutadores, enrutadores, puntos de acceso, ordenadores, etc.).
   * Comprensión de los controles físicos (puertas, cerraduras, cámaras, personal de seguridad).
   * Aprender qué puertos están abiertos/cerrados en un cortafuegos para permitir/bloquear un tráfico específico.
   * Crear un mapa de la red para determinar qué servicios están ejecutando los hosts y dónde se está enviando el tráfico.

Una vez que el equipo rojo tiene una idea más completa del sistema, desarrollan un plan de acción diseñado para atacar las vulnerabilidades específicas de la información que recogieron anteriormente.

Por ejemplo, un miembro del equipo rojo puede saber que un servidor está ejecutando Microsoft Windows Server 2016 R2 (un sistema operativo de servidor) y que las políticas de dominio por defecto podrían estar todavía en uso.

Así, Microsoft "envía" su software en su estado predeterminado dejando a los administradores de red la tarea de actualizar las políticas, lo que Microsoft recomienda hacer lo antes posible para reforzar la seguridad de la red. Si todavía está en dicho estado, el atacante puede comprometer las medidas de seguridad en uso.

Una vez que se identifican las vulnerabilidades, el equipo rojo las intenta explotar para obtener acceso a su red. Una vez que el atacante se encuentra en su sistema, lo normal es que use técnicas de escalada de privilegios con las que intenta robar las credenciales de un administrador que tiene acceso a los niveles más altos de información crítica.





#### Especial Elements
- [Evidence](#evidence)
- [Side-by-Side](#side-by-side)
- [Star](#star)
- [Especial Breaker](#especial-breaker)
- [Spoiler](#spoiler)

#### External Elements
- [Gist](#gist)
- [Codepen](#codepen)
- [Slideshare](#slideshare)
- [Videos](#videos)

---

## Evidence

You can try the evidence!

<span class="evidence">Paragraphs can be written like so. A paragraph is the basic block of Markdown. A paragraph is what text will turn into when there is no reason it should become anything else.</span>

{% highlight html %}
<span class="evidence">Paragraphs can be written like so. A paragraph is the basic block of Markdown. A paragraph is what text will turn into when there is no reason it should become anything else.</span>
{% endhighlight %}

---

## Side-by-side

Like the [Medium](https://medium.com/) component.

**Image** on the left and **Text** on the right:

{% highlight html %}
<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="{{ site.url }}/{{ site.picture }}" alt="Alt Text">
        <figcaption class="caption">Photo by John Doe</figcaption>
    </div>

    <div class="toright">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>
</div>
{% endhighlight %}

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="{{ site.url }}/{{ site.picture }}" alt="Alt Text">
        <figcaption class="caption">Photo by John Doe</figcaption>
    </div>

    <div class="toright">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>
</div>

**Text** on the left and **Image** on the right:

{% highlight html %}
<div class="side-by-side">
    <div class="toleft">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitations ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>

    <div class="toright">
        <img class="image" src="{{ site.url }}/{{ site.picture }}" alt="Alt Text">
        <figcaption class="caption">Photo by John Doe</figcaption>
    </div>
</div>
{% endhighlight %}

<div class="side-by-side">
    <div class="toleft">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>

    <div class="toright">
        <img class="image" src="{{ site.url }}/{{ site.picture }}" alt="Alt Text">
        <figcaption class="caption">Photo by John Doe</figcaption>
    </div>
</div>

---

## Star

You can give evidence to a post. Just add the tag to the markdown file.

{% highlight raw %}
star: true
{% endhighlight %}

---

## Especial Breaker

You can add a especial *hr* to your text.

{% highlight html %}
<div class="breaker"></div>
{% endhighlight %}

<div class="breaker"></div>

---

## Spoiler

You can add an especial hidden content that appears on hover.

{% highlight html %}
<div class="spoiler"><p>your content</p></div>
{% endhighlight %}

<div class="spoiler"><p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p></div>

---

## Gist

You can add Gists from github.

{% highlight raw %}
{ % gist sergiokopplin/91ff4220480727b47224245ee2e9c291 % }
{% endhighlight %}

{% gist sergiokopplin/91ff4220480727b47224245ee2e9c291 %}

---

## Codepen

You can add Pens from Codepen.

{% highlight html %}
<p data-height="268" data-theme-id="0" data-slug-hash="gfdDu" data-default-tab="result" data-user="chriscoyier" class='codepen'>
    See the Pen <a href='https://codepen.io/chriscoyier/pen/gfdDu/'>Crappy Recreation of the Book Cover of *The Flame Alphabet*</a> by Chris Coyier (<a href='https://codepen.io/chriscoyier'>@chriscoyier</a>) on <a href='https://codepen.io'>CodePen</a>.
</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
{% endhighlight %}

<p data-height="268" data-theme-id="0" data-slug-hash="gfdDu" data-default-tab="result" data-user="chriscoyier" class='codepen'>See the Pen <a href='https://codepen.io/chriscoyier/pen/gfdDu/'>Crappy Recreation of the Book Cover of *The Flame Alphabet*</a> by Chris Coyier (<a href='https://codepen.io/chriscoyier'>@chriscoyier</a>) on <a href='https://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

---

## Slideshare

Add your presentations here!

{% highlight html %}
<iframe src="//www.slideshare.net/slideshow/embed_code/key/hqDhSJoWkrHe7l" width="560" height="310" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe>
{% endhighlight %}

<iframe src="//www.slideshare.net/slideshow/embed_code/key/hqDhSJoWkrHe7l" width="560" height="310" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe>

---

## Videos

Do you want some videos? Youtube, Vimeo or Vevo? Copy the embed code and paste on your post!

**Example**

{% highlight html %}
<iframe width="560" height="310" src="https://www.youtube.com/embed/r7XhWUDj-Ts" frameborder="0" allowfullscreen></iframe>
{% endhighlight %}

<iframe width="560" height="310" src="https://www.youtube.com/embed/r7XhWUDj-Ts" frameborder="0" allowfullscreen></iframe>

[1]: https://daringfireball.net/projects/markdown/
[2]: https://www.fileformat.info/info/unicode/char/2163/index.htm
[3]: https://www.markitdown.net/
[4]: https://daringfireball.net/projects/markdown/basics
[5]: https://daringfireball.net/projects/markdown/syntax
[6]: https://kune.fr/wp-content/uploads/2013/10/ghost-blog.jpg
