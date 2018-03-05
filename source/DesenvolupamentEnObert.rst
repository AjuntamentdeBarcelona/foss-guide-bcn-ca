************************
Desenvolupament en obert
************************

.. _treballar-en-obert-dia-1:

Treballar en obert des del "dia 1"
==================================

Les mesures d'aquest apartat tenen a veure amb l'obertura del projecte i que cal
posar en pràctica des del primer dia de la fase de desenvolupament, ja que quant
més temps es gestiona un projecte de forma tancada, més costós és després
obrir-lo. Si s'espera massa, pot ser que algunes mesures no s'arribin a
implementar mai, ja que el seu cost resultaria prohibitiu.

Treballar en obert vol dir que els següents elements son públicament
accessibles (per lectura), en formats oberts i sense haver d'usar eines
privatives o contractar serveis de pagament, des del dia 1 del projecte:

-  El repositori de codi.
-  El gestor d'incidències (on, entre d'altres, es notifiquen i
   gestionen els defectes).
-  Els documents de disseny.
-  La documentació d'usuari/-a.
-  Els canals de comunicació on l'equip de desenvolupament pren les
   decisions tècniques.

Treballar en obert NO vol dir (necessàriament) que:

-  Persones externes al projecte tinguin accés d'escriptura al
   repositori (son lliures de copiar el codi en un repositori propi i
   modificar-lo allà).
-  Tothom tingui permís per escriure notificacions de defectes i
   intervenir al gestor d'incidències, cada projecte pot triar la seva
   política de QA.
-  L'equip del projecte hagi de llegir i respondre totes les
   notificacions de defectes (si estan obertes per escriptura) ni totes
   les preguntes als canals de comunicació oberts.
-  L'equip del projecte hagi de revisar totes les suggerències i
   contribucions (*pull requests*, *patches*) que rebi, si es considera
   que els recursos estan millor invertits en una altra tasca.

És molt important que tots els caps de projecte es llegeixin els
següents apartats, on es justifica abastament aquesta mesura:

-  http://producingoss.com/en/setting-tone.html#be-open-from-day-one
-  http://producingoss.com/en/governments-and-open-source.html#starting-open-for-govs

A mode de resum:

-  Tenir canals de comunicació oberts des del dia 1 no vol dir que els
   "estranys" ens hagin de distreure des del dia 1. En el present
   document s'explica com deixar clar quins son els nostres compromisos,
   que podem modular a cada fase.
-  És impossible compensar els incentius que tenen els desenvolupadors
   per fer coses de manera "ràpida i lletja" amb futures amenaces
   d'obertura. Si no s'actua en obert des de l'inici, inevitablement
   incorreran en `deute
   tecnològic <https://en.wikipedia.org/wiki/Technical_debt>`__ amb la
   intenció d'arreglar les coses en un futur (que mai arriba).
-  Quan arriba el dia d'"obrir el codi", ens trobem de cop i volta que
   tenim:

   -  Configuracions d'usuari específiques i contrasenyes dins del
      repositori.
   -  Notificacions de defectes que contenen informació sensible que no
      es pot fer pública.
   -  Correspondència entre desenvolupadors on es barreja informació
      tècnica útil amb opinions personals que no estaven pensades per a
      que tothom les pogués llegir.
   -  Dependències sobre components de software que no es poden usar en
      un projecte de codi obert, o que generen problemes de llicències.
   -  Documentació o procediments de *build* escrits amb eines
      propietàries que no permeten la seva publicació.
   -  (I una llista inacabable de coses).

-  L'obertura del codi provoca haver de prendre decisions difícils, que
   no es produirien si hagués estat obert des de l'inici (perdre temps
   netejant l'historial de defectes vs. crear-ne un de nou i perdre
   l'historial complert, etc).
-  Es crea un gran "esdeveniment d'obertura" que suposa un alt risc per
   al projecte, ja que s'han de fer molts canvis de cop, i tot el
   projecte i les seves potencials vulnerabilitats queden exposades
   també de cop (i molts ulls, no sempre ben intencionats, estaran
   mirant). Abans de l'esdeveniment, això crea incertesa i preocupació.
   Després de l'esdeveniment, pot provocar una allau d'incidències que
   en condicions normals haguessin arribat escalonadament.

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
   
