Guia per gestionar projectes de programari lliure
=================================================

*Read a simplified README in other languages: `English <README.rst>`__.*

La *Guia per gestionar projectes de programari lliure* de l’**Ajuntament de
Barcelona** és un document d’ús intern amb directrius i recomanacions a aplicar
en tots els projectes que utilitzen components de programari lliure i de codi
obert. Abarca aspectes com la cerca i disseny de solucions, la contractació de
serveis, el desenvolupament i implantació de sistemes d’informació, i la
participació en comunitats obertes.

La Guia desenvolupa i concreta els principis sobre ús de programari lliure
establerts a la `Mesura de govern per a la digitalització oberta
<http://ajuntament.barcelona.cat/digital/ca/documentacio>`__, d’octubre de 2017,
traslladant a l’Ajuntament les millors pràctiques del sector.

Aquest repositori conté el codi font en llenguatge de marques reStructuredText a
partir del qual es genera automàticament la versió HTML del document. El
document està escrit en català. Com a excepció a la regla general, tant els
missatges de *commit* com les discussions al `gestor d’incidències
<https://github.com/AjuntamentdeBarcelona/foss-guide-bcn-ca/issues>`__ es troben
també en català.

Contribuir a aquest document
----------------------------

L’Ajuntament de Barcelona anirà modificant aquest document a mesura que
apareguin nous casos d’ús, o que les pràctiques del sector evolucionin. Les
modificacions es discutiran al `gestor d’incidències
<https://github.com/AjuntamentdeBarcelona/foss-guide-bcn-ca/issues>`__. Tot i
que la participació en les discussions està oberta a tothom, l’Ajuntament de
Barcelona és qui decideix quines modificacions incorporar en futures versions
del document.

A més d’assenyalar errades i proposar canvis, es pot contribuir amb propostes
concretes de redacció. Els passos necessaris son:

1. Instal·lar els següents paquets de Python:

   -  ``Sphinx``
   -  ``sphinx_rtd_theme``
   -  ``sphinxcontrib-needs``

   El *build* del document ha estat provat amb Python 3 i la versió de Sphinx
   1.6.7. L’arrel del repositori conté un fitxer ``requirements.txt`` que es pot
   fer servir per instal·lar tots els paquets necessaris.

2. Fer un *fork* del repositori.

3. Realitzar modificacions a qualsevol dels fitxers amb extensió ``rst`` que hi
   ha al directori ``source``. El document està escrit utilitzant `Sphinx
   <http://www.sphinx-doc.org>`__, en format reStructuredText.

4. Executar la comanda de *build* (veure la `documentació de Sphinx
   <http://www.sphinx-doc.org/en/stable/tutorial.html#adding-content>`__) i
   comprovar que tot es visualitza bé obrint ``build/html/index.html`` amb un
   navegador.

5. Fer *commit* dels canvis.

6. Fer *push* del nou *commit*.

7. Crear un *pull request* explicant en una frase breu el contingut dels canvis
   proposats.

Llicència
---------

La *Guia per gestionar projectes de programari lliure* de l’Ajuntament de
Barcelona es distribueix sota la llicència `CC-BY-SA-4.0
<https://creativecommons.org/licenses/by-sa/4.0/>`__.
