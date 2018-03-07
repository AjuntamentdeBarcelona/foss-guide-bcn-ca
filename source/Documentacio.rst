************
Documentació
************

.. mes:: Utilitzar, per a tota la documentació del projecte, formats de wiki o formats de marques oberts
   :tags: Integració; Plugin; NouProducte; Publicació

   Per la web orientada a usuaris del projecte és acceptable escriure
   directament HTML. La resta de documentació, estigui o no inclosa en el
   repositori de codi, estarà en el format de wiki corresponent, o bé en un dels
   següents formats:
   
   - ReStructuredText (és el que fa servir per defecte Sphinx)
   - Markdown
   - Org Mode
   
.. mes:: Documentar el projecte per tal que tercers siguin capaços d'entendre'l, configurar-lo i desplegar-lo
   :tags: Contractar; Integració; Adaptació; Plugin; NouProducte
      
   Les entitats adjudicatàries de contractes –tant de desenvolupament com de
   desplegament– han d'entendre que no tindran el monopoli de la configuració,
   el desplegament i el manteniment del producte.
   
.. mes:: Crear i mantenir un Manual d'ús a la wiki de GitHub del projecte
   :tags: Integració; Plugin; NouProducte; Publicació
      
   Des de ben aviat hi ha d'haver una documentació accessible via web que
   expliqui com utilitzar el producte a diferents nivells o per a diferents
   rols: usuaris corrents, administradors, etcètera. En el cas de llibreries de
   codi els usuaris son programadors que no participen en el projecte.
   
   S'ha de valorar bé en quins idiomes ha d'estar aquesta documentació, depenent
   de quin sigui l'àmbit esperat d'ús del producte. Es pot tenir el català o el
   castellà com a llengua principal de la documentació, però com a mínim les
   tasques principals d'administració cal també explicar-les en anglès. Si
   arriben mostres d'interès des d'altres territoris, convindrà que tota la
   documentació d'usuari es trobi també traduïda a l'anglès. En el cas de
   llibreries de codi o eines de desenvolupament, tota la documentació ha
   d'estar des de l'inici en anglès.
   
   La documentació mai serà complerta i estarà en constant evolució. Per això
   convé que sigui fàcilment actualitzable per diferents persones i recomanem
   inicialment usar una wiki. Fer servir la mateixa wiki de GitHub ens evita
   haver de preparar més infraestructura i fa que la documentació es trobi
   automàticament enllaçada des de la pàgina web del repositori.
   
   Fins que no hi hagi molta documentació d'usuari/-a, és recomanable
   mantenir-la tota junta en una mateixa pàgina de la wiki, amb una taula de
   continguts a l'inici, i no subdividir-la en pàgines, ja que així es facilita
   la cerca de paraules clau utilitzant les funcions de cerca del navegador. Des
   d'aquesta pàgina convé enllaçar la resta d'elements de documentació com les
   instruccions d'instal·lació, possibles tutorials, o la possible llista de
   FAQ.
   
   Enllaçar des de:
   
   - La web del projecte.
   - El fitxer ``README`` del repositori principal.
   
.. alt:: Crear i mantenir un Manual d'ús en Sphinx i publicar-lo a les GitHub Pages
   :tags: Plugin; NouProducte

   Aquesta és una alternativa per a projectes que creixen molt i que
   possiblement hagin començat posant la documentació a la wiki. S'ha de
   traspassar tota la informació que hi hagi a la wiki al nou format, i eliminar
   la wiki per no confondre als usuaris. Si es té clar des del principi que el
   projecte requerirà una bona quantitat de documentació, es pot optar des de
   l'inici per aquesta via.
   
   Tota la documentació anirà a un subdirectori ``doc`` dins de l'arrel del
   repositori i s'escriurà o bé en ReStructuredText o bé en Markdown, els dos
   llenguatges de marques que suporta Sphinx.
   
   En aquest cas, per tractar-se de projectes grans i que han d'aspirar a
   arribar a públics amplis, la documentació haurà d'estar necessàriament en
   anglès, sense perjudici de que es pugui traduir a d'altres llengües.
   
   Tenir el codi i la documentació en un mateix repositori, lluny de ser un
   problema, facilita que ambdós vagin sincronitzats i que això quedi reflectit
   a l'historial de *commits*.
   
   Enllaçar des de:
   
   - La web del projecte.
   - El fitxer ``README`` del repositori principal.
   
   Un exemple el podem trobar a:
   `<https://github.com/commercialhaskell/stack/tree/master/doc>`_
   