.. alt:: Vincular el repositori principal a un sistema d'integració contínua de codi obert
   :tags: Dia1; Adaptació; Plugin; NouProducte; Publicació
   
   Recomanem una de les següents eines:
   
   -  Jenkins
   -  Gitlab CI
   -  Travis CI
   
.. mes:: Pujar el codi al repositori principal
   :tags: Dia1; Plugin; NouProducte
   
   Fer descarregable tot el codi font del projecte. De dues maneres:
   
   -  Des del repositori Git principal amb ``git clone``.
   -  En un únic arxiu en format ``zip`` o ``tar.gz``, com a mínim des del
      moment que existeixi una primera *release* pública.
   
.. mes:: Dia1; Pujar un fitxer ``README`` al repositori principal
   :tags: Plugin; NouProducte; Publicació
   
   Ha d'incloure la declaració de propòsit i la resta d'informacions que al
   llarg d'aquest document es menciona que s'han d'incloure en el
   ``README``.
   
   S'ha de redactar en anglès i el format ha de ser text amb algun
   llenguatge de marques lleuger. Pot no tenir extensió si conté només text
   pla o una extensió que indiqui amb quin format de marques s'ha
   d'interpretar (és a dir, en realitat es el fitxer tindrà nom
   ``README.md`` si està escrit en Markdown).
   
   El contingut d'aquest fitxer (concretament la versió que hi hagi penjada
   a la branca ``master``), formatat segons les convencions del llenguatge
   de marques que s'hagi utilitzat, és el que GitHub mostra com a portada
   de la web de desenvolupament. Per tant, convé comprovar que el format és
   correcte i que es visualitza bé en un navegador web.
   
.. mes:: Implementar procediments de *build* i instal·lació amb eines lliures i d'ús estès
   :tags: Dia1; Plugin; NouProducte; Publicació
   
   És molt important no esperar gens a construir i documentar un sistema de
   *build* del programari, ja que sense això l'esforç que ha de realitzar
   qualsevol desenvolupador per provar l'eina serà probablement massa gran
   com perquè ningú ho intenti.
   
   Per suposat no es pot obligar als usuaris i potencials col·laborador
   d'un projecte de codi obert a dependre d'eines que no siguin alhora
   programari lliure, i dins d'aquestes convé triar les d'ús més estès i
   que resultin més familiars a la majoria de desenvolupadors. Això últim
   pot variar d'una comunitat a una altra. Alguns exemples d'eines de
   *build* (algunes també serveixen per als procediments de configuració i
   instal·lació) d'ús comú i que recomanem son:
   
   -  Per a projectes Java: Maven, Ant (també serveix per altres
      llenguatges).
   -  Per a projectes Python recomanem seguir els consell de
      http://python-packaging.readthedocs.io/en/latest/index.html, que
      inclouen també informació sobre empaquetament.
   -  Per a projectes JavaScript (i per *front-end* en general): Gulp.js.
   -  Per a projectes Ruby: Rake.
   -  Ús general: CMake, Nix.
   
.. mes:: Dia1; Pujar el text de la llicència al repositori principal
   :tags: Plugin; NouProducte; Publicació
   
   La llicència anirà en text pla en un fitxer anomenat ``LICENSE`` (sense
   extensió), al directori arrel del repositori.
   
   El text de les dues llicències recomanades (que cal copiar de forma
   literal) el podem trobar a:
   
   -  https://www.gnu.org/licenses/agpl.txt
   -  https://joinup.ec.europa.eu/sites/default/files/inline-files/EUPL%20v1_2%20EN(1).txt
   
   El fitxer ``LICENSE`` ha d'estar en anglès. En el cas d'utilitzar la
   llicència EUPL-1.2, que té traduccions oficials, podem opcionalment
   incloure fitxers ``LICENSE.ca.txt`` i ``LICENSE.es.txt``. Les diferents
   traduccions es troben a
   https://joinup.ec.europa.eu/page/eupl-text-11-12.
   
