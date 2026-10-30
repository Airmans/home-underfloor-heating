# Padlófűtés – felmérés és körönkénti szabályozás

A projekt célja a meglévő otthoni padlófűtési rendszer bizonyítékokra épülő felmérése, a körönkénti szabályozás megtervezése, valamint a biztonságos megvalósításhoz szükséges műszaki és dokumentációs terv elkészítése.

> **Jelenlegi állapot (2026-10-30):** PF-00 jóváhagyva és lezárva; a PF-01 felmérés megfigyelési és adatgyűjtési keretben folyamatban van. Az élő rendszerre ható műveletekhez külön jóváhagyás szükséges.

## Projektközpont és feladatkezelés

- **Notion projekt:** [Padlófűtés – felmérés és körönkénti szabályozás](https://app.notion.com/p/4063e49c5f5f8175a389dd906fbf129d)
- **PF-00 – Előkészítés, meglévő bizonyítékok és hatókör jóváhagyása:** [Notion-feladat](https://app.notion.com/p/4063e49c5f5f81c1806dd9a7d9a97c53)
- **PF-01 – Jóváhagyás után: fűtési rendszer helyszíni felmérése:** [Notion-feladat](https://app.notion.com/p/4063e49c5f5f819f8011f25cc85b3080)

A Notion a projektfeladatok, döntések, státuszok és a felmérés központi nyilvántartása. Ez a GitHub-repozitórium a verziókezelt műszaki dokumentáció és a kapcsolódó fájlok helye.

## Célok

- A meglévő fűtési rendszer és a rendelkezésre álló dokumentáció feltárása.
- A padlófűtési körök, a hidraulikai kialakítás és a szabályozási lehetőségek azonosítása.
- A körönkénti szabályozáshoz szükséges termosztátok, érzékelők, szelepmozgatók, vezérlők és tápellátás követelményeinek meghatározása.
- A Home Assistant-integráció lehetőségeinek és függőségeinek felmérése.
- A biztonsági, üzemeltetési, karbantartási és hibakezelési szempontok dokumentálása.
- Fokozatos, ellenőrizhető megvalósítási terv készítése, a szükséges tesztekkel és visszaállítási lehetőségekkel.

## Munkamódszer és bizonyítottság

Minden lényeges műszaki adatnál rögzíteni kell a forrást, a megfigyelés vagy dokumentum dátumát, valamint a bizonyítottsági szintet:

- **Ellenőrzött** – közvetlen megfigyelés, mérés vagy egyértelmű, hiteles dokumentum támasztja alá.
- **Részben ellenőrzött** – van alátámasztás, de további ellenőrzés szükséges.
- **Korábbi forrásból átvett** – másik projektből vagy korábbi felmérésből származik; az eredeti forrást és dátumot meg kell őrizni.
- **Ellenőrizetlen** – feltételezés vagy még nem igazolt információ.

A feltételezéseket nem szabad ellenőrzött tényként kezelni. A korábbi felmérésekből átvett információknál az eredeti forrásra és dátumra hivatkozni kell.

## Biztonsági és jóváhagyási szabályok

A jóváhagyott hatókörig kizárólag előkészítő, dokumentációs és tervezési munka végezhető. Külön, előzetes felhasználói jóváhagyás szükséges minden olyan lépéshez, amely:

- megváltoztatja a fűtés tényleges működését vagy vezérlését;
- Home Assistant- vagy más élő rendszerkonfigurációt módosít;
- elektromos bekötéssel, vezetékezéssel vagy szereléssel jár;
- hidraulikai beszabályozást vagy fűtést módosító tesztet végez.

Biztonsági vagy műszaki bizonytalanság esetén a munkát meg kell állítani, a kérdést dokumentálni kell, és döntést kell kérni. Jelszót, tokent, API-kulcsot és más titkot nem szabad a repóban vagy a Notion dokumentációban tárolni.


## Home Assistant MCP-kapcsolat

**Ellenőrizve:** 2026-10-30 (Europe/Budapest). A ChatGPT és a Home Assistant közötti MCP-kapcsolat működik: a `sensor.gepeszet_padlofutes_homero_padlofutes_eloremeno_homerseklet` entitás aktuális állapota sikeresen lekérdezhető volt a Home Assistant MCP-eszközén keresztül.

**Bizonyítottság:** Ellenőrzött – sikeres, élő, kizárólag olvasási célú entitáslekérdezés. Ez nem jelenti az összes MCP-művelet, integráció vagy hosszú távú rendelkezésre állás tesztelését.

**Felhasználás:** meglévő entitások, szenzorállapotok, előzmények és konfigurációs adatok célzott, olvasási célú vizsgálata a PF-01 felméréshez. A Home Assistant MCP a projekthez elérhető adatforrás; a korábbi bizonyítékokat nem kell indokolatlanul újra felmérni.

**Korlát:** a kapcsolat technikai képessége nem jelent felhatalmazást beavatkozásra. HA-konfiguráció, automatizmus, relé, szelep, fűtés vagy egyéb élő állapot módosítása csak külön, konkrét felhasználói jóváhagyással lehetséges. Hitelesítő adatokat, tokeneket és privát kapcsolati URL-eket nem tárolunk a GitHubban vagy a Notionban.

## Kapcsolódás a Home Computer Architecture projekthez

A [Home Computer Architecture repó](https://github.com/Airmans/home-computer-architecture) az otthoni IT-infrastruktúra elsődleges dokumentációs forrása. Ebből a projektből kizárólag a padlófűtéshez ténylegesen szükséges infrastruktúra-adatok vehetők át, az eredeti forrás, dátum és bizonyítottsági szint megőrzésével. A HCA projektben fűtési dokumentációt nem kell tárolni, és a már elvégzett IT-felméréseket nem szabad indokolatlanul megismételni.

## Javasolt dokumentációs felépítés

A dokumentumok a projekt előrehaladtával, a jóváhagyott feladatok alapján kerülnek létrehozásra. A felépítést nem szabad kész felmérés látszatát keltve előre feltölteni:

- `docs/` – műszaki felmérések, döntések, tervek és tesztjegyzőkönyvek.
- [Kazán és kazánoldali fűtésvezérlés](docs/kazan-es-kazanoldali-vezerles.md) – a kazánhoz kapcsolódó ismert adatok és nyitott kérdések.
- [Tado-termosztátok és időprogramok](docs/tado-termosztatok-es-idoprogramok.md) – eszközadatok, ütemezések és alkalmazásbeállítások.
- [Padlófűtési rendszer](docs/padlofutesi-rendszer.md) – külön felmérési adatlap a körökhöz és a hidraulikai kialakításhoz; a műszaki adatok felmérésre várnak.
- [Villamos elosztó](docs/villamos-eloszto.md) – fényképes megfigyelés és azonosításra váró elemek.
- `docs/evidence/` – releváns fényképek, címkék, rajzok és más bizonyítékok, amennyiben biztonságosan és megfelelően tárolhatók.
- `README.md` – projektcél, munkamódszer, biztonsági szabályok és dokumentációs navigáció.

A fájlnevek és a dokumentumjegyzék a PF-00 jóváhagyása után, a ténylegesen szükséges dokumentumok alapján pontosíthatók.


## Dokumentációs és forrásjegyzék

### Műszaki dokumentumok

- [Kazán és kazánoldali vezérlés](docs/kazan-es-kazanoldali-vezerles.md)
- [Padlófűtési rendszer és hidraulika](docs/padlofutesi-rendszer.md)
- [Padlófűtési körök és beszabályozás](docs/padlofutesi-korok-es-beszabalyozas.md)
- [Tado-termosztátok és időprogramok](docs/tado-termosztatok-es-idoprogramok.md)
- [Villamos elosztó](docs/villamos-eloszto.md)
- [Home Assistant-entitásleltár – ellenőrzési jegyzőkönyv](docs/home-assistant-entitasleltar-2026-10-30.md)

### Alaprajzok és eredeti bizonyítékok

- [PF-AL-00 – Eredeti építészeti alaprajz](docs/evidence/PF-AL-00-epiteszeti-alaprajz-eredeti-E-01.pdf)
- [PF-AL-01 – Nappali és konyha nyitott légtere](docs/evidence/PF-AL-01-nyitott-legterek-nappali-konyha.png)
- [PF-AL-02 – Nyitott terek és kapcsolatok](docs/evidence/PF-AL-02-nyitott-legterek-es-kapcsolatok.png)
- [PF-AL-03 – Padlófűtési körök és helyiségek](docs/evidence/PF-AL-03-padlofutesi-korok-es-helyisegek.png)
- [Padlófűtési körök és beállítások – forrásmunkafüzet](docs/evidence/padlofutes-beallitas-20261027.xlsx)

### Home Assistant-entitásnyilvántartás

- [Aktív Google Sheets – öt összevont munkalap](https://docs.google.com/spreadsheets/d/1C8MwPN9XDqlxIxq9Y7W9ttQdPe2uHFV2CqkSH99d3x0/edit)
- [Teljes archív Google Sheets – 43 munkalap](https://docs.google.com/spreadsheets/d/1bVRrP_qyaME_BwdqW0-GveBN2Kbxl0v_vSNa11RjfAo/edit)

A 38 eredeti munkalap 3407 forrássorából 3401 egyedi entitás került az aktív leltárba. A forrásegyezőség, a hat többforrású entitás és a fennmaradó kérdések a [jegyzőkönyvben](docs/home-assistant-entitasleltar-2026-10-30.md) találhatók. A fűtési szempontból releváns HA-érzékelők célzott felmérése még nyitott.


## Notion részfeladatok

A státuszok, lezárási feltételek és jóváhagyások elsődleges forrása a Notion. A dokumentum megléte önmagában nem jelent feladatlezárást.

| Feladat | Hivatkozás |
| --- | --- |
| PF-01.01 – Hőtermelő és vezérlőbemenetek | [Notion](https://app.notion.com/p/4063e49c5f5f815682abe1a0005b0f68) |
| PF-01.02 – Osztó-gyűjtő és hidraulika | [Notion](https://app.notion.com/p/4063e49c5f5f8193b5dcd0b0c052202e) |
| PF-01.03 – Körök és helyiségek megfeleltetése | [Notion](https://app.notion.com/p/4063e49c5f5f81b48c0be7003286c98f) |
| PF-01.04 – Termosztátok és szabályozás | [Notion](https://app.notion.com/p/4063e49c5f5f81cf9cc6fad61f53adf6) |
| PF-01.05 – Helyiségi érzékelők és HA-adatok | [Notion](https://app.notion.com/p/4063e49c5f5f813d851dfdf77eccbdf1) |
| PF-01.08 – Hőszivattyús átállás követelményei | [Notion](https://app.notion.com/p/4063e49c5f5f813aaaa9d9f63162f99c) |
| PF-01.09 – Hiánylista és kockázati jegyzék | [Notion](https://app.notion.com/p/4063e49c5f5f8128aacce002ff9da016) |
| PF-02.01 – Körönkénti szabályozás hardverigénye | [Notion](https://app.notion.com/p/4063e49c5f5f81909326ce080a4391f5) |
| PF-02.02 – Home Assistant-integráció és logika | [Notion](https://app.notion.com/p/4063e49c5f5f81888137e6a329ed4713) |

## Dátumok és változáskövetés

A projekt dokumentációjában a dátumokat és időbélyegeket **Europe/Budapest** időzóna szerint kell rögzíteni. A dokumentumokban különüljön el a felmérés dátuma, a dokumentum létrehozásának vagy módosításának dátuma és az adat forrásának dátuma, ha ezek eltérnek.

A műszaki döntéseket és a feladatok státuszát a Notionban kell vezetni; a GitHubon a dokumentumok verziótörténete követi a változásokat.
