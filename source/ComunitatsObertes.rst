******************
Comunitats obertes
******************

En un projecte de codi obert hi ha molts nivells de participació, i convé no
tancar-se a cap d'ells. A més del l'equip principal de desenvolupament,
normalment persones contractades per a tal fi, pot haver-hi col·laboracions
puntuals o continuades per part d'altres persones. Aquest capítol es centra en
els aspectes més socials de com treballar en el tipus de comunitat que es crea
al voltant d'aquests projectes.

Contribuir en comunitats obertes
================================
   
El concepte de contribució va més enllà del codi. També pot consistir en:

- Traduccions
- Documentació
- Notificació de deficiències (*Bug reports*)
- Altres

Una norma bàsica és que les contribucions son sempre individuals, tant en els
nostres projectes com quan contribuïm a projectes externs. Això vol dir que es
pot traçar sempre quina persona concreta l'ha realitzat, encara que treballi o
participi en nom d'alguna organització. Les raons d'això son que:

- És l'única entitat per la que els projectes de codi obert estan
  estructuralment equipats per gestionar.
- Dins dels projectes de codi obert la reputació és com la moneda que fa
  funcionar tota la maquinària, i aquesta es guanya o es perd de forma
  individual. Segons la solidesa demostrada en contribucions anteriors es
  confiarà més o menys en el codi que ha fet algú, les seves opinions als canals
  de comunicació i presa de decisions tindran més o menys pes, etc.
- Els desenvolupadors que treballen habitualment en projectes de codi obert
  estan acostumats a aquest model. Fa més senzilles les interaccions quan es
  col·labora a distància. També és d'interès per ells per construir-se una
  carrera professional.

L'altra consideració important en aquest apartat, aplicable si volem modificar
un component extern ja existent, és que sempre és molt convenient que les
nostres modificacions al codi quedin incorporades, tard o d'hora, al producte
original. Amb això aconseguim:

- Reduir el cost futur de manteniment. Si la integració és total, pot ser fins i
  tot que el manteniment de les funcionalitats integrades ens surti a cost 0.
- Beneficiar-nos de futures millores del producte original aportades per altres
  parts.
- Si més gent utilitza la nostra funcionalitat, l'Ajuntament apareixerà com una
  institució que aporta al projecte i al comú global de les comunitats de
  programari lliure. Això a la llarga li pot donar capacitat prestigi i
  influència.

