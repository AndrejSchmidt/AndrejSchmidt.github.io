---
layout: assignment
number: 1
title: "Osobná webová prezentácia na GitHub pages"
---
## Zadanie
Vytvorte webovú prezentáciu (webové sídlo) o sebe. Zamerajte sa jednak na vaše profesné záujmy (napr. projekty, ktoré riešite/riešili ste, čo vás v informatike najviac baví, fascinuje = váš developerský profil) a jednak vaše osobné záujmy, hobby.

Celé znenie zadania si môžete prečítať [tu](https://wiki.fiit.stuba.sk/study/bc/info/wp/2018-19/zadanie1/).

## Dokumentácia
### Rozloženie stránok (layouty)
Webové sídlo pozostáva z hlavného layoutu, obsahujúceho vertikálny navigačný panel s piatimi sekciami stránky a pätičku, do ktorého sa následne vkladá príslušný obsah. 
Príspevky blogu majú vlastný layout obsahujúci dátum zverejnenia a sekcia vyhradená pre tento predmet má vlastný layout na stránky so zadaním.

### Prvky použité v šablónach
* Premenné
   
    Zoznam použitých premenných:
    site.posts  
    site.assignment  
    page.title  
    page.url   
    assignment.title  
    assignment.number  
    post.title  
    post.date

* Kolekcia

    Zadania v sekcii Webové publikovanie sú riešené pomocou kolekcií.

* Filtre a tagy

    Pri zostavovaní stránky sa používajú štandardné Liquid tagy:

    {{ "{% if " }}%} s príslušným koncovým tagom  
    {{ "{% else " }}%}  
    {{ "{% for " }}%} s príslušným koncovým tagom

    a filtre:

    downcase – ktorý mení písmenká reťazca na malé  
    split – ktorý delí reťazec podľa zadaného delimitra  
    date – mení dormát dátumu do príslušnej formy

* Plugin

    Sídlo používa plugin [Jemoji](https://github.com/jekyll/jemoji), ktorý umožňuje používať GitHub-flavored emoji, ktoré fungujú aj na GitHub Pages :wink:.


### Štýly

Štýly použité na stránke sú vlastná tvorba.

.