.. mes:: Publicar unes breus Directrius per desenvolupadors (*Developer Guidelines*)
   :tags: Dia1; Plugin; NouProducte; Publicació
   
   Aquesta guia estableix les convencions tècniques i socials que
   determinen les interaccions entre desenvolupadors, i entre
   desenvolupadors i usuaris. És d'aplicació per tots els desenvolupadors,
   tant els contractats per l'Ajuntament, com els externs, com el personal
   del mateix Ajuntament.
   
   S'ha de redactar en anglès i ha de ser, o bé una pàgina de la pròpia
   wiki de GitHub, o bé un fitxer de text amb llenguatge de marques
   lleuger.
   
   La guia pot créixer amb al temps, però a l'inici només cal deixar clares
   tres coses:
   
   #. Quins son els canals de comunicació de que disposa el projecte i per
      a què s'utilitza cadascun.
   #. Instruccions de com reportar defectes (*bugs*) i de com fer
      contribucions al projecte.
   #. Una descripció breu de com és la governança del projecte: qui i com
      pren les decisions. En molts casos només caldrà dir que durant la
      duració del contracte en vigor l'Ajuntament és qui prioritza les
      funcionalitats a desenvolupar, els defectes a arreglar. També té la
      última paraula sobre les solucions tècniques a adoptar, les
      contribucions a integrar i les versions a publicar. Es pot dir que en
      un futur s'estudiarà un model de governança adequat a l'evolució de
      les circumstàncies del projecte.
   
   Aquestes Directrius per desenvolupadors han d'estar enllaçades com a
   mínim des de:
   
   -  El fitxer ``README`` del repositori principal.

Contractació per desenvolupar en obert
======================================
   
.. mes:: Adjudicar a entitats amb experiència en desenvolupament obert
   :tags: Contractar; Adaptació; Plugin; NouProducte
   
   Per moltes condicions que es posin al contracte, si l'empresa
   adjudicatària no té experiència participant en projectes de codi obert,
   el més probable és que el producte no acabi sent obert del tot. En la
   majoria de casos això no té perquè ser resultat d'una mala disposició,
   sinó fruit del desconeixement.
   
.. alt:: Fer un contracte secundari de validació i verificació independent (IV&V)
   :tags: Contractar; Adaptació; Plugin; NouProducte
   
   Contractar alguna entitat que sí tingui experiència demostrable en
   participar de manera sostinguda en projectes de codi obert. Aquesta
   entitat actuarà com un col·laborador extern del projecte i farà
   revisions de codi i anàlisis de processos, reportant directament a
   l'IMI.
   
   En un projecte de codi obert el que s'està contractant no és només el
   codi, sinó també el procés.
   
   Afegir aquest servei a la oficina tècnica del projecte.
   
.. alt:: Tenir en compte l'experiència en projectes de codi obert que acreditin els concursants en l'adjudicació
   :tags: Contractar; Adaptació; Plugin; NouProducte
   
.. mes:: Demanar als concursants que acreditin experiència en projectes de codi obert dels participants
   :tags: Contractar; Adaptació; Plugin; NouProducte
   
   Ho han de fer aportant referències a la seva participació individual en
   repositoris i fòrums oberts (StackOverflow, etc.), dels projectes en que
   hagin participat.
   
.. rec:: Partir el projecte en grups de funcionalitat que es puguin licitar en diferents lots
   :tags: Contractar; NouProducte
   
   Bé sigui contractant per lots, bé sigui externalitzant tasques concretes
   com la revisió de codi i del desplegament, com estableix la
   `Alternativa: Fer un contracte secundari de validació i verificació
   (V&V) independent <#fer-contracte-validacio-independent>`__.
   
   A més de ser una política alineada amb la Guia de contractació
   tecnològica, és molt favorable pels interessos del projecte disseminar
   el coneixement sobre el producte. Les *reserves de coneixement
   distribuïdes* son una de les principals fortaleses dels projectes de
   codi obert.
   
   També ajuda molt a que des de l'inici del desenvolupament s'estableixin
   processos de treball en obert.

.. mes:: Obligar als adjudicataris a parametritzar tot usant fitxers de configuració
   :tags: Contractar; Adaptació; Plugin; NouProducte

   No utilitzar *valors màgics* al codi.

Difusió del projecte
====================
   
