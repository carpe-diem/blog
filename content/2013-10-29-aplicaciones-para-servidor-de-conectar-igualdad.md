---
title: "Aplicaciones para servidor de Conectar Igualdad"
taxonomies:
  categories: ["Applications"]
  tags: ["Python"]
extra:
    add_toc: true
---


Ya esta libera el CD de instalación para los servidores del plan Conectar Igualdad.

Este proyecto, lo realizamos cuando trabajaba en la Coopetativa de Trabajo [Devecoop](https://www.devecoop.com/) Ltda. Surgio de la necesidad de las escuelas, de tener
disponible en la intranet de los colegios aplicaciones como wordpress, Moodle, etc. Pero como no todas las escuelas tienen
internet, se tuvo que buscar otra solución.

El CD se va a repartir en las escuelas oficialmente, pero desconozco cuando.


Uno de los puntos que tuvimos que resolver es que el administrador del servidor, no tiene permisos para instalar paquetes en la virtual,
asi que no podiamos usar herramientas como pyGTK. Esto lo solucionamos incorporando pyzenity en el código.

En esta versión libre, incorporo la aplicación [ALBA](http://www.proyectoalba.com.ar/) que es un Sistema Informático Abierto de Gestión Unificada para Unidades Educacionales.
En la versión oficial, nos pidieron que la saquemos, asi que solo esta en esta versión libre.

El código esta disponible en [github](https://github.com/carpe-diem/conectar-igualdad-server-apps).

Una vez que se eligen y se instalan las aplicaciones, estas estan disponibles en la url del servidor de apps. Tambíen ahí estan los manuales.

Link directo a la guia de instalación [Instalación](https://github.com/carpe-diem/conectar-igualdad-server-apps/raw/master/manuales/Instalacion.pdf).

Link directo al [detalle de aplicaciones](https://github.com/carpe-diem/conectar-igualdad-server-apps/raw/master/manuales/detalles_aplicaciones.pdf).