.. rec:: Crear i mantenir un llistat de FAQ
   :tags: NouProducte; Publicació
   
   Si es realitza de forma reactiva però diligent, amb preguntes reals dels
   usuaris, pot facilitar molt que la gent trobi ràpidament la informació que
   necessita i pot resultar una manera molt rentable d'invertir els recursos del
   projecte.
   
.. rec:: Crear un tutorial explicant com fer pas a pas algunes tasques habituals
   :tags: Plugin; NouProducte; Publicació
   
.. mes:: Pujar un fitxer amb instruccions d'instal·lació al repositori principal
   :tags: Dia1; Integració; Plugin; NouProducte; Publicació
   
   El procediment d'instal·lació desenvolupat a la `Mesura: (Dia 1) Implementar
   procediments de *build* i instal·lació amb eines lliures i d'ús estès
   <#implementar-procediments-build-installacio>`__ ha d'estar explicat en un
   fitxer ``INSTALL`` a l'arrel del repositori principal.
   
   S'ha de redactar en anglès i el format ha de ser text amb algun llenguatge de
   marques lleuger.
   
   Convé incloure alguna mesura o comanda de diagnòstic que permeti a l'usuari
   saber si la instal·lació s'ha executat correctament (per exemple, executar un
   joc de proves, i especificar el resultat esperat).
   
   El fitxer d'instal·lació ha d'estar enllaçat com a mínim des de:
   
   - El fitxer ``README`` del repositori principal.
   
.. rec:: Complementar la documentació d'usuari/-a amb captures de pantalla, vídeos o demos
   :tags: NouProducte

   Per projectes web grans que vulguin atraure l'atenció de moltes persones, el
   millor reclam és un *demo site*.
   
   Un vídeo explicant l'ús i les característiques de l'eina també pot resultar
   molt atractiu.
   
   Si el producte té una interfície d'usuari gràfica, és molt recomanable
   acompanyar les explicacions amb captures de pantalla. També es poden
   utilitzar en el llistat de funcionalitats descrit a la `Mesura: Especificar
   en llocs fàcilment accessibles un llistat de funcionalitats
   <#h:2dc43f4e-e755-4fe5-be4e-1f9dd58fe9e9>`__.
   
.. mes:: Especificar, en un lloc visible, una llicència de distribució per al Manual d'ús
   :tags: Integració; Plugin; NouProducte; Publicació

   Per defecte utilitzar la llicència `Creative Commons Zero v1.0 Universal
   <https://creativecommons.org/share-your-work/public-domain/cc0>`__ (CC0-1.0).
   
   Un resum de les seves característiques es pot trobar a:
   https://tldrlegal.com/license/creative-commons-cc0-1.0-universal.
   
   En el cas de la documentació no té per què fer-se servir la mateixa llicència
   que per al programari en sí, i de fet en aquest cas sí que son admissibles
   les llicències de Domini Públic).
   
   En cas de crear documentació per projectes externs, utilitzar les llicències
   que aquests projectes ja estiguin fent servir.
   
.. mes:: Especificar, en un lloc visible, una llicència de distribució per als documents de disseny i estudis encarregats
   :tags: Document
   
   Per defecte utilitzar la llicència `Creative Commons Attribution Share Alike
   4.0 <https://creativecommons.org/licenses/>`__ (CC-BY-SA-4.0).

   Seguir: `<https://wiki.creativecommons.org/wiki/Website/Publish>`__ i
   `<https://creativecommons.org/choose/#metadata>`__.
   
   Per entendre les seves característiques es pot consultar:
   `<https://tldrlegal.com/license/creative-commons-attribution-sharealike-4.0-international-(cc-by-sa-4.0)>`_.
