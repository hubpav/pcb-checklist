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
- Nečekejte jednu dlouhou direktivní tabulku

---

#### @color[#87cefa](Úvod 1:)
## @color[orange](Důvod pro checklist)

@ul
- 1. Někdo začíná a potřebuje vodítko
- 2. Potřebujeme posílit stávající procesy
- 3. Návod pro nové kolegy
- 4. Nechceme opakovat stejné chyby
@ulend

Note:
- Od určitého objemu se chyby stávají

---

#### @color[#87cefa](Úvod 2:)
## @color[orange](Svatý grál výroby)

@ul
- Přesnost
- Opakovatelnost
- Dostupnost
- Trasovatelnost
- Přenositelnost
- Celková kvalita
@ulend

Note:
- Trasovatelnost:
    - Analýza poruch
    - Servis a reklamace
- Kvalita:
    - Vnímání designér x výrobce
- Dostupnost:
    - Mění se v čase
---

#### @color[#87cefa](Úvod 3:)
## @color[orange](Struktura prezentace)

@ul
- 1. Skladové hospodářství
- 2. Před návrhem
- 3. Fáze návrhu
- 4. Příprava podkladů
- 5. Zadání do výroby
@ulend

---

@snap[midpoint]
#### @color[#87cefa](Část 1:)
## @color[#adff2f](Skladové hospodářství)
@snapend

---

#### @color[#87cefa](Skladové hospodářství 1:)
## @color[orange](Centrální databáze I.)

@ul
- Jakákoliv forma databáze obsahující informace o všech kdy použitých součástkách
- Od komplexního ERP systému až po Google Sheets
- Nutnost na víc než jeden projekt
- Výhodou propojení na ECAD x ECAD v roli ERP systému
    - Pro informace do knihoven (design fáze)
    - Pro generování výstupů (úspora času)
- Vazba na nákup, výrobu, obchod
@ulend

Note:

---

#### @color[#87cefa](Skladové hospodářství 2:)
## @color[orange](Centrální databáze II.)

@ul
- Nástroj v HARDWARIO
- GitLab (repozitář hardware a knihoven)
- GitLab CI (continuous integration)
- Python skript
    - Spouštění na commit nebo ručně (lokálně)
    - Vstup: Databáze, knihovny, projekty
    - Výstup: Knihovny, projektový BOM
- Pomáhá při plánování - tabulka požadovaných množství, výstup: souhrnný BOM
@ulend

---

#### @color[#87cefa](Skladové hospodářství 3:)
## @color[orange](Struktura databáze I.)

@ul
- Interní part number
    - Primární klíč každé součástky
    - Uvedení kategorie (IC,R,C,BAT,...)
    - Příklad: HIO-IC-TMP112
- Stav součástky
    - NEW = nová, neověřená
    - ACT = aktivní, ověřená a používaná
    - NRD = aktivní, ale ne pro nové designy
    - EOL = konec životnosti
@ulend

---

#### @color[#87cefa](Skladové hospodářství 4:)
## @color[orange](Struktura databáze II.)

@ul
- Stručný popis, např. podtitulek z datasheetu
- Přílohy (nabídky, výkresy, datasheety, atd.)
- Označení pouzdra (0402, SOIC-8)
    - Montážní technologie (SMT/THT)
- Aktuální stav skladu
    - Zásoba a umístění
    - Datum naskladění (nutné pro sledování expirace)
- Použito v projektech
- Osazovací popisek (např. 100 nF) - pro ruční osazení
@ulend

Note:
- Montážní technologie - důležité pro part list

---

#### @color[#87cefa](Skladové hospodářství 5:)
## @color[orange](Struktura databáze III.)

@ul
- Výrobce (může být více)
    - Jméno + kontakt
    - Part number výrobce
- Dodavatel (může být více)
    - Jméno + kontakt
    - Part number dodavatele
    - MOQ, MPU, L/T
    - Ceny (EUR/USD/CZK)
@ulend