.. mes:: Escollir un bon nom per al projecte
   :tags: NouProducte; Publicació
   
   Això és més important en projectes de codi obert que en projectes
   tradicionals perquè adquirir usuaris i desenvolupadors fora dels confins
   de l'Ajuntament pot determinar el grau d'èxit del projecte.
   
   Es poden trobar algunes indicacions més concretes a
   http://producingoss.com/en/getting-started.html#choosing-a-name.
   
.. rec:: Adquirir el nom en els espais d'Internet importants
   :tags: NouProducte; Publicació
   
   Per projectes grans és recomanable pensar des del principi en quins
   llocs i plataformes d'Internet s'haurà de tenir presència i assegurar la
   disponibilitat dels dominis o noms d'usuari corresponents. A més d'un o
   més dominis ICANN propis, pot ser que un projecte vulgui tenir presència
   a GitHub o Twitter, per exemple. Utilitzar a tot arreu el mateix nom
   d'usuari facilita la identificació del projecte per part de persones que
   encara no hi estan massa involucrades.
   
.. mes:: Redactar una declaració de propòsit clara i posar-la a llocs destacats
   :tags: Integració; NouProducte; Publicació
   
   La declaració de propòsit és un text curt, d'un o dos paràgrafs, que
   permet a la gent decidir en 30 segons si els interessa seguir llegint
   sobre el projecte o no. Ha d'anar acompanyada dels enllaços necessaris
   per si la resposta afirmativa. En el redactat es pot donar per suposats
   uns coneixements mínims de l'àrea d'aplicació del projecte. Les persones
   que no disposen d'aquests coneixements probablement no estaran
   interessades en el projecte.
   
   El text s'ha de tenir redactat com a mínim en anglès i en català, per
   utilitzar la versió que convingui en cada cas.
   
   Ha d'aparèixer com a mínim als següents llocs:
   
   -  La pàgina d'inici de la web orientada a usuaris del projecte, cas de
      tenir-ne. S'ha de poder veure sense necessitat de fer scroll en un
      ordinador de sobretaula.
   -  El fitxer ``README`` del repositori principal.
   -  El llistat de projectes a https://ajuntamentdebarcelona.github.io.
   -  Cada vegada que el projecte s'introdueix a un repositori o llistat de
      projectes de codi obert, per exemple el `Join Up de la Unió
      Europea <https://joinup.ec.europa.eu/>`__.
   
.. mes:: Especificar en llocs destacats que el projecte és lliure
   :tags: Plugin; NouProducte; Publicació
   
   Aquesta mesura fa que els potencials col·laboradors no hagin de buscar
   massa per saber si estaran disposats a contribuir o no al projecte.
   
   És important, a més, indicar sota quina llicència concreta es
   distribueix el programari (incloent la versió), utilitzant el nom
   complert o bé l'identificador, el que més convingui en cada cas,
   exactament com apareixen a https://spdx.org/licenses/.
   
   Especificar la llicència com a mínim en els següents llocs:
   
   -  La pàgina d'inici de la web orientada a usuaris del projecte, cas de
      tenir-ne. S'ha de poder veure sense necessitat de fer *scroll* en un
      ordinador de sobretaula.
   -  El fitxer ``README`` del repositori principal.
   -  El llistat de projectes a https://ajuntamentdebarcelona.github.io.
   -  Cada vegada que el projecte s'introdueix a un repositori o llistat de
      projectes de codi obert, per exemple el `Join Up de la Unió
      Europea <https://joinup.ec.europa.eu/>`__.
   
   En quant a la web orientada a usuaris del projecte, és important no
   relegar aquesta informació a una pàgina de "descàrregues" o de
   "desenvolupament" que requereixi més d'un clic.
   
