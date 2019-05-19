@snap[midpoint]

# PCB CHECKLIST
### Pavel Hübner

HARDWARIO s.r.o.

Twitter: @pavelhubner

GitHub: github.com/hubpav

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
---

#### Úvod 3:
## Struktura prezentace

@ul
- 1. Skladové hospodářství
- 2. Před návrhem
- 3. Design fáze
- 4. Generování podkladů
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
- Propojení na ECAD
- Propojení na generování výstupů
- Vazba na nákup, výrobu, obchod
@ulend

---

#### Skladové hospodářství 2:
## Struktura databáze 1/3

@ul
- Interní part number
    - Uvedení kategorie (IC,R,C,BAT,...)
    - Příklad: HIO-IC-TMP112
- Stav součástky
    - NEW/ACT/NRND/EOL
- Osazovací popisek
    - Pomáhá při ručním osazení
@ulend

Note:
- Interní part number = klíč

---

#### Skladové hospodářství 3:
## Struktura databáze 2/3

@ul
- Stručný popis
- Přílohy (výkresy, datasheety, atd.)
- Pouzdro
    - Označení (0402,SOIC-8)
    - Montážní technologie (SMT/THT)
- Aktuální zásoba (umístění)
@ulend

Note:
- Montážní technologie - důležité pro part list

---

#### Skladové hospodářství 4:
## Struktura databáze 3/3

@ul
- Výrobce (n)
    - Jméno + kontakt
    - Interní označení
- Dodavatel (n)
    - Jméno + kontakt
    - Interní označení
    - MOQ, MPU, L/T
    - Ceny (EUR/USD/CZK)
@ulend

Note:
- Volná skladová karta
- Více výrobců
- Více dodavatelů
- Ceny v čase

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

---

@snap[midpoint]
## Před návrhem
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
## Fáze návrhu
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
## Tvorba knihoven

@ul
- Praktická kategorizace
- Nezapomenout interní part number
- Konzistentní pravidla
- Konzultace s technology u výrobce
- Správná specifikace balení:
    - Bulk, Cut Tape
    - Tape & Reel, Tray
    - DigiReel
@ulend

---

#### Fáze návrhu 4:
## Tvorba schématu

@ul
- Razítko (identifikátor + revize)
- Pojmenované všechny signály
- Diody ve skleněném pouzdře
- TODO...
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
@ulend

---

#### Fáze návrhu 7:
## Kontrola ERC/DRC

@ul
- "Je to jen varování"
- Šablonové nastavení
@ulend

---

## Checklist před dokončením

@ul
- Označení desky (Rx.y)
- Prostor pro trasovatelný kód
- Značky pro OA (fiducials)
- Badmarky
- Osazovací plánek
  - Poziční a hodnotový
- Aktuální vygenerovaný ground plane
- ERC/DRC
@ulend

---

## Generování podkladů

@ul
- Prostor pro trasovatelný kód
- Značky pro OA (fiducials)
- Badmarky
- Osazovací plánek
  - Poziční a hodnotový
- Aktuální vygenerovaný ground plane
- ERC/DRC
@ulend

---

## Generování Gerber

@ul
- Obrys desky
- Frézování (pokovené/nepokovené)
- Měď všechny vrstvy
- Maska T/B
- Potisk T/B
- Pájecí pasta T/B - v případě planžety
@ulend

---

## Panelizace desky

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

---

## Výroba desky

- Název desky, počet kusů, termín
- Technologie
    - Počet vrstev + layer stack
    - Barva masky
    - Povrchová úprava
    - Testování
- Výrobní data

---

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



---

## Výrobní dokumentace

@ul
- Gerber
- NC Drill
- PCB stack
- Panelizace
- Part list
- BOM
- Osazovací plánky
    - Poziční
    - Hodnotové
- Popis oživení
- Popis testování
@ulend

---

## Specifikace výroby

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
- FUCKUP: Nejednou jsme jeli do Pragoboardu pro planžetu.

---

## Sledování výroby

@ul
- Potvrzení přijetí zakázky
- Potvrzení správnosti podkladových materiálů
    - Iterační proces
- Pravidelná komunikace a kontrola
    - Alokace na lince
    - Plnění subdodávek
@ulend

---

## Převzetí zakázky

@ul
- Předávací protokol
- Servisní operace
    - Testery
- Zpětná vazba výrobci
- Zpětná vazba zadavateli
    - Konstruktérovi
@ulend

---

@snap[midpoint]
## Diskuze
@snapend