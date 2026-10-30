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

## Dátumok és változáskövetés

A projekt dokumentációjában a dátumokat és időbélyegeket **Europe/Budapest** időzóna szerint kell rögzíteni. A dokumentumokban különüljön el a felmérés dátuma, a dokumentum létrehozásának vagy módosításának dátuma és az adat forrásának dátuma, ha ezek eltérnek.

A műszaki döntéseket és a feladatok státuszát a Notionban kell vezetni; a GitHubon a dokumentumok verziótörténete követi a változásokat.