Note:
- Ceny v čase
- Důležitá je přesnost
- Kompromis mezi cenou a dostupností
- Dlouhé čekací lhůty

---

#### @color[#87cefa](Skladové hospodářství 6:)
## @color[orange](Optimalizace součástek)

@ul
- Parametry, dostupnost, cena
- Hledání průniků
    - Existující produkty
    - V rámci designu
- Výrobní technologie
- TCO (Total Cost of Ownership)
- Ve výrobní fázi (ECO)
    - Popis změny, rozsah, produkty, lidé
@ulend

---

@snap[midpoint]
#### @color[#87cefa](Část 2:)
## @color[#adff2f](Před návrhem)
@snapend

---

##### @color[#87cefa](Před návrhem 1:)
## @color[orange](Projektová šablona)

@ul
- Specifikace produktu
- Vlastník produktu (PO)
- Cílový zákazník
- Požadované certifikace
- Odhad životního cyklu:
    - Kolik toho budeme vyrábět?
    - Jak dlouho budeme vyrábět?
@ulend

Note:

---

##### @color[#87cefa](Před návrhem 2:)
## @color[orange](Výrobní etapy I.)

@ul
- Příklad rozdělení:
    - Funkční vzorek < 10 ks
    - Prototypová série < 100 ks
    - Ověřovací série < 1000 ks
    - Sériová výroba
- Rozdělení podle ceny a složitosti
- Každá etapa má stanovený termín plnění
@ulend

Note:

---

##### @color[#87cefa](Před návrhem 3:)
## @color[orange](Výrobní etapy II.)

@ul
- Od termínu se stanoví harmonogram
- Příklad plánování pro ověřovací sérii 500 ks
    - 12-16 týdnů nákup materiálu
    - 3 týdny výroba desky
    - 2 týdny osazení
    - 2 týdny oživení
- Interní oponentura před/po každé etapě
@ulend

---

#### @color[#87cefa](Před návrhem 4:)
## @color[orange](Technologické možnosti)

@ul
- Výrobce desek
    - Prototypová výroba - např. Gatema, Pragoboard
    - Sériová výroba - např. MMAB
- Možnosti ručního osazení
- Technologické zázemí
- Požadavky na výrobní tester
- Jak se řeší kompletace a balení
- Jak se řeší skladování
@ulend

Note:
- Výrobce desek - kompatibilita materiálů
- Rentgen

---

@snap[midpoint]
#### @color[#87cefa](Část 3:)
## @color[#adff2f](Fáze návrhu)
@snapend

---

##### @color[#87cefa](Fáze návrhu 1:)
## @color[orange](Technická rozvaha)

@ul
- Blokový diagram
- Výběr součástek
    - Jednání s výrobci/distributory
- Výběr nástrojů
- Technická specifikace
- Oponentura technického konceptu
@ulend

---

#### @color[#87cefa](Fáze návrhu 2:)
## @color[orange](Návrhový cyklus desky)

@ul
- 1. Tvorba knihoven
- 2. Návrh zapojení
- 3. Rozmístění součástek
- 4. Návrh spojů
- 5. Kontrola ERC/DRC
- 6. Generování podkladů
- 7. Odeslání do výroby
@ulend

---

#### @color[#87cefa](Fáze návrhu 3:)
## @color[orange](Tvorba knihoven I.)

@ul
- Praktická kategorizace (hio-resistors, hio-capacitors, hio-microcontrollers, ...)
- Přiřazení interního skladovacího čísla
- Konzistentní pravidla a důslednost
- Správná specifikace balení v označení součástky:
    - Bulk, Cut Tape, DigiReel
    - Tube, Tape & Reel, Tray
@ulend

Note:
- Pohlídat, že např. konektory mají osazovací čepičky

---

#### @color[#87cefa](Fáze návrhu 4:)
## @color[orange](Tvorba knihoven II.)

