***************************
Organització d'aquesta guia
***************************

Aquesta guia consta d'un seguit de directrius que hem dividit en:

- **Mesures** que cal implementar i complir a tots els projectes.
- **Recomanacions** que no és obligatori aplicar, però que poden ser d'utilitat
  en determinades situacions.

És responsabilitat dels i les cap de projecte validar si les mesures s'estan
implementant correctament, i decidir quines recomanacions cal aplicar.

Algunes mesures son prou complexes com per merèixer ser fraccionades en
**sub-mesures** que puguin ser validades individualment.

Algunes mesures son impossibles d'aplicar en determinats projectes, i en aquest
cas s'intenta donar algunes **alternatives** (directrius que es troben
etiquetades d'aquesta manera al llarg del document). Cada mesura i les seves
potencials alternatives es troben mútuament enllaçades.

Cada mesura, recomanació o alternativa consta de:

- Un identificador únic per a tot el document.
- Un llistat d'etiquetes.

Les **etiquetes** ajuden a restringir en quins moments i en quins tipus de
projecte son importants cada mesura i cada recomanació. Poden servir, per
exemple, per generar un *checklist* de coses que la direcció del projecte
necessita comprovar.

Els apartats d'aquest capítol expliquen els tipus d'etiquetes que es fan servir
al llarg de la Guia. La resta de capítols d'aquesta guia ordenen les mesures i
recomanacions en àrees temàtiques i donen el context necessari per entendre la
rellevància de cada mesura.

A l':ref:`Annex: Llistats de mesures i recomanacions per etiquetes` es poden
trobar diferents llistats de mesures i recomanacions categoritzats per
etiquetes.


Etiquetes per escenaris d'ús
============================

En aquest apartat es defineixen diferents situacions o **escenaris** que es
poden produir en els projectes tecnològics en relació als components de
programari lliure i de codi obert en els que es basen. Aquests escenaris
determinen després quines mesures i recomanacions afecten a cada projecte.

Cada **projecte** defineix un sistema d'informació, i cada sistema d'informació
consta d'una determinada quantitat de **components** de programari. Uns
components es distingeixen dels altres perquè cada component té el seu propi
**repositori** de codi font. (Ocasionalment trobem components complexes que, per
raons pràctiques, tenen el seu codi repartit en diferents repositoris que es
versionen i distribueixen coordinadament). Els diferents components d'un
determinat sistema poden executar-se tots en una mateixa màquina, o bé poden
trobar-se distribuïts en diferents màquines. També poden executar-se com a part
del mateix procés o en processos diversos.

Els escenaris contemplats son els següents:

===================  ===========================================================
Etiqueta             Descripció
===================  ===========================================================
:code:`Integració`   **Integrar components existents**: es necessita implantar
                     un nou sistema que es pot construir en base a components ja
                     existents.
:code:`Adaptació`    **Modificar un component extern**: cal afegir funcionalitat
                     a un component ja disponible, o bé millorar-lo solucionant
                     deficiències, afegint traduccions, etc.
:code:`Plugin`       **Estendre una plataforma amb components endollables**: es
                     requereix crear nous components que s'integrin en una
                     plataforma o *framework* ja disponible i que facilita
                     aquesta tasca.
:code:`NouProducte`  **Crear un component nou**: es necessita crear una solució
                     nova des de zero.
:code:`Publicació`   **Publicar codi d'un component propi ja existent**: es
                     disposa d'un codi propi desenvolupat sota contractes
                     anteriors i que mai ha estat publicat, i es vol alliberar
                     en un repositori públic.
:code:`Document`     **Publicar documentació no vinculada a un únic projecte**:
                     es disposa d'una documentació no directament vinculada a
                     codi però que es vol alliberar en un repositori públic.
===================  ===========================================================

Tots els escenaris, a excepció dels escenaris :code:`Integració` i
:code:`Document`, fan referència a un únic component de programari. Per tant, en
un mateix projecte poden concórrer diferents escenaris si components diferents
es troben afectats de diferent manera.

Deixem fora de l'anàlisi contribucions a projectes que no impliquen una
modificació del codi d'un component, o la creació d'un repositori, com poden ser
contribucions a la documentació o facilitació de l'adopció de certes eines per
part de tercers.

Els escenaris :code:`Integració`, :code:`Adaptació`, :code:`Plugin` i
:code:`NouProducte` poden opcionalment requerir una **migració**, en cas que ens
trobem en la situació d'implantar un sistema que substitueix, en part o
totalment, les funcions d'un sistema anterior.

Escenari :code:`Integració`
---------------------------

Aquest escenari pot comportar la creació d'un o més repositoris propis, però no
per guardar-hi el codi de cap aplicació pròpiament, sinó per:

- Vincular-hi eines de gestió de projectes tals com gestors d'incidències
- Guardar o enllaçar documentació associada amb l'ús i operació del sistema
- Guardar fitxers de configuració i scripts necessaris per al desplegament del
  sistema