.. mes:: Especificar en llocs fàcilment accessibles un llistat de funcionalitats
   :tags: Plugin; NouProducte; Publicació
   
   Serveix per què la gent acabi de decidir si el projecte pot cobrir o no
   les seves necessitats.
   
   Enllaçar de forma visible com a mínim des de:
   
   -  La pàgina d'inici de la web orientada a usuaris del projecte, cas de
      tenir-ne. L'enllaç s'ha de poder veure sense necessitat de fer scroll
      en un ordinador de sobretaula.
   -  El fitxer ``README`` del repositori principal.
   
   Millor en forma de llistat amb vinyetes i frases simples, o d'una manera
   encara més gràfica. Molts cops és una mena d'extensió de la *declaració
   de propòsit*.
   
   Si una funcionalitat encara no està implementada es pot especificar
   entre parèntesis: *planned* o *work-in-progress*.
   
   Com s'explica amb més detall a la mesura *M: Especificar i mantenir una
   pàgina amb l'estat de desenvolupament del projecte*, no té sentit, i de
   fet pot ser molt contraproduent, falsejar o exagerar els veritables
   mèrits tècnics del producte.
   
.. mes:: Especificar en llocs fàcilment accessibles els principals requeriments tècnics
   :tags: Plugin; NouProducte; Publicació
   
   Per exemple quina arquitectura hardware/software es necessita per
   instal·lar-ho, quin sistema operatiu, etc. També és una informació
   necessària per què un potencial usuari esbrini si pot utilitzar la
   solució o no.
   
   Enllaçar de forma visible com a mínim des de:
   
   -  La pàgina d'inici de la web orientada a usuaris del projecte, cas de
      tenir-ne. L'enllaç s'ha de poder veure sense necessitat de fer scroll
      en un ordinador de sobretaula.
   -  El fitxer ``README`` del repositori principal.
   
   Millor en forma de llistat amb vinyetes i frases simples.
   
.. rec:: Especificar en llocs fàcilment accessibles les diferències amb productes similars
   :tags: Plugin; NouProducte; Publicació
   
   Destacar sobretot els avantatges respecte les eines més conegudes i ben
   establertes, lliures o propietàries, però no amagar les limitacions.
   
   Enllaçar de forma visible des de la web orientada a usuaris del
   projecte, cas de tenir-ne. Les diferències estrictament tècniques també
   es poden enllaçar des de la web de desenvolupament.
   
.. mes:: Especificar i mantenir una pàgina amb l'estat de desenvolupament del projecte
   :tags: Plugin; NouProducte; Publicació
   
   Es tracta d'escriure un llistat, que es va actualitzant periòdicament a
   cada *release* o fita important, que contingui:
   
   -  Les *release* anteriors, amb la data de publicació i els principals
      canvis que s'hi van introduir.
   -  Futures *release* o fites del projecte amb data temptativa de
      realització, a mode de full de ruta molt esquemàtic.
   
   L'objectiu d'aquesta pàgina és contribuir a visibilitzar tres coses:
   
   -  Quines fites s'han assolit ja.
   -  Cap a on es dirigeix el projecte i com de lluny es troben les fites
      que s'espera assolir.
   -  Com d'actius son el projecte i la seva comunitat, i com de ben
      mantingut està el codi.
   
   Enllaçar com a mínim des de:
   
   -  La web orientada a usuaris del projecte.
   -  El fitxer ``README`` del repositori principal.
   
   És molt important ser transparents i no falsejar l'estat real del
   projecte. És més perniciós atraure usuaris amb expectatives que no es
   podran complir que no pecar de conservadorisme a l'hora d'exposar el
   progrés realitzat o esperat. Tots els projectes tenen defectes i
   facilita la vida a tothom (desenvolupadors, promotors del projecte i
   potencials usuaris externs) tractar-los amb transparència. Molts
   projectes de programari lliure exitosos contenen a la seva pàgina un
   apartat titulat *Known bugs*, i alguns d'aquests defectes romanen allà
   durant anys.
   
   A més, en el cas del codi obert, tot el codi i tot el procés de
   desenvolupament està a la vista de tothom, i tothom pot instal·lar i
   provar el producte. Qualsevol pot refutar les nostres afirmacions si no
   son certes, com s'explica a
   http://producingoss.com/en/marketing.html#goldfish-bowl.
   
