***********************
Infraestructura tècnica
***********************

La infraestructura tècnica necessària per a allotjar un projecte de programari
lliure consta típicament de diferents elements i eines, molts cops vinculades
entre sí de maneres complexes. En aquest capítol recomanem algunes eines i
pràctiques d'ús comú en el sector.

Un principi general que es veu concretat en les mesures d'aquest capítol és que
les persones que participen en un projecte mai s'han de veure obligades a
instal·lar programari privatiu a les seves màquines.

Llocs web associats al projecte
===============================

Un projecte de programari pot tenir típicament dos tipus de lloc web:

- **Una web de desenvolupament**, orientada a persones que contribueixen al
  projecte amb codi o documentació tècnica, contractades per l'Ajuntament o no.
- **Una web orientada a persones usuàries i participants en general**. Això
  inclou a persones o entitats que puguin voler instal·lar i usar el programari
  fora de l'Ajuntament, però també a gent interessada en el projecte encara que
  no siguin usuàries directes del programari. En aquesta web s'ha de facilitar i
  incentivar a participar en el projecte amb contribucions menys (o gens)
  tècniques: finançament, documentació d'usuària, test de *pre-releases*,
  difusió, traduccions, etcètera.

Normalment els dos tipus de contingut son necessaris, però no sempre cal que es
trobin en dos llocs separats, amb noms de domini diferents. En cada projecte que
lideri, l'Ajuntament haurà de valorar fins a quin punt les necessitats i
mentalitats dels dos conjunts de persona son diferents i resulta per tant
impossible que un únic model de web s'adeqüi als dos grups.

A l'apartat `Repositori de codi i control de versions`_ s'explica com crear la
web de desenvolupament, que és l'única que es necessita des de bon començament.
A mida que el projecte creix, es pot valorar si cal també un lloc orientat a
d'altres perfils de participant.

