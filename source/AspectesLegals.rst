***************
Aspectes legals
***************

Els projectes de codi obert es basen en un conjunt de tecnologies, mètodes de
treball i maneres de col·laborar, però tot plegat no se sostindria sense un
dispositiu legal molt especial que son les llicències de programari lliure. L'ús
de llicències lliures garanteix de per sí una sèrie de drets inalienables, el
que permet en certa manera flexibilitzar la política de propietat intel·lectual
(PI).

Propietat intel·lectual
=======================

Fins ara, els contractes amb proveïdors establien que tot el software
desenvolupat per a l'Ajuntament en el context del contracte, així com la
documentació associada, son propietat de l'Ajuntament.

Amb les llicències lliures, encara que no es tingui la propietat legal del codi,
aquest es podrà utilitzar tants cops com sigui necessari i per la tasca que es
desitgi, a més de poder modificar-lo, adaptar-lo i redistribuir-lo. Així que
l'Ajuntament podria renunciar a tota la PI, però de moment i de manera
conservadora la seguim reclamant, com a política per defecte (amb les excepcions
que s'indiquen a les alternatives de més avall). L'única cosa que no es pot fer
sense ser els propietaris legals del codi és re-llicenciar.

El principal criteri per valorar qui s'ha de quedar amb la PI en el cas de
projectes nous és pensar quina entitat garanteix millor que es prendran en cada
moment les mesures adequades per difondre el projecte, facilitar contribucions
de tercers, fer-lo créixer fins assolir els objectius i fer-lo sostenible a
llarg termini.

.. mes:: Establir l'Ajuntament de Barcelona com a propietari del nou codi font i la nova documentació
   :id: M_4DC
   :tags: Contractar; Adaptació; Plugin; NouProducte; Publicació
   :links: A_C87; A_EE9; A_3B6

   És la opció per defecte, però no la única. Se li imposa al contractista una
   cessió de titularitat de tot el codi i documentació generades.

   Té especialment sentit que l'Ajuntament vulgui concentrar tots els drets de
   propietat sobre projectes emblemàtics, d'utilitat principalment entre
   administracions públiques, i sobre els quals pretengui determinar en gran
   mesura les regles de governança.

.. alt:: Cedir la propietat del nou codi font al propietari legal del codi original
   :tags: Contractar; Adaptació

   Quan adaptem un producte ja existent, pot ser que per acceptar la inclusió
   del nostre codi al producte original ens demanin signar una CLA o contracte
   equivalent. Si no és així les parts de desenvolupi l'Ajuntament poden ser de
   la seva propietat.

.. alt:: Cedir la propietat del codi font a una entitat independent sense ànim de lucre
   :tags: Contractar; Plugin; NouProducte; Publicació

   Hi ha una tercera opció, si l'objectiu és que la titularitat recaigui
   finalment en una entitat externa encarregada de la gestió i governança del
   projecte a llarg termini. Per la naturalesa de la funció a realitzar, aquesta
   entitat tindrà normalment forma legal de fundació. Això té sentit en
   projectes on, a més de l'Ajuntament, hi participin financerament i en la
   presa de decisions d'altres entitats públiques, privades o del tercer sector.
   En aquest cas cal establir per contracte una cessió de drets, que pot ser
   directament a la fundació corresponent, o bé en primer terme a l'Ajuntament,
   que és qui fa el contracte, per tal que sigui aquest qui cedeixi els drets a
   la fundació en un moment posterior.

   Aquesta entitat pot gestionar altres projectes alliberats per l'Ajuntament o
   d'altres entitats associades de l'àmbit públic.

.. alt:: Establir l'empresa o entitat proveïdora com a propietària del nou codi font i la documentació
   :id: A_C87
   :tags: Contractar; Plugin; NouProducte

   Té sentit deixar la titularitat en mans de l'empresa que desenvolupa en cas
   de:
   
   - Components de programari que son d'utilitat general, incloent empreses i no
     només administracions públiques.
   - El proveïdor és una empresa o cooperativa amb una trajectòria contrastada
     de publicació de programari lliure i gestió de comunitats obertes, i té una
     estratègia creïble d'explotació del producte basada en llicències lliures.

Triar una llicència per al codi
===============================

Separarem la decisió en tres casos, depenent de l'escenari:

1. :code:`NouProducte` o :code:`Publicació`: triem, per defecte, la llicència
   AGPL.
2. :code:`Adaptació`: modifiquem un projecte extern ja existent. En aquest cas
   hem de respectar la llicència que ja tingui.
3. :code:`Plugin`: triem una llicència d'ús comú en l'ecosistema en que volem
   integrar un component modular.

.. mes:: Triar la llicència AGPL-3.0 com a llicència de distribució del projecte
   :tags: NouProducte; Publicació
   :links: A_038

   La llicència `GNU Affero General Public License v3.0
   <https://www.gnu.org/licenses/why-affero-gpl.html>`__ (AGPL-3.0) té totes les
   característiques que necessitem per als projectes de l'Ajuntament:
   
   - És una llicència amb *copyleft*, tal com obliga la llei espanyola per a les
     administracions públiques que creïn productes de codi obert, i tal com és
     raonable reclamar a les administracions per evitar una apropiació privada
     del que ha estat finançat amb diner públic.
   - Per aplicacions en que els usuaris interactuen principalment a través
     d'Internet, no permet crear un servei tancat utilitzant programari amb
     aquesta llicència (estableix l'accés per xarxa com una forma de distribució
     a efectes de la llicència). És el que s'anomena a vegades *copyleft* de
     xarxa.
   - L'òrgan de governança de la llicència és el projecte GNU, que és una
     organització sense ànim de lucre que treballa en benefici de les comunitats
     de programari lliure. Per tant, és aquest grup d'activistes i expertes qui
     dissenyarà les futures versions de la llicència (per adaptar-se a noves
     circumstàncies tècniques o legals) i les estratègies de defensa legal front
     a possibles atacs a les llibertats que estableix el seu text.
   
   Les raons principals per triar aquesta llicència com a opció per defecte son
   les següents:
   
   - Pertany a la família de llicències de la GNU GPL, que és la més coneguda.
     La majoria de desenvolupadors estan familiaritzats amb les seves condicions
     i això fa que ningú hagi de dedicar temps a investigar la llicència per
     decidir si vol participar en el projecte o no.
   - Optar per les llicències d'ús més generalitzat redueix el risc de
     fragmentació d'aquest procomú immaterial universal que suposa el programari
     lliure, risc provocat per la proliferació de llicències i les seves
     incompatibilitats recíproques.
   
   **Inconvenient.** Està escrita en anglès. A títol informatiu es poden fer
   servir traduccions a d'altres llengües, però només la versió original té
   validesa legal.

.. alt:: Triar la llicència EUPL-1.2 com a llicència de distribució del projecte
   :tags: NouProducte; Publicació

   La llicència `European Union Public License 1.2
   <https://joinup.ec.europa.eu/page/introduction-eupl-licence>`__ (EUPL-1.2) és
   una llicència creada per la Comissió Europea.
   
   Presenta com avantatge sobre les llicències de la família GNU GPL el fet de
   disposar de traduccions legalment vàlides a totes les llengües oficials de la
   Unió Europea: https://joinup.ec.europa.eu/page/eupl-text-11-12. També en el
   seu disseny s'ha tingut en compte la diversitat legal dels estats membre en
   quant a terminologia sobre copyright, garanties i jurisdicció aplicable.
   
   De la mateixa manera que la AGPL-3.0, disposa de *copyleft* i de *copyleft*
   de xarxa. Les condicions de *copyleft* que estableix en cas d'enllaçat
   (*linking*) amb altres productes son més suaus que les de l'AGPL-3.0, i més
   semblants a les de la LGPL. No obstant això, molts juristes pensen que
   aquestes diferències poden ser irrellevants de cara als tribunals europeus.
   El detall de les diferències amb la GPL-3.0 (i de retruc amb l'AGPL-3.0) es
   detallen a: https://joinup.ec.europa.eu/news/eupl-or-gplv3-comparison-t.
   
   Utilitzar aquesta llicència (en la seva darrera versió, la 1.2) hauria de
   suposar un risc de fragmentació baix pel procomú del programari lliure, ja
   que en el seu redactat estableix compatibilitat explícita amb les principals
   famílies de llicències amb *copyleft*, incloses les de GNU. Es poden trobar
   més detalls sobre la compatibilitat de la EUPL-1.2 amb altres llicències a:
   https://joinup.ec.europa.eu/page/eupl-compatible-open-source-licences.
   
   L'òrgan de governança de la llicència és la Comissió Europea, a través de la
   seva iniciativa Join Up.
   
   **Inconvenient.** És una llicència molt menys coneguda i estesa que les de la
   família GNU GPL. Molts desenvolupadors dubtaran de fer-la servir. En el
   millor dels casos se'ls podrà convèncer de que les seves condicions son molt
   similars a les de l'AGPL-3.0. En el pitjor escenari, preferiran contribuir a
   un altre projecte amb una llicència a la que estiguin habituats.

.. mes:: Utilitzar per a tot el codi que modifica un component ja existent la seva llicència original
   :tags: Contractar; Adaptació

   Quan modifiquem un component, i per tal que les nostres modificacions puguin
   potencialment incorporar-se al producte original, cal respectar la llicència
   que ens ve donada, malgrat en el cas de llicències permissives podríem
   modificar-la.

   En el cas d'un desenvolupament sota contracte, cal especificar en els plecs
   aquesta circumstància.

   Si hem respectat la :ref:`mesura S_58B <mesura_S_58B>`, el component que
   estem modificant tindrà una llicència lliure.

.. mes:: Triar una llicència d'ús comú en l'ecosistema o plataforma tecnològica del component a desenvolupar
   :tags: Contractar; Plugin

   Si hem de construir una extensió endollable a una plataforma existent (el
   *core* de la qual, per la :ref:`mesura S_58B <mesura_S_58B>`, ha de ser
   lliure), tenim un cert marge per triar la llicència. Convé triar una
   llicència entre les més utilitzades dins del *framework* o plataforma en
   qüestió, per tal de facilitar l'acceptació del nou component per part de la
   comunitat. Ens interessa que més gent utilitzi i contribueixi a mantenir el
   nostre component. Si entre aquestes llicències més populars es troben la AGPL
   o la EUPL, les triarem.

Complir amb les obligacions de les llicències
=============================================

.. mes:: Escriure una checklist amb les obligacions de les llicències usades i fer seguiment del seu compliment
   :tags: Integració; Adaptació; Plugin; NouProducte; Publicació

   Cada llicència atorga drets i obligacions diferents, tant per als usuaris com
   per als desenvolupadors. Cal garantir que es compleix amb les obligacions de
   totes les llicències dels components principals del projecte, les hagem triat
   nosaltres o no.
   
   Poden ser de molta utilitat els resums que mostra la pàgina
   https://tldrlegal.com/, per exemple:
   
   -  https://tldrlegal.com/license/gnu-affero-general-public-license-v3
   -  https://tldrlegal.com/license/european-union-public-licence

   També pot servir aquest resum (cal fixar-se sobretot en l'apartat
   "Conditions" de cada llicència): https://choosealicense.com/licenses/.
   
   En el cas de la EUPL també convé llegir el document `Guidelines for users and
   developers
   <https://joinup.ec.europa.eu/page/guidelines-users-and-developers>`__.

.. mes:: Pujar el text de la llicència al repositori principal
   :tags: Dia1; Plugin; NouProducte; Publicació
   
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
   
.. mes:: Incloure la notificació de copyright i de llicència a cada fitxer de codi
   :tags: Adaptació; Plugin; NouProducte; Publicació

   La majoria de llicències especifiquen una condició anomenada en anglès "License
   and copyright notice".
   
   Tots els fitxers de codi del repositori (excloent scripts de *build* o
   d'instal·lació) han de portar a dalt de tot del fitxer una notificació
   que faci explícit quines persones o entitats son propietàries legals del
   codi (en anglès, *copyright holder*), i quina és la llicència que
   estableix els termes de la distribució.
   
   És important assenyalar sota quina versió concreta de la llicència es fa
   la distribució, i recomanem assenyalar que es donarà per realitzada una
   actualització automàtica a futures versions de la llicència quan
   aquestes es publiquin (normalment per adaptar-se a noves situacions
   tècniques o jurídiques que no s'havien pogut preveure), sense necessitat
   d'actualitzar tots els fitxers de codi. En els exemples de més avall
   això s'indica mitjançant frases com "either version X of the License, or
   (at your option) **any later version**" o bé "version X or – as soon
   they will be approved by the European Commission - **subsequent
   versions** of the EUPL".
   
   La notificació ha d'anar obviament dins d'un comentari, utilitzant la
   sintaxi per a comentaris que cada llenguatge de programació utilitzi. I
   ha d'incloure tots els anys en que s'hagin realitzat modificacions al
   fitxer. Aquest seria un exemple, si utilitzem la AGPL-3.0 sobre codi
   java, suposant que el propietari del codi sigui l'Ajuntament de
   Barcelona::

      /* Copyright (C) 2017, 2018 Ajuntament de Barcelona
      *
      * This program is free software: you can redistribute it and/or modify it under
      * the terms of the GNU Affero General Public License as published by the Free
      * Software Foundation, either version 3 of the License, or (at your option) any
      * later version.
      *
      * This program is distributed in the hope that it will be useful, but WITHOUT
      * ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
      * FOR A PARTICULAR PURPOSE. See the GNU General Public License for more
      * details.
      *
      * You should have received a copy of the GNU Affero General Public License
      * along with this program. If not, see <http://www.gnu.org/licenses/>
      */
     
     /* This file implements a system for ...
      */
     
     import ...

   El mateix exemple utilitzant la EUPL-1.2::

      /* Copyright (C) 2017, 2018 Ajuntament de Barcelona
       *
       * Licensed under the EUPL, Version 1.2 or – as soon they will be approved by
       * the European Commission - subsequent versions of the EUPL (the "Licence");
       * You may not use this work except in compliance with the Licence. You may
       * obtain a copy of the Licence at:
       *
       * https://joinup.ec.europa.eu/software/page/eupl
       *
       * Unless required by applicable law or agreed to in writing, software
       * distributed under the Licence is distributed on an "AS IS" basis, WITHOUT
       * WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
       * Licence for the specific language governing permissions and limitations under
       * the Licence.
       */
      
      /* This file implements a system for ...
       */
      
      import ...

.. mes:: Establir un procediment per garantir la integritat de les contribucions
   :tags: Contractar; Plugin; NouProducte; Publicació

   Això significa que de tot el codi inclòs al repositori es té permís de la
   persona que l'ha escrit (que no sempre es la persona que fa el *commit*) per
   ser allà sota les condicions de la llicència del projecte.
   
   Si els propietaris del codi han de ser diferents dels autors (per exemple
   perquè la propietat és de l'Ajuntament de Barcelona), cal aconseguir una
   cessió de drets. Aquesta cessió es pot aconseguir de les següents maneres:
   
   -  Via un contracte tipus "contributor Agreement"
   -  Via el propi contracte de la licitació corresponent
   -  A través directament de la llicència del programari

.. mes:: Obligar a tots el contribuïdors de codi externs a enviar un DCO i signar cada commit
   :tags: Plugin; NouProducte; Publicació

   El **Developer's Certificate of Origin (DCO)** és document utilitzat per
   verificar que els desenvolupadors que fan contribucions al projecte coneixen
   i accepten la seva llicència.