.. rec:: Establir mesures per visibilitzar millor el progrés i el grau d'activitat del projecte
   :tags: Plugin; NouProducte; Publicació
   
   Es poden posar indicadors i alimentadors automàtics a la pàgina d'inici
   de les webs (tant a la d'usuaris com la de desenvolupament), o en altres
   llocs, amb informacions que provinguin, per exemple, de:
   
   -  El repositori, per exemple els darrers missatges de *commit*.
   -  El sistema d'integració continua, per exemple quins *builds* o
      conjunts de testos han funcionat o fallat darrerament.
   -  El sistema de notificació d'incidències o defectes.
   -  Twitter del projecte o d'usuaris de l'aplicació.
   
   També es pot mostrar de manera gràfica una mena de calendari de progrés
   amb les diferents versions.
   
   Es pot agafar com exemple la manera que mostra la informació de
   `projectes d'exemple el Launchpad
   d'Ubuntu <https://launchpad.net/inkscape>`__.
   
   L'objectiu és enfortir i fer més visual tot allò esmentat a la `Mesura:
   Especificar i mantenir una pàgina amb l'estat de desenvolupament del
   projecte <#h:a22a9688-f8e2-473d-baf5-8989693a41c1>`__.
   
.. rec:: Negociar a priori la manera de fer visibles les aportacions patrocinades per l'Ajuntament
   :tags: Adaptació; Plugin
   
   A l'Ajuntament de Barcelona li pot interessar que els projectes de
   programari que no han estat iniciats per l'Ajuntament, però als quals
   realitza contribucions de qualsevol tipus (extensions, traduccions,
   hores de treball de manteniment) reconeguin i donin publicitat a
   aquestes contribucions. La manera en que això es concreti dependrà de
   cada projecte i de la naturalesa de les aportacions. Alguns exemples
   poden ser:
   
   -  Esment en una llista pública d'entitats que participen o
      contribueixen al projecte.
   -  Aparició del logo de l'Ajuntament a la web del projecte.
   
   És convenient, abans d'iniciar la col·laboració, parlar amb la comunitat
   de desenvolupament del projecte sobre quin reconeixement desitjaria
   obtenir l'Ajuntament en cada cas.
   
Empaquetat i desplegament
=========================
   
.. mes:: Obligar a l'adjudicatari que fa el desplegament a usar el mateix codi publicat al repositori principal
   :tags: Contractar; Adaptació; Plugin; NouProducte

   Com a condició de transparència, el codi font que en cada moment
   s'utilitza per construir (*build*) i desplegar els serveis en producció
   ha d'estar disponible en el repositori públic de l'Ajuntament,
   preferentment sota la branca ``master``. Qualsevol *patch* de seguretat,
   millora o modificació de qualsevol tipus que s'apliqui al codi en
   producció s'ha de reflectir al repositori.
   
   El codi disponible al repositori públic és el que està cobert totalment
   per una llicència lliure. No s'hi pot fer cap afegit.
   
.. rec:: Establir una política de versions explícita en el fitxer ``README``
   :tags: Plugin; NouProducte; Publicació
   
   Convé que cada repositori tingui una política de versions explícita. Els
   projectes de programari utilitzen normalment identificadors de versions
   basats en seqüències de nombres de l'estil ``MAJOR.MINOR.PATCH``.
   
   Cal escollir una política de versions adient a cada projecte. Cada
   comunitat tecnològica (Java, Python, Drupal, etcètera) pot tenir una
   política de versions preferent i és aconsellable informar-se de quina és
   i adherir-s'hi. En cas que no hi hagi una política clara podem
   adherir-nos a una política genèrica i ben coneguda, com el `Semantic
   Versioning <http://semver>`__.
   
Formats i estàndards oberts
===========================
   
.. mes:: Comprovar que la interfície d’usuari que compleix amb els estàndards del W3C, en cas d'aplicacions web
   :tags: Plugin; NouProducte
   
   Les interfícies web d’usuari, tant les d’ús per als ciutadans com les
   d’administració i ús intern, han de complir amb els estàndards del World
   Wide Web Consortium (W3C) i no han de requerir l’ús de funcionalitats
   proporcionades per extensions propietàries dels navegadors. La
   presentació s’ha de visualitzar correctament, i el producte ha de ser
   plenament funcional, amb els navegadors de la família Gecko (Firefox),
   WebKit/Blink (Chrome, Safari, Konqueror) o Trident/EdgeHTML (Microsoft).
   
.. mes:: Utilitzar formats oberts en l'intercanvi de documents amb el ciutadà i amb altres sistemes
   :tags: Adaptació; Plugin; NouProducte; Publicació
   
   Tot l’intercanvi de documents amb el ciutadà que impliqui la descàrrega
   o càrrega de fitxers s’ha de produir exclusivament amb formats oberts,
   segons la definició que en dona la Guia de Compra Tecnològica de
   l’Ajuntament de Barcelona. L’emmagatzematge intern de documents per part
   de l’aplicació es produirà també en aquests mateixos formats. En
   particular, tot l’intercanvi de fitxers de text es farà o bé mitjançant
   OpenDocument Format (https://www.oasis-open.org), o bé en format PDF.
   L’intercanvi d’imatges, àudio i vídeo també es realitzarà mitjançant
   formats oberts pels quals existeixin implementacions lliures en les
   principals plataformes informàtiques incloent GNU/Linux.
   
Internacionalització
====================
   
.. mes:: Definir i pressupostar els requeriments tècnics per què el producte pugui ser traduït i internacionalitzat
   :tags: Contractar; Adaptació; Plugin; NouProducte

   Tots els missatges mostrats a l'usuari han d'estar internacionalitzats.
   Utilitzar els mecanismes habituals en cada llenguatge/plataforma.
   
Obrir un codi que era tancat
============================
   
.. mes:: Jutjar la conveniència o no de publicar un codi en poder de l'Ajuntament
   :tags: Publicació
   
   Abans de publicar sota llicència lliure un component o sistema software
   ja existent i en ús a l'Ajuntament de Barcelona cal comprovar que:
   
   -  Correspon a una necessitat general: pot ser d'utilitat per a més
      institucions o organitzacions, a més de l'Ajuntament.
   -  Té algun aspecte que el diferencia favorablement d'altres solucions
      obertes existents.
   -  L'Ajuntament de Barcelona és titular legal de tot el codi que es
      pretén alliberar, o pot fer gestions per obtenir aquesta titularitat.
   -  Es pot executar sobre plataformes lliures.
   -  El codi (i la documentació associada) té la qualitat i la maduresa
      suficients, o bé els requeriments de millora estan clarament
      identificats i existeix una estratègia per abordar-los.
   -  L'obertura de la solució no suposarà riscos legals per a cap part.
   -  Es disposa dels recursos per respondre a incidències de manteniment
      mentre no es traspassi aquesta responsabilitat a d'altres entitats,
      possiblement una comunitat oberta de desenvolupadors i usuaris.
   
.. mes:: Buscar al repositori de codi informació sensible o configuracions d'usuari
   :tags: Publicació
   
.. mes:: Avisar als nous espais públics orientats a desenvolupadors que aquest era un projecte tancat
   :tags: Publicació
   
   Es tracta d'explicar que el projecte ha funcionat fins a un determinat
   moment com un projecte tancat i per tant cal esperar certes
   inconveniències. Convé reduir les expectatives del nous usuaris i
   desenvolupadors en quant a qualitat i transparència d'alguns elements
   del projecte. S'han d'explicar els compromisos als que s'ha hagut
   d'arribar per fer possible l'obertura. Per exemple, és possible que en
   el repositori de codi hi hagi moltes dades sensibles (dades d'usuaris
   concrets, etc.) i que s'hagi optat per perdre l'historial del control de
   versions i crear un repositori nou *top-skim* que només contingui la
   darrera versió..
   
   Aquesta informació convé publicar-la com a mínim a:
   
   -  La web de desenvolupament (ara pública i oberta).
   -  Llistes de correu públiques.
   
   L'objectiu d'aquesta mesura és evitar un allau de peticions
   inassumibles.
   
.. rec:: Avisar als desenvolupadors de les possibles conseqüències de la imminent obertura del projecte
   :tags: Publicació
   
   Si tenim alguna manera, per exemple mitjançant llistes de correu
   privades, d'accedir a les persones que han participat o que participen
   en un projecte que anem a obrir, és convenient notificar aquest fet. El
   fet d'obrir un codi que no es va escriure des de l'inici per ser obert
   pot provocar incomoditat als seus autors, i cal explicar que això és
   normal. Es pot referir el següent treball per ajudar a aclarir la
   situació: http://producingoss.com/en/opening-closed-projects.html.
