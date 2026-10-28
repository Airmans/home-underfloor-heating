# Padlófűtési körök és jelenlegi beszabályozás

**Rögzítés dátuma:** 2026-10-27, Europe/Budapest  
**Állapot:** a körkiosztás és a beállítások a felhasználó által megosztott Excel és alaprajz alapján dokumentálva.  
**Bizonyítottság:** a táblázatban látható értékek forrásból átvéve; a jelenlegi beállításokat a felhasználó 2026-10-27-én kifejezetten megerősítette.

## Források

- Elsődleges forrás: felhasználó által megosztott `Padlófűtés beállítás.xlsx` munkafüzet, benne a körkiosztással, méretekkel, korrekciós tényezőkkel és alaprajzzal.
- Verziókezelt forrásfájl: [`docs/evidence/padlofutes-beallitas-20261027.xlsx`](evidence/padlofutes-beallitas-20261027.xlsx). A felhasználó 2026-10-27-én letöltötte és ellenőrizte a GitHubon tárolt fájlt; visszajelzése szerint rendben van.
- Felhasználói megerősítés: a `Poz` oszlopban szereplő értékek a jelenlegi tényleges beállításokat tükrözik.
- Ellenőrzés dátuma: 2026-10-27, Europe/Budapest.

## Körök és helyiségek

| Kör | Helyiség(ek) | Táblázat szerinti terület | Korrekció | Poz |
|---:|---|---:|---:|---:|
| 1 | Fürdő, WC, előszoba | 14,1 m² | 100% | 0,7 |
| 2 | Előszoba, konyha | 11,8 m² | 80% | 0,5 |
| 3 | Zoé | 13,5 m² | 140% | 1,0 |
| 4 | Zsombi | 13,5 m² | 140% | 1,0 |
| 5 | Konyha | 19,8 m² | 100% | 1,0 |
| 6 | Nappali | 19,5 m² | 100% | 1,0 |
| 7 | Háló | 11 m² | 80% | 0,5 |
| 8 | Dolgozó, gardrób | 11 m² | 20% | 0,1 |

A munkafüzetben szereplő területek és a `Korrekció` oszlop értékei az eredeti táblázatból kerültek át. A képletek értelmezésekor a 19,5 m²-es nappali szerepel referencia-területként; a képletellenőrzés nem helyettesíti a helyszíni hidraulikai mérést.

## Helyszíni elrendezés és korábbi felmérés

- A körök helyiségekhez rendelését a felhasználó korábban hőkamerával mérte fel.
- A forrásmunkafüzet alaprajzán a körszámok és az érintett zónák is fel vannak tüntetve.
- A rajzon fehérrel jelölt terület a felhasználó közlése szerint a háztartási helyiség, ahol a kazán és az osztó-gyűjtő található.
- A felhasználó szerint a jelenlegi beállítások mellett a szobák hőmérséklete megközelítőleg azonos.

## Bizonyítottság és korlátok

- **Ellenőrzött a forrásban:** a körszámok, a táblázatban megadott helyiségek, területek, korrekciók és `Poz` értékek a megosztott munkafüzetben láthatók.
- **A fájl megléte és felhasználói ellenőrzése megerősített:** a felhasználó 2026-10-27-én letöltötte a GitHubon tárolt Excel-fájlt, és visszaigazolta, hogy rendben van. Ez nem jelent független műszaki validálást a táblázat adatainak helyességéről.
- **Ellenőrzött felhasználói megerősítés alapján:** a `Poz` értékek a jelenlegi tényleges beállítások.
- **Korábbi mérési forrásból átvett:** a hőkamerás körazonosítás és az alaprajzi zónakiosztás; a korábbi hőkamerás mérési jegyzőkönyv külön nincs csatolva ebben a dokumentumban.
- **Felhasználói tapasztalat:** a szobák nagyjából azonos hőmérsékletűek a jelenlegi beszabályozással; ehhez itt nincs csatolt, egyidejű hőmérséklet-adatsor.
- A `Poz` oszlop mértékegysége és az értékek pontos fizikai jelentése a munkafüzeten kívüli műszaki dokumentáció nélkül nincs önállóan igazolva; az értékeket változatlanul, a forrás szerinti jelöléssel rögzítettük.

## Tervezési következmény

A jelenlegi beszabályozás a későbbi körönkénti szabályozás tervezésének kiindulási állapota. A tervezés során nem szabad automatikusan megváltoztatni a `Poz` értékeket. Előbb azonosítani kell a szelepek és működtetők kompatibilitását, valamint meg kell tervezni, hogyan marad meg a hidraulikai beszabályozás a zónavezérlés mellett.

## Biztonsági korlát

