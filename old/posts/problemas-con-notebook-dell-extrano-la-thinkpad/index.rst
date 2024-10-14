.. title: Problemas con Notebook Dell (Extraño la Thinkpad)
.. slug: problemas-con-notebook-dell-extrano-la-thinkpad
.. date: 2019-10-18 22:55:50 UTC-03:00
.. tags: dell, systemd, Archlinux, Gnu/Linux 
.. category: Configuración
.. link: 
.. description: 
.. type: text
.. previewimage:


Hace un tiempo tuve que comprar una nueva notebook. Mi Thinkpad T430 ya estaba bastante obsoleta.

Por un tema de precios, tuve que desistir que seguir con la línea de Lenovo, y opte por una Dell (Dell G3)

Instale Archlinux y lo configure como siempre, y aunque tuve algunos problemas que solucionar por la compatibilidad de Dell con linux
(Por ejemplo, la placa de video), había un solo problema que me volvía loco, que era cuando cerraba la notebook y pasaba a estado sleep.


.. image:: /images/problemas-con-notebook-dell-extrano-la-thinkpad.png
   :align: center
   :width: 50%
   :alt: Dell G3

El problema es que al "despertarla", el touchpad no respondía. Encontré que volviendo a cargar el módulo ``i2c_hid`` volvía a funcionar 

.. TEASER_END

el Touchpad, así que al principio dejaba una consola abierta para hacer ``modprobe -r i2c_hid`` y ``modprobe i2c_hid``.

Luego de unos días, lo solucione definitivamente. Por una lado  agregue ``i2c_hid`` en ``/etc/suspend-modules.conf``.

Luego cree el archivo ``/usr/lib/systemd/system-sleep/suspend-modules`` con lo siguiente.


.. code-block:: bash

    #!/bin/bash

    case $1 in
        pre)
            for mod in $(</etc/suspend-modules.conf); do
                modprobe -r $mod
            done
        ;;
        post)
            for mod in $(</etc/suspend-modules.conf); do
                modprobe $mod
            done
        ;;
    esac
