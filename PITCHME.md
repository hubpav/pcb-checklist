@snap[midpoint]
## @color[#adff2f](PCB CHECKLIST)
#### @color[orange](Pavel Hübner)
##### @color[#87cefa](HARDWARIO s.r.o.)
@snapend

@snap[south span-100]
pavel.hubner@hardwario.com<br>
Twitter: @pavelhubner<br>
@snapend

---

@snap[midpoint]
## @color[#adff2f](Úvod)
@snapend

Note:

- Uvedené pohledy jsou čistě subjektivní
- Každá firma/konstruktér si tvoří vlastní checklisty
- Ukazuje to cestu, jak to děláme my
- Nečekejte jednu dlouhou direktivní tabulku
- Textová prezentace

---

#### @color[#87cefa](Úvod 1:)
## @color[orange](Důvod pro checklist)

- #1: Někdo začíná a potřebuje vodítko
- #2: Potřebujeme posílit stávající procesy
- #3: Návod pro nové kolegy
- #4: Nechceme opakovat stejné chyby
- #5: Finanční úspora

Note:
- Většina zkušených
- Máme mezi sebou i začínající
- Od určitého objemu se chyby stávají

---

#### @color[#87cefa](Úvod 2:)
## @color[orange](Svatý grál výroby)

- Přesnost
- Opakovatelnost
- Dostupnost
- Trasovatelnost
- Přenositelnost
- Celková kvalita

Note:
- Přesnost:
    - Jasně specifikované podklady, abychom vyloučili prostor domněnky
- Dostupnost:
    - Mění se v čase
- Trasovatelnost:
    - Sourcing
    - Analýza poruch
    - Servis a reklamace
- Celková kvalita:
    - Vnímání designér x výrobce
---

#### @color[#87cefa](Úvod 3:)
## @color[orange](Struktura prezentace)

- Část 1: Skladové hospodářství
- Část 2: Před návrhem
- Část 3: Fáze návrhu
- Část 4: Příprava podkladů
- Část 5: Zadání do výroby

---

@snap[midpoint]
#### @color[#87cefa](Část 1:)
## @color[#adff2f](Skladové hospodářství)
@snapend

---

#### @color[#87cefa](Skladové hospodářství 1:)
## @color[orange](Centrální databáze I.)

- Jakákoliv forma databáze obsahující informace o všech kdy použitých součástkách
- Od komplexního ERP systému až po Google Sheets
- Nutnost na víc než jeden projekt
- Výhodou propojení na ECAD x ECAD v roli ERP systému
    - Pro informace do knihoven (design fáze)
    - Pro generování výstupů (úspora času)
- Vazba na nákup, výrobu, obchod

Note:
- Vyberte si takové nástroje, které budete schopni systematicky udržovat

---

#### @color[#87cefa](Skladové hospodářství 2:)
## @color[orange](Centrální databáze II.)

- Nástroj v HARDWARIO
- GitLab (repozitář hardware a knihoven)
- GitLab CI (continuous integration)
- Python skript
    - Spouštění na commit nebo ručně (lokálně)
    - Vstup: Google Sheet, knihovny, projekty
    - Výstup: Knihovny, projektový BOM
- Pomáhá při plánování - tabulka požadovaných množství, výstup: souhrnný BOM

Note:
- GitLab
    - Management systém nad Git
    - Self-hosted nebo cloudá verze
    - Kdo zná Git?
- EAGLE + XML soubory
- Suplujeme chybějící funkce sofistikovanějšího systému
- Altium Vault řeší out-of-the-box

---

#### @color[#87cefa](Skladové hospodářství 3:)
## @color[orange](Struktura databáze I.)

- Interní part number
    - Primární klíč každé součástky
    - Uvedení kategorie (IC,R,C,BAT,...)
    - Příklad: HIO-IC-TMP112
- Stav součástky
    - NEW = nová, neověřená
    - ACT = aktivní, ověřená a používaná
    - NRD = aktivní, ale ne pro nové designy
    - EOL = konec životnosti

Note:

---

#### @color[#87cefa](Skladové hospodářství 4:)
## @color[orange](Struktura databáze II.)

- Stručný popis, např. podtitulek z datasheetu
- Přílohy (nabídky, výkresy, datasheety, atd.)
- Označení pouzdra (0402, SOIC-8)
    - Montážní technologie (SMT/THT)
- Aktuální stav skladu
    - Zásoba a umístění
    - Datum naskladění (nutné pro sledování expirace)
