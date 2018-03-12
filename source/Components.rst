********************
Gestió de components
********************

Cerca i selecció de components de codi obert
============================================

A no ser que la nostra necessitat sigui molt especialitzada, és probable que ja
existeixi una solució lliure (o combinació de solucions) que resolgui el
problema, com a mínim en part.

Cal tenir en compte que els projectes de codi obert ofereixen més possibilitats
de transformació i adaptació a les nostres necessitats que les aplicacions
tradicionals.

Conèixer si un projecte s'adequa a les nostres necessitats i compleix amb els
mínims exigibles a nivell tècnic, legal i social pot resultar costós. Però els
beneficis de trobar un projecte existent al que sumar-se, enlloc d'inventar
novament la roda (i evitar l'anomenat **síndrome "Not invented here, NIH"**)
poden ser extraordinaris, tant a curt com a llarg termini:

- Pot ser que d'entrada moltes de les funcionalitats que necessitem ja estiguin
  implementades, i puguem construir molt ràpidament prototips i proves de
  concepte.
- Podem beneficiar-nos de l'experiència adquirida per altres usuaris que ja han
  intentat implantar un sistema semblant al que volem, potser descobrint
  oportunitats que no havíem pensat.
- Podem compartir la despesa de construir una eina complexa amb d'altres usuaris
  i entitats. Això inclou potencials futures funcionalitats i ampliacions, que
  poden interessar també a d'altres usuaris.
- Si el producte té una base d'usuaris suficients, obtenim una eina que
  evoluciona en el temps, millorant amb les aportacions d'altres parts,
  adaptant-se a futurs canvis tecnològics, incorporant noves funcionalitats
  nostres o de tercers. Amb molt poca despesa en manteniment obtenim
  sostenibilitat a llarg plaç i una reducció del perill de crear **deute
  tecnològic**.

.. mes:: Buscar un projecte o component existent que resolgui el problema, potser parcialment
   :tags: Avantprojecte; Integració; Adaptació; Plugin; NouProducte

   A més de fer servir dels motors de cerca habituals, convé buscar directament
   a llocs com:
   
   - `GitHub <https://github.com/>`_
   - `Freshcode.club <https://freshcode.club/>`_
   - `OpenHub <https://openhub.net/>`_
   - `Repositori de solucions de la iniciativa Joinup de la UE
     <https://joinup.ec.europa.eu/solutions>`_
   - `Cercador de solucions del Centro de Transferencia de Tecnología
     <https://administracionelectronica.gob.es/ctt/buscadorSoluciones.htm>`_
   
   Depenent de la plataforma o arquitectura tecnològica amb la que es treballi,
   també cal cercar en repositoris especialitzats, tals com:
   
   - Repositori de Drupal
   - Repositori de CKAN
      
.. mes:: Omplir una graella comparativa dels diferents components a avaluar per cobrir una necessitat
   :tags: Avantprojecte; Integració; Adaptació; Plugin; NouProducte
   :links: S_58B, S_453; S_223; S_5BD; S_160; S_0F3; S_1C4; S_24A; S_2F1

   Això pot haver-se de repetir per cadascun dels components d'un sistema.

   Exemple de graella:
   
   +-----------------+-----------------+-----------------+-----------------+
   | Element         | Component A     | Component B     | Component C     |
   +=================+=================+=================+=================+
   | Nom             |                 |                 |                 |
   +-----------------+-----------------+-----------------+-----------------+
   | Llicència (i    |                 |                 |                 |
   | condicions que  |                 |                 |                 |
   | ens poden       |                 |                 |                 |
   | afectar)        |                 |                 |                 |
   +-----------------+-----------------+-----------------+-----------------+
   | % de la         |                 |                 |                 |
   | funcionalitat   |                 |                 |                 |
   | que necessitem  |                 |                 |                 |
   +-----------------+-----------------+-----------------+-----------------+
   | Projectes IMI   |                 |                 |                 |
   | que ja          |                 |                 |                 |
   | l'utilitzen i   |                 |                 |                 |
   | persones        |                 |                 |                 |
   | familiaritzades |                 |                 |                 |
   +-----------------+-----------------+-----------------+-----------------+
   | Suport          |                 |                 |                 |
   | comercial       |                 |                 |                 |
   +-----------------+-----------------+-----------------+-----------------+
   | Altres          |                 |                 |                 |
   | organitzacions  |                 |                 |                 |
   | grans que       |                 |                 |                 |
   | l'utilitzen     |                 |                 |                 |
   +-----------------+-----------------+-----------------+-----------------+
   | Activitat al    |                 |                 |                 |
   | *bug tracker*   |                 |                 |                 |
   +-----------------+-----------------+-----------------+-----------------+
   | Diversitat de   |                 |                 |                 |
   | *commits*       |                 |                 |                 |
   +-----------------+-----------------+-----------------+-----------------+
   | Diversitat      |                 |                 |                 |
   | d'organitzacion |                 |                 |                 |
   | s               |                 |                 |                 |
   +-----------------+-----------------+-----------------+-----------------+
   | To i utilitat   |                 |                 |                 |
   | dels fòrums de  |                 |                 |                 |
   | discussió       |                 |                 |                 |
   +-----------------+-----------------+-----------------+-----------------+
   | Comunicació     |                 |                 |                 |
   | pública del     |                 |                 |                 |
   | projecte        |                 |                 |                 |
   +-----------------+-----------------+-----------------+-----------------+
   | Mètriques de    |                 |                 |                 |
   | qualitat del    |                 |                 |                 |
   | codi            |                 |                 |                 |
   +-----------------+-----------------+-----------------+-----------------+
   | Altres          |                 |                 |                 |
   | consideracions  |                 |                 |                 |
   +-----------------+-----------------+-----------------+-----------------+

   Altres coses que es poden tenir en compte, a més de les sub-mesures de més
   avall:
   
   - Facilitat d'adaptació i evolució dels diferents components
   - Cost immediat i cost a llarg termini, incloent els costos de sortida
   - Existència d'una comunitat informal o xarxa de suport local i global
   - Solucions innovadores (i valor que això aporta)
   - Impacte sobre la privacitat i la sobirania de dades

.. _mesura_S_58B:

.. sub:: Triar components amb una llicència aprovada per la OSI o per la FSF
   :id: S_58B
   :tags: Integració; Adaptació; Plugin

   Els dos conjunts de llicències vàlides son gairebé idèntics:

   - `<https://opensource.org/licenses>`_
   - `<https://www.gnu.org/licenses/license-list.en.html>`_

.. sub:: Afavorir components amb una major diversitat i pes dels contribuïdors
   :tags: Avantprojecte; Integració; Adaptació; Plugin; NouProducte

   Aquí entenem contribucions en un sentit ampli: *commits* al repositori de
   codi, *bug reports*, traduccions, etc.

   És més important la diversitat (persones i entitats diferents que participen)
   que la quantitat de les contribucions (per exemple, nombre de *commits* per
   mes).

   Si el component presenta contribucions per part d'organitzacions importants
   (empreses d'una certa mida, universitats, institucions), és més probable que
   encara que algun dels contribuïdors falli el projecte continuï. Però també
   pot ser molt bona senyal que moltes persones a títol individual facin
   contribucions i que es tinguin en compte.

.. sub:: Afavorir components amb activitat recent

   Primer de tot cal mirar l'activitat al *bug tracker*, observant:

   - Quantitat de notificacions de deficiències. No ens ha d'espantar que hi
     hagi moltes notificacions obertes i no resoltes, el nombre d'incidències
     tendeix a créixer linealment amb el nombre d'usuaris, però en canvi el
     nombre de desenvolupadors acostuma a créixer més lentament.
   - Que els desenvolupadors estiguin responent a les incidències. Insistim: si
     el nombre d'usuaris és gran, hi haurà sempre moltes incidències obertes,
     però sí és important observar que els desenvolupadors participen
     habitualment al *bug tracker*, que no l'hagin abandonat.

   Després cal mirar l'activitat pública del projecte, tenint en compte:

   - Antiguitat de les darreres *releases* públiques, notícies publicades en
     forma de blog o similar.
   - El to, la utilitat i la diversitat de participants en el fòrums de
     discussió i canals de comunicació públics del projecte.

.. sub:: Afavorir components amb una documentació complerta i al dia

   Que la documentació estigui en un repositori públic i que hi hagi una bona
   diversitat de persones que hi contribueixin també és un molt bon senyal.

.. sub:: Afavorir components per als quals existeixi suport comercial
   :tags: Avantprojecte; Integració; Adaptació; Plugin; NouProducte

   En productes amb llicència lliure sempre serà possible contractar algú per
   tal que els modifiqui, mantingui o resolgui problemes. No obstant això,
   obtenim una major garantia d'èxit si ja existeixen empreses o persones que
   ofereixen suport professional sobre el component en qüestió, i que per tant
   cal assumir que el coneixen bé.

   És millor que hi hagi diferents empreses oferint serveis comercials sobre el
   producte que no només una, ja que en aquest segon cas incorreríem en una
   dependència més forta cap a aquests empresa. És habitual un model de negoci
   en el que la mateixa empresa que desenvolupa el producte (potser sense gaire
   suport comunitari extern) ofereix també suport comercial sobre el mateix. No
   s'ha de descartar de per sí, però és millor que el suport professional
   es trobi diversificat.
   
   L'existència d'empreses que ja d'entrada ofereixen serveis professionals
   sobre un producte pot facilitar també realitzar una avaluació temptativa del
   cost que suposarà adaptar-lo o mantenir-lo.

.. sub:: Afavorir components que facilitin l'accés a la informació sobre el desenvolupament i la instal·lació
   :tags: Avantprojecte; Integració; Adaptació; Plugin; NouProducte

   La transparència és un pilar bàsic dels projectes de programari lliure, sense
   el qual és molt difícil que tota la resta funcioni bé.

   Que un component ofereixi instruccions detallades i precises do com
   instal·lar-lo facilita que es pugui fer una avaluació tècnica independent del
   mateix.

.. sub:: Afavorir components amb bones mètriques de qualitat del codi
   :tags: Avantprojecte; Integració; Adaptació; Plugin; NouProducte
   
   El fet que tant el codi com les eines de gestió de projectes (*bug-trackers*,
   llistes de correu, fòrums) siguin públiques fa que sobre els projectes de
   programari lliure sigui possible extreure algunes mètriques objectives molt
   difícils d'aconseguir en el cas de programari privatiu.

   Algunes mètriques que es poden obtenir per certs projectes:

   - Quantitat de comentaris, a `OpenHub <https://openhub.net/>`_.
   - Percentatge de codi cobert pels casos de prova.
   
.. sub:: Afavorir components amb els que l'IMI ja ha adquirit familiaritat
   :tags: Avantprojecte; Integració; Adaptació; Plugin; NouProducte
   
   Quan necessitem adaptar un component de codi obert ja existent, conèixer per
   endavant el projecte i la comunitat que el sustenta presenta molts
   avantatges:
   
   - Pot ser que l'IMI tingui ja identificades persones clau dins la comunitat.
   - Es pot fer una estimació més realista del cost en temps i en diners de les
     modificacions que es pretén fer, i de les possibilitats que siguin
     integrades al producte original.
   
.. sub:: Afavorir components amb una llicència compatible amb la GPL
   :tags: Integració; Adaptació; Plugin

   Aquesta informació la dona la Free Software Foundation al seu llistat de
   llicències: `<https://www.gnu.org/licenses/license-list.en.html>`_.

   Les llicències de la família de la GPL son unes de les més comunes. Per
   evitar conflictes de llicència amb altres components que possiblement
   necessitarem, convé que tots els nostres components siguin compatibles amb
   GPL.

.. sub:: Afavorir components que formin part de la distribució estable de Debian
   :tags: Avantprojecte; Integració; Adaptació; Plugin; NouProducte
   
   Tot component de la solució que estigui inclòs en la distribució Estable de
   Debian en el moment de dissenyar el projecte, o que es pugui executar sobre
   Debian Estable sense necessitat d'adaptació, i que sigui multi-arquitectura,
   es considera un component durador i fiable.
   
   Si més no, afavorir components que puguin executar-se, en la seva versió
   estàndard descarregable a la web del projecte, sobre plataformes lliures,
   preferiblement GNU/Linux i sense que existeixin restriccions en quant a:
   
   - Requerir una distribució particular de GNU/Linux (per exemple un programari
     que només s'executi en entorns CentOS i no sobre Debian).
   - Versions massa específiques dels elements principals de la plataforma,
     sobretot si es tracta de versions massa antigues o fora del seu període de
     manteniment estàndard (per exemple un programari que requereixi un kernel
     de Linux en una versió 3.*, o unes llibreries bàsiques del sistema
     desfasades).
   - Requerir una arquitectura de hardware específica (per exemple, solucions
     que només s'executin en màquines Intel).
   
.. mes:: Considerar totes les possibilitats i totes les implicacions abans d'iniciar un fork social
   :tags: Avantprojecte; Adaptació; NouProducte

   Quan es disposa d'un codi que ha estat publicat amb llicència lliure però es
   necessita evolucionar el producte en una direcció incompatible amb els plans
   de qui governa el projecte, pot ser necessari fer un *fork* (en el sentit
   fort del terme, o "*fork* social").

   Fer un *fork* té molts inconvenients, i per tant ha de ser un últim recurs.
   D'una banda, dificulta molt compartir codi amb el producte original a partir
   del moment del *fork*. I potser més significatiu, suposa dividir la comunitat
   original i obligar a cada desenvolupador a decidir quin projecte prioritza.
   
Gestió de dependències
======================
   
.. mes:: Dur un registre exhaustiu de tots els paquets de programari utilitzats, que han de ser lliures
   :tags: Contractar; Integració; Adaptació; Plugin; NouProducte; Publicació
   
   En cas de contracte, posar-ho als plecs i afegir que l'IMI té l'última
   paraula sobre la inclusió d'una dependència.

   .. admonition:: Exemple de clàusula: **Gestió de les dependències de programari**.

      L’adjudicatari durà un registre exhaustiu de tots els paquets de
      programari utilitzats en la solució, que han d’estar distribuïts sota una
      llicència de programari acceptada per la Open Source Initiative (OSI,
      https://opensource.org/licenses) o bé pel projecte GNU
      (https://www.gnu.org/licenses/license-list.en.html). Com a requisit
      addicional, la llicència de tots els paquets utilitzats no ha de produir
      problemes d’incompatibilitat amb la llicència principal del producte, la
      EUPL-1.2. L’Ajuntament de Barcelona es reserva la potestat d’exigir que es
      retiri una dependència de programari del producte si considera que pot
      constituir un risc legal i l’adjudicatari està obligat a substituir el
      paquet per un altre, o bé cobrir la funcionalitat amb desenvolupament
      propi.
   
.. rec:: Utilitzar un programari de monitorització de llicències
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació
   
   Com per exemple:

   - https://www.fossology.org/
   - http://creadur.apache.org/
   
.. mes:: No copiar dependències externes al repositori si no és per una causa excepcional
   :tags: Plugin; NouProducte; Publicació
   
   A vegades es decideix copiar un sub-component que es troba disponible en un
   repositori propi al repositori del component que estem construint (sigui en
   forma de codi font, binari o de *bytecode*). Es diu que aquesta dependència
   es troba *bundled*. A vegades es busca amb això un desplegament o un cicle de
   desenvolupament més senzill, però es considera una mala pràctica ja que:
   
   - Els canvis i actualitzacions en el sub-component embruten la història de
     canvis del component principal.
   - És més difícil donar compte correctament de la autoria i llicenciament de
     cada part del codi.
   
   Poden donar-se circumstàncies excepcionals que justifiquin no obeir aquesta
   mesura.
   
.. mes:: Buscar les dependències inadequades i trobar substituts amb llicència lliure
   :tags: Publicació
   
   S'han d'eliminar els components:
   
   - Amb llicència propietària.
   - Propietat de l'Ajuntament de Barcelona, però que de moment no es puguin
     obrir.
   - Que presentin algun tipus d'incompatibilitat de llicència amb altres
     components del producte a obrir.
   - Que no puguin ser instal·lats en un sistema operatiu lliure.
   
.. rec:: Finançar una auditoria de seguretat del component a utilitzar
   :tags: Integració; Adaptació; Plugin
   
.. rec:: Finançar trobades i hackatons relacionades amb el component a utilitzar
   :tags: Integració; Adaptació; Plugin
   
.. rec:: Integrar personal de l'IMI en les tasques de desenvolupament
   :tags: Contractar; Integració; Adaptació; Plugin; NouProducte
   
   Es pot establir per contracte i pot ser qualsevol tasca relacionada amb
   el desenvolupament:
   
   - Escriptura de codi
   - Escriptura de documentació
   - Revisions de codi
   - Creació, execució i anàlisi de bateries de proves
   
   L'objectiu és tenir personal propi familiaritzat amb un programari que es
   seguirà utilitzant en el futur, un cop s'acabi el contracte de
   desenvolupament actual. Es tracta d'aprofundir en la sobirania i evitar el
   màxim la dependència de proveïdors únics.
   
Substitució de serveis privatius habituals
==========================================

.. mes:: Utilitzar Piwik (si es necessita una eina d'analítica web)
   :tags: Contractar; Integració; Adaptació; Plugin; NouProducte; Publicació
      
   No utilitzar Google Analytics. Utilitzar eines com Piwik en el seu lloc.
   
.. mes:: Publicar apps Android a F-Droid (Si un dels productes és una app Android)
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació
   
   En el cas d'apps per la plataforma Android, publicar les apps al repositori
   lliure F-Droid, a més del repositori Google Play o aquells que més gent
   utilitzi.
   
.. mes:: Utilitzar OpenStreetMap (si es necessita presentar informació cartogràfica present en aquesta eina)
   :tags: Contractar; Integració; Adaptació; Plugin; NouProducte; Publicació
   
   No utilitzar Google Maps.
