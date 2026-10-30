# Home Assistant entitásleltár – összevonás és ellenőrzés

**Ellenőrzés dátuma:** 2026-10-30 (Europe/Budapest)  
**Kapcsolódó feladat:** [PF-01.05](https://app.notion.com/p/4063e49c5f5f813d851dfdf77eccbdf1)  
**Bizonyítottság:** Ellenőrzött – a Google Sheets-munkalapok egyezősége; részben ellenőrzött – a nyilvántartott HA-entitások aktuális valós állapota.

## Elsődleges források

- [Aktív, öt munkalapos Google Sheets entitásnyilvántartás](https://docs.google.com/spreadsheets/d/1C8MwPN9XDqlxIxq9Y7W9ttQdPe2uHFV2CqkSH99d3x0/edit)
- [2026-10-30-i teljes archív másolat, 43 munkalappal](https://docs.google.com/spreadsheets/d/1bVRrP_qyaME_BwdqW0-GveBN2Kbxl0v_vSNa11RjfAo/edit)

## Végleges dokumentációs állapot

A 38 eredeti integrációs munkalap 3407 entitássorát az összevont nyilvántartás 3401 egyedi entitásazonosítóval tartalmazza. A forrásmunkalapok és sorok a központi leltár T–U oszlopaiban követhetők. A 38 eredeti munkalap eltávolítása előtt teljes Google Sheets-másolat készült, és az archív másolat 43 lapját, valamint a 3401 központi entitásazonosítót az eredetivel egyezőnek ellenőriztük. Az aktív fájlban ezt követően csak az alábbi lapok maradtak:

1. 01 Áttekintés
2. 02 Összes entitás
3. 03 Eszközök
4. 04 Integrációk
5. 05 Ellenőrzendők

**Tételes ellenőrzés:** 38 eredeti munkalap, 3407 forrássor; 0 hiányzó entitásazonosító, 0 hiányzó forráshivatkozás. A 37 nem érintett munkalap 14 eredeti adatmezője egyezik a központi leltárral. A Segédentitások lapon hat átfedő entitás összesen 30 leíró mezőeltérést mutatott; ezek nem azonosító- vagy állapoteltérések, és mindkét eredeti forráshivatkozás megmaradt.

## Hat többforrású entitás

| Entitás | Eredeti források | Értelmezés |
| --- | --- | --- |
| `sensor.inverter_aramtermeles_pillanatnyi` | Segédentitások!54; Huawei Solar!53 | template-platform és inverterhez kapcsolt eszközleírás |
| `sensor.inverter_aramtermeles_pillanatnyi_l1` | Segédentitások!55; Huawei Solar!50 | ugyanez, L1 |
| `sensor.inverter_aramtermeles_pillanatnyi_l2` | Segédentitások!56; Huawei Solar!51 | ugyanez, L2 |
| `sensor.inverter_aramtermeles_pillanatnyi_l3` | Segédentitások!57; Huawei Solar!52 | ugyanez, L3 |
| `humidifier.furdo_paratlanitas` | Shelly!30; Segédentitások!91 | generic_hygrostat-platform és Shelly-eszközkapcsolat |
| `humidifier.haztartasi_paratlanitas` | Shelly!90; Segédentitások!92 | generic_hygrostat-platform és Shelly-eszközkapcsolat |

A hat esetben az eltérő oszlopok: A (eszköznév), B (terület), K (leírás), L (forrás/integráció), N (megjegyzés). A forráskülönbség nem bizonyítja, hogy a platform és a kapcsolódó fizikai eszköz integrációja azonos. Az eredeti értékek az archívumban megmaradtak.

## Nyitott kérdések és korlátok

A „05 Ellenőrzendők” munkalap 1059 ellenőrzendő egyedi entitást sorol fel; ez nem 1059 bizonyítottan hibás eszköz. A munkalap korábbi HA-regiszter- és állapotlekérdezésekből származó eltéréseket is tartalmaz. Az „01 Áttekintés” szerinti 2382 aktuális HA-regiszterben ellenőrzött és 1019 csak korábbi leltárban szereplő entitás a leltár forrásadata, nem e dokumentum készítésekor újra lekérdezett HA-állapot. A 249 eszközcsoport név/terület/integráció szerinti csoportosítás, nem 249 igazolt HA device ID.

A teljes leltár nem egyenlő a PF-01.05 fűtési szempontból releváns szenzorainak lezárt megfeleltetésével. A releváns érzékelők és a hiányzó/átnevezett entitások célzott vizsgálata a PF-01.05 feladatban folytatandó. A HCA dokumentációt nem másoljuk át.

**Módosítások határa:** csak Google Drive-nyilvántartás és dokumentáció módosult; Home Assistant-konfiguráció, automatizmus és fűtési rendszer nem.