- Použito v projektech X,Y,Z
- Osazovací popisek (např. 100 nF) - pro ruční osazení

Note:
- Stručný popis injektujeme do knihovny z centrální databáze
- Montážní technologie - důležité pro part list

---

#### @color[#87cefa](Skladové hospodářství 5:)
## @color[orange](Struktura databáze III.)

- Výrobce (může být více)
    - Jméno + kontakt
    - Part number výrobce
- Dodavatel (může být více)
    - Jméno + kontakt
    - Part number dodavatele
    - MOQ, MPU, L/T
    - Ceny (EUR/USD/CZK)

Note:
- Ceny v čase
- Důležitá je přesnost
- Kompromis mezi cenou a dostupností
- Dlouhé čekací lhůty

---

#### @color[#87cefa](Skladové hospodářství 6:)
## @color[orange](Optimalizace součástek)

- Parametry, dostupnost, cena
- Hledání průniků
    - Existující produkty
    - V rámci designu
- Výrobní technologie
- TCO (Total Cost of Ownership)
- Ve výrobní fázi (ECO)
    - Popis změny, rozsah, produkty, lidé

Note:
- Projektové bundle ceny

---

@snap[midpoint]
#### @color[#87cefa](Část 2:)
## @color[#adff2f](Před návrhem)
@snapend

---

##### @color[#87cefa](Před návrhem 1:)
## @color[orange](Projektová šablona)

- Specifikace produktu
- Vlastník produktu (PO)
- Cílový zákazník
- Požadované certifikace
- Odhad životního cyklu:
    - Kolik toho budeme vyrábět?
    - Jak dlouho budeme vyrábět?

Note:
- Product owner
- Agile development
- Kontext aplikace
- EMC/EMI/ESD/EN/ATEX
---

##### @color[#87cefa](Před návrhem 2:)
## @color[orange](Výrobní etapy I.)

- Příklad rozdělení:
    - Funkční vzorek < 10 ks
    - Prototypová série < 100 ks
    - Ověřovací série < 1000 ks
    - Sériová výroba
- Rozdělení podle ceny a složitosti
- Každá etapa má stanovený termín plnění

Note:

---

##### @color[#87cefa](Před návrhem 3:)
## @color[orange](Výrobní etapy II.)

- Od termínu se stanoví harmonogram
- Příklad plánování pro ověřovací sérii 500 ks
    - 12-16 týdnů nákup materiálu
    - 3 týdny výroba desky
    - 2 týdny osazení
    - 2 týdny oživení
- Nástroje Redmine, Gantt
- Interní oponentura před/po každé etapě


Note:
- Nástroj bez PO vás nespasí

---

#### @color[#87cefa](Před návrhem 4:)
## @color[orange](Technologické možnosti)

- Výrobce desek
    - Prototypová výroba - např. Gatema, Pragoboard
    - Sériová výroba - např. MMAB
- Možnosti ručního osazení
- Technologické zázemí
- Požadavky na výrobní tester
- Jak se řeší kompletace a balení
- Jak se řeší skladování

Note:
- Výrobce desek - kompatibilita materiálů
- Technologické zázemí
    - Rentgen - LGA/BGA must-have, hlavně pro rozjezd výroby
- IPC třídy hustoty

---

@snap[midpoint]
#### @color[#87cefa](Část 3:)
## @color[#adff2f](Fáze návrhu)
@snapend

---

##### @color[#87cefa](Fáze návrhu 1:)
## @color[orange](Technická rozvaha)

- Systémový diagram
- Blokový diagram
- Technická specifikace
- Výběr součástek
    - Jednání s výrobci/distributory
- Výrobní technologie
- Oponentura technického konceptu

Note:
- Velikost pouzder
- Jednostranná/oboustranná montáž
- Pozor na moduly
- Technologie pájení

---

#### @color[#87cefa](Fáze návrhu 2:)
## @color[orange](Návrhový cyklus desky)

- #1: Tvorba knihoven
- #2: Návrh zapojení
- #3: Rozmístění součástek
- #4: Návrh spojů
- #5: Kontrola ERC/DRC
- #6: Generování podkladů
- #7: Odeslání do výroby

Note:
- DFM/DFA/DFT analýza v každém kroku návrhu

---

#### @color[#87cefa](Fáze návrhu 3:)
## @color[orange](Tvorba knihoven I.)

