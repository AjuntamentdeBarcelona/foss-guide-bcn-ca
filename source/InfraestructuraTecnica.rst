***********************
Infraestructura tècnica
***********************

Control de versions i web de desenvolupament
============================================

.. mes:: Establir la web de desenvolupament a l'espai GitHub de l'Ajuntament
   :tags: Dia1; Adaptació; Plugin; NouProducte; Publicació

   A la web de desenvolupament hi ha d'haver el repositori principal de
   codi, utilitzant Git com a eina de control de versions. Es crearà un
   projecte ``https://github.com/AjuntamentDeBarcelona/NOM-DEL-PROJECTE``
   on es publicarà el codi. Que sigui el repositori principal vol dir que
   és el sistema de control de versions vinculat al gestor d'incidències (i
   possiblement a d'altres eines de desenvolupament com el sistema
   d'integració continua).
   
   Això no vol dir que no puguin haver-hi rèpliques (miralls) del
   repositori o parts del mateix en altres llocs (espais GitHub d'altres
   organitzacions, de desenvolupadors particulars, la pàgina web de les
   empreses adjudicatàries de contractes públics, etc).
   
   El nom del projecte a GitHub es recomana que sigui tot en minúscules i
   amb les paraules de què està format separades per guions. Per exemple:
   https://github.com/AjuntamentdeBarcelona/decidim-barcelona.
   
   El codi ha d'estar present en aquest lloc des de l'inici del projecte,
   sense esperar a que hi hagi *releases* públiques. El repositori ha de
   contenir com a mínim les següents branques:
   
   -  Una branca ``master``
   
   La raó de tenir les eines de desenvolupament integrades amb un
   repositori propi evita que un futur es vegin amenaçats actius importants
   del projecte com son l'historial d'incidències.
   
   Hi ha moltes alternatives viables i raonables a GitHub, i fins i tot
   algunes alternatives viables a Git com a programari de control de
   versions, però GitHub ofereix prous avantatges com per què sigui la
   opció per defecte:
   
   -  És la plataforma més utilitzada per projectes de codi obert, dóna
      molta visibilitat.
   -  La majoria de desenvolupadors la coneixen i no han d'aprendre noves
      eines i procediments ad-hoc per al projecte.
   -  Ofereix una bona integració amb la resta d'infraestructura tècnica i
      social d'un projecte: gestió d'incidències, integració continua,
      canals de comunicació entre desenvolupadors, etc.
   -  Permet també guardar i mostrar (part de) la documentació d'un
      projecte, que pot ser una wiki. La presentació de la informació és
      suficientment agradable com per permetre aplaçar la construcció d'una
      web orientada a usuaris del projecte.
   
   **Inconvenient**. Tot i ser un servei gratuït per un gran ventall de
   possibles usos, no tot el codi de la infraestructura que hi ha darrera
   de GitHub és lliure, i en darrera instància s'està establint una
   dependència amb una empresa que no sabem com evolucionarà en el futur.
   Més endavant poden aparèixer opcions que facin reconsiderar aquesta
   recomanació de fer servir GitHub com a opció per defecte.