- Guardar fitxers de configuració i scripts necessaris per executar entorns de
  prova i d'integració continua, incloent *virtualització* i *containerització*
- Guardar elements de disseny i personalització del sistema
- Guardar instruccions d'instal·lació i ús del sistema
- Guardar tests d'integració dels diferents components

En quant als elements de personalització, destaquem la **traducció** dels
literals que es mostren a l'usuari i d'altres aspectes de la localització i
internacionalització (l10n, i18n). Contemplem dues possibilitats:

#. Es compleixen les següents dues condicions: (1) el programari a traduir està
   dissenyat per incorporar traduccions de la interfície, i (2) les traduccions
   a realitzar poden ser d'utilitat general per a d'altres potencials usuaris de
   l'eina. En aquest cas s'intentarà contribuir aquestes traduccions al projecte
   original i per tant ens trobaríem en l':ref:`escenari Adaptació`.
#. Alguna de les dues condicions anteriors no es compleix i emmagatzemem els
   fitxers necessaris per efectuar la traducció a un repositori propi.

.. admonition:: Exemple

   Un exemple hipotètic seria un portal web construït utilitzant un gestor de
   continguts com Wordpress, amb una base de dades MariaDB.

   Es tracta de components estàndard de programari lliure, però per facilitar-ne
   la gestió pot convenir guardar en un repositori elements de personalització
   com plantilles, fitxers CSS, imatges, llistat d'extensions de Wordpress a
   carregar, així com imatges de Docker que incloguin tots els elements
   necessaris per al desplegament.

Escenari :code:`Adaptació`
--------------------------

Aquest escenari pot comportar la creació d'un o més repositoris propis amb els
mateixos continguts descrits per a l':ref:`escenari Integració`. En canvi, el
tret distintiu d'aquest escenari és el patrocini per part de l'Ajuntament de
Barcelona del desenvolupament d'alguna contribució significativa a un producte
de programari lliure que pugui ser potencialment incorporada al producte
original (encara que aquesta integració no es realitzi mentre dura el propi
desenvolupament). Aquestes contribucions han de materialitzar-se en un conjunt
de *commits* en un repositori que estigui vinculat d'alguna manera al repositori
del producte original.

Les contribucions poden ser de diversa naturalesa:

- Noves funcionalitats que l'Ajuntament de Barcelona necessita i que poden ser
  d'interès per a més entitats o usuaris
- Traduccions complertes (o amb una cobertura significativa) de la interfície
  d'usuari, així com altres millores de localització (l10n) i
  internacionalització (i18n) que poden ser d'utilitat general per a d'altres
  potencials usuaris de l'eina

Si les traduccions o elements de localització es troben barrejats amb elements
de personalització propis de l'Ajuntament, o bé el producte original no està
dissenyat per incorporar noves traduccions i localitzacions, aleshores no es pot
plantejar una contribució com a tal i ens trobaríem a l':ref:`escenari
Integració`.

.. admonition:: Exemple: Bústia ètica de l'Ajuntament de Barcelona

   Existia un programari original, el de Globaleaks_, al qual se li han
   incorporat les funcionalitats de generació d'expedient intern i de devolució
   de resposta a l'usuari en forma de PDF. Aquestes funcionalitats formen part
   ara mateix de la branca *master* del `repositori principal de Globaleaks`_.

   En el mateix projecte s'han desenvolupat tasques de personalització,
   incloent la traducció de la interfície al català, però com que alguns
   literals no son d'ús general sinó que son personalitzacions pròpies de
   l'Ajuntament, la traducció en sí no s'ha pogut contribuir al projecte
   original.

.. _Globaleaks: https://www.globaleaks.org/
.. _`repositori principal de Globaleaks`:
   https://github.com/globaleaks/GlobaLeaks

Escenari :code:`Plugin`
-----------------------

Es tracta d'un escenari intermig entre la integració de funcionalitats noves a
un producte ja existent (:ref:`escenari Adaptació`) i el desenvolupament d'un
nou producte (:ref:`escenari-nouproducte`) i comparteix característiques dels
dos.

D'una banda, es parteix d'un programari ja existent al qual s'ha d'afegir
funcionalitat. De l'altre, l'arquitectura d'aquest programari és modular i
preveu l'extensió mitjançant un mecanisme estandaritzat que permet una evolució
semi-independent dels nous mòduls, de tal manera que en alguns aspectes
s'assemblen bastant a un producte nou. En particular, els nous mòduls tenen el
seu repositori propi (que no és una còpia del repositori del producte original),
i les entregues estan desvinculades de les del producte marc.

.. admonition:: Exemple: Open Data Barcelona

   El `portal de dades obertes de l'Ajuntament`_ està basat en el programari de
   portal dades de codi obert CKAN_. Aquest producte és `fàcilment extensible`_
   mitjançant *plugins* o extensions i durant el desenvolupament del nou portal
   va ser necessari tant modificar una extensió ja existent (això es
   correspondria amb l':ref:`escenari Adaptació`) com crear-ne de noves.

.. _CKAN: https://ckan.org/
.. _`portal de dades obertes de l'Ajuntament`:
   http://opendata-ajuntament.barcelona.cat/
.. _`fàcilment extensible`:
   http://docs.ckan.org/en/latest/extensions/plugin-interfaces.html

.. _escenari-nouproducte:

Escenari :code:`NouProducte`
----------------------------

Quan no es troba cap component o combinació de components que satisfan una
determinada necessitat, s'ha d'encarregar la implementació d'un producte nou.
Aquest producte pot basar-se en altres components preexistents, com
*frameworks*, biblioteques, gestors de bases de dades, etc.

.. admonition:: Exemple: Decidim.Barcelona.

   El Decidim_ és una eina de democràcia participativa per ciutats i
   organitzacions. El desenvolupament va estar patrocinat des de l'inici per
   l'Ajuntament de Barcelona, tot i que ara més organitzacions que l'utilitzen
   comencen a aportar-hi recursos. Es basa en el *framework* per desenvolupament
   web `Ruby on Rails`_. Aquest *framework* facilita molt el desenvolupament de noves
   aplicacions web, però aquestes no consisteixen simplement en una integració i
   configuració de components.

   La història del Decidim_ és una mica rocambolesca perquè inicialment es va
   intentar fer una adaptació d'un programari ja existent, el Consul_. Més tard
   va ser necessari fer un *fork* del programari original, i finalment es va
   optar per reescriure de nou l'aplicació (millorant, entre d'altres, la
   modularitat del codi).