El que sí és interessant tenir des del principi és un nom de domini propi (o una
URL permanent sota algun domini de l'Ajuntament), que si cal es pugui redirigir
cap a on es trobi inicialment la web del projecte (possiblement un lloc com
GitHub).

.. rec:: Reservar una URL permanent per al projecte, i usar-la sempre per fer-hi referència
   :tags: Dia1; Integració; Plugin; NouProducte; Publicació

   Es tracta que des del començament l'Ajuntament tingui sota el seu control la
   URL que es farà servir per identificar el projecte a Internet. Encara que la
   web del projecte es trobi allotjada en un lloc com GitHub, utilitzar una
   redirecció permetrà en un futur, si es decideix moure de lloc la web de
   desenvolupament, mantenir la mateixa adreça pública.

   Hi ha dues opcions:

   - Reservar una URL permanent sota algun domini propietat de l'Ajuntament.
   - Comprar un (o més) nom(s) de domini per al projecte.
   
.. rec:: Crear una web orientada a la participació no tècnica, que es basi en tecnologies lliures
   :tags: Integració; Plugin; NouProducte; Publicació

   Aquesta web es pot crear en el moment que es consideri oportú, quan el
   projecte assoleixi una mida o projecció significatives.

   Pot ser una web multilingüe. Cada projecte ha de decidir a quines llengües
   traduir-la en funció de quins públics resultin prioritaris.

   Aquest lloc web ha d'incloure:

   - Un enllaç a la web de descàrrega, amb instruccions de com instal·lar el
     programari. Aquest enllaç ha de ser ben visible a la portada.
   - Un apartat "Get Involved" o "Community" on s'informa de les diferents
     maneres d'involucrar-se en el projecte. També ha d'estar ben visible a la
     portada.
   - Un enllaç a la web de desenvolupament. Aquest es pot trobar, o bé a
     l'apartat "Community", o bé a la portada, per exemple amb un enllaç que
     digui "Developers" o bé un enllaç del tipus "Fork on GitHub".

   Existeixen moltes eines i *frameworks* de gestió de contingut i publicació de
   llocs web lliures i de qualitat excel·lent, així que no hauria de ser un
   problema trobar-ne un que s'ajusti a les necessitats del projecte: Drupal,
   Wordpress (sense les extensions privatives), i molts més.

Repositori de codi i control de versions
========================================

Un element central de la web de desenvolupament d'un projecte és un repositori
de codi –públic i sota control de versions– que serveixi de base per
centralitzar les modificacions que han de formar part de cada nova entrega
(*release*) del producte.

En l'escenari :code:`NouProducte` o :code:`Plugin` l'Ajuntament haurà de crear
aquest repositori. En el cas d'una :code:`Integració` o :code:`Adaptació`,
l'Ajuntament tindrà la seva pròpia còpia (*clone* o *fork*) del repositori
original (*upstream*), on centralitzarà els treballs corresponents a les
modificacions del seu interès. A aquest repositori que crea l'Ajuntament i que
serveix, o bé per realitzar les entregues d'un producte original, o bé per
centralitzar les contribucions a un projecte extern, en direm **repositori
principal**. Poden existir moltes altres còpies públiques i privades del codi.

Com s'indica en les mesures de més avall, el repositori principal s'allotjarà a
GitHub, un servei que utilitza Git com a sistema de control de versions
distribuït. El vocabulari i conceptes fonamentals per entendre el seu
funcionament es pot trobar a :prodoss:`Version Control Vocabulary
<en/vc.html#vc-vocabulary>`.

Hi ha moltes alternatives viables i raonables a GitHub, i fins i tot algunes
alternatives viables a Git com a programari de control de versions, però GitHub
ofereix prous avantatges com per què sigui la opció per defecte:

- La majoria de desenvolupadores la coneixen i no han d'aprendre noves eines i
  procediments ad-hoc per al projecte.
- Llança el missatge de que el projecte està obert a col·laboració.
- Ofereix una bona integració amb la resta d'infraestructura tècnica i social
  d'un projecte: gestió d'incidències, integració contínua, canals de
  comunicació per a desenvolupament, etc.
- Permet també guardar i mostrar (part de) la documentació d'un projecte, que
  pot ser una wiki. La presentació de la informació és suficientment agradable
  com per permetre aplaçar la construcció d'una web orientada a persones
  usuàries i participants en general del projecte.
- És la plataforma més utilitzada per projectes de codi obert, dóna molta
  visibilitat.
- Qualsevol alternativa ha d'oferir unes garanties similars en quant a
  durabilitat i sostenibilitat.

.. admonition:: **Inconvenient**: GitHub no és 100% codi obert.

   Tot i ser un servei gratuït per un gran ventall de possibles usos, no tot el
   codi de la infraestructura que hi ha darrera de GitHub és lliure, i en
   darrera instància s'està establint una dependència amb una empresa que no
   sabem com evolucionarà en el futur. Més endavant poden aparèixer opcions que
   facin reconsiderar aquesta recomanació de fer servir GitHub com a opció per
   defecte.

.. mes:: Crear el repositori principal a l'espai GitHub de l'Ajuntament
   :tags: Dia1; Adaptació; Plugin; NouProducte; Publicació

   Es crearà a GitHub un projecte
   ``https://github.com/AjuntamentDeBarcelona/NOM-DEL-PROJECTE`` on es publicarà
   el codi. L'Ajuntament té creat dins de GitHub un compte a nivell
   d'*organització* anomenat ``ajuntamentdebarcelona``, que serà el propietari
   (*owner*) del repositori.

   Això no vol dir que no puguin haver-hi rèpliques (miralls) del repositori o
   parts del mateix en altres llocs (espais GitHub d'altres organitzacions, de
   desenvolupadors particulars, la pàgina web de les empreses adjudicatàries de
   contractes públics, etcètera).
   
   El nom del projecte a GitHub es recomana que sigui tot en minúscules i amb
   les paraules de què està format separades per guions. Per exemple:
   `<https://github.com/AjuntamentdeBarcelona/decidim-barcelona>`_.
   
   El codi ha d'estar present en aquest lloc des de l'inici del projecte, sense
   esperar a que hi hagi *releases* públiques.
   
.. alt:: Crear un repositori públic en un lloc diferent del GitHub de l'Ajuntament
   :tags: Adaptació; Plugin; NouProducte; Publicació

   Pot haver-hi motius que facin recomanable tenir el repositori principal (el
   vinculat al gestor d'incidències) en llocs com:
   
   - L'espai GitHub d'una altra organització.
   - BitBucket o d'altres plataformes similars.
   - Un portal Gitlab d'alguna organització que participi en el desenvolupament
     del projecte (o en un futur un portal Gitlab de l'Ajuntament de Barcelona).
   
   Alguns d'aquests motius poden ser:
   
   - És un projecte on intervenen més participants del sector públic, i es crea
     una consorci o organització ad-hoc.
   - L'empresa que desenvolupa té un fort lideratge sobre el projecte, més gran
     que el que pugui tenir l'Ajuntament, i vol tenir la infraestructura bàsica
     sota el seu control.
   
   Si s'opta per aquesta alternativa, s'ha de tenir en compte que:
   
   - No podem renunciar a Git com a sistema de control de versions: és l'eina
     molt majoritàriament utilitzada avui en dia i que tots els desenvolupadors
     coneixen, i facilita unes bones pràctiques de gestió de projectes en obert
     que amb sistemes més antics (com CSV o Subversion) resulten molt més
     farragoses. Si determinats procediments s'han d'executar necessàriament
     sobre una altra eina, per exemple Subversion, la solució és fer el
     desenvolupament en obert sobre Git, i mantenir un mirall Subversion
     automatitzat utilitzant la comanda ``git svn dcommit``, com s'explica per
     exemple a
     `<http://www.kerrybuckley.org/2009/10/06/maintaining-a-read-only-svn-mirror-of-a-git-repository/>`_.
   - En qualsevol cas hi ha d'haver una rèplica actualitzada del repositori
     principal a l'espai GitHub de l'Ajuntament, per donar visibilitat a totes
     les contribucions a projectes de codi obert que realitza.
   - Al fitxer ``README`` contingut (i mostrat) a l'espai GitHub de
     l'Ajuntament, a l'espai GitHub.io i a la resta de llocs amb enllaç al codi
     font, d'indicarà quin és el repositori (o repositoris) principal on es
     porta a terme el desenvolupament.
   - Siguin on siguin, tant l'eina de gestió d'incidències com el sistema
     d'integració continua han de ser públics i s'han de poder utilitzar per
     part de tothom sense pagar subscripcions a cap servei.
   - Tot el codi font del projecte ha de ser descarregable per qualsevol persona
     en tot moment. GitHub facilita això proveint de botons per descarregar un
     arxiu ``zip`` o bé mostrant les comandes necessàries per clonar el
     repositori utilitzant Git. Si No es fa servir GitHub s'ha d'aconseguir que
     el lloc públic del repositori faciliti també aquestes dues modalitats de
     descàrrega (arxiu ``zip`` o ``tar.gz`` i comanda ``git clone``).

.. mes:: Utilitzar el respositori de GitHub com la web de desenvolupament del projecte
   :tags: Dia1; Plugin; NouProducte; Publicació

   La portada de la web serà un fitxer ``README`` a l'arrel del repositori.
   Aquest fitxer pot estar en format text pla, Markdown, o d'altres llenguatges
   de marques suportats per GitHub i que aquest interpreta i formata quan es
   visita la pàgina.

.. mes:: Establir permisos al repositori principal adequats a cada tipus de participant
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació; Document

   GitHub té el concepte de **propietari** (*owner*) d'un repositori, que
   correspondrà a un compte que l'Ajuntament té com a organització
   (``ajuntamentdebarcelona``).

   La resta de permisos es detallen a les submesures.

   - Qualsevol treballador de l'IMI que tingui un
     compte personal a GitHub que formi part de la organització
     ``ajuntamentdebarcelona`` tindrà permisos d'
   - Es pot donar permisos d'**administrador** del repositori a persones de l'IMI

   I, opcionalment, una persona de cada entitat externa que participa en el
   desenvolupament sota contractes amb l'IMI.
   
.. sub:: Donar permís d'escriptura al repositori principal a totes les persones de l'equip de desenvolupament
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació; Document
   
   Això inclou tant persones internes com subcontractades. A més, fer pública la
   llista actual de *commiters* en un fitxer a l'arrel del repositori anomenat
   ``MAINTAINERS``. Ha de contenir el nom i adreça de correu electrònic de cada
   persona.
   
.. sub:: Donar permís de lectura del repositori principal a tothom
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació; Document

   Tothom ha de poder llegir i clonar el codi.
   
.. rec:: Donar permís d'escriptura al repositori principal a desenvolupadors externs confiables
   :tags: Plugin; NouProducte; Publicació

   Si una persona porta molt temps fent contribucions de qualitat al projecte, a
   un nivell semblant que les persones contractades per l'Ajuntament, se la pot
   premiar amb un permís per escriure al repositori. Es corre un risc baix amb
   això, perquè el control de versions fa que tot sigui traçable i els canvis
   revertibles.
   
   Se li ha d'aclarir, per evitar mal entesos, quines seran les regles de
   governança i qui seguirà tenint la darrera paraula a l'hora d'acceptar
   contribucions.
   
.. rec:: Pujar traduccions del fitxer README al repositori principal
   :tags: NouProducte; Publicació
   
   Si els potencials usuaris del projecte son principalment locals, pot ser
   convenient traduir el contingut del fitxer ``README`` o part del mateix. Això
   es pot fer posant nous fitxers a l'arrel del repositori, amb noms com
   (suposant que el llenguatge de marques utilitzat sigui Markdown, i d'aquí
   l'extensió ``.md``): ``README.ca.md`` o ``README.es.md``. En aquest cas convé
   enllaçar totes aquestes traduccions entre elles, al principi de cada fitxer.
   Un exemple es pot veure a `https://github.com/tiimgreen/github-cheat-sheet
   <https://github.com/tiimgreen/github-cheat-sheet>`_.
   
.. mes:: Especificar al README una persona de contacte del projecte
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
   
.. mes:: No pujar al repositori fitxers binaris ni fitxers producte del procés de build (amb excepcions)
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació
   
   Excepcions:
   
   - Petites imatges (logos generals del projecte, etc.)
   
.. mes:: Mantenir la informació de configuració en fitxers separats i en un altre repositori (3.4)
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
   
.. rec:: Re-sincronitzar cada setmana el repositori propi amb el repositori del projecte upstream
   :tags: Adaptació
   
   Per permetre finalment integrar els nostres canvis, i que les nostres
   notificacions de defectes tinguin sentit.
   
Gestor d'incidències
====================

Una eina que tots els projectes de codi obert necessiten és un gestor
d'incidències. Als projectes de l'Ajuntament li assignarem les següents
funcions:

- Notificar els defectes detectats (*bug tracker*) per part tant d'usuaris com
  de desenvolupadors. També fer-ne transparent el tractament, evolució i
  eventual solució. És important que els *commit* que resolen un defecte o
  assenyalin en el seu missatge. `GitHub té una sintaxi especial per fer això
  <https://help.github.com/articles/closing-issues-using-keywords/>`__.
- Fer seguiment de les tasques pendents. Això permet després vincular un o més
  *commit* amb el tancament d'una tasca. També poder veure a qui s'assignen les
  tasques i com es prioritzen. Opcionalment s'hi poden especificar dates
  estimades de realització. Tot plegat contribueix a la transparència i
  traçabilitat del procés de desenvolupament.
- Fer seguiment de com es gestionen les contribucions de diferents parts,
  mitjançant el mecanisme de *pull request*. Fins i tot es pot obrir el gestor
  d'incidències a peticions de funcionalitats (*feature request*) i es pot
  utilitzar l'espai de GitHub com a lloc on es prioritzen i gestionen de manera
  pública.
  
S'ha de tenir en compte que el gestor d'incidències no és només important per al
dia a dia dels desenvolupadors, sinó que molts observadors del projecte també el
fan servir com a mesura de fins a quin punt estan davant d'un projecte seriós.

Aquest gestor d'incidències ha d'estar operatiu i públic durant tota la vida
útil del producte, més enllà de la duració que tinguin els contractes amb
l'Ajuntament.

.. mes:: Vincular el repositori principal al gestor d'incidències de GitHub
   :tags: Dia1; Adaptació; Plugin; NouProducte; Publicació

   De nou és la opció per defecte, en aquest cas per la seva vinculació
   automàtica amb el repositori de GitHub i perquè compleix els nostres
   requeriments d'accessibilitat i transparència.
   
   S'hauran d'establir des de l'inici algunes categories bàsiques
   d'incidència, que després poden modificar-se segons les necessitats de
   cada projecte: ``Bug``, ``Request``, etcètera.

.. alt:: Vincular el repositori principal a un gestor d'incidències públic
   :tags: Dia1; Adaptació; Plugin; NouProducte; Publicació
   
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
   
.. rec:: Utilitzar el gestor d'incidències per tasques, entregues i noves funcionalitats
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació

   La integració entre el repositori i el *issue tracker* de GitHub fa que en
   combinació siguin una bona eina per col·laborar en la realització de
   qualsevol tasca relacionada amb el codi, i no només la resolució de *bugs*.
      
.. mes:: Redactar i mantenir una política de gestió d'incidències
   :tags: Contractar; Plugin; NouProducte; Publicació
   
   Ha d'especificar:
   
   - Tipus d'incidència (deficiències, tasques, *milestones*, etc).
   - Etapes per les que passen.
   
   Se li pot encarregar aquesta tasca a l'adjudicatari. Si no en té una de
   pròpia l'IMI n'hauria de proporcionar una per defecte.
   
.. rec:: Donar permisos per reportar incidències a tothom, fins i tot anònimament
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació

   Configurar el gestor d'incidències per tal que no sigui imprescindible
   crear-s'hi un compte per fer-hi reportar *deficiències* o qualsevol altre
   element, per facilitar al màxim les aportacions. Activar les mesures
   anti-spam que siguin necessàries (per exemple *captchas*).

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
   
.. mes:: Fer la notificació de defectes al bug tracker oficial del producte a modificar
   :tags: Contractar; Adaptació; Plugin

   Quan estem adaptant un producte existent, una de les majors contribucions que
   podem fer al projecte és ajudar a detectar, aïllar i solucionar deficiències
   que pugui tenir.

   Cal obligar per contracte als adjudicataris a prendre's la molèstia de
   notificar correctament les deficiències, d'acord amb les directrius de cada
   projecte, per ajudar a millorar el producte *upstream*.

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

Els primers canals de comunicació entre desenvolupadors son els missatges de
*commit* del repositori i els fils del gestor d'incidències. Moltes decisions
tècniques es prenen en aquests fils, però convé que les discussions que s'hi
duen a terme siguin sempre molt focalitzades i estrictament tècniques. Quan
l'àmbit de la discussió s'eixampla, cal recórrer a d'altres canals.

Tots els projectes nous han de crear inicialment una llista de correu o fòrum de
discussió per a desenvolupament, amb arxius públics. En aquest canal és on es
demana la opinió a les diferents parts o persones que participen en el projecte,
i on es prenen les decisions estratègiques.

Inicialment hi haurà poca distància en quant a inquietuds i llenguatge entre els
desenvolupadors i els primers usuaris (*early adopters*), que acostumen a estar
molt motivats. Per això, en molts casos podran compartir el mateix canal. Més
endavant pot ser necessari crear canals de comunicació especialitzats pels
diferents tipus de participant.

Depenent de la naturalesa i composició de l'equip, pot resultar convenient
disposar també d'un xat que permeti una comunicació més immediata. De tota
manera el xat és complementari amb la llista o fòrum, mai l'ha de substituir. La
llista o fòrum és on queda registrada de forma referenciable tota la història
del projecte (debats, decisions, etcètera), que és un actiu molt valuós per a
tota la comunitat present i futura del projecte.

.. mes:: Crear una llista o fòrum de desenvolupament que inicialment servirà també per usuaris
   :tags: Plugin; NouProducte; Publicació

   Inicialment el projecte tindrà un sol fòrum de discussió dedicat que
   compartiran tant les persones que realitzen el desenvolupament com aquelles
   que simplement siguin usuàries del producte (*early adopters*).

   Recomanem utilitzar l'eina `Discourse <https://discourse.org/>`_, que fusiona
   les llistes de correu tradicionals amb un fòrum via web. Cal activar les
   opcions per a que qui ho desitgi pugui fer tota la interacció a través de
   correu electrònic. Un projecte que utilitza aquesta eina i que està en proves
   a l'Ajuntament és `Alvus <https://alvus.barcelona>`_.

   Alternativament podem utilitzar Mailman 3. La llista es pot dir
   ``NOM-DEL-PROJECTE-dev``.
   
   Activar l'arxiu i utilitzar-lo profusament.
   
   Inicialment en català i/o castellà. Quan apareguin participants en altres
   llengües, crear una llista en anglès.

   Els principals desenvolupadors hi han de ser presents, però no tenen
   obligació de respondre a totes les peticions. Al fòrum o llista cadascú hi
   intervé a títol individual. Fa més confiable el producte que es pugui
   contactar amb les persones que hi ha a darrera.
   
.. rec:: Crear una llista de correu per persones que usen el producte, si el projecte creix
   :tags: Plugin; NouProducte; Publicació
   
   Activar l'arxiu.
   
.. rec:: Crear un xat de desenvolupament per la comunicació immediata de l'equip
   :tags: Plugin; NouProducte; Publicació
   
   Usar `gitter.im <https://gitter.im>`_ o `riot.im <https://riot.im>`_.
   
.. mes:: Usar els pull-requests de GitHub per fer revisions de codi públiques de totes les contribucions externes
   :id: M_BD2
   :tags: Plugin; NouProducte; Publicació
