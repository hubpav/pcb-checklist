@snap[midpoint]
# PCB CHECKLIST
### Pavel Hübner
HARDWARIO s.r.o.<br>
@snapend

@snap[south]
E-mail: pavel.hubner@hardwario.com<br>
Twitter: @pavelhubner<br>
@snapend

---

@snap[midpoint]
## Úvod
@snapend

Note:

- Uvedené pohledy jsou čistě subjektivní
- Každá firma/konstruktér si tvoří vlastní checklisty
- Nečekejte jednu dlouhou direktivní tabulku

---

#### Úvod 1:
## Důvod pro checklist

@ul
- 1. Někdo začíná a potřebuje vodítko
- 2. Potřebujeme zlepšit procesy
- 3. Návod pro nové kolegy
- 4. Nechceme opakovat stejné chyby
@ulend

Note:
- Od určitého objemu se chyby stávají

---

#### Úvod 2:
## Svatý grál výroby

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

#### Úvod 3:
## Struktura prezentace

@ul
- 1. Skladové hospodářství
- 2. Před návrhem
- 3. Fáze návrhu
- 4. Příprava podkladů
- 5. Zadání do výroby
@ulend

---

@snap[midpoint]
## (1) Skladové hospodářství
@snapend

---

#### Skladové hospodářství 1:
## Centrální databáze

@ul
- Nutnost na víc než jeden projekt
- Propojení na ECAD
- Propojení na generování výstupů
- Vazba na nákup, výrobu, obchod
@ulend

Note:
- TODO Screenshoty
- Jiné vnímání na IČO, startup, korporace

---

#### Skladové hospodářství 2:
## Struktura databáze 1/3

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
- Osazovací popisek (např. 100 nF)
    - Pomáhá při ručním osazení
@ulend

---

#### Skladové hospodářství 3:
## Struktura databáze 2/3

@ul
- Stručný popis, např.: z headline datasheetu
    - TMP112x High-Accuracy, Low-Power, Digital Temperature Sensors With SMBus and Two-Wire Serial Interface in SOT563
- Přílohy (výkresy, datasheety, atd.)
- Pouzdro
    - Označení (0402,SOIC-8)
    - Montážní technologie (SMT/THT)
- Aktuální zásoba (umístění)
    - Datum naskladění (nutné pro sledování expirace)
@ulend

Note:
- Montážní technologie - důležité pro part list

---

#### Skladové hospodářství 4:
## Struktura databáze 3/3

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
- Volná skladová karta
- Více výrobců
- Více dodavatelů
- Ceny v čase
- Důležitá je přesnost
- Kompromis mezi cenou a dostupností
- Dlouhé čekací lhůty

---

#### Skladové hospodářství 5:
## Optimalizace součástek

@ul
- Parametry, dostupnost, cena
- Hledání průniků
    - Existující produkty
    - V rámci designu
- Výrobní technologie
- Ve výrobní fázi:
    - Dostupnost
@ulend

Note:
- Průběžný proces

---

@snap[midpoint]
## (2) Před návrhem
@snapend

---

##### Před návrhem 1:
## Projektová šablona

@ul
- Specifikace produktu
- Vlastník produktu
- Cílový zákazník
- Požadované certifikace
- Odhad životního cyklu:
    - Kolik toho budeme vyrábět?
    - Jak dlouho budeme vyrábět?
@ulend

Note:

---

##### Před návrhem 2:
## Výrobní etapy

@ul
- Příklad rozdělení:
    - Funkční vzorek < 10 ks
    - Prototypová série < 100 ks
    - Ověřovací série < 1000 ks
    - Sériová výroba
- Termín a množství
- Oponentura před/po každé etapě
@ulend

Note:

---

#### Před návrhem 3:
## Technologické možnosti

@ul
- Výrobce desek
    - Prototypová výroba
    - Sériová výroba
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
## (3) Fáze návrhu
@snapend

---

##### Fáze návrhu 1:
## Technická rozvaha

@ul
- Blokový diagram
- Výběr součástek
    - Jednání s výrobci/distributory
- Výběr nástrojů
- Technická specifikace
- Oponentura
@ulend

---

#### Fáze návrhu 2:
## Návrhový cyklus desky

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

#### Fáze návrhu 3:
## Tvorba knihoven I.

@ul
- Praktická kategorizace
- Přiřadit interní part number
- Konzistentní pravidla a důslednost
- Správná specifikace balení v part number:
    - Bulk, Cut Tape, DigiReel
    - Tube, Tape & Reel, Tray
