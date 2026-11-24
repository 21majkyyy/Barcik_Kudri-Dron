# Dron

**Autori:** Marián Barcík (softvér), Radovan Kudri (hardvér)
**Trieda:** 3.BTL

## Cieľ projektu

Navrhnúť a zostrojiť dron typu kvadrokoptéra s vlastnou riadiacou jednotkou ESP32, ovládaný webovou aplikáciou
v mobilnom telefóne cez WiFi. Dron stabilizuje let pomocou PID regulátora a má bezpečnostné funkcie – predletovú
kontrolu, núdzové zastavenie a automatické pristátie pri strate signálu alebo vybitej batérii.

## Postup spustenia aplikácie

> Plánovaný postup – dron je vo fáze návrhu a zostavovania, firmvér a aplikácia sa pripravujú.

1. Nabite batériu LiPo 3S a pripojte ju k dronu (dron položte na rovnú plochu).
2. Počkajte na signalizáciu pripravenosti (zelená LED, 2 pípnutia).
3. Pripojte mobilný telefón k WiFi sieti `DRON-BK` (heslo dostane pilot od tímu).
4. V prehliadači otvorte adresu ovládacej aplikácie `http://192.168.4.1`.
5. Pred letom stlačte `ARM` a aktiváciu potvrďte podržaním tlačidla.

Podrobný návod bude v priečinku `06_Dokumentacia`.

## Štruktúra projektu

```
Barcik_Kudri-Dron/
├── 01_Poziadavky/        Čo má systém robiť – zadanie, roly, požiadavky
├── 02_Analyza/           Ako funguje problémová oblasť – procesy, use cases
├── 03_Navrh/             Ako systém vytvoríme
├── 04_Implementacia/     Funkčný zdrojový kód
│   └── src/
├── 05_Testovanie/        Ako overíme, že program funguje
├── 06_Dokumentacia/      Ako aplikáciu spustiť a používať
└── README.md
```
