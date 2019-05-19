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

- 1. Skladové hospodářství
- 2. Design vstupy
- 3. Design fáze
- 4. Generování podkladů
- 5. Zadání do výroby

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

#### Skladové hospodářství 4:
## Optimalizace součástek

@ul
- Parametry, dostupnost, cena
- Hledání průniků
    - Existující produkty
    - V rámci designu
- Výrobní technologie
@ulend

---

@snap[midpoint]
## Před návrhem
@snapend

---

##### Před návrhem 1:
## Designové vstupy

@ul
- Vlastník produktu
- Specifikace produktu
- Cílový zákazník
- Požadované certifikace
- Odhad životního cyklu:
    - Kolik toho budeme vyrábět?
    - Jak dlouho budeme vyrábět?
@ulend

---

##### Před návrhem 2:
## Projektové etapy

@ul
- Příklad rozdělení:
    - Funkční vzorek < 10 ks
    - Prototypová série < 100 ks
    - Ověřovací série < 1000 ks
    - Sériová výroba
- Termín a množství
- Každá fáze uzavřená oponenturou
@ulend

---

#### Před návrhem 3:
## Technologické možnosti

@ul
- Výrobce desek
    - Prototypová výroba
    - Sériová výroba
- Možnosti ručního osazení
- Sériová výroba desky
- Požadavky na výrobní tester
@ulend

Note:
- Zázemí RTG

---

##### Před návrhem 4:
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

@snap[midpoint]
## Fáze návrhu
@snapend

---

#### Fáze návrhu 1:
## PCB design cyklus

- 1. Tvorba knihoven
- 2. Návrh zapojení
- 3. Rozmístění součástek
- 4. Routing spojů
- 5. PCB review
- 6. Odeslání do výroby

---

## Designové opatření

@ul
- Rozdíl mezi dobrou deskou a skvělou deskou
    - Počet jejich interací

- DFM by měl být od začátku procesu
- Minimalizace lidské práce
- Diody ve skleněném pouzdře
- Keramické kondenzátory blízko kraji desky
    - Mechanické namáhání nejen při separaci soulepu
    - Zvážit použití flex term přívodů
- Impedanční přizpůsobení
- Moduly z jedné strany
- Minimum solder mask sliver
- Board origin bottom left
- Unterminated traces

- malovýrobá dostupnost:
    - Bulk
    - Cut Tape
    - Tape & Reel
    - Tray
    - DigiReel
- Netahejte měď až do kraje desky
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