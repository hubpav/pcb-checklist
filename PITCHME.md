@snap[midpoint]
# PCB Checklist
### Pavel Hübner

HARDWARIO s.r.o.

Twitter: @pavelhubner
GitHub: github.com/hubpav

@snapend

---
@snap[midpoint]
## Cíl výrobního procesu
@snapend

- Přesnost
- Přenositelnost
- Opakovatelnost
- Dostupnost
- Předvídatelnost
- Trasovatelnost

---

@snap[midpoint]
## Před návrhem
@snapend

@box[text-orange span-80 fragment](Mars Attacks # Greetings earthlings. We come in peace!)

---

##### Před návrhem:
## Designové vstupy

@ul
- Kolik toho budeme vyrábět
- Jak dlouho budeme vyrábět
- Jak bude vypadat "release train"?
- Dostupnost součástek?
@ulend

Note:
- Timing pro jednotlivé dávky

---

#### Před návrhem:
## Technologické možnosti

@ul
- Prototypová výroba desky
- Sériová výroba desky
@ulend

---

## Skladové hospodářství

@ul
- Centrální databáze
- Propojení na ECAD
- Propojení na generování výstupů
@ulend

---

#### Skladové hospodářství:
## Centrální databáze 1/2

@ul
- Interní part number
    - Uvedení kategorie
    - Příklad: HIO-IC-TMP112
- Stav součástky
    - NEW/ACT/NRND/EOL
- Osazovací popisek
    - Pomáhá pro ruční osazení
- Stručný popis
- Pouzdro
    - Označení (0402, SOIC-8)
    - Montážní technologie (SMT/THT)
- Aktuální zásoba

---

#### Skladové hospodářství:
## Centrální databáze 2/2

@ul
- Výrobce (N)
    - Jméno
    - Označení
- Dodavatel (N)
    - Jméno
    - Označení
    - MOQ / MPU
    - L/T
    - Ceny
        - EUR/USD/CZK
@ulend

Note:
- Interní part number = klíč
- Montážní technologie - párování na part list
- Volná skladová karta
- Více výrobců
- Více dodavatelů
- Ceny v čase

---

## Optimalizace součástek

@ul
1. Parametry
2. Dostupnost
3. Cena
@ulend

---

@snap[midpoint]
## Checklist před dokončením
@snapend

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
- Gerber
- NC Drill
- Part list
- BOM
- Osazovací plánky
    - Poziční
    - Hodnotové
- Prostor pro trasovatelný kód
- Značky pro OA (fiducials)
- Badmarky
- Osazovací plánek
  - Poziční a hodnotový
- Aktuální vygenerovaný ground plane
- ERC/DRC

@ulend


---

## Panelizace desky

---

## Výrobní dokumentace

---

## Specifikace výroby

---

@snap[midpoint]
## Diskuze
@snapend