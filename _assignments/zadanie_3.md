---
layout: assignment
number: 3
title: "XML prezentácia"
---
## Zadanie
Analyzujte možnosti zápisu jednoduchej prezentácie v jazyku XML. Identifikujte základné súčasti prezentácie a navrhnite XML elementy pre ich označkovanie (metadátové, štrukturálne, inline). Dbajte na znovupoužiteľnosť a vyvarujte sa redundancií. Návrh elementov zrealizujte opísaním typu dokumentu pomocou vybraného jazyka (DTD, XSD, RELAX NG) spolu s vysvetlením účelu jednotlivých elementov. Vo vami navhrnutom jazyku vytvorte ukážkovú prezentáciu, ktorá bude demonštrovať možnosti tvorby prezentácií podľa definície typu dokumentu.

Celé znenie zadania si môžete prečítať [tu](https://wiki.fiit.stuba.sk/study/bc/info/wp/2018-19/zadanie3/).

## Dokumentácia
### Prezentácia
Navrhnutá prezentácia je súbor snímok s elementom ```<snimka>``` v koreňovom elemente ```<prezentacia>```, ktoré môžu obsahovať ľubovoľný počet prvkov ```<odsek>```, ```<obrazok>``` a ```<zoznam>``` v ľubovoľnom poradí. Každá snímka povinne obsahuje jeden ```<nadpis>```. Zoznam je tvorený prvkami ```<polozka>```. Obrazok má atribút ```zdroj```, v ktorom je uvedený zdroj, z ktorého sa má čerpať obrázok. Snímkam v koreňovom elemente predchádza element ```<hlavicka>```, ktorý obsahu informácie ako ```<nazov>```, ```<podnadpis>```, ```<autor>```, ```<datum_publikacie>```, ```<skola>``` a ```<fakulta>```.

Obsahom prezentácie je krátky výcuc z mojej bakalárskej práce. Výsledné dokumenty využívajú parametre zapísané v dokumente params.xml. Pomocou parametrov môžeme nastaviť, či sa má byť na prednej strane dátum a či majú zvyšné strany obsahovať meno fakulty. XML prezentácie aj parametrov využíva na validáciu XML Schema.

### Transformácia do XHTML
Na transformáciu treba použiť to_xhtml.bat, v ktorom upravíme cestu k Saxon 9HE. Transformácia vytvorí počet xhtml súborov zodpovedajúci počtu snímok plus úvodná snímka obsahujúca informácie z hlavičky XML dokumentu. Všetky elementy z XML prexentácie majú sú prevedené do podoby XHTML stránky pomocou štandardných HTML elementov. Z dôvodu nedostatku času som sa v tomto zadaní rozhodol využiť populárny open-sourcový toolkit [Bootstrap](https://getbootstrap.com/).

### Transformácia do PDF
Pri transformácii do pdf sa využíva to_pdf.bat, ktorý na vstupe dostane XML s prezentáciou a XSL transformáciami, z ktorých následne vytvorí dočasný XML súbor, ktorý pomocou xep.bat prevedia na pdf. Pri prípadnom transformovaní sa treba uistiť, že všetky cesty v .bat súboroch ukazujú na požadované súbory. Samotná prezentácia je veľmi jednoduchá, využíva základné XSL-FO prvky na reprezentáciu hlavných častí prezentácie.