.. alt:: Establir el web de desenvolupament a un lloc públic diferent del GiHub de l'Ajuntament
   :tags: Adaptació; Plugin; NouProducte; Publicació

   Pot haver-hi motius que facin recomanable tenir el repositori principal
   (el vinculat al gestor d'incidències) en llocs com:
   
   -  L'espai GitHub d'una altra organització
   -  BitBucket o d'altres plataformes similars
   -  Un portal Gitlab d'alguna organització que participi en el
      desenvolupament del projecte (o en un futur un portal Gitlab de
      l'Ajuntament de Barcelona)
   
   Alguns d'aquests motius poden ser:
   
   -  És un projecte on intervenen més participants del sector públic, i es
      crea una consorci o organització ad-hoc.
   -  L'empresa que desenvolupa té un fort lideratge sobre el projecte, més
      gran que el que pugui tenir l'Ajuntament, i vol tenir la
      infraestructura bàsica sota el seu control.
   
   Si s'opta per aquesta alternativa, s'ha de tenir en compte que:
   
   -  No podem renunciar a Git com a sistema de control de versions: és
      l'eina molt majoritàriament utilitzada avui en dia i que tots els
      desenvolupadors coneixen, i facilita unes bones pràctiques de gestió
      de projectes en obert que amb sistemes més antics (com CSV o
      Subversion) resulten molt més farragoses. Si determinats procediments
      s'han d'executar necessàriament sobre una altra eina, per exemple
      Subversion, la solució és fer el desenvolupament en obert sobre Git,
      i mantenir un mirall Subversion automatitzat utilitzant la comanda
      ``git svn dcommit``, com s'explica per exemple a
      http://www.kerrybuckley.org/2009/10/06/maintaining-a-read-only-svn-mirror-of-a-git-repository/.
   -  En qualsevol cas hi ha d'haver una rèplica actualitzada del
      repositori principal a l'espai GitHub de l'Ajuntament, per donar
      visibilitat a totes les contribucions a projectes de codi obert que
      realitza.
   -  Al fitxer ``README`` contingut (i mostrat) a l'espai GitHub de
      l'Ajuntament, a l'espai GitHub.io i a la resta de llocs amb enllaç al
      codi font, d'indicarà quin és el repositori (o repositoris) principal
      on es porta a terme el desenvolupament.
   -  Siguin on siguin, tant l'eina de gestió d'incidències com el sistema
      d'integració continua han de ser públics i s'han de poder utilitzar
      per part de tothom sense pagar subscripcions a cap servei.
   -  Tot el codi font del projecte ha de ser descarregable per qualsevol
      persona en tot moment. GitHub facilita això proveint de botons per
      descarregar un arxiu ``zip`` o bé mostrant les comandes necessàries
      per clonar el repositori utilitzant Git. Si No es fa servir GitHub
      s'ha d'aconseguir que el lloc públic del repositori faciliti també
      aquestes dues modalitats de descàrrega (arxiu ``zip`` o ``tar.gz`` i
      comanda ``git clone``).

.. mes:: Pujar el codi al repositori principal
   :tags: Dia1; Plugin; NouProducte
   
   Fer descarregable tot el codi font del projecte. De dues maneres:
   
   -  Des del repositori Git principal amb ``git clone``.
   -  En un únic arxiu en format ``zip`` o ``tar.gz``, com a mínim des del
      moment que existeixi una primera *release* pública.
   
.. mes:: Establir com a administrador del repositori principal una persona encarregada de l'IMI
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació; Document

   I, opcionalment, una persona de cada entitat externa que participa en el
   desenvolupament sota contractes amb l'IMI.
   
.. mes:: Establir permisos de *commit* al repositori principal a tots els desenvolupadors persones de l'equip
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació; Document
   
   Això inclou tant persones internes com subcontractades. A més, fer pública la
   llista actual de *commiters* en un fitxer a l'arrel del repositori anomenat
   ``MAINTAINERS``. Ha de contenir el nom i adreça de correu electrònic de cada
   persona.
   
.. rec:: Donar permisos de *commit* al repositori principal a desenvolupadors externs confiables
   :tags: Plugin; NouProducte; Publicació
   
   Si una persona porta molt temps fent contribucions de qualitat al projecte, a
   un nivell semblant que les persones contractades per l'Ajuntament, se la pot
   premiar amb un permís per escriure al repositori. Es corre un risc baix amb
   això, perquè el control de versions fa que tot sigui traçable i els canvis
   revertibles.
   
   Se li ha d'aclarir, per aclarir mal entesos, quines seran les regles de
   governança i qui seguirà tenint la darrera paraula a l'hora d'acceptar
   contribucions.
   
.. rec:: Pujar traduccions del fitxer ``README`` al repositori principal
   :tags: NouProducte; Publicació
   
   Si els potencials usuaris del projecte son principalment locals, pot ser
   convenient traduir el contingut del fitxer ``README`` o part del mateix. Això
   es pot fer posant nous fitxers a l'arrel del repositori, amb noms com
   (suposant que el llenguatge de marques utilitzat sigui Markdown, i d'aquí
   l'extensió ``.md``): ``README.ca.md`` o ``README.es.md``. En aquest cas convé
   enllaçar totes aquestes traduccions entre elles, al principi de cada fitxer.
   Un exemple es pot veure a `https://github.com/tiimgreen/github-cheat-sheet
   <https://github.com/tiimgreen/github-cheat-sheet>`_.
   
.. mes:: Especificar al ``README`` una persona de contacte del projecte
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació; Document
   
   Incloure una adreça de correu electrònic.
   
.. mes:: Utilitzar l'anglès com a llengua per a tot el desenvolupament
   :tags: Integració; Adaptació; Plugin; NouProducte
   
   Han d'estar obligatòriament en anglès:
   
   - Els comentaris que acompanyen el propi codi
   - Qualsevol document referent al disseny i l'arquitectura del producte
   - Tots els comentaris dels *commit* al repositori
   - Totes les entrades al gestor d'incidències i els fils de discussió que se'n
     deriven
   - Els fils de discussió que acompanyen cada petició d'aportació (*pull
     request*)
   - El fitxer ``README`` del repositori principal
   - El fitxer ``INSTALL``
   - El fitxer ``CONTRIBUTING``
   - El fitxer ``CONTRIBUTORS``
   - El fitxer ``LICENSE``
   
   En el cas del gestor d'incidències, si aquest deixa introduir-les a qualsevol
   persona i se n'introdueix alguna en una altra llengua, algú de l'equip s'ha
   d'encarregar de traduir-la, o bé de sol·licitar a l'autor que la tradueixi.
   
.. mes:: No pujar al repositori fitxers binaris ni fitxers producte del procés de *build* (amb excepcions)
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació
   
   Excepcions:
   
   - Petites imatges (logos generals del projecte, etc.)
   
.. mes:: Mantenir la informació de configuració en fitxers separats i en un altre repositori
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació
   
   Això facilita la reutilització del codi. És incorrecte posar la configuració:
   
   - *Hardwired* en el propi codi
   - En fitxers dels que es fa *commit* al mateix repositori que conté el codi.
   
.. mes:: No pujar al repositori informació sensible d'usuaris, de l'Ajuntament o de tercers
   :tags: Contractar; Integració; Adaptació; Plugin; NouProducte; Publicació
   
   Com pugui ser: usuaris i contrasenyes, claus públiques o d'altres credencials
   reals usades en el sistema en producció.

   A les condicions d'execució del contracte, establir penalitzacions si
   s'infringeix aquesta regla.
   
.. mes:: Re-sincronitzar cada setmana la branca de desenvolupament pròpia amb el ``master`` de l'original
   :tags: Adaptació
   
   Per permetre finalment integrar els nostres canvis, i que les nostres
   notificacions de defectes tinguin sentit.
   
Gestor d'incidències
====================
   
.. mes:: Vincular el repositori principal al gestor d'incidències de GitHub
   :tags: Dia1; Adaptació; Plugin; NouProducte; Publicació

   De nou és la opció per defecte, en aquest cas per la seva vinculació
   automàtica amb el repositori de GitHub i perquè compleix els nostres
   requeriments d'accessibilitat i transparència.
   
   S'hauran d'establir des de l'inici algunes categories bàsiques
   d'incidència, que després poden modificar-se segons les necessitats de
   cada projecte: {- TODO: bla -}
   
   S'ha de tenir en compte que el gestor d'incidències no és només
   important per al dia a dia dels desenvolupadors, sinó que molts
   observadors del projecte també el fan servir com a mesura de fins a quin
   punt estan davant d'un projecte seriós.
   
   Té les següents funcions:
   
   -  Notificar els defectes detectats (*bug tracker*) per part tant
      d'usuaris com de desenvolupadors. També fer-ne transparent el
      tractament, evolució i eventual solució. És important que els
      *commit* que resolen un defecte o assenyalin en el seu missatge.
      `GitHub té una sintaxi especial per fer
      això <https://help.github.com/articles/closing-issues-using-keywords/>`__.
   -  Fer seguiment de les tasques pendents. Això permet després vincular
      un o més *commit* amb el tancament d'una tasca. També poder veure a
      qui s'assignen les tasques i com es prioritzen. Opcionalment s'hi
      poden especificar dates estimades de realització. Tot plegat
      contribueix a la transparència i traçabilitat del procés de
      desenvolupament.
   -  Fer seguiment de com es gestionen les contribucions de diferents
      parts, mitjançant el mecanisme de *pull request*. Fins i tot es pot
      obrir el gestor d'incidències a peticions de funcionalitats (*feature
      request*) i es pot utilitzar l'espai de GitHub com a lloc on es
      prioritzen i gestionen de manera pública.
   
   Aquest gestor d'incidències ha d'estar operatiu i públic durant tota la
   vida útil del producte, més enllà de la duració que tinguin els
   contractes amb l'Ajuntament.

.. alt:: Vincular el repositori principal a un gestor d'incidències públic
   :tags: Dia1; Adaptació; Plugin; NouProducte; Publicació
   
   Com a mínim ha de fer les funcions pròpies d'un sistema de notificació i
   seguiment de defectes (*bug tracker*), però pot complir més funcions,
   com s'explica a [Vincular repo a gestor d'incidències de GitHub].
   
   Si es fa servir aquesta alternativa, tenir en compte que:
   
   -  Necessàriament ha de ser públic, en el sentit que:
   
      -  Tothom ha de poder registrar-se com usuari del sistema sense pagar
         cap subscripció, i així participar en el desenvolupament.
      -  Tothom ha de poder visualitzar les incidències i fer-ne un
         seguiment, sense necessitat de registrar-se com usuari.
   
      El *issue tracker* de GitHub compleix aquestes dues condicions.
   -  Ha d'estar enllaçat des del fitxer ``README`` del repositori de codi.
   -  Si es vol tenir el gestor d'incidències en infraestructura pròpia de
      l'Ajuntament, utilitzar una de les següents eines lliures: Gitlab,
      Redmine, Trac.
   