Ez a dokumentum csak megfigyelési és tervezési célú rögzítés. A körök elzárása/nyitása, a `Poz` értékek módosítása, a hidraulikai beállítások megváltoztatása vagy a fűtést befolyásoló próba külön, konkrét felhasználói jóváhagyást igényel.


## Áramlásmérők 2026-10-28-i leolvasása

**Rögzítés időpontja:** 2026-10-28, Europe/Budapest.  
**Forrás:** a felhasználó által ugyanazon a napon küldött áramlásmérő-fényképek és azokhoz adott leolvasások.  
**Bizonyítottság:** felhasználó által leolvasott értékek; a fényképek vizuálisan támogatják az értelmezést, de ez nem kalibrált mérés. Az áramlásmérő skáláján a „L/min” jelölés látható.

| Kör | Leolvasott térfogatáram | Állapot / megjegyzés | Bizonyítottság |
|---:|---:|---|---|
| 1 | 3,55 L/min | A felhasználó leolvasása | Részben ellenőrzött |
| 2 | 3,20 L/min | A felhasználó leolvasása | Részben ellenőrzött |
| 3 | 2,68 L/min | Korábbi 3,4-es leolvasást a felhasználó korrigálta | Részben ellenőrzött |
| 4 | 2,72 L/min | Korábbi 2,5-ös leolvasást a felhasználó korrigálta | Részben ellenőrzött |
| 5 | 2,50 L/min | A felhasználó leolvasása | Részben ellenőrzött |
| 6 | 3,12 L/min | A felhasználó leolvasása | Részben ellenőrzött |
| 7 | 0 L/min | A felhasználó ellenőrizte; a kör le van zárva | Ellenőrzött felhasználói közlés alapján |
| 8 | 2,95 L/min | A felhasználó leolvasása | Részben ellenőrzött |

Az értékek a fényképek készítésekor fennálló állapotot rögzítik, nem garantáltan aktuálisak későbbi időpontban. A kör 7-es 0 L/min értéke a felhasználó közlése szerint a kör szándékos lezárásából ered. A fenti adatokat nem használjuk automatikusan új beszabályozási célértékként.

**Biztonság:** a leolvasás dokumentálása nem jelent engedélyt bármely kör nyitására/zárására vagy a térfogatáram módosítására. Minden ilyen beavatkozás külön, konkrét felhasználói jóváhagyást igényel.

## Körök, helyiségek, nyomvonalak és hőhatások – frissített értelmezés (2026-10-28)

### Felhasználó által kijelölt elsődleges zónák

| Kör | Elsődleges vezérlési hozzárendelés | Terület |
|---:|---|---:|
| 1 | Fürdő, WC, előszoba | 14,1 m² |
| 2 | Előszoba, konyha | 11,8 m² |
| 3 | Zoé szobája | 13,5 m² |
| 4 | Zsombi szobája | 13,5 m² |
| 5 | Konyha | 19,8 m² |
| 6 | Nappali | 19,5 m² |
| 7 | Háló | 11 m² |
| 8 | Dolgozó, gardrób | 11 m² |

A terület- és zónacímkék a felhasználó által megadott körkiosztásból származnak. A 4. kör a felhasználó pontosítása szerint a konyhát is fűti; ezért a 4. kör Zsombi szobáján túl a konyhához is hőleadási kapcsolatot kell rendelni. A konyha a felhasználó szerint a 4. és az 5. körből is kap fűtést. A 4. kör konyhai hőleadásának pontos térbeli kiterjedése és aránya a jelenleg elérhető információból nem számszerűsíthető.

### Csővezetési útvonalak

- A 2., 3. és 4. kör csöve a fürdőn (az 1-es kör helyiségcsoportján) keresztül halad.
- Az 5. és 6. kör közvetlenül a háztartási helyiségből érkezik.
- A 7. kör csöve a 8. kör felső helyiségén, a dolgozón keresztül halad.
- A körök teljes padlón belüli nyomvonala és a köztes csőszakaszok pontos hőleadása nincs teljes egészében felmérve.

### Nyitott légterek

A felhasználó által 2026-10-28-án megadott alaprajzi értelmezés:

1. A nappali és a konyha egy nagy, egybefüggő légtér.
2. A nappali–konyha tér és az előszoba részben ajtó nélküli, nyitott kapcsolatban áll.
3. A háló és a gardrób között nincs ajtó.
4. A dolgozó jellemzően nyitott a háló felé.
5. A fürdő és a háztartási helyiség között nincs ajtó.

Ezek alapján a helyiségek közötti hőmérsékleti hatás nem kizárólag a padlócsövek helyzetétől függ: a nyitott légterek miatt egy kör más helyiségek komfortjára is hatással lehet. A hatás mértéke jelenleg nincs műszeresen elkülönítve.

### Felhasználói tapasztalat a jelenlegi beszabályozásról

