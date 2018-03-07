********************
Gestió de components
********************

Cerca i selecció de components de codi obert
============================================

.. mes:: Buscar un projecte o component existent que resolgui el problema, potser parcialment
   :tags: Avantprojecte

   A no ser que la nostra necessitat sigui molt especialitzada, és probable que
   ja existeixi una solució lliure (o combinació de solucions) que resolgui el
   problema, com a mínim en part. A més de fer servir dels motors de cerca
   habituals, convé buscar directament a llocs com:
   
   - `GitHub <https://github.com/>`_
   - `Freshcode.club` <https://freshcode.club/>`_
   - `OpenHub <https://openhub.net/>`_
   - `Repositori de solucions de la iniciativa Joinup de la UE
     <https://joinup.ec.europa.eu/solutions>`_
   - `Cercador de solucions del Centro de Transferencia de Tecnología
     <https://administracionelectronica.gob.es/ctt/buscadorSoluciones.htm>`_
   
   Depenent de la plataforma o arquitectura tecnològica amb la que es treballi,
   també cal cercar en repositoris especialitzats, tals com:
   
   - Repositori de Drupal
   - Repositori de CKAN
   
   Cal tenir en compte que els projectes de codi obert ofereixen més
   possibilitats de transformació i adaptació a les nostres necessitats que les
   aplicacions tradicionals.
   
   Conèixer si un projecte s'adequa a les nostres necessitats i compleix amb els
   mínims exigibles a nivell tècnic, legal i social pot resultar costós. Però
   els beneficis de trobar un projecte existent al que sumar-se, enlloc
   d'inventar novament la roda (i evitar l'anomenat **síndrome "Not invented
   here, NIH"**) poden ser extraordinaris, tant a curt com a llarg termini:
   
   - Pot ser que d'entrada moltes de les funcionalitats que necessitem ja
     estiguin implementades, i puguem construir molt ràpidament prototips i
     proves de concepte.
   - Podem beneficiar-nos de l'experiència adquirida per altres usuaris que ja
     han intentat implantar un sistema semblant al que volem, potser descobrint
     oportunitats que no havíem pensat.
   - Podem compartir la despesa de construir una eina complexa amb d'altres
     usuaris i entitats. Això inclou potencials futures funcionalitats i
     ampliacions, que poden interessar també a d'altres usuaris.
   - Si el producte té una base d'usuaris suficients, obtenim una eina que
     evoluciona en el temps, millorant amb les aportacions d'altres parts,
     adaptant-se a futurs canvis tecnològics, incorporant noves funcionalitats
     nostres o de tercers. Amb molt poca despesa en manteniment obtenim
     sostenibilitat a llarg plaç i una reducció del perill de crear **deute
     tecnològic**.
   
.. mes:: Omplir una graella comparativa dels diferents components a avaluar per cobrir una necessitat
   :tags: Avantprojecte; Integració; Adaptació; Plugin; NouProducte
   
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
   
.. sub:: Afavorir components amb els que l'IMI ja ha adquirit familiaritat
   :tags: Avantprojecte; Integració; Adaptació; Plugin; NouProducte
   
   Quan necessitem adaptar un component de codi obert ja existent, conèixer per
   endavant el projecte i la comunitat que el sustenta presenta molts
   avantatges:
   
   - Pot ser que l'IMI tingui ja identificades persones clau dins la comunitat.
   - Es pot fer una estimació més realista del cost en temps i en diners de les
     modificacions que es pretén fer, i de les possibilitats que siguin
     integrades al producte original.
   
.. sub:: Afavorir components per als que existeixin empreses que ofereixin suport comercial
   :tags: Avantprojecte; Integració; Adaptació; Plugin; NouProducte
   
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
   
.. sub:: Avaluar l'activitat pública del projecte
   :tags: Avantprojecte; Integració; Adaptació; Plugin; NouProducte
   
   - Mirar primer de tot l'activitat al *bug tracker*
   - Mesurar la diversitat de *commits*, no la quantitat
   - Avaluar la diversitat d'organitzacions que hi participen
   - Avaluar el to i utilitat dels fòrums de discussió
   - Avaluar la comunicació pública del projecte (web, notícies, entregues)
   
.. sub:: Avaluar la qualitat del codi
   :tags: Avantprojecte; Integració; Adaptació; Plugin; NouProducte
   
   El fet que tant el codi com les eines de gestió de projectes (*bug-trackers*,
   llistes de correu, fòrums) siguin públiques fa que sobre els projectes de
   programari lliure sigui possible extreure algunes mètriques objectives molt
   difícils d'aconseguir en el cas de programari privatiu.
   
   
.. mes:: Considerar totes les possibilitats i totes les implicacions abans d'iniciar un *"social fork"*
   :tags: Avantprojecte; Adaptació; NouProducte
   
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
   
.. rec:: Finançar trobades i *hackatons* relacionades amb el component a utilitzar
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
