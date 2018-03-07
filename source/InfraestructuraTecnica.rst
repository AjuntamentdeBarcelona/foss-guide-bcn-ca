***********************
Infraestructura tècnica
***********************

Control de versions i web de desenvolupament
============================================

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
   
Altres canals de comunicació
============================
   
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
