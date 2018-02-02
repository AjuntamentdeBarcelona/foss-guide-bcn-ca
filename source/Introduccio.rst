***********
Introducció
***********

L'Ajuntament de Barcelona disposa d'una política d'ús i desenvolupament de
programari lliure i de codi obert establerta en la `Mesura de govern per a la
digitalització oberta: Programari lliure i desenvolupament àgil de serveis a
l'administració pública
<http://ajuntament.barcelona.cat/digital/ca/documentacio>`_, d'octubre de 2017.

Aquesta política consta d'un seguit de principis i directrius que s'exposen als
documents següents, annexos a la mesura:

- :mesgov:`Codi de pràctiques tecnològiques<guia_adt_2_codi_de_practiques_tecnologiques_cat_2017_af.pdf>`
- :mesgov:`Guia sobre sobirania tecnològica<guia_adt_4_guia_sobre_sobirania_tecnologica_cat_2017_af_2.pdf>`
- :mesgov:`Guia de compra pública de TIC<guia_adt_6_guia_de_compra_publica_tic_cat_af_9en.pdf>`

El present document concreta aquests principis i directrius en un conjunt de
mesures i recomanacions que han de guiar al personal de l'IMI en la gestió
diària de projectes basats en programari lliure, en aspectes com:

- La cerca i disseny de solucions
- La contractació de serveis
- El desenvolupament, implantació i manteniment de sistemes d'informació
- La participació en comunitats obertes

Objectius d'aquesta guia
========================

L'objectiu d'aquesta guia és doble:

#. Facilitar al personal de l'IMI un ús efectiu de tecnologies basades en
   programari lliure i de codi obert, de manera que se n'aprofitin al màxim els
   avantatges i es minimitzin els potencials riscos.
#. Preservar la reputació de l'Ajuntament de Barcelona com a institució que
   col·labora en projectes de programari lliure de manera transparent, confiable
   i tenint en compte les millors pràctiques del sector.

Els beneficis que s'espera obtenir de l'ús de programari lliure i estàndards
oberts es detallen a la pròpia :mesgov:`Mesura de govern per a la digitalització
oberta<le_mesuradegovern_v2.pdf>` (pàgina 22). Els reproduïm aquí:

- **Transparència**: el codi font pot ser examinat i auditat per qualsevol que
  tingui els coneixements tècnics suficients, sense necessitat de permís
  explícit del fabricant o de l’Ajuntament. Sense aquesta propietat es fa
  difícil confiar en la neutralitat i seguretat d’una quantitat creixent de
  processos governamentals i administratius que es troben implementats en forma
  de software, com els processos de votació.
- **Interoperabilitat**: l’ús de formats i estàndards oberts permet que
  diferents sistemes, possiblement de diferents fabricants, funcionin
  conjuntament sense obstacles legals i tècnics. Això obre possibilitats
  d’integració entre diferents sistemes, per exemple per reutilitzar dades i
  millorar processos. També garanteix que no s’obliga als ciutadans i ciutadanes
  a utilitzar solucions tecnològiques de proveïdors específics per interactuar
  amb l’Administració.
- **Sobirania**: la transparència i la interoperabilitat redueixen molt la
  dependència respecte d’estratègies comercials dels fabricants. L’usuari, en
  aquest cas l’Ajuntament, pot decidir amb més llibertat quins sistemes
  evolucionar, redimensionar o substituir, així com establir polítiques pròpies
  en quant a seguretat, privacitat, actualitzacions i accés als sistemes. En el
  cas de les organitzacions, la sobirania també fomenta el control sobre els
  processos propis i la generació i conservació de coneixement.
- **Flexibilitat**: els sistemes poden adequar-se millor a les necessitats dels
  usuaris i usuaries, i es poden adaptar i estendre a mida que aquestes
  necessitats evolucionen, sense dependre de cap proveïdor concret. No només el
  desenvolupament és més flexible, també l’avaluació d’alternatives resulta més
  senzilla i barata, i les condicions d’operació i manteniment es poden
  modificar més fàcilment.
- **Sostenibilitat**: la interoperabilitat permet que es puguin substituir
  aquelles parts dels sistemes que cal renovar sense que les dades no quedin mai
  inservibles. Una major sobirania implica també un menor risc d’obsolescència
  de qualsevol part dels sistemes, inclòs el hardware. La col·laboració (entre
  persones i entitats) que promouen les llicències lliures pot ser de gran ajuda
  a l’hora de fer més estable i durador un sistema.