Tenir en compte, però, que podem planificar per facilitar aquesta integració,
però normalment no podrem garantir que es produeixi en les etapes inicials d'un
projecte. Cada comunitat té les seves regles de governança i presa de decisions,
i s'han de respectar. Però el que sí convé fer és informar en tot moment dels
nostres plants i intentar que convergeixin amb els de la comunitat a la que ens
adrecem. Com diu a
`<http://producingoss.com/en/contracting.html#community-review-acceptance>`_:

   "No pensis en l'escrutini de la comunitat com un obstacle a salvar, pensa
   en ell com un equip de disseny i un departament de qualitat a cost zero.
   [L'escrutini i participació de la comunitat] És un benefici a buscar
   agressivament, no un obstacle a suportar".

.. mes:: Fer que l'autoria de cada contribució (codi, documentació o missatge) sigui individual
   :tags: Adaptació; Plugin; NouProducte
   
   No amagar les contribucions de l'equip, ni a un projecte propi, ni a un
   d'extern, sota una identitat corporativa. És a dir, tant als *commit* al
   repositori, com quan es participa en canals de comunicació del projecte o en
   eines de gestió, utilitzar noms d'usuari i adreces de correu individuals de
   cada persona participant.
   
   Si un mateix individu contribueix a un projecte de programari a vegades com a
   treballador contractat directament o indirecta per l'Ajuntament, i d'altres
   vegades com a voluntari en el seu temps lliure, aleshores ha d'utilitzar dues
   adreces de correu diferents, segons el cas:
   
   - Una de personal quan faci contribucions voluntàries.
   - Una de l'empresa, o bé una proporcionada per l'Ajuntament, quan compleixi
     amb tasques especificades al seu contracte.

.. mes:: Informar dels nostres plans a les comunitats tècniques del component a modificar
   :tags: Adaptació
   
   Si el que volem és modificar i adaptar un component ja existent, cal que
   siguem oberts i clars respecte de les nostres motivacions. En ser el
   component de programari lliure, no ens poden negar fer-hi modificacions. No
   obstant això, és molt convenient informar prèviament de les nostres
   necessitats, i de la nostra planificació tècnica.

   Cal esforçar-se per tal que la comunitat de suport del component a modificar
   entengui i s'involucri en la nostra proposta.
   
.. rec:: Informar dels nostres plans a d'altres comunitats tècniques rellevants
   :tags: Adaptació; Plugin; NouProducte
   
   Les comunitats de programari lliure acostumen a estar molt interessades en
   aportar idees, coneixement tècnic, i fins i tot hores de feina més enllà
   d'això, davant de reptes tècnics i projectes que creguin que les poden
   beneficiar.
   
   Els projectes de l'IMI estudiaran les possibilitats de col·laboració amb les
   comunitats locals de programari lliure i tecnologies innovadores per promoure
   la innovació social i tecnològica.
   
.. mes:: Contractar desenvolupadors reconeguts dins del projecte que es vol modificar
   :tags: Contractar; Adaptació; Plugin
   :links: A_1F9
   
   Pot ser directament o a través del contracte amb una empresa o cooperativa
   adjudicatària.
   
   Mai hi ha garanties de que les modificacions que necessitem fer seran
   acceptades dins del producte original, però comptar amb desenvolupadors
   reconeguts és la via que ens dóna més opcions d'aconseguir-ho. Aquests poden
   aportar, a més del coneixement tècnic que puguin tenir:
   
   - Una visió des de dins de quines propostes tècniques poden tenir millor
     acceptació.
   - El valor que aporta ser una veu respectada dins de la comunitat que pren
     decisions.
   
.. alt:: Obligar a l'adjudicatari a mesures que facilitin integrar els canvis al producte original
   :tags: Contractar; Adaptació
   
   Això inclou:
   
   - Descriure amb claredat les tasques col·laboratives en que s'espera que
     l'adjudicatari s'involucri, i explicar que això forma part del pressupost,
     com es descriu a la `Mesura: Pressupostar el sobrecost de participar en la
     comunitat oberta del producte a modificar
     <#h:a6bb27a3-2b23-4585-81ca-dc5b4d29ccd7>`__.
   - Que l'adjudicatari accepti i apliqui les Directrius de desenvolupament, les
     normes de redacció de documentació i el Codi de conducta del projecte, si
     en té, o altres documents escrits que regulin les normes que puguin
     existir, tant generals com a les específiques per canals de comunicació
     concrets. En cas de que el projecte no hagi formalitzat un corpus propi de
     normes internes, aplicaran les normes usuals de *netiqueta*, p.ex.
     https://www.ietf.org/rfc/rfc1855.txt.
   - Que determinats perfils de l'adjudicatari es creïn usuaris als canals de
     comunicació del projecte.
   - Que s'informi periòdicament a la comunitat de les modificacions
     planificades, de la part executada, de les decisions tècniques que es van
     prenent.
   - Que s'informi puntualment a l'IMI de tot el *feedback* rebut per part de la
     comunitat, tant positiu com negatiu, sobre les pretensions d'integrar nova
     funcionalitat.
   
   El personal de l'IMI haurà de fer seguiment de tot això i potser intervenir
   directament en els debats de la comunitat.
   
.. mes:: Penalitzar els adjudicataris si hi ha canvis en la plantilla del projecte
   :tags: Contractar; Adaptació; Plugin; NouProducte
   
   A tenir en compte en la redacció del plec de contractació.
   
   Una alta rotació penalitza qualsevol projecte, però especialment quan es
   participa en projectes de codi obert. Els desenvolupadors que marxen no només
   s'emporten amb ells un el coneixement tècnic que puguin acumular, sinó el seu
   estatus dins la comunitat i les relacions humanes que hi puguin haver
   desenvolupat.
   
.. mes:: Pressupostar el sobrecost de participar en la comunitat oberta del producte a modificar
   :tags: Contractar; Adaptació; Plugin

   S'ha d'especificar de la manera més detallada possible com i en quina mesura
   l'IMI espera que l'adjudicatari s'involucrarà en el projecte i difondrà les
   funcionalitats a desenvolupar, tant en:

   - Les comunitats de desenvolupament implicades
   - Potencials usuaris i usuaries
   
.. rec:: Mantenir un canal de comunicació privat permanent per discutir conflictes d'interès
   :tags: Adaptació; Plugin
   
   Idealment un fil de correu.
   
   Quan es contracta gent per participar en un projecte de codi obert ja
   establert, sobretot si son desenvolupadors que ja participaven al projecte,
   els interessos del projecte de l'Ajuntament i els del projecte de codi obert
   original poden entrar en conflicte. Els desenvolupadors tindran la sensació
   que han de servir a dos caps i que no sempre es pot satisfer als dos.
   
   S'ha de demanar màxima transparència en aquests casos i intentar anticipar
   aquestes situacions.
   
Gestió i governança de comunitats obertes
=========================================

.. mes:: Donar reconeixement a les persones que fan contribucions al projecte
   :tags: Plugin; NouProducte
   
   En un fitxer ``CONTRIBUTORS`` a l'arrel del repositori. A nivell
   individual.
   
.. rec:: Pressupostar el sobrecost d'incentivar la creació d'una comunitat oberta
   :tags: NouProducte
   
   Això inclou coses com que els desenvolupadors dediquin temps a:
   
   - Revisar codi de tercers
   - Respondre missatges als canals de comunicació del projecte
   - Intervenir a StackOverflow
   
.. mes:: Redactar i actualitzar un document intern establint el grau de compromís que volem tenir amb cada part
   :tags: NouProducte
   
   Prestar especial atenció als possibles *early adopters*.
   
.. rec:: Establir per contracte que l'adjudicatari ha d'incloure contribucions externes si ho decideix l'Ajuntament
   :tags: Contractar; Plugin; NouProducte
   
   .. admonition:: Exemple de clàusula: **Contribucions externes**.
   
      Durant la duració del contracte, incloent el període de garantia,
      l’adjudicatari té l’obligació d’integrar aquelles contribucions externes
      que l’Ajuntament de Barcelona consideri que milloren el codi o la
      documentació pública i que no impliquen el desenvolupament de
      funcionalitat no prevista en el contracte per part de l’adjudicatari, per
      exemple aquelles que solucionen bugs.
   
.. mes:: Publicar unes breus Directrius per desenvolupadors (Developer Guidelines)
   :tags: Dia1; Plugin; NouProducte; Publicació
   
   Aquesta guia estableix les convencions tècniques i socials que determinen les
   interaccions entre desenvolupadors, i entre desenvolupadors i usuaris. És
   d'aplicació per tots els desenvolupadors, tant els contractats per
   l'Ajuntament, com els externs, com el personal del mateix Ajuntament.
   
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
   
   - El fitxer ``README`` del repositori principal.

.. rec:: Publicar unes Directrius per desenvolupadors (Developer Guidelines) detallades (si el projecte creix)
   :tags: Plugin; NouProducte; Publicació
   
   Per projectes grans, i sense que sigui la primera mesura a prendre, pot ser
   interessant treballar i publicar unes Directrius per desenvolupadors més
   extenses i detallades que el que es proposa a la `Mesura: (Dia 1) Publicar
   unes breus Directrius per desenvolupadors (*Developer Guidelines*)
   <#publicar-breus-directrius-desenvolupadors>`__.
   
   Coses que s'hi poden incloure:
   
   - Convencions de codificació
   - Convencions per a la documentació
   
   Alguns exemples:
   
   - `<http://subversion.apache.org/docs/community-guide/>`_
   - `<https://wiki.documentfoundation.org/Development>`_
   
.. rec:: Redactar un model de governança per la comunitat global que dona suport al producte
   :tags: NouProducte; Publicació
   
   Els projectes que generen sistemes i eines completament FOSS a través d'un
   servei de desenvolupament promogut i finançat per l'Ajuntament hauran
   d'incloure un model de governança que inclogui, entre d'altres: una
   aproximació a la definició de la comunitat (d'altres Ajuntaments,
   especialistes com geodata [??] o biblioteques, etc.), les eines de suport, la
   comunicació i el marketing, els processos per la inclusió de contribucions
   externes, la gestió de la propietat intel·lectual i la sostenibilitat més
   enllà del projecte.
   
   La governança de la comunitat i la gestió tècnica d'aquests projectes,
   inclosa l'aprovació del codi per a la seva incorporació al projecte i la
   definició de requeriments (*roadmap*), son aspectes diferents. Es promourà la
   diversitat de contribucions però l'IMI mantindrà el control efectiu dels
   desenvolupaments finançats per fons públics.

Ús adequat dels canals de comunicació
=====================================
   
.. mes:: Evitar els debats privats
   :tags: Adaptació; Plugin; NouProducte
   
   És molt temptador tenir fòrums de debat tancats on un petit grup de persones
   discuteixen tots els aspectes del projecte, tant a nivell tècnic com social,
   i que d'allà en surtin les decisions. Però convé tenir molt en compte que en
   els projectes de codi obert resulten imprescindible els canals de comunicació
   oberts i públics, que tothom pot llegir i als que tothom es pot subscriure
   amb certa facilitat. Les raons son les següents:
   
   - És molt difícil que la gent vulgui fer contribucions significatives a un
     projecte on les decisions es prenen de forma opaca i com a política de fets
     consumats. Això no vol dir que la governança del projecte hagi de funcionar
     com una democràcia. El requisit primordial és la **transparència**: la gent
     voldrà saber per què i com es prenen les decisions, i potser també dir-hi
     la seva, sense que necessàriament la opció que proposen sigui l'escollida.
     Els desenvolupadors experimentats saben que el projecte té unes necessitats
     i que no tothom pot participar en les decisions amb el mateix pes. Que al
     final les decisions les prengui l'Ajuntament és quelcom que tothom entendrà
     si es deixa clar des de l'inici, com s'especifica a la `Mesura: (Dia 1)
     Publicar unes breus Directrius per desenvolupadors (*Developer Guidelines*)
     <#publicar-breus-directrius-desenvolupadors>`__.
   - És sorprenent la quantitat de bones idees que desinteressadament poden
     arribar a través dels canals de comunicació públics, si en aquests es
     discuteixen tots els aspectes del projecte i hi ha un clima de treball
     cordial.
   - Si les comunicacions es fan en llistes de correu públiques i arxivades, es
     pot consultar tot l'historial de decisions i no tornar a repetir debats.
   - Que els canals siguin oberts i públics incentiva una cultura comunicativa
     més eficaç, educada i assertiva.
   
.. mes:: Establir el "Contributor Covenant" com a Codi de conducta del projecte i dels seus canals de comunicació
   :tags: Plugin; NouProducte
   
   El **Codi de conducta** d'un projecte és un document o conjunt de documents
   que regulen les normes socials d'actuació per als participants en el
   projecte, incloent els següents aspectes:
   
   - Normes de participació en tots els canals de comunicació telemàtics
     associats al projecte, tals com xats, llistes de correu públiques i
     privades, eines de seguiment d'incidències (*issue trackers*), eines de
     desenvolupament de funcionalitats i *pull-requests*, wikis, blogs, Twitter,
     fòrums, etc.
   - Normes de conducta per activitats presencials de la comunitat associada al
     projecte, tals com trobades i congressos.
   
   Un codi de conducta serveix per tenir una referència escrita de quins
   comportaments es consideren inadequats per als participants del projecte. En
   concret el de `<https://www.contributor-covenant.org/>`_ l'utilitzen
   darrerament molts projectes de codi obert, i per tant pot ser que molts
   desenvolupadors ja hi estiguin familiaritzats. També es troba traduït a
   vàries llengües.
   
   Enllaçar com a mínim des de:
   
   - El fitxer ``README`` del repositori principal.
   - Les Directrius per desenvolupadors de la mesura *Mesura: (Dia 1) Publicar
     unes breus Directrius per desenvolupadors (*Developer Guidelines*)*.
   
.. mes:: No deixar passar cap insult o atac personal als canals de comunicació
   :tags: Plugin; NouProducte
   
   Convé mantenir una política de tolerància zero en aquest aspecte. Això no vol
   dir expulsar a la gent a la primera de canvi (en ocasions no serà ni tan sols
   possible), vol dir que algú s'ha d'encarregar de fer constar sistemàticament
   que certs comportaments no es toleren en aquest projecte.
   
   Si es considera oportú, es pot fer referència a les seccions pertinents del
   Codi de conducta (`Mesura: Establir el "Contributor Covenant" com a Codi de
   conducta del projecte i dels seus canals de comunicació
   <#h:c3405dee-679e-42e0-9ba6-141a0ad06965>`__).
   
   A `<http://producingoss.com/en/setting-tone.html#prevent-rudeness>`_ es donen
   alguns detalls de com gestionar aquestes situacions.
