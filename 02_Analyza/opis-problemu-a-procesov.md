# Opis problému a procesov

## Opis problému

Dron typu kvadrokoptéra je lietajúce zariadenie so štyrmi rotormi. Na rozdiel od lietadla nemá prirodzenú
stabilitu – bez neustálej regulácie otáčok motorov by sa okamžite prevrátil. Systém preto musí niekoľko stokrát
za sekundu zisťovať polohu dronu a upravovať otáčky jednotlivých motorov.

Pohyb dronu vzniká rozdielom otáčok motorov:

- **stúpanie a klesanie** – všetky motory zrýchlia alebo spomalia rovnako,
- **náklon vpred, vzad a do strán** – motory na jednej strane sa točia rýchlejšie ako na druhej,
- **otáčanie okolo zvislej osi** – dvojica motorov točiacich sa v smere hodinových ručičiek zrýchli oproti druhej dvojici.

Pilot nezadáva otáčky motorov priamo, ale požadovaný pohyb (plyn, náklon, otáčanie). Systém požadovaný pohyb
prepočíta na otáčky motorov a súčasne vyrovnáva nežiaduce výchylky (vietor, nerovnomerné rozloženie hmotnosti).

Hlavné riziká, ktoré musí systém riešiť:

- **strata spojenia** s ovládačom – dron nesmie odletieť ani spadnúť,
- **vybitie batérie** počas letu – napätie batérie LiPo nesmie klesnúť pod bezpečnú hranicu,
- **nechcené spustenie motorov** – rotujúce vrtule môžu spôsobiť zranenie,
- **nesprávne údaje zo senzorov** – bez kalibrácie dron nevie, kedy je vo vodorovnej polohe.

## Procesy

### 1. Príprava a let

1. Pilot pripojí batériu, dron vykoná test senzorov a signalizuje pripravenosť.
2. Pilot sa pripojí k dronu z mobilného telefónu (UC-001).
3. Pilot požiada o aktiváciu motorov; systém vykoná predletovú kontrolu a po potvrdení motory aktivuje (UC-002).
4. Pilot ovláda let, systém stabilizuje dron a posiela telemetriu (UC-003, UC-005, UC-013).
5. Pilot pristane a deaktivuje motory (UC-010).

### 2. Riešenie mimoriadnych situácií

- Nebezpečenstvo → pilot okamžite zastaví motory (UC-004).
- Strata spojenia na viac ako 1 s → dron sa vyrovná a riadene pristane (UC-006).
- Nízke napätie batérie → upozornenie pilota, pri kritickom napätí automatické pristátie (UC-007).

### 3. Servis a údržba

1. Technik sa prihlási do servisného režimu.
2. Technik podľa potreby kalibruje senzory (UC-008), nastaví parametre regulácie (UC-009),
   stiahne záznam letu (UC-011) alebo aktualizuje firmvér (UC-012).
3. Všetky servisné činnosti sa vykonávajú iba pri vypnutých motoroch.

Podrobné scenáre sú v priečinku `pripady-pouzitia/`, prehľad a diagram v súbore `use-case-diagram-a-scenare.docx`.