@ul
- Prefixy součástky
    - Reference Designator / Name
    - [Inspirace vycházející ze standardů](https://en.wikipedia.org/wiki/Reference_designator)
- V názvu pouzdra specifikace technologie pájení:
    - Suffix _T pro manuální montáž
    - Suffix _R pro SMT montáž - pájení reflow
    - Suffix _W pro SMT montáž - pájení vlnou
- Konzultace s technology u výrobce

@ulend

Note:
- Pohlídat, že např. konektory mají osazovací čepičky

---

#### @color[#87cefa](Fáze návrhu 5:)
## @color[orange](Tvorba schématu I.)

@ul
- Pojmenované všechny signály
- Tip: I2C adresy do schématu
    - Nástroj na extrahování I2C adres
- Vhodné umístění komentářů, např.:
    - Mezní kmitočet filtru
    - Napětí na referenci
- Mechanické komponenty součástí schématu
@ulend

---

#### @color[#87cefa](Fáze návrhu 6:)
## @color[orange](Tvorba schématu II.)

@ul

@ulend


---

#### @color[#87cefa](Fáze návrhu 7:)
## @color[orange](Návrh spojů I.)

@ul
- Nulová souřadnice desky v levém dolním rohu
- Identifikátor + revize na desce
- Minimální můstky na masce 100 um
- Impedanční přizpůsobení a specifikace stacku
- Čištění nezakončených spojů
- Netahejte měď až do kraje desky
@ulend

---

#### @color[#87cefa](Fáze návrhu 8:)
## @color[orange](Návrh spojů II.)

@ul
- Keramické kondenzátory blízko kraji desky
    - Zvážit použití flex term přívodů
    - Mechanické namáhání nejen při separaci soulepu
- Pozor na diody ve skleněném pouzdře
- Jasná specifikace pokoveného a nepokoveného frézování
- Minimální vzdálenost mezi test pointy 2 mm
@ulend

---

#### @color[#87cefa](Fáze návrhu 9:)
## @color[orange](Návrh spojů III.)

@ul
- Razítko (identifikátor + revize)
- Nulová souřadnice desky v levém dolním rohu
- Identifikátor + revize na desce
- Minimum solder mask sliver
- Impedanční přizpůsobení
- Měď od kraje desky min. 0.3 mm
- Součástky od hrany desky min. 1 mm
    - Pozor na keramické kondenzátory min. 3 mm
    - Mechanické namáhání nejen při separaci soulepu
    - Zvážit použití flex term přívodů (např. AVX od 1 uF)
- Unterminated traces
@ulend

- Keramické kondenzátory blízko kraji desky
- Naváděcí díry pro jehlové pole

---

#### @color[#87cefa](Fáze návrhu 10:)
## @color[orange](Náležitosti I.)

@ul
- Označení desky
    - Názvem (SOIL SENSOR), příp. kódem (HX153)
- Číslo revize desky např. formát Rx.y
    - x = major číslo (mění kompatibilita)
    - y = minor číslo (oprava, drobné vylepšení)
    - V případě verzovacího systému vytvořit tag
    - Jméno tagu např.: hio-soil-sensor-r1.3
@ulend

---

#### @color[#87cefa](Fáze návrhu 11:)
## @color[orange](Náležitosti II.)

@ul
- Prostor pro trasovatelný kód
    - Speciální vrstva - součást Gerber dat výrobci
    - Laserové gravírování Data Matrix kódu
- Naváděcí díry pro jehlové pole
@ulend

---

#### @color[#87cefa](Fáze návrhu 12:)
## @color[orange](Náležitosti III.)

@ul
- Značky pro osazovací automat (fiducials)
    - Kulatý pad o průměru 1 mm
    - Odmaskování o průměru 2 mm
    - Restrict na okolí o průměru 2.4 mm
- Nulová souřadnice desky v levém dolním rohu
    - Někteří výrobci mají problém se zápornými souřadnicemi
- Naváděcí díry pro jehlové pole (min. průměr trnu 3 mm, díra 3.2 mm)
@ulend

---

#### @color[#87cefa](Fáze návrhu 13:)
## @color[orange](Náležitosti IV.)

@ul
- Místo pro "bad mark"
    - Možnost ručně označit defektní DPS v soulepu
    - Uplatnění již od výrobce DPS
    - Odmaskovaný čtverec v mědi 10x10 mm
- Identifikace vrstev mědi (kontrola)
    - Číslování
    - Čtverečky
@ulend

---

#### @color[#87cefa](Fáze návrhu 14:)
## @color[orange](Kontrola ERC/DRC)

@ul
- Pozor na "Je to jen varování"
- Šablonové nastavení
- Vygenerovat všechny polygony
- Cíl: Nothing to do!
- Statistiky (šířky spojů, prokovy, jména spojů)
- Nezapomenout kontrolovat masku a pastu (pozor na variantní osazení, nanesená pasta může vadit)
@ulend

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

@ul
- Soupiska součástek (BOM)
- Gerber + NC drill data
- Specifikace vrstev
- Výkres panelizace
- Seznam pozic (pick and place)
- Osazovací plánky (poziční/hodnotové)
- Popis oživení a testování
@ulend

---

#### @color[#87cefa](Příprava podkladů 2:)
## @color[orange](Gerber + NC drill data)

@ul
- Aktuální vygenerovaný ground plane
- ERC/DRC
- Obrys desky
- Frézování (pokovené/nepokovené)
- Měď všechny vrstvy
- Maska T/B
- Potisk T/B
- Pájecí pasta T/B - v případě planžety
@ulend

---

#### @color[#87cefa](Příprava podkladů 3:)
## @color[orange](Panelizace desky I.)

@ul
- Jeden design na panel
- Optimalizace obrysu
- Typy separace
    - V-drážky (V Grooving)
    - Frézování (Milling)
    - Můstky (Tab breakout)
@ulend

---

#### @color[#87cefa](Příprava podkladů 4:)
## @color[orange](Panelizace desky II.)

@ul
- Technologické okolí
    - "Tooling strip"
    - Po krajích zhruba 10 mm
    - Montážní díry
    - Pomocné využití - testování řízené impedance
    - Bad marky
@ulend

---

@snap[midpoint]
#### @color[#87cefa](Část 5:)
## @color[#adff2f](Zadání do výroby)
@snapend

---

#### @color[#87cefa](Zadání do výroby 1:)
## @color[orange](Objednání DPS)

@ul
- Název desky, počet kusů, termín
- Technologie
    - Počet vrstev + layer stack
    - Barva masky
    - Povrchová úprava
    - Testování
- Výrobní data
@ulend

Note:
- Vyrobili jsme 6vrstvou desku se 4 vrstvami.

---

#### @color[#87cefa](Zadání do výroby 2:)
## @color[orange](Objednání výroby)

@ul
- Označení zakázky
- Požadované množství
- Požadovaný termín
- Rozsah angažovanosti
    - Nákup materiálu
    - Objednání desek
    - Zajištění planžety
    - Osazení desek
    - Testování
    - Kompletace
- Dokumentační balíček
@ulend

Note:
- Nejednou jsme jeli do Pragoboardu pro planžetu.

---

#### @color[#87cefa](Zadání do výroby 3:)
## @color[orange](Sledování zakázky)

@ul
- Potvrzení přijetí zakázky
- Potvrzení správnosti podkladových materiálů
    - Iterační proces
- Pravidelná komunikace a kontrola
    - Alokace na lince
    - Plnění subdodávek
@ulend

Note:
- Stalo se nám, že vše bylo vykomunikováno, ale neuskutečnilo se "GO".

---

#### @color[#87cefa](Zadání do výroby 4:)
## @color[orange](Předání zakázky)

@ul
- Předávací protokol
- Servisní operace
    - Testery
- Zpětná vazba:
    - Výrobci
    - Objednateli
    - Konstruktérovi
@ulend

---

@snap[midpoint]
## @color[#adff2f](Diskuze)
@snapend

---

- Pozor na diody ve skleněném pouzdře
