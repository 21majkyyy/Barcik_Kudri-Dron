# Zadanie a cieľ projektu

**Projekt:** Dron
**Trieda:** 3.BTL
**Tím:** Marián Barcík (softvér), Radovan Kudri (hardvér)

## Zadanie

Navrhnúť a zostrojiť dron typu kvadrokoptéra s vlastnou riadiacou jednotkou na báze mikrokontroléra ESP32,
ktorý sa ovláda webovou aplikáciou v mobilnom telefóne cez WiFi.

## Cieľ projektu

- postaviť funkčný dron (rám, pohon, napájanie, senzory) – hardvér,
- naprogramovať firmvér, ktorý stabilizuje let pomocou PID regulátora – softvér,
- vytvoriť ovládaciu aplikáciu s virtuálnymi joystickmi a zobrazením telemetrie – softvér,
- zabezpečiť bezpečnú prevádzku: predletová kontrola, núdzové zastavenie, automatické pristátie
  pri strate signálu a pri vybitej batérii.

## Rozsah

- **V rozsahu:** let v manuálnom režime so stabilizáciou, ovládanie cez WiFi, telemetria, servisný režim
  (kalibrácia, nastavenie PID), bezpečnostné funkcie.
- **Rozšírenia (ak zostane čas):** udržiavanie výšky, záznam letových dát, aktualizácia firmvéru cez WiFi, kamera.
- **Mimo rozsahu:** autonómny let podľa GPS.

## Rozdelenie práce

| Člen tímu | Oblasť | Úlohy |
|---|---|---|
| Marián Barcík | Softvér | firmvér ESP32, PID regulácia, komunikácia, webová aplikácia |
| Radovan Kudri | Hardvér | výber komponentov, rám, pohon, napájanie, zapojenie senzorov |
