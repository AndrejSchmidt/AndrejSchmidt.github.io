---
layout: assignment
number: 2
title: "Zadanie 2: Transformácia vybraného dokumentu do formátu DocBook"
---
## Zadanie
Predmetom 2. zadania je spracovanie vybraného dokumentu (ideálne bakalárskeho projektu) z pôvodného ľubovoľného (Word, OpenOffice, LaTeX, …) formátu do formátu DocBook a vygenerovanie cieľového tvaru v PDF. Výsledný dokument bude mať rozsah minimálne 10 a maximálne 15 strán. Do rozsahu sa nezapočítavajú úvodné strany (obsah, zoznamy obrázkov a tabuliek), použitá literatúra a prílohy.

Celé znenie zadania si môžete prečítať [tu](https://wiki.fiit.stuba.sk/study/bc/info/wp/2018-19/zadanie2/).

## Dokumentácia
### Konverzia dokumentu
Transformovaný dokument je správa o bakalárskej práci, ktorá bola pôvodne vypracovaná v systéme LaTex. Z neho bola vyexportovaná vo formáte pdf, následne zkonvertovaná na docx a pomocou online služby [XMLmind](http://www.xmlmind.com/w2x/docx_to_docbook.html) prevedená do DocBook xml.

### Elementy použité v dokumente
Na členenie textu sa využívajú elementy ```<chapter>``` a ```<section>```. Každý celok práce má ```<title>``` a spravidla obsahuje odstavce ```<para>```, prípadne obrázky ```<figure>```. V texte sa dá presúvať pomocou odkazov ```<link>``` na text a ```<xref>``` na obrázky. V texte sa nachádzajú tiež odkazy na zdroje ```<bibliography>``` pod elementom ```<citation>```. Za zoznamom zdrojov sa nachádza register pojmov ```<index />``` s hierarchicky usporiadnými pojmami a dodatok ```<appendix>```.


Medzi ďalšie použité elementy patrí ```<emphasis>```, ```<subscript>``` a ```<superscript>``` na zvýraznenie určitých častí textu, ```<footnote>``` na poznámku pod čiarou a ```<table>``` s príslušnými elementmi na vytvorenie tabuľky. Zdroje obsahujú element ```<url>``` s príslušným odkazom na zdroj.

### Zmeny v xsl
Xsl dokumenty boli pozmenené minimálne. Z prednej strany bol odstránený obrázok s logom fakulty, do názvu univerzity bolo pridané obmedzenie, nech sa nerozdeľujú slová a české slovo „Vedoucí“ bolo preložené na „Vedúci“. Taktiež bolo pridané zobrazovanie zoznamu obrázkov a tabuliek.