.. rec:: Utilitzar el gestor d'incidències per tasques, *releases* i noves funcionalitats
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació
   
   I no només com a *bug tracker*.
   
.. mes:: Redactar i mantenir una política de gestió d'incidències
   :tags: Contractar; Plugin; NouProducte; Publicació
   
   Ha d'especificar:
   
   - Tipus d'incidència (deficiències, tasques, *milestones*, etc).
   - Etapes per les que passen
   
   Se li pot encarregar aquesta tasca a l'adjudicatari. Si no en té una de
   pròpia l'IMI n'hauria de proporcionar una per defecte.
   
.. rec:: Donar permisos per reportar incidències a tothom
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació
   
   Sempre es pot vetar a alguna persona que doni problemes o reconsiderar
   aquesta política si no funciona en un projecte.
   
.. rec:: Establir una persona encarregada de filtrar les incidències a mida que arriben
   :tags: Contractar; Plugin; NouProducte; Publicació
   
   S'ha d'encarregar d'eliminar duplicats, spam, etc.
   
   Complementar això amb un avís de que és necessari primer buscar duplicats i
   comprovar amb una altra persona, en privat, que el problema es reprodueix en
   una segona màquina.
   
   Pressupostar aquesta tasca si es fa sota un contracte amb una empresa o
   cooperativa.
   
