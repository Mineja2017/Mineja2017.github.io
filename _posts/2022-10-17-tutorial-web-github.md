---
layout: single
title: Tutorial de como crar una web (como esta) en GitHub Pages
excerpt: "Github Pages es una herramineta gratuita que Github ofrece para crear páginas web, en este tutorial veremos como crear una web con esta herramienta gracias al uso de una plantilla."
date: 2022-10-17
classes: wide
header:
  teaser: /assets/images/tuto-web/github-logo.png
  teaser_home_page: true
  #icon: /assets/images/hackthebox.webp
categories:
  - Tutorial
tags:  
  - Github Pages
  - Tutorial
---


[Github Pages](https://pages.github.com/ "Github Pages") es una herramineta gratuita que Github ofrece para crear páginas web, en este tutorial veremos como crear una web con esta herramienta gracias al uso de una plantilla.

## Preparación

**ATENCION**:  Este tutorial se usará Windows como sistema operativo.  
Los requisitios para empezar con nuestra web serán los siguientes:  
- Tener una cuenta creada en Github (Si no tienes una puedes crearla [aquí](https://github.com/signup))
- Descargar el programa [Github Desktop](https://desktop.github.com/) para gestionar el repositorio
- Un editor de texto (yo recomiendo [Sublime Text](https://www.sublimetext.com/) pero se puede utilizar cualquier otro que nos marque sintaxis)

## Repositorio

Para crear la web primero necesitaremos buscar una plantilla que se editable. Podemos encontrar muchas a través del buscador del propio Github pero yo he eligido justamente la de la web que estas viendo, que se puede encontar en el siguiente enlace.  
- <https://github.com/slemire/slemire.github.io>

1. Para dar crédito a la persona que previamente ha creado la plantilla solo debemos hacer click en el boton donde pone *"Fork"*, esto creara un repositorio igual a este que nosotros podremos editar mas adelante
![](/assets/images/tuto-web/github-fork.png)

2. Se nos abrira una pantalla que nos pedira en el nombre del proyecto que queremos crear, aquí debemos poner un nombre al proyecto que siga el siguiente esquema: ***nombre de usuario**.github.io* (Importante respetar el *github.io* porque sino Github no reconocerá que es una pagina web)
![](/assets/images/tuto-web/github-name.png)

3. Le damos a aceptar y ya tendremos nuestro repositorio creado
![](/assets/images/tuto-web/github-name2.png)

En caso de que no quieras usar esta plantilla dejo por aquí un par mas:
- <https://github.com/supun-io/jekyll-theme-leaf>
- <https://github.com/tocttou/hacker-blog>

## Preparación del entorno

Ahora que tienes el repositorio con la informacion de la pagina web debemos activar el entorno de Github Pages para lanzar la web al público.  

- Desde el panel pricipal de nuestro repositorio nos dirigiremos a *Setting*>*Pages*>*Branch* y aqui seleccionaremos *master*, *root* y le daremos a guardar tal y como se muestras en la imágenes:
![](/assets/images/tuto-web/enviroment-setup1.png)

![](/assets/images/tuto-web/enviroment-setup2.png)

![](/assets/images/tuto-web/enviroment-setup3.png)

- Después nos dirijiremos a *Enviroments* y a *github-pages*, seleccionaremos *All branches* donde pone *Select Branches*:

![](/assets/images/tuto-web/enviroment-setup4.png)

![](/assets/images/tuto-web/enviroment-setup5.png)

![](/assets/images/tuto-web/enviroment-setup6.png)

- La Configuración ya está lista, ahora solo tendremos que esperar unos minutos a que la pagina este disponible en *nombre de usuario.github.io*


## Instalar Ruby, Jekyll y bundler

Ahora debemos instalar uno paquetes que nos ayudarán a lanzar la web de manera local para ver los cambios antes de que sean publicados.

1. Descargaremos Ruby2.7 desde este [link](https://github.com/oneclick/rubyinstaller2/releases/download/RubyInstaller-2.7.6-1/rubyinstaller-devkit-2.7.6-1-x86.exe) y lo instalaremos dejando marcadas las opciones por defecto. Despues de finalizar la instalación se abrira una terminal en windows que te preguntará que tipo de instalación que deseas. Debes seleccionar el número **3** y cuando te vuelva a preguntar esto mismo ya podrás cerrar la terminal (en caso de que la terminal no aparezaca, abre una terminal manualmente y escribe lo siguiente: `ridk install`.
![](/assets/images/tuto-web/ruby1.png)  

2. Una vez instalado ruby, en el buscador de windows escribiremos *cmd* y abriremos una terminal. Escribiremos `gem install jekyll bundler` y cuando esta instalación escribiremos `bundle install`.

## Github Desktop

1. Una vez tenemos ruby instalado necesitaremos el repositorio en nuestro PC para poder hacer lso cambios y luego publicarlos. Aquí es donde entra en juego **Github Desktop**. Una vez instalado iniciarmos sesión en el botçon azul y vincularemos la cuenta de Github con la aplicación.
![](/assets/images/tuto-web/github1.png)  

2. Depués seleccionaremos *clonar repositorio de la web*, el nombre del repositorio que queramos clonar y por ultimo, aceptaremos las opciones por defecto.
![](/assets/images/tuto-web/github2.png)
![](/assets/images/tuto-web/github3.png)
![](/assets/images/tuto-web/github4.png)

## lanzar la web en local

Antes de editar nuestra web, vamos a lanzarla en local para poder ver como van quedando los cambios antes de publicarlo de manera oficial.

1. Navegamos desde el explorador de Windows hasta donde se encuentre la carpeta (suele estar en *Documentos*>*Github*>*Nombre del repositorio*) y haremos click derecho en barra de busqueda y copiaremos la información de la ruta.
![](/assets/images/tuto-web/local1.png)  

2. Abriremos una terminal y escribiremos `cd` y acto seguido pegaremos la ruta.
![](/assets/images/tuto-web/local2.png)  

3. Una vez en el directorio escribiremos el siguiente comomando para lanzar la web: `bundle exec jekyll serve` y le daremos unos segundos para que cargue toda la configuración

4. En nuestro navegador pondremos la ruta `localhost:4000` en la barra de busqueda y podremos ver una copia exacta de nuestra web que irá editándose a medida que hagamos cambios en ella. (si te salta un error de que no se puede acceder, dale unos segundos mas para cargar). Si queremos detener que la web se muestre en local solo debemos ir a la terminal y pulsa la combinación de teclas *Contol* + *C* y escribir la *S* dos veces.

## Edicion de la web

La pagina web ya está lista, pero como podemos comprobar tiene un monton de información y publicaciones que nosotros no queremos. Así que ahora es cuando vamos a editar la web propiamente dicha para poder subir nuestra informacion. Como se puede editar en muchos aspectos, solo dejaré algunos ejemoplos.

### Configuración

Desde este apartado podremos cambiar principalmente la barra de la derecha con la información personal. Ejecutaremos *Sublime Text* y abriremos en archivo llamado *_config.yml*. Dejaré algunos ejemplos de como cambiar algunas cosas.

- Si queremos editar la informacion del **sitio web** (idioma, titulo de la pagina, imagen de banner, etc) nos dirijiremos a la linea donde pone lo siguiente y sustituiremos los campos por la información deseada:
```yaml
# Site Settings
locale                   : "en-US"
title                    : "snowscan.io" #--> Titulo de la pestaña
title_separator          : "-"
name                     : "Snowscan" #--> Nombre de usuario
description              : "Posts about security, CTFs and networking" --> Descripción de usuario
url                      : "https://snowscan.io" # the base hostname & protocol for your site e.g. "https://mmistakes.github.io"
baseurl                  : # the subpath of your site, e.g. "/blog"
repository               : "slemire/slemire.github.io"  #--> GitHub usuario/repositorio ej: "Mineja2017/Mineja2017.github.io"
logo                     : "/assets/images/masthead.png" #--> Banner de la web, si quieres cambiarlo debes subirlo con el mismo nombre a la misma carpeta
teaser                   : # --> Teaser de la web
breadcrumbs              : true # true, false (default)
words_per_minute         : 200
```
Si por otro lado queremos editar la informacion que aparece a la izquierda se hara en la siguiente sección. Aqui podremos links a las redes que aparecen listadas para que estan aparezcan en la web. En caso de que no queramos poner nada, podemos comentar con un *#* esa parte.

```yaml
# Site Author
author:
  name             : "Mineja" #--> Nombre que aparece debajo de la foto
  avatar           : "/assets/images/avatar.png" #->> Ruta de la foto
  bio              : "Estudiante" #--> Biografia
  location         : "Madrid" #--> Aquo puedes poner tu ciudad
  email            : "j.garcia.47@villalkor.com" #--> Un email 
  uri              :
  home             : # null (default), "absolute or relative url to link to author home"
  bitbucket        :
  codepen          :
  dribbble         :
  flickr           :
  facebook         :
  foursquare       :
  github           : "Mineja2017"
  gitlab           :
  google_plus      :
  keybase          : #
  instagram        :
  lastfm           :
  linkedin         : # 
  pinterest        :
  soundcloud       :
  stackoverflow    : # "123456/username" (the last part of your profile url, e.g. https://stackoverflow.com/users/123456/username)
  steam            : # "steamId" (the last part of your profile url, e.g. https://steamcommunity.com/id/steamId/)
  tumblr           :
  twitter          : #
  vine             :
  weibo            :
  xing             :
  youtube          : #
```

- Si queremos editar las **publicaciones** debemos ir la carpeta *_posts*. Borraremos todos los archivos menos 1 (nos servirá de plantilla) y lo abriremos con *Sublime Text*. Al principio del documento podremos editar la información que se ve desde el inicio y el resto se vera al hacer click. Debe quedar algo asi:

```markdown
---
layout: single
title: #Titulo Principal
excerpt: "" #Descripcion del artículo
date: 2022-10-17 #Fecha de publicación
classes: wide
header:
  teaser: /assets/images/tuto-web/github-logo.png #Foto que aparece con cada articulo
  teaser_home_page: true
  icon: /assets/images/hackthebox.webp #Pequeño icono que aparece debajop del título
categories:
  - Tutorial #Categorial de la publicacion 
tags:  
  - Github Pages #Etiquetas de la publicacion 
  - Tutorial
---
```

Aqui dejo un [link](https://markdown.es/sintaxis-markdown/#codigosbloque) a una guia con la sintaxis basica de markdown para que puedas editar el post como prefieras.

- Para subir imagenes simplemente debemos ir a `/assets/images` y borrar todo el contenido. Despues subiremos las imagenes que queramos (recomiendo organizarlas en carpetas). Para referenciarlas en las publicaciones o en cualquier otro documento, solo debemos escribir la ruta donde están guardadas (Empezando desde la carpeta del proyecto). Un ejemplo seria este:
```markdown
![](/assets/images/tuto-web/local2.png)
```  

## Publicar los cambios

Para publicar los cambios solo debemos detener la terminal con *Control* + *C* y dirigirnos a Github Desktop

1. Una vez en Github Desktop veremos que podemos publicar un cambio en este menu de la parte inferior. Solo deberemos escribir el nombre nombre que le vamos a dar al cambio y una descripción.
![](/assets/images/tuto-web/subir1.png) 

2. Despues pulsaremos en el botón para subir a la web y listo, en unos minutos la web "oficial" estará editada.
![](/assets/images/tuto-web/subir2.png)