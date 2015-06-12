=======================
Wake up the geek way!
=======================

.. slide::
   :class: first center

Gael Pasgrimaud `@gawel_ <http://twitter.com/gawel_>`_

PSES 2015

About me
========

- Pythonista `@bearstech <http://twitter.com/bearstech>`_

- Membre fondateur de l'`AFPy <http://www.afpy.org>`_

3615-2.0 Ma vie
================

- Paris

- Bearstech

- ...

Skate
=====

.. step::
   :hide-title: true

.. figure:: static/skate.jpg

La bougeotte
============

- Devenir mobile

- Vivre sans meuble

- Avec le moins d'éléctronique possible: un vieux MacBook, un vieux android, un téléphone voip.

Du coup...
==========

- Départ de Paris en Mai 2014

- SDF de Mai à Septembre

- Sédentarisation pour le hors saison...

Sunset
====

.. step::
   :hide-title: true

.. figure:: static/sunset.jpg

Surf
====

.. step::
   :hide-title: true

.. figure:: static/surfbikerack2.jpg


Résultat
========

- Plus de vie sociale

- Plus de sortie

- Plus de meubles

- Plus d'éléctronique

- Plein de nouveaux projets python!

asyncio
=======

Module introduit dans python3.4 permettant l'asynchrone sans de code spaghetti

Qu'est ce que le spaghetti?
=============================

.. code-block:: javascript

    $.get('/', function(data) {
        $.post('/', function(data) {
            setTimeout(function() { $.get('/timeout', function(data) {
                ...
                }, 1000)
            }
        }
    }

Avec asyncio
============

.. code-block:: python

    resp = yield from http.get('/')
    resp = yield from http.post('/', (yield from resp.body))
    yield from asyncio.sleep(.1)
    resp = yield from http.get('/timeout')

Cas d'utilisation
=================

- irc: irc3

- asterisk AMI: panoramisk

- cron like: aiocron


Le meilleur réveil du monde
===========================

irc bearstech + irssi + irc3 + aiocron + panoramisk


