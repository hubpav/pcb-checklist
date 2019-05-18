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

@ul
- Přesnost
- Opakovatelnost
- Dostupnost
- Předvídatelnost
- Trasovatelnost
- Přenositelnost
@ulend

---

@snap[midpoint]
## Před návrhem
@snapend

---

##### Před návrhem:
## Designové vstupy

@ul
- Specifikace produktu
- Kolik toho budeme vyrábět
- Jak dlouho budeme vyrábět
- Jak bude vypadat výrobní pipeline
@ulend

Note:
- Timing pro jednotlivé dávky

---

##### Před návrhem:
## Technická rozvaha

@ul
- Blokový diagram
- Výběr součástek
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

#### Skladové hospodářství:
## Optimalizace součástek

@ul
- Parametry
- Dostupnost
- Cena
@ulend

Důležitá je schopnost iterace

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

## Panelizace desky

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