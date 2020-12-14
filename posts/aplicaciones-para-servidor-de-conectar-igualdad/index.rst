.. link: 
.. description: Aplicaciones sin conexión para servidores de conectar igualdad 
.. tags: python, pyzenity, Conectar Igualdad, Wordpress, Moodle, Italc, Mediawiki, Atrium, Elgg, Alba
.. date: 2013/10/29 12:43:29
.. title: Aplicaciones para servidor de Conectar Igualdad
.. slug: aplicaciones-para-servidor-de-conectar-igualdad
.. category: aplicaciones
.. type: text


Ya esta libera el CD de instalación para los servidores del plan Conectar Igualdad.

Este proyecto, lo realizamos cuando trabajaba en la Coopetativa de Trabajo Devecoop_ Ltda. Surgio de la necesidad de las escuelas, de tener
disponible en la intranet de los colegios aplicaciones como wordpress, Moodle, etc. Pero como no todas las escuelas tienen
internet, se tuvo que buscar otra solución.

El CD se va a repartir en las escuelas oficialmente, pero desconozco cuando.

.. TEASER_END

Uno de los puntos que tuvimos que resolver es que el administrador del servidor, no tiene permisos para instalar paquetes en la virtual, 
asi que no podiamos usar herramientas como pyGTK. Esto lo solucionamos incorporando pyzenity en el código.

En esta versión libre, incorporo la aplicación ALBA_ que es un Sistema Informático Abierto de Gestión Unificada para Unidades Educacionales.
En la versión oficial, nos pidieron que la saquemos, asi que solo esta en esta versión libre.

El código esta disponible en github_.

Una vez que se eligen y se instalan las aplicaciones, estas estan disponibles en la url del servidor de apps. Tambíen ahí estan los manuales.

Link directo a la guia de instalación_.

Link directo al detalle_ de aplicaciones.


.. _Devecoop: www.devecoop.com

.. _ALBA: http://www.proyectoalba.com.ar/

.. _github: https://github.com/carpe-diem/conectar-igualdad-server-apps

.. _instalación: https://github.com/carpe-diem/conectar-igualdad-server-apps/raw/master/manuales/Instalacion.pdf

.. _detalle: https://github.com/carpe-diem/conectar-igualdad-server-apps/raw/master/manuales/detalles_aplicaciones.pdf
