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

---

#### Úvod 1:
## Proč checklist?

@ul
- 1. Někdo začíná a potřebuje vodítko
- 2. Chceme zlepšit stávající procesy
- 3. Protože jsme jen lidi a zapomínáme
@ulend

---

#### Úvod 2:
## Checklist pomáhá zlepšit...

@ul
- Přesnost
- Opakovatelnost
- Dostupnost
- Trasovatelnost
- Přenositelnost
@ulend

Note:

Trasovatelnost:
- Analýza poruch
- Servis a reklamace

---

#### Úvod 3:
## Kdy se už checklist vyplatil?

@ul
- Úspořil čas
- Úspořil peníze
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

Note:

Specifikace:
- Timing pro jednotlivé dávky

---

##### Před návrhem 2:
## Projektové etapy

@ul
- Název etapy, např.:
    - Funkční vzorek
    - Prototypová série
    - Ověřovací série
    - Sériová výroba
- Termín a množství
- Oponentura
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

TODO

---

@snap[midpoint]
## Skladové hospodářství
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

---

#### Skladové hospodářství 3:
## Struktura databáze 2/3

@ul
- Stručný popis
- Přílohy (výkresy, datasheety, atd.)
- Pouzdro
    - Označení (0402,SOIC-8)
    - Montážní technologie (SMT/THT)
- Aktuální zásoba
@ulend

---

#### Skladové hospodářství 4:
## Struktura databáze 3/3

@ul
- Výrobce (N)
    - Jméno + kontakt
    - Interní označení
- Dodavatel (N)
    - Jméno + kontakt
    - Interní označení
    - MOQ, MPU, L/T
    - Ceny (EUR/USD/CZK)
@ulend

Note:
- Interní part number = klíč
- Montážní technologie - důležité pro part list
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

## Designové opatření

@ul
- Diody ve skleněném pouzdře
- Keramické kondenzátory blízko kraji desky
    - Mechanické namáhání nejen při separaci soulepu
    - Zvážit použití flex term přívodů
- Impedanční přizpůsobení
- Moduly z jedné strany

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