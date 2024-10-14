.. title: Corrector ortográfico para Vim
.. slug: corrector-ortografico-para-vim
.. date: 2019-10-20 20:39:17 UTC-03:00
.. tags: Vim, Nikola 
.. category: Vim 
.. description: Corrector de ortografía para Vim 
.. type: text
.. previewimage: /images/corrector-ortografico-para-vim-1.png

Los que me conocen, o trabajaron conmigo saben que me gusta mucho la consola, ya que me resulta más cómodo y rápido para trabajar.
Y además utilizo vim para programar.

Cuando comence a probar nikola para el blog, me gusto la idea de poder escribir los posts en vim, pero me resultaba tedioso revisar si me faltaba 
algun acento, o si se pasaba alguna falta de ortografía.

Así fue como llegue a esta funcionalidad de vim :)


.. image:: /images/corrector-ortografico-para-vim-1.png
   :align: center
   :scale: 50 %
   :alt: Corrector ortográfico para Vim


*Spell*

El soporte para el corrector ortográfico se agrego en Vim 7.

.. TEASER_END

*Configuración*

El comando para habilitarlo es::

    :set spell 

Para habilitarlo en ingles::

    :set spell spelllang=en_us


Para habilitarlo en español, primero hay que descargar el diccionario::

    # cd /usr/share/vim/vim81/spell/
    # wget http://ftp.vim.org/vim/runtime/spell/es.utf-8.spl

Luego habilitarlo::

    :set spell spelllang=es


Una vez habilitado, se marcaran los errores y las sugerencias de sintaxis. Situados en modo visual sobre
la palabra con error, al escribir ``z=``, saldrá una lista de palabras recomendadas para su reemplazo.


.. image:: /images/corrector-ortografico-para-vim-2.png
   :align: center
   :scale: 50 %
   :alt: Corrector ortográfico para Vim


Dejo una lista de las opciones mas utilizadas, y un enlace a la `documentación oficial`__.

* ``[s``  Ir al próximo error.
* ``]s``  Ir al error anterior.
* ``zg``  Agrega la palabra al diccionario.
* ``zug`` Elimina la palabra del diccionario.
* ``z=``  Despliega lista de opciones para reemplazar la palabra.



.. _enlace: http://vimdoc.sourceforge.net/htmldoc/spell.html

__ enlace_

