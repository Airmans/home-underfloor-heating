# Padlófűtés – meglévő hidraulikai rendszer és körök

**Dokumentumállapot:** folyamatban lévő helyszíni felmérés.  
**Utolsó frissítés:** 2026-10-27, Europe/Budapest.  
**Bizonyítottság:** az alábbi megállapításoknál külön jelölve.

## Cél és hatókör

Ebben a dokumentumban kerül rögzítésre a padlófűtési oldal tényleges kialakítása: osztó-gyűjtő, körök, helyiségekhez rendelés, szelepek és szelepmozgatók, szivattyú/keverőkör (ha van), csővezetékek, hidraulikai beszabályozásra utaló jelölések, hőmérséklet-monitorozás, valamint a későbbi körönkénti szabályozás műszaki feltételei.

## Azonosított osztó-gyűjtő

| Adat | Megállapítás | Bizonyítottság / forrás |
| --- | --- | --- |
| Gyártó | FERRO | **Ellenőrzött** – 2026-10-27-én megosztott helyszíni fényképen olvasható márkajelzés |
| Körök száma | 8 kör látható | **Ellenőrzött** – 2026-10-27-én megosztott áttekintő fénykép |
| Felső gerenda | Átfolyásmérőkkel szerelt | **Ellenőrzött** – fénykép alapján |
| Alsó gerenda | 8 fehér kézi sapka látható a körökhöz tartozó szelepeken | **Ellenőrzött** – fénykép alapján; a szelepbetétek pontos típusa még nincs azonosítva |
| Lehetséges típus | SN-RZP08S vagy SN-RZPU08S | **Részben ellenőrzött** – a külső kialakítás és a FERRO adatlapok alapján, pontos altípus nincs megerősítve |
| Gerenda névleges mérete | 1" mindkét megjelölt változat gyártói adatlapján | **Korábbi forrásból átvett** – felhasználó által megadott FERRO adatlapok: [SN-RZP](https://www.ferro.hu/sn-rzp-1-tipusu-g1-8-koros-acel-oszto-gyujto-aramlasmerovel-es-elzaroszeleppel), [SN-RZPU](https://www.ferro.hu/sn-rzpu-s-tipusu-3-4-8-koros-acel-oszto-gyujto-termofejezheto-csatlakozasi-lehetoseggel-aramlasmerovel) |
| Visszatérő oldali szelep csatlakozása | A gyártói adatlapok M30×1,5 termoelektromos működtető csatlakoztatásának lehetőségét említik | **Korábbi forrásból átvett** – a beépített szelep kompatibilitása helyszíni ellenőrzést igényel |
| Főbekötés / pontos altípus | A konkrétan beépített változat nincs egyértelműen azonosítva | **Ellenőrizetlen** |

## Hőmérséklet-monitorozás és nyomásmérő

| Adat | Megállapítás | Bizonyítottság / forrás |
| --- | --- | --- |
| Előremenő hőmérséklet | A felhasználó közlése szerint Home Assistantban monitorozva van, csőre rögzített csőhőmérővel | **Korábbi forrásból átvett** – felhasználói közlés, 2026-10-27 |
| Visszatérő hőmérséklet | A felhasználó közlése szerint Home Assistantban monitorozva van, csőre rögzített csőhőmérővel | **Korábbi forrásból átvett** – felhasználói közlés, 2026-10-27 |
| Kapcsolódó eszköz | A felhasználó Shelly 1 eszközt nevezett meg a hőmérséklet-monitorozással kapcsolatban | **Részben ellenőrzött** – a pontos bekötés, hőmérséklet-érzékelő típusa és az, hogy a Shelly 1 közvetlenül vagy köztes eszközön keresztül vesz-e részt a mérésben, még nincs dokumentálva |
| Nyomásmérő | A felhasználó közlése szerint az osztó-gyűjtő alsó gerendájának bal oldalára van rögzítve nyomásmérő | **Részben ellenőrzött** – helyszíni közeli fényképen a mérő és a skála még nem azonosított; leolvasott érték nincs rögzítve |

### A monitorozás további ellenőrzéséhez szükséges adatok

- A Home Assistantban használt előremenő- és visszatérő-hőmérséklet entitások neve.
- A csőhőmérők / hőmérséklet-érzékelők pontos típusa és csatlakoztatása.
- A Shelly 1 pontos szerepe a mérési láncban. A „Shelly 1” megnevezés önmagában nem bizonyítja, hogyan történik a hőmérséklet mérése.
- A nyomásmérő skálájának, mértékegységének és aktuális értékének fényképe, ha biztonságosan leolvasható. Az aktuális nyomásérték még nincs rögzítve.

## Még felmérendő adatok

| Terület | Rögzítendő bizonyíték |
| --- | --- |
| Padlófűtési körök | Körjelölések, átfolyásmérők aktuális leolvasása, ha jól látható |
| Helyiség-hozzárendelés | Melyik kör melyik helyiséget fűti; bizonyíték és bizonyosság |
| Szelepek | Szelepbetétek pontos típusa és a működtető csatlakoztathatósága |
| Hidraulika | Szivattyú, keverőszelep, bypass és más elemek, ha vannak |
| Jelenlegi vezérlés | Van-e már körönkénti vezérlő vagy csak központi kazánigény |
| Hőmérséklet-mérés | HA entitások, érzékelők, mérési pontok és bekötés pontosítása |

## Biztonsági korlát

A felmérés alapértelmezésben fényképes megfigyelés és dokumentumgyűjtés. Szelepek állítását, körök elzárását, hidraulikai beszabályozást, elektromos szerelést vagy a fűtés tényleges működését befolyásoló tesztet külön, konkrét felhasználói jóváhagyás nélkül nem szabad végezni.
