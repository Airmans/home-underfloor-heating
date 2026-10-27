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

### Home Assistant / Shelly

A 2026-10-27-én megosztott Home Assistant-eszközoldal és felhasználói közlés alapján:

| Adat | Megállapítás | Bizonyítottság / forrás |
| --- | --- | --- |
| Eszköz neve | „Padlófűtés hőmérő” | **Ellenőrzött** – Home Assistant képernyőkép, 2026-10-27 |
| Eszköztípus / modell | Shelly 1 / SHSW-1, gen1 hardver | **Ellenőrzött** – eszközinformációs képernyőkép, 2026-10-27 |
| Firmware | 20230913-112003/v1.14.0-gcb84623 | **Ellenőrzött** – eszközinformációs képernyőkép, 2026-10-27 |
| Eszköz IP-címe | 192.168.10.92 | **Ellenőrzött a megosztott képernyőkép alapján** – 2026-10-27; ez az eszköz akkori megjelenített IP-címe, nem garantáltan állandó cím |
| Előremenő hőmérséklet entitás | `sensor.gepeszet_padlofutes_homero_padlofutes_eloremeno_homerseklet` | **Ellenőrzött** – a felhasználó által megadott entitásazonosító, 2026-10-27 |
| Visszatérő hőmérséklet entitás | `sensor.gepeszet_padlofutes_homero_padlofutes_visszatero_homerseklet` | **Ellenőrzött** – a felhasználó által megadott entitásazonosító, 2026-10-27 |
| Képernyőképen látható előremenő érték | 23,8 °C | **Ellenőrzött mint pillanatfelvétel** – Home Assistant képernyőkép, 2026-10-27; nem tekintendő tartós vagy aktuális értéknek későbbi időpontban |
| Képernyőképen látható visszatérő érték | 23,4 °C | **Ellenőrzött mint pillanatfelvétel** – Home Assistant képernyőkép, 2026-10-27; nem tekintendő tartós vagy aktuális értéknek későbbi időpontban |
| Mérési pontok | A felhasználó közlése szerint csőre rögzített csőhőmérők mérik az előremenő és visszatérő csövet | **Korábbi forrásból átvett** – felhasználói közlés, 2026-10-27 |
| Érzékelők és fizikai bekötés | A HA eszközoldal két hőmérséklet-entitást mutat az eszközhöz rendelve, de a fizikai érzékelő típusa és csatlakoztatásának módja a képernyőképekből nem állapítható meg | **Részben ellenőrzött** |

**Megjegyzés:** a Home Assistant képernyőkép bizonyítja, hogy a két hőmérséklet-entitás a „Padlófűtés hőmérő” nevű Shelly-eszköz oldalán jelenik meg. Önmagában nem igazolja a hőmérséklet-érzékelők pontos típusát vagy fizikai bekötését. Ezeket később a mérési lánc dokumentálásakor kell tisztázni.

### Nyomásmérő

| Adat | Megállapítás | Bizonyítottság / forrás |
| --- | --- | --- |
| Elhelyezés | A felhasználó közlése szerint az osztó-gyűjtő alsó gerendájának bal oldalára van rögzítve nyomásmérő | **Részben ellenőrzött** – felhasználói közlés, 2026-10-27 |
| Skála, mértékegység és leolvasott érték | Még nincs dokumentálva | **Ellenőrizetlen** – szükséges a számlap jól olvasható fényképe |

## A monitorozás további ellenőrzéséhez szükséges adatok

- A csőhőmérők / hőmérséklet-érzékelők pontos típusa és csatlakoztatása.
- A két hőmérséklet-entitás eszközoldalán megjelenő attribútumok, ha a mérési forrást tisztázni kell.
- A nyomásmérő skálájának, mértékegységének és aktuális értékének fényképe, ha biztonságosan leolvasható. Az aktuális nyomásérték még nincs rögzítve.

## Kapcsolódó dokumentum – körkiosztás és beszabályozás

A nyolc kör helyiség-hozzárendelése, a táblázat szerinti területek, korrekciós tényezők és a felhasználó által megerősített jelenlegi `Poz` beállítások külön dokumentumban szerepelnek: [Padlófűtési körök és jelenlegi beszabályozás](padlofutesi-korok-es-beszabalyozas.md). Az eredeti Excel-forrás tervezett repo-útvonala: `evidence/padlofutes-beallitas-20261027.xlsx`; feltöltésre még vár.

## Még felmérendő adatok

| Terület | Rögzítendő bizonyíték |
| --- | --- |
| Padlófűtési körök | Körjelölések, átfolyásmérők aktuális leolvasása, ha jól látható |
| Helyiség-hozzárendelés | Melyik kör melyik helyiséget fűti; bizonyíték és bizonyosság |
| Szelepek | Szelepbetétek pontos típusa és a működtető csatlakoztathatósága |
| Hidraulika | Szivattyú, keverőszelep, bypass és más elemek, ha vannak |
| Jelenlegi vezérlés | Van-e már körönkénti vezérlő vagy csak központi kazánigény |

## Biztonsági korlát

A felmérés alapértelmezésben fényképes megfigyelés és dokumentumgyűjtés. Szelepek állítását, körök elzárását, hidraulikai beszabályozást, elektromos szerelést vagy a fűtés tényleges működését befolyásoló tesztet külön, konkrét felhasználói jóváhagyás nélkül nem szabad végezni.