- A 7. kört a felhasználó lezárta, mert a háló–gardrób–dolgozó blokk túl meleg volt. A gardrób a háló felé nyitott; a dolgozó is jellemzően nyitott a háló felé.
- A 8. kör nem zárható le a jelenlegi komfortcél mellett, mert a felhasználó naponta dolgozik a dolgozóban, és az ablakot gyakran nyitja; ilyenkor a fűtés fontos a komforthoz.
- A 2. és 3. kör helyiségei a felhasználó tapasztalata szerint 4–5 °C-kal hűvösebbek voltak a többi helyiségnél, ezért ezeket korábban feljebb állította.
- A felhasználó a körök területét korábbi hőkamerás vizsgálat alapján határozta meg. A körökhöz összesen 114,2 m²-t rendelt; a 6,86 m²-es, körrel külön nem jelölt háztartási helyiséggel együtt 121,2 m² adódik, amely a felhasználó szerint megfelel a 121,36 m²-es hasznos alapterületnek. Ez a számtani egyezés a felhasználó korábbi felmérésének konzisztenciáját támogatja, de önmagában nem független geometriai vagy hőtechnikai validáció.

### Épületadatok és hőtechnikai értelmezés

- Belmagasság: 2,55 m.
- Könnyűszerkezetes ROTAREX acélvázas falazat; a felhasználó által idézett műszaki leírás szerint 8 cm kőzetgyapot a falvázban és 15 cm EPS külső hőszigetelés.
- Padló: 10 cm EPS100.
- Tető: 30 cm Rockwool Multirock kőzetgyapot.
- Nyílászárók: a megadott műszaki leírásban Uw ≤ 0,8 W/m²K.

**Forrásminősítés:** a fenti szerkezeti adatok a felhasználó által idézett építészeti műszaki leírásból származnak; helyszíni rétegrend-feltárás nem történt. A tényleges helyiségenkénti hőveszteség és a szükséges térfogatáram ezekből az adatokból önmagában nem számítható ki.

## Tervezési reláció: melyik kör hogyan hathat más helyiségekre?

| Kör | Közvetlen / elsődleges hatás | Lehetséges további hatás | Miért |
|---:|---|---|---|
| 1 | Fürdő, WC, előszoba | Háztartási helyiség | A fürdő és a háztartási helyiség között nincs ajtó; az előszoba más nyitott zónákkal is kapcsolatban van |
| 2 | Előszoba, konyha | Nappali | A konyha–nappali egybefüggő tér, az előszoba részben nyitott a térhez |
| 3 | Zoé szobája | Fürdőn átvezető csőszakasz hőleadása | A cső a fürdőn keresztül halad; a hatás mértéke nem ismert |
| 4 | Zsombi szobája | Konyha; fürdőn átvezető csőszakasz | A felhasználó szerint a konyhát is a 4. kör és az 5. kör fűti |
| 5 | Konyha | Nappali, részben előszoba | Közös vagy nyitott légtérkapcsolat |
| 6 | Nappali | Konyha, részben előszoba | Közös vagy nyitott légtérkapcsolat |
| 7 | Háló | Gardrób, dolgozó | Nyitott légkapcsolat; a kör jelenleg lezárt |
| 8 | Dolgozó, gardrób | Háló | Nyitott légkapcsolat; a dolgozó hőigényét a gyakori ablaknyitás is befolyásolja |

A táblázat tervezési hipotézis, nem számszerű hőátadási modell. A helyiségenkénti hőmérséklet-érzékelés és a későbbi, külön jóváhagyott mérési terv segíthet elkülöníteni a közvetlen körhatást, az átvezető csövek hatását és a nyitott légterek hatását. A körönkénti szabályozás tervezésénél minden körhöz elsődleges vezérlési zónát kell rendelni, miközben a másodlagos hőhatásokat is figyelembe kell venni.

## Verziókezelt alaprajzi bizonyítékok (2026-10-28, Europe/Budapest)

A felhasználó által a GitHubon elhelyezett négy tervfájl a `docs/evidence/` mappában található. Ezeket a körök és a helyiségek közötti kapcsolatok dokumentálására használjuk; nem tekintjük a színezett ábrákat méretezett csőfektetési tervnek.

- [PF-AL-00 – Eredeti építészeti alaprajz, É-01, 1:100 (PDF)](evidence/PF-AL-00-epiteszeti-alaprajz-eredeti-E-01.pdf) – eredeti tervforrás.
- [PF-AL-01 – Nyitott légtér: nappali és konyha (PNG)](evidence/PF-AL-01-nyitott-legterek-nappali-konyha.png) – a nappali–konyha egybefüggő terének és a körök területi jelölésének szemléltetése.
- [PF-AL-02 – Nyitott légterek és helyiségkapcsolatok (PNG)](evidence/PF-AL-02-nyitott-legterek-es-kapcsolatok.png) – háló–gardrób, nappali–előszoba, illetve fürdő–háztartási helyiség kapcsolat.
- [PF-AL-03 – Padlófűtési körök és helyiségek (PNG)](evidence/PF-AL-03-padlofutesi-korok-es-helyisegek.png) – a nyolc kör felhasználó által meghatározott helyiség- és terület-hozzárendelése.