- **Eficiència**: factors com l’estalvi de costos associats al pagament de
  llicències, una major competència entre proveïdors, un menor risc
  d’obsolescència, i la possibilitat de compartir costos amb altres entitats,
  fan que el programari lliure i basat en estàndards oberts sigui la millor
  opció per garantir l’eficiència que la llei exigeix a l’Administració. La
  ingent base de programari combinable existent permet en molts dominis
  aconseguir solucions molt adaptades a la necessitat final amb un baix ús de
  recursos.
- **Fiabilitat i seguretat**: la independència d’estratègies comercials fa que
  l'entitat usuària pugui exigir serveis de major qualitat i aprofitar-se de
  totes les correccions i millores aportades per la comunitat de desenvolupament
  i suport de cada eina.
- **Innovació**: la transparència, i una afortunada combinació de col·laboració
  i competència, fan del programari lliure un terreny enormement fèrtil per la
  innovació tecnològica, social i de processos. D’aquesta producció de
  coneixement se’n beneficien directament aquelles persones que produeixen i
  utilitzen el programari, i indirectament tota la societat

Per materialitzar i maximitzar aquests beneficis cal, a més del compromís de
basar l'arquitectura tècnica de l'IMI en una quantitat creixent de programari
lliure, conèixer i explotar les particularitats dels projectes i les comunitats
obertes.

Malgrat l'enorme diversitat existent entre els projectes de codi obert, amb el
temps han emergit una sèrie de pràctiques que comparteixen la majoria de
projectes i organitzacions que assoleixen un cert èxit. Això inclou aspectes
tant tècnics, com legals, com de gestió de projectes. Algunes d'aquestes
pràctiques podríem dir que son d'adopció obligatòria, en el sentit que les
dinàmiques de treball dels projectes oberts premien determinades conductes i en
penalitzen d'altres.

Aquestes pràctiques estan orientades a facilitar la màxima diversitat de
participants, molts cops sense una coordinació centralitzada, i a preservar al
mateix temps la qualitat del producte. En alguns casos poden diferir
substancialment de la forma de treballar quan es desenvolupa sense una voluntat
de publicar el codi. Per tant, el procés d'aprenentatge i adaptació de l'IMI
tindrà un cost, però creiem que es veurà superat en escreix per la millora
organitzativa que suposarà --en simbiosi amb la incorporació de metodologies
àgils--, a més de tots els beneficis mencionats més amunt. Com diu Karl Fogel a
:prodoss:`Producing Open Source Software<en/introduction.html>`:

  "els projectes de codi obert en que participa la teva organització son una
  membrana a través de la qual els teus gestors i projectes es troben exposats
  de manera regular a gent i idees externes a la teva jerarquia organitzativa.
  És com obtenir els beneficis d'anar a un congrés, però al mateix temps seguir
  amb el treball diari i sense haver de pagar el viatge. En un projecte de
  codi obert exitós aquests beneficis, una vegada arriben, superen àmpliament
  els costos".

En definitiva, aquest document pretén explicar les millors pràctiques
disponibles per utilitzar i desenvolupar programari de codi obert. Ho fa
codificant i adaptant a l'IMI aquestes bones pràctiques, de manera que serveixi
de guia en el procés d'aprenentatge i en la presa de decisions.

Per saber-ne més
================

Un molt bon recurs per entendre tots els aspectes tècnics, legals i socials que
envolten el desenvolupament de programari lliure és el llibre de Karl Fogel
:prodoss:`Producing Open Source Software<en/index.html>` (en l'edició de 2017,
només disponible electrònicament i consultable lliurement per Internet). En
l'elaboració d'aquesta Guia s'han tingut en compte moltes de les recomanacions
recollides al llibre.

La Guia conté també una gran quantitat de recomanacions que tenen a veure amb la
contractació de diferents serveis. Un bon document per entendre les
particularitats de la contractació de programari lliure des de l'administració
pública és la :joinup:`Guideline on public procurement of Open Source
Software<document/guideline-public-procurement-open-source-software>`, publicat
al 2010 per Rishab Aiyer Ghosh, Ruediger Glott, Patrice-Emmanuel Schmitz i
Abdelkrim Boujraf, per encàrrec de la Comissió Europea sota la iniciativa
:joinup:`Joinup </>`.
