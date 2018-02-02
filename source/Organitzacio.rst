***************************
Organització d'aquesta guia
***************************

Aquesta guia consta d'un seguit de directrius que hem dividit en:

- **Mesures** que s'han de procurar complir a tots els projectes on tingui
  sentit la seva aplicació.
- **Recomanacions** que fem per si poden ser d'utilitat en situacions
  determinades.

En el cas de les mesures qui gestiona el projecte s'ha d'encarregar de validar
si la mesura es compleix o no. En el cas de les recomanacions, el primer que cal
és pendre una decisió: aplicar-la o no. Que l'aplicació de les recomanacions
sigui opcional no les fa menys importants que les mesures.

Algunes mesures son impossibles d'aplicar en determinats projectes, i en aquest
cas s'intenta donar algunes **alternatives** (directrius que es troben
etiquetades d'aquesta manera al llarg del document). Cada mesura i les seves
potencials alternatives es troben mútuament enllaçades.

Cada mesura, recomanació o alternativa consta de:

- Un identificador únic per a tot el document.
- Un llistat d'etiquetes.

Les etiquetes ajuden a restringir en quins moments i en quins tipus de projecte
son importants cada mesura i cada recomanació. Poden servir, per exemple, per
què la direcció del projecte pugui generar un *checklist* de coses a comprovar.

La següents seccions d'aquest capítol expliquen els tipus d'etiquetes que es fan
servir al llarg de la guia.

La resta de capítols d'aquesta guia organitzen les mesures, recomanacions i
alternatives en àrees temàtiques i donen el context necessari per entendre la
rellevància de cada mesura.

Escenaris d'ús
==============

En aquesta secció es defineixen diferents situacions que es poden produir en els
projectes tecnològics en relació als components de programari lliure i de codi
obert en els que es basen, a les que anomenem **escenaris**. Aquests escenaris
determinen després quines directrius concerneixen a cada projecte.

Cada **projecte** defineix un sistema d'informació, i cada sistema d'informació
consta d'una determinada quantitat de **components** de programari. Uns
components es distingeixen dels altres perquè cada component té el seu propi
**repositori** de codi font. (Ocasionalment trobem components complexes que, per
raons pràctiques, tenen el seu codi repartit en diferents repositoris que es
versionen i distribueixen coordinadament). Els diferents components d'un
determinat sistema poden executar-se tots en una mateixa màquina, o bé poden
trobar-se distribuïts en diferents màquines. També poden executar-se com a part
del mateix procés o en processos diversos.

Tots els escenaris, a excepció dels escenaris A i F, fan referència a components
de programari. Per tant, en un mateix projecte poden concórrer diferents
escenaris si components diferents es troben afectats de diferent manera.

Els escenaris son els següents:

.. |escenari-A| replace:: Integrar components existents
.. |escenari-B| replace:: Modificar un component extern
.. |escenari-C| replace:: Estendre una plataforma amb components endollables
.. |escenari-D| replace:: Crear un component nou
.. |escenari-E| replace:: Publicar codi d'un component propi ja existent
.. |escenari-F| replace:: Publicar documentació no vinculada a un únic projecte

.. role:: raw-html(raw)
   :format: html

========  ======================================================================
   A      :raw-html:`<strong>`\ |escenari-A|\ :raw-html:`</strong>`.
          Es necessita implantar un nou sistema que es pot construir amb
          components ja existents.
   B      :raw-html:`<strong>`\ |escenari-B|\ :raw-html:`</strong>`.
          Cal afegir funcionalitat a un component ja disponible, o bé
          millorar-lo solucionant deficiències, afegint traduccions, etc.
   C      :raw-html:`<strong>`\ |escenari-C|\ :raw-html:`</strong>`.
          Es requereix crear nous components que s'integrin en una plataforma
          o *framework* ja disponible i que facilita aquesta tasca.
   D      :raw-html:`<strong>`\ |escenari-D|\ :raw-html:`</strong>`.
          Es necessita crear una solució nova des de zero.
   E      :raw-html:`<strong>`\ |escenari-E|\ :raw-html:`</strong>`.
          Es disposa d'un codi propi desenvolupat sota contractes anteriors i
          que mai ha estat publicat, i es vol alliberar en un repositori públic.
   F      :raw-html:`<strong>`\ |escenari-F|\ :raw-html:`</strong>`.
          Es disposa d'estudis, treballs de recerca, elements de disseny gràfic
          (com per exemple logotips) que no pertanyen a cap projecte en concret
          i que es volen alliberar en un repositori públic.
========  ======================================================================

Deixem fora de l'anàlisi contribucions a projectes que no impliquen una
modificació del codi d'un component, o la creació d'un repositori, com poden ser
contribucions a la documentació o facilitació de l'adopció de certes eines per
part de tercers.

