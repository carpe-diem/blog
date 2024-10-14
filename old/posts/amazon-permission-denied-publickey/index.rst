.. link: 
.. description: Permission denied en aws 
.. tags: Amazon, EC2, Gnu/Linux
.. date: 2013/11/04 14:26:59
.. title: Amazon Permission denied (publickey)
.. slug: amazon-permission-denied-publickey
.. category: AWS
.. type: text
.. previewimage: /images/amazon-permission-denied-publickey.png


El otro día tenía que hacer un deploy de una aplicación en el servidor de un cliente en amazon.
Al intentar acceder por ssh, recibía como respuesta "Permission denied (publickey)".

No podía acceder de ninguna otra manera. Tuve que hacer algunos pasos y pude solucionarlo.

Mi problema era que alguien cambio los permisos del home, incluyendo el directorio ~/.ssh/.

.. TEASER_END

Les paso como lo solucione.

* Parar la instancia.
* Ir a Volumes, encontrar el disco de la instancia con problemas y poner "dettach".
* Si no tenes otra instancia, crear una micro instancia y poner attach volume.

.. image:: /images/amazon-permission-denied-publickey.png
   :align: center
   :scale: 50 %
   :alt: Amazon Permission denied (publickey)

* El disco ya esta montado en la nueva instancia, así que podes debugear hasta encontrar el problema.
* Dettach de la nueva instancia.
* Attach a la instancia vieja. En este caso, el punto de montaje debe ser /dev/sda1 (como estaba antes).
* Iniciar nuevamente la instancia
