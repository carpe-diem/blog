---
title: "Permission denied en aws"
taxonomies:
  categories: ["Infrastructure"]
  tags: ["Amazon", "EC2", "Gnu/Linux"]
extra:
    add_toc: true
---



El otro día tenía que hacer un deploy de una aplicación en el servidor de un cliente en amazon.
Al intentar acceder por ssh, recibía como respuesta "Permission denied (publickey)".

No podía acceder de ninguna otra manera. Tuve que hacer algunos pasos y pude solucionarlo.

Mi problema era que alguien cambio los permisos del home, incluyendo el directorio ~/.ssh/.


Les paso como lo solucione.

* Parar la instancia.
* Ir a Volumes, encontrar el disco de la instancia con problemas y poner "dettach".
* Si no tenes otra instancia, crear una micro instancia y poner attach volume.

{{ iimg(src="/images/amazon-permission-denied-publickey.png", alt="Amazon Permission denied (publickey)") }}

* El disco ya esta montado en la nueva instancia, así que podes debugear hasta encontrar el problema.
* Dettach de la nueva instancia.
* Attach a la instancia vieja. En este caso, el punto de montaje debe ser /dev/sda1 (como estaba antes).
* Iniciar nuevamente la instancia