@ulend

Note:
- Pohlídat, že např. konektory mají osazovací čepičky

---

#### Fáze návrhu 4:
## Tvorba knihoven II.

@ul
- V názvu pouzdra specifikace technologie pájení:
    - Suffix _T pro manuální montáž
    - Suffix _R pro SMT montáž - pájení reflow
    - Suffix _W pro SMT montáž - pájení vlnou
- Konzultace s technology u výrobce

@ulend

Note:
- Pohlídat, že např. konektory mají osazovací čepičky

---

#### Fáze návrhu 4:
## Tvorba schématu

@ul
- Razítko (identifikátor + revize)
- Pojmenované všechny signály
- Pozor na diody ve skleněném pouzdře
- I2C adresy do schématu pod součástky
@ulend

---

#### Fáze návrhu 5:
## Návrh spojů I.

@ul
- Razítko (identifikátor + revize)
- Nulová souřadnice desky v levém dolním rohu
- Identifikátor + revize na desce
- Minimum solder mask sliver
- Impedanční přizpůsobení
- Netahejte měď až do kraje desky
- Unterminated traces
- Keramické kondenzátory blízko kraji desky
    - Zvážit použití flex term přívodů
    - Mechanické namáhání nejen při separaci soulepu
@ulend

---

#### Fáze návrhu 6:
## Návrh spojů II.

@ul
- Razítko (identifikátor + revize)
- Nulová souřadnice desky v levém dolním rohu
- Identifikátor + revize na desce
- Minimum solder mask sliver
- Impedanční přizpůsobení
- Netahejte měď až do kraje desky
- Unterminated traces
- Keramické kondenzátory blízko kraji desky
    - Zvážit použití flex term přívodů
    - Mechanické namáhání nejen při separaci soulepu
- Naváděcí díry pro jehlové pole
@ulend

---

#### Fáze návrhu 7:
## Technologické náležitosti

@ul
- Číslo revize desky např. formát Rx.y
    - x = major číslo (mění kompatibilita)
    - y = minor číslo (oprava, drobné vylepšení)
    - V případě verzovacího systému vytvořit tag
    - Např.: `hio-soil-sensor-r1.3`
- Prostor pro trasovatelný kód
    - Speciální vrstva - součást Gerber dat výrobci
- Značky pro osazovací automat (fiducials)
    - Kulatý pad o průměru 1 mm
    - Odmaskování o průměru 2 mm
    - Restrict na ostatní měď o průměru 2.4 mm
- Nulová souřadnice desky v levém dolním rohu
    - Někteří výrobci mají problém se zápornými souřadnicemi
- Naváděcí díry pro jehlové pole (min. průměr trnu 3 mm, díra 3.2 mm)
- Místo pro "bad mark"
- Identifikace vrstev mědi (kontrola)
@ulend

---

#### Fáze návrhu 8:
## Kontrola ERC/DRC

@ul
- "Je to jen varování"
- Šablonové nastavení
- Vygenerovat všechny polygony
- Cíl: Nothing to do!
- Statistiky (šířky spojů, prokovy, jména spojů)
@ulend

Note:
- Dodatečný prokov na spojení zemí a jeho odvrtávání

---

@snap[midpoint]
## (4) Příprava podkladů
@snapend

---

#### Příprava podkladů 1:
## Přehled dokumentace

@ul
- Soupiska součástek (BOM)
- Gerber + NC drill data
- Specifikace vrstev
- Výkres panelizace
- Seznam pozic (Pick and place)
- Osazovací plánky (poziční/hodnotové)
- Popis oživení a testování
@ulend

---

#### Příprava podkladů 2:
## Gerber + NC drill data

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

#### Příprava podkladů 3:
## Panelizace desky

@ul
- Jeden design na panel
- Optimalizace obrysu
- Typy separace
    - V-drážky (V Grooving)
    - Frézování (Milling)
    - Můstky (Tab breakout)
- Technologické okolí
    - "Tooling strip"
    - Po krajích zhruba 10 mm
    - Montážní díry
    - Pomocné využití - testování řízené impedance
@ulend

---

@snap[midpoint]
## (5) Zadání do výroby
@snapend

---

#### Zadání do výroby 1:
## Objednání DPS

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

#### Zadání do výroby 2:
## Objednání výroby

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

#### Zadání do výroby 3:
## Sledování zakázky

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

#### Zadání do výroby 4:
## Předání zakázky

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
## Diskuze
@snapend
