---
title: 'App de Declaración Jurada'
published: true
date: '09-10-2020 20:56'
taxonomy:
    category:
        - blog
    tag:
        - Java
        - Application
        - Quarkus
        - Postgres
        - Microservices
        - Rest
        - APi
hide_git_sync_repo_link: false
dateformat: 'd-m-Y H:i'
blog_url: /
show_sidebar: true
show_breadcrumbs: true
show_pagination: true
hide_from_post_list: false
feed:
    limit: 10
twitterenable: true
twittercardoptions: summary
twittershareimg: /home/Wallpaper-Java-Duke-01.png
articleenabled: false
musiceventenabled: false
orgaenabled: false
orga:
    ratingValue: 2.5
orgaratingenabled: false
eventenabled: false
personenabled: false
musicalbumenabled: false
productenabled: false
product:
    ratingValue: 2.5
restaurantenabled: false
restaurant:
    acceptsReservations: 'yes'
    priceRange: $
facebookenable: false
continue_link: true
sharer:
    enabled: true
---

Todo comienza con un amigo que tiene algunas canchas de squash y durante el covid-19, todas las personas que ingresan al club deben firmar una declaración jurada en papel con un bolígrafo.
Cuál es la consecuencia de eso, tenemos que tomar bolígrafo para firmar un papel ... ¿QUÉ? ¡La idea es salir del papel y tocar cosas!
Entonces planeamos tener un código QR en la entrada del club y cuando ingreses, con tu celular escanea eso y firma digitalmente las preguntas de la declaración jurada.
Esa es una aplicación "simple", así que decidí desarrollarla en [Quarkus](https://quarkus.io/).
La base de los requisitos de la aplicación tiene:
1.- La Entidad (las pistas de squash).
2.- el Usuario que está accediendo al club, que debe registrarse en el mismo.
3.- Y la Declaración Jurada que deberá firmar el Usuario en la Entidad.
  
Hice la aplicación en 4 días y uso _KISS_ (Keep It Simple Stupid) como premisa. Las Entidades y los Usuarios se almacenan en una base de datos, y la Declaración Jurada es un formulario estático que tiene algunas preguntas que responder. El inicio de sesión, no existe, es solo un formulario de registro con los campos que la Declaración Jurada necesita como Nombre, apellido y ubicación.

¡Así que funciona! prueba y despliegue. Geniales. Todos están felices.

===

## Ir más lejos
Sin embargo, decido ir más lejos.
Primero, un inicio de sesión para tener Usuarios, Entidades / Espacio y Declaración para administrarlos.
Un tablero para controlar quién accede al club y qué Declaración se ha firmado.
Entre momentos, podemos comprobar cómo se relacionan los usuarios en la cancha.
Podríamos hacer nuestras propias declaraciones juradas.
Gestionar la Entidad, definiendo propiedades y Espacios. Los espacios son los lugares / canchas donde la gente se para.

Entonces la aplicación comienza a crecer con algunas cosas interesantes.
La tecnología de base de datos utilizada es [ElephantSQL](https://www.elephantsql.com/) para probar [Postgres](https://www.postgresql.org/) en la red.
Esta es una elegante aplicación web Java con protocolo RESTEasy / JAX-RS. Dije clásico porque vengo de JavaEE con Jboss, por eso.

## Mirando mas alla
¿Qué podría hacer? Hágalo [Reactivo](https://quarkus.io/guides/getting-started-reactive). Quarkus aporta reactividad en todos los aspectos del ciclo de vida; en base de datos, backend y front.
Utilice Panache, para el repositorio.
Haga API primero.
Una nueva interfaz, tal vez agregue [Svelte](https://svelte.dev/) (está invitado a colaborar) o [https://quasar.dev/](https://quasar.dev/) (cómo dijo, 2Qute to Be Real)
Agregue soporte de correo para conectar usuarios.
Prueba hecha para verificar la funcionalidad de la aplicación.
¿Qué tal si agregamos blockchain a cada declaración?

Para obtener más información sobre Quarkus.io, visite [https://quarkus.io/](https://quarkus.io/).

Puedes acceder al repositorio de github en <i class = "fa fa-github fa-2x"> </i> [https://github.com/wuiler/declaracion/](https://github.com/wuiler/declaracion/)