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

Mesures i recomanacions relacionades:

.. needfilter::
   :tags: Dia1
   :layout: table

Contractació per a desenvolupar en obert
========================================
   
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
   
.. rec:: Adquirir el nom en els espais d'Internet importants (3.3, 7.0)
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

Parametrització, configuració i instal·lació
============================================

.. mes:: Implementar procediments de build i instal·lació amb eines lliures i d'ús estès
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
   
Ús de formats i estàndards oberts
=================================
   
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
   
Apertura d'un codi que era tancat
=================================

En aquest apartat s'explica com preparar un codi que era tancat per, a partir de
la decisió de publicar-lo, poder-lo evolucionar i mantenir en obert.

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