### Az alaprajzokból és felhasználói pontosításokból rögzített relációk

| Kör | Elsődleges vezérlési zóna | További, figyelembe veendő kapcsolat | A kapcsolat alapja | Bizonyítottság |
|---:|---|---|---|---|
| 1 | Fürdő, WC, előszoba | Háztartási helyiség | A fürdő és a háztartási helyiség között nincs ajtó; a kör zónája az előszobát is tartalmazza | Zónakiosztás: felhasználó által meghatározott; nyitott kapcsolat: felhasználói közlés |
| 2 | Előszoba, konyha | Nappali | Az előszoba részben ajtó nélkül kapcsolódik a nappali–konyha térhez | Felhasználói közlés és alaprajz |
| 3 | Zoé szobája | Fürdőn átvezető csőszakasz; közvetett légtérhatás csak akkor, ha a tényleges ajtókapcsolat ezt lehetővé teszi | A cső a fürdőn keresztül halad; a teljes padlóbeli nyomvonal nem dokumentált | Útvonal: felhasználói közlés; hőhatás mértéke: ellenőrizetlen |
| 4 | Zsombi szobája | Konyha; fürdőn átvezető csőszakasz | A felhasználó szerint a konyhát a 4. és az 5. kör is fűti | Felhasználói közlés; a konyhai hőleadás aránya nem ismert |
| 5 | Konyha | Nappali, részben előszoba | Közös nappali–konyha tér, részben nyitott előszoba-kapcsolat | Zónakiosztás és légtérkapcsolat: felhasználói közlés |
| 6 | Nappali | Konyha, részben előszoba | Közös nappali–konyha tér, részben nyitott előszoba-kapcsolat | Zónakiosztás és légtérkapcsolat: felhasználói közlés |
| 7 | Háló | Gardrób és dolgozó felé fennálló nyitott légkapcsolat | A 7-es kör a felhasználó közlése szerint lezárt; a gardrób nyitott a hálóra, a dolgozó is jellemzően nyitott a háló felé; a cső a dolgozón keresztül halad | Nyitott kapcsolatok és lezárás: felhasználói közlés; az áramlásmérő 0 L/min értéke külön fényképes leolvasással alátámasztott |
| 8 | Dolgozó, gardrób | Háló | A dolgozó jellemzően nyitott a háló felé; gyakori ablaknyitás befolyásolja a dolgozó komfortigényét | Felhasználói közlés |

**Értelmezési korlát:** a fenti táblázat a vezérlési logika megtervezéséhez készült relációs modell, nem számszerű hőátadási vagy hidraulikai modell. A csövek köztes szakaszainak hőleadása, a körönkénti hőteljesítmény és a helyiségek közötti hőmérsékleti hatás jelenleg nincs elkülönítetten megmérve.

### Épületadatok a tervezési modellhez

A felhasználó 2026-10-28-án megadott építészeti műszaki leírása szerint:
- belmagasság: 2,55 m;
- könnyűszerkezetes, ROTAREX acélvázas fal;
- falvázban 8 cm kőzetgyapot és kívül 15 cm EPS;
- padlóban 10 cm EPS100;
- tetőben 30 cm Rockwool Multirock kőzetgyapot;
- nyílászárók megadott Uw értéke legfeljebb 0,8 W/m²K.

**Forrásminősítés:** korábbi/átvett építészeti műszaki leírás és felhasználói közlés; helyszíni rétegrend-feltárás nem történt. Ezek az adatok önmagukban nem elegendők a helyiségenkénti hőveszteség vagy a szükséges térfogatáram kiszámításához.

### Területi összegzés – felhasználói ellenőrzés alapján

A felhasználó a körök által lefedett területet korábbi hőkamerás vizsgálat alapján összesen 114,2 m²-re számolta. A külön körrel nem jelölt, 6,86 m²-es háztartási helyiséggel együtt 121,2 m² adódik, ami közel van a megadott 121,36 m² hasznos alapterülethez. Ez a számtani egyezés konzisztencia-ellenőrzés, nem független geometriai mérés.

**Fontos döntés:** a felhasználó nem kéri a jelenlegi beszabályozási állapot célértékként való megőrzését. A dokumentációban a kör-hozzárendelések és a tervrajzi kapcsolatok a későbbi szabályozási logika alapjai; a korábbi áramlás- és beállítási értékek nem tekinthetők javasolt célértékeknek. Bármely tényleges beállításmódosítás külön jóváhagyást igényel.