.. mes:: Fer la notificació de defectes al *bug tracker* oficial del producte a modificar
   :tags: Adaptació; Plugin

Infraestructura d'integració i proves
=====================================

.. rec:: Vincular el repositori principal a un sistema d'integració contínua de codi obert
   :tags: Dia1; Adaptació; Plugin; NouProducte; Publicació
   
   Recomanem una de les següents eines:
   
   -  Jenkins
   -  Gitlab CI
   -  Travis CI
   
Canals de comunicació interns i externs
=======================================
   
.. mes:: Crear una llista de correu de desenvolupament que inicialment servirà també per usuaries *early-adopters*
   :tags: Plugin; NouProducte; Publicació

   Recomanem utilitzar l'eina Discourse.

   Alternativament podem utilitzar Mailman 3. La llista es pot dir
   ``NOM-DEL-PROJECTE-dev``.
   
   Activar l'arxiu i utilitzar-lo profusament.
   
   Inicialment en català i/o castellà. Quan apareguin participants en altres
   llengües, crear una llista en anglès. Els principals desenvolupadors hi han
   de ser presents, però no tenen obligació de respondre a totes les peticions.
   
   Fa més confiable el producte que les persones que es pugui contactar amb les
   persones que hi ha a darrera.
   
   Inicialment la separació entre usuaris (*early adopters*) i desenvolupadors
   és tènue. Més endavant cal crear canals de comunicació especialitzats pels
   diferents tipus de participant.
   
.. rec:: Crear una llista de correu d'usuaries, si el projecte creix
   :tags: Plugin; NouProducte; Publicació
   
   Activar l'arxiu.
   
.. rec:: Crear un xat de desenvolupament per la comunicació immediata de l'equip
   :tags: Plugin; NouProducte; Publicació
   
   Usar `gitter.im <https://gitter.im>`_ o `riot.im <https://riot.im>`_.
   
.. mes:: Usar els *pull-requests* de GitHub per fer revisions de codi públiques de totes les contribucions externes
   :tags: Plugin; NouProducte; Publicació