.. _Decidim: https://decidim.org/
.. _`Ruby on Rails`: http://rubyonrails.org/
.. _Consul: https://github.com/consul/consul

Escenari :code:`Publicació`
---------------------------

L'Ajuntament de Barcelona és el propietari legal de molt codi que es troba en ús
actualment, però que mai ha estat publicat. Les mesures i recomanacions
específiques d'aquest escenari expliquen les comprovacions addicionals
necessàries per publicar, sota una llicència lliure, un codi que no va ser
inicialment pensat per distribuir lliurement.

Por haver-hi diferents raons que justifiquin la publicació d'un codi, sempre que
compleixi amb certs requisits de qualitat. Una possible situació és que es
vulgui iniciar un nou contracte de desenvolupament per estendre o adaptar
":ref:`en obert <Desenvolupament en obert>`" un component ja existent (això
equivaldria a una combinació del l':ref:`escenari Adaptació` i l':ref:`escenari
Publicació`).

Escenari :code:`Document`
-------------------------

A vegades es vol fer públic un document que s'ha redactat (o que s'ha
encarregat) i que pot no estar directament vinculat amb un sol projecte de
programari. Es pot tractar d'estudis de mercat, treballs de recerca, elements de
disseny gràfic (com per exemple logotips), etc.

Etiquetes per a fases i moments dels projectes
==============================================

A l'hora de categoritzar les mesures i recomanacions també és interessant tenir
en compte en quin moment s'han d'aplicar. Com a regla general, podem considerar
que els projectes tecnològics passen per les següents fases:

- **Concepció**: fase en la que es descobreix una nova necessitat o sorgeix la
  idea del projecte, i que normalment inclou l'elaboració d'un avantprojecte i
  possiblement d'altres estudis previs.
- **Contractació**: redacció dels plecs per a l'adquisició de serveis (de
  desenvolupament o d'una altra naturalesa).
- **Desenvolupament**: creació del codi, documentació i d'altres artefactes,
  incloent l'establiment de la infraestructura necessària per a la construcció
  dels mateixos.
- **Pas a producció**: desplegament del servei, incloent la possible migració de
  dades i processos des d'un o més sistemes previs.
- **Explotació**: fase que s'estén durant tota la vida útil del sistema en
  producció, incloent les tasques d'operació i manteniment.

Tenint en compte tot això, a la Guia es fan servir les següents etiquetes per
assenyalar moments destacats dels projectes:

=====================  =========================================================
Etiqueta               Descripció
=====================  =========================================================
:code:`Avantprojecte`  Mesures a tenir en compte en la redacció del
                       avantprojectes.
:code:`Contractar`     Mesures a tenir en compte en la redacció dels plecs per a
                       la contractació de serveis.
:code:`Dia1`           Mesures a aplicar des del primer dia d'inici de la fase
                       de desenvolupament (veure l'apartat
                       :ref:`treballar-en-obert-dia-1`).
:code:`Release`        Mesures a tenir en compte en el moment que es fa pública
                       una nova versió del producte.
=====================  =========================================================
