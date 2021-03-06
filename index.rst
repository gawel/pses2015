.. impress::
   :func: linear

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

- Avec le moins d'électronique possible: un vieux MacBook, un vieux android, un
  téléphone voip.

Du coup...
==========

- Départ de Paris en Mai 2014

- SDF de Mai à Septembre

- Sédentarisation pour le hors saison...

Sunset
=======

.. step::
   :hide-title: true

.. figure:: static/sunset.jpg

Résultat
========

- Plus de vie sociale

- Plus de sortie

- Plus de meubles

- Plus d'éléctronique

- Plein de nouveaux projets python!

- Et...

Surf
====

.. step::
   :hide-title: true

.. figure:: static/surfbikerack2.jpg


asyncio
=======

Module introduit dans python3.4 permettant l'asynchrone sans de code spaghetti

Qu'est ce que le spaghetti?
=============================

Javascript!

Des callback de callback de callback

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

Pas de callback. Lecture linéaire compréhensible.

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

- irc privé bearstech

- vm bearstech en DC + tmux + irssi

- serveur asterisk

- irc3 + aiocron + panoramisk

- téléphone voip

Dans la vrai fausse vie
=======================

.. figure:: static/irssi.jpg

Et le matin
===========

::

    2015-06-12 09:00:00 INFO alarm matin launched
    2015-06-12 09:00:00 INFO ison {'names': ['gawel']}
    2015-06-12 09:00:00 INFO whois {'idle': '31821', ...}
    2015-06-12 09:00:00 INFO Ring matin for gawel
    2015-06-12 09:00:01 INFO irc3.alarm.gawel is ringing
    2015-06-12 09:00:16 INFO Hangup <Message ...> after 15s
    2015-06-12 09:00:16 INFO irc3.alarm.gawel is ringing
    2015-06-12 09:00:16 INFO Hangup <Message ...> after 0s

Check le pseudo, l'idle, puis sonne. Raccroche au bout de 15s.

Ne réveille pas si on est réveillé. Tadaah!

Links
=====

- `asyncio <https://docs.python.org/3.4/library/asyncio.html>`_

- `Talk de Victor Stinner @PyconFr <http://www.infoq.com/fr/presentations/exploration-boucle-evenement-asyncio>`_ (`slides <https://speakerdeck.com/haypo/exploration-de-la-boucle-devenements-asyncio>`_)

- `irc3 <https://github.com/gawel/irc3>`_

- Ces slides `https://gawel.github.io/pses2015/
  <https://gawel.github.io/pses2015/>`_
