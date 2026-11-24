# Dron

**Autori:** Marián Barcík (softvér), Radovan Kudri (hardvér)
**Trieda:** 3.BTL

## Cieľ projektu

Navrhnúť a zostrojiť dron typu kvadrokoptéra s vlastnou riadiacou jednotkou ESP32, ovládaný webovou aplikáciou
v mobilnom telefóne cez WiFi. Dron stabilizuje let pomocou PID regulátora a má bezpečnostné funkcie – predletovú
kontrolu, núdzové zastavenie a automatické pristátie pri strate signálu alebo vybitej batérii.

## Postup spustenia aplikácie

1. Nabite batériu LiPo 3S a pripojte ju k dronu (dron položte na rovnú plochu).
2. Počkajte na signalizáciu pripravenosti (zelená LED, 2 pípnutia).
3. Pripojte mobilný telefón k WiFi sieti `DRON-BK` (heslo dostane pilot od tímu).
4. V prehliadači otvorte adresu `http://192.168.4.1`.
5. Pred letom stlačte `ARM` a aktiváciu potvrďte podržaním tlačidla.

Podrobný návod bude v priečinku `06_Dokumentacia`.

## Štruktúra projektu

```
Barcik_Kudri-Dron/
├── 01_Poziadavky/        Čo má systém robiť
├── 02_Analyza/           Ako funguje problémová oblasť
├── 03_Navrh/             Ako navrhneme riešenie
├── 04_Implementacia/     Zdrojové kódy a aplikácia
│   └── src/
├── 05_Testovanie/        Overovanie správnosti
├── 06_Dokumentacia/      Návody a inštalácia
└── README.md
```