- Praktická kategorizace
- Ukázka [kategorizace](https://gist.github.com/hubpav/3115b4a44a9600dc3f6eef0879bd4e56)
- Přiřazení interního skladovacího čísla
- Konzistentní pravidla a důslednost
- Správná specifikace balení v označení součástky:
    - Bulk, Cut Tape, DigiReel
    - Tube, Tape & Reel, Tray

Note:
- Pohlídat, že např. konektory mají osazovací čepičky

---

#### @color[#87cefa](Fáze návrhu 4:)
## @color[orange](Tvorba knihoven II.)

- Prefixy součástky
    - Reference Designator / Name
    - [Inspirace vycházející ze standardů](https://en.wikipedia.org/wiki/Reference_designator)
- V názvu pouzdra specifikace technologie pájení:
    - Suffix _T pro manuální montáž
    - Suffix _R pro SMT montáž - pájení reflow
    - Suffix _W pro SMT montáž - pájení vlnou
- Konzultace s technology u výrobce


Note:
- Pohlídat, že např. konektory mají osazovací čepičky
- Suffixy pro IPC

---

#### @color[#87cefa](Fáze návrhu 5:)
## @color[orange](Tvorba schématu)

- Sběrnice, hier. schémata, wire harness
- Pojmenované všechny signály
- Tip: I2C adresy do schématu
    - Nástroj na extrahování I2C adres
- Vhodné umístění komentářů, např.:
    - Mezní kmitočet filtru
    - Napětí na referenci
- Mechanické komponenty součástí schématu

---

#### @color[#87cefa](Fáze návrhu 7:)
## @color[orange](Návrh spojů I.)

- Minimální můstky na masce 0.1 mm
- Impedanční přizpůsobení a specifikace stacku
- Čištění nezakončených spojů
- Spojování prokovů
- Jasná specifikace pokoveného a nepokoveného frézování

---

#### @color[#87cefa](Fáze návrhu 8:)
## @color[orange](Návrh spojů II.)

- Keramické kondenzátory blízko kraji desky
    - Zvážit použití flex term přívodů
    - Mechanické namáhání nejen při separaci soulepu
- Pozor na diody ve skleněném pouzdře
- Minimální vzdálenost mezi test pointy 2 mm

---

#### @color[#87cefa](Fáze návrhu 9:)
## @color[orange](Návrh spojů III.)

- Impedanční přizpůsobení
- Měď od kraje desky min. 0.3 mm
- Součástky od hrany desky min. 1 mm
    - Pozor na keramické kondenzátory min. 3 mm
    - Mechanické namáhání nejen při separaci soulepu
    - Zvážit použití flex term přívodů (např. AVX od 1 uF)

---

#### @color[#87cefa](Fáze návrhu 10:)
## @color[orange](Náležitosti I.)

- Označení desky
    - Názvem (SOIL SENSOR), příp. kódem (HX153)
- Číslo revize desky např. formát Rx.y
    - x = major číslo (mění kompatibilita)
    - y = minor číslo (oprava, drobné vylepšení)
    - V případě verzovacího systému vytvořit tag
    - Jméno tagu např.: hio-soil-sensor-r1.3

---

#### @color[#87cefa](Fáze návrhu 11:)
## @color[orange](Náležitosti II.)

- Prostor pro trasovatelný kód
    - Číslo, čárový kód, QR / data matrix
    - Speciální vrstva - součást Gerber dat výrobci
    - Laserové gravírování grafického kódu
    - Prostor 5x5 mm

---

#### @color[#87cefa](Fáze návrhu 12:)
## @color[orange](Náležitosti III.)

- Značky pro osazovací automat (fiducials)
    - Kulatý pad o průměru 1 mm
    - Odmaskování o průměru 2 mm
    - Restrict na okolí o průměru 2.4 mm
- Nulová souřadnice desky v levém dolním rohu
    - Někteří výrobci mají problém se zápornými souřadnicemi
- Naváděcí díry pro jehlové pole (min. průměr trnu 3 mm, díra 3.2 mm)

+++?image=assets/img/fiducial.png&position=center&size=80%

---

#### @color[#87cefa](Fáze návrhu 13:)
## @color[orange](Náležitosti IV.)

- Místo pro "bad mark"
    - Možnost ručně označit defektní DPS v technologickém okolí panelu
    - Uplatnění již od výrobce DPS
    - Odmaskovaný čtverec v mědi min. 1x1 mm
    - Lihový fix nebo štítek
- Identifikace vrstev mědi (kontrola)
    - Číslování
    - Čtverečky

+++?image=assets/img/layers.png&position=center&size=80%

---

#### @color[#87cefa](Fáze návrhu 14:)
## @color[orange](Kontrola ERC/DRC)

- Pozor na "Je to jen varování"
- Šablonové nastavení
- Vygenerovat všechny polygony
- Kontrola vzdušných spojů
- Statistiky (šířky spojů, prokovy, jména spojů)
- Nezapomenout kontrolovat masku a pastu (pozor na variantní osazení, nanesená pasta může vadit)

Note:
- Dodatečný prokov na spojení zemí a jeho odvrtávání

---

@snap[midpoint]
#### @color[#87cefa](Část 4:)
## @color[#adff2f](Příprava podkladů)
@snapend

---

#### @color[#87cefa](Příprava podkladů 1:)
## @color[orange](Přehled dokumentace)

- Soupiska součástek (BOM)
- Gerber + NC drill data
- Specifikace vrstev (layer stack)
- Výkres panelizace
- Seznam pozic (pick and place)
- Osazovací plánky (poziční/hodnotové)
- Popis oživení a testování

+++?image=assets/img/names.png&position=center&size=80%

+++?image=assets/img/values.png&position=center&size=80%

---

#### @color[#87cefa](Příprava podkladů 2:)
## @color[orange](Gerber + NC drill data)

- Aktuální vygenerovaný ground plane
- ERC/DRC
- Obrys desky
- Frézování (pokovené/nepokovené)
- Měď všechny vrstvy
- Maska T/B
- Potisk T/B
- Pájecí pasta T/B - v případě planžety

---

#### @color[#87cefa](Příprava podkladů 3:)
## @color[orange](Panelizace desky I.)

- Jeden design na panel
- Optimalizace obrysu
- Typy separace
    - V-drážky (V Grooving)
    - Frézování (Milling)
    - Můstky (Tab breakout)

+++?image=assets/img/pcb-panel-wrong.jpg&position=center&size=80%
+++?image=assets/img/pcb-panel-drilling.jpg&position=center&size=80%

---

#### @color[#87cefa](Příprava podkladů 4:)
## @color[orange](Panelizace desky II.)

- Technologické okolí
    - "Tooling strip"
    - Po krajích zhruba 10 mm
    - Montážní díry
    - Pomocné využití - testování řízené impedance
    - Bad marky

Note:
- TODO obrazek

---

@snap[midpoint]
#### @color[#87cefa](Část 5:)
## @color[#adff2f](Zadání do výroby)
@snapend

---

#### @color[#87cefa](Zadání do výroby 1:)
## @color[orange](Objednání DPS)

- Název desky, počet kusů, termín
- Technologie
    - Počet vrstev + layer stack
    - Barva masky
    - Povrchová úprava
    - Testování
- Výrobní data

Note:
- Zbytečně nešetřete počet vrstev
- Vyrobili jsme 6vrstvou desku se 4 vrstvami.

---

#### @color[#87cefa](Zadání do výroby 2:)
## @color[orange](Objednání výroby u EMS)

- Označení zakázky
- Požadované množství
- Požadovaný termín
- Dokumentační balíček
- Operace po osazení
    - Mytí
    - Lakování

Note:
- Nejednou jsme jeli do Pragoboardu pro planžetu.

---

#### @color[#87cefa](Zadání do výroby 3:)
## @color[orange](Objednání výroby u EMS)

- Rozsah realizace
    - Nákup materiálu
    - Objednání desek
    - Zajištění planžety
    - Osazení desek
    - Testování, kompletace

Note:

---

#### @color[#87cefa](Zadání do výroby 4:)
## @color[orange](Sledování zakázky)

- Potvrzení přijetí zakázky
- Potvrzení správnosti podkladových materiálů
    - Iterační proces
- Pravidelná komunikace a kontrola
    - Alokace na lince
    - Plnění subdodávek

Note:
- Stalo se nám, že vše bylo vykomunikováno, ale neuskutečnilo se "GO".

---

#### @color[#87cefa](Zadání do výroby 4:)
## @color[orange](Předání zakázky)

- Předávací protokol
- Servisní operace
    - Testery
- Zpětná vazba:
    - Výrobci
    - Objednateli
    - Konstruktérovi

---

@snap[midpoint]
## @color[#adff2f](Diskuze)
@snapend

---