Els escenaris A-D poden opcionalment requerir una **migració**, en cas que ens
trobem en la situació d'implantar un sistema que substitueix, en part o
totalment, les funcions d'un sistema anterior.

Escenari A: |escenari-A|
------------------------

Aquest escenari pot comportar la creació d'un o més repositoris propis, però no
per guardar-hi el codi de cap aplicació pròpiament, sinó per:

- Vincular-hi eines de gestió de projectes tals com gestors d'incidències
- Guardar o enllaçar documentació associada amb l'ús i operació del sistema
- Guardar fitxers de configuració i scripts necessaris per al desplegament del
  sistema
- Guardar fitxers de configuració i scripts necessaris per executar entorns de
  prova i d'integració continua, incloent virtualització i *containerització*
- Guardar elements de disseny i personalització del sistema
- Guardar instruccions d'instal·lació i ús del sistema
- Guardar tests d'integració dels diferents components

En quant als elements de personalització, destaquem la **traducció** dels
literals que es mostren a l'usuari i d'altres aspectes de la localització i
internacionalització (l10n, i18n). Contemplem dues possibilitats:

#. Es compleixen les següents dos condicions:

   - El programari a traduir està dissenyat per incorporar traduccions de la
     interfície
   - Les traduccions a realitzar poden ser d'utilitat general per a d'altres
     potencials usuaris de l'eina

   En aquest cas s'intentarà contribuir aquestes traduccions al projecte
   original i per tant ens trobaríem en l'escenari B.
#. Alguna de les dues condicions anteriors no es compleix i emmagatzemem els
   fitxers necessaris per efectuar la traducció a un repositori propi.

..

    **Exemple.** Un exemple hipotètic seria un portal web construït utilitzant
    un gestor de continguts com Wordpress, amb una base de dades MariaDB.

    Es tracta de components estàndard de programari lliure, però per
    facilitar-ne la gestió pot convenir guardar en un repositori elements de
    personalització com plantilles, fitxers CSS, imatges, llistat d'extensions de
    Wordpress a carregar, així com imatges de Docker que incloguin tots els
    elements necessaris per al desplegament.

Escenari B: |escenari-B|
------------------------

Aquest escenari pot comportar la creació d'un o més repositoris propis amb els
mateixos continguts descrits per a l'escenari A. En canvi, el tret distintiu
d'aquest escenari és el patrocini per part de l'Ajuntament de Barcelona del
desenvolupament d'alguna contribució significativa a un producte de programari
lliure que pugui ser potencialment incorporada al producte original (encara que
aquesta integració no es realitzi mentre dura el propi desenvolupament).
Aquestes contribucions han de materialitzar-se en un conjunt de *commits* en un
repositori que estigui vinculat d'alguna manera al repositori del producte
original.

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
plantejar una contribució com a tal i ens trobaríem a l'escenari A.

..

    **Exemple.** Bústia ètica de l'Ajuntament de Barcelona.

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

Escenari C: |escenari-C|
------------------------

Es tracta d'un escenari intermig entre la integració de funcionalitats noves a
un producte ja existent (escenari B) i el desenvolupament d'un nou producte
(escenari D).

    **Exemple.** Open Data Barcelona.

Escenari D: |escenari-D|
------------------------

    **Exemple.** Decidim.Barcelona.

Dos sub-escenaris:

#. Projectes emblemàtics
#. Projectes que es publiquen per raons pràctiques

Entre les raons pràctiques trobem:

- Tenir tot el codi concentrat en un lloc
- Garantir unes bones pràctiques i així una certa qualitat

Escenari E: |escenari-E|
------------------------

Hi ha una situació particular en que l'escenari E i el B es combinen per a un
mateix component: es publica el codi del component amb l'expectativa
d'estendre'l "en obert".

Escenari F: |escenari-F|
------------------------

Fases dels projectes
====================

En la organització de la guia s'ha considerat que els projectes poden passar per
les següents fases:

- **Concepció (I)**. Fase en la que es descobreix una nova necessitat o sorgeix
  la idea del projecte. Normalment inclou l'elaboració d'un avantprojecte i
  pot incloure d'altres estudis previs.
- **Contractació (C)**. Redacció dels plecs per a l'adquisició de serveis de
  desenvolupament.
- **Desenvolupament (D)**. Establiment de la infraestructura necessària per a la
  construcció dels components de software necessaris i tasques d'acompanyament
  durant tot el procés de desenvolupament.
- **Pas a producció (P)**. Desplegament del servei, incloent la possible
  migració de dades i processos des d'un o més sistemes previs.
- **Explotació (E)**: Fase que s'estén durant tota la vida útil del sistema en
  producció, incloent les tasques d'operació i manteniment.
