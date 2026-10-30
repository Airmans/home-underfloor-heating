# Kazán és kazánoldali fűtésvezérlés

**Rögzítés dátuma:** 2026-10-27, Europe/Budapest  
**Források:** a felhasználó által korábban megosztott négy kazánfotó, Tado-alkalmazás képernyőképei és írásos közlései.  
**Bizonyítottság:** a típustábla adatai a korábban áttekintett fényképek alapján ellenőrzöttek; a vezérlési út és a bemenet típusa még részben ellenőrzött vagy ellenőrizetlen.  
**Hatókör:** meglévő állapot dokumentálása; kazánpróba, bekötésvizsgálat vagy beavatkozás nem történt.

## Hőtermelő azonosítása

| Adat | Megállapítás | Bizonyítottság / forrás |
|---|---|---|
| Gyártó és modell | Bosch Tronic Heat 3500 H | **Ellenőrzött** – korábban megosztott négy kazánfotó, típustábla; 2026-10-27 |
| Névleges hőteljesítmény | 18 kW | **Ellenőrzött** – típustábla-fotó |
| Villamos teljesítmény | 18,1 kW | **Ellenőrzött** – típustábla-fotó |
| Tápellátás | 3N~ 230/400 V, 50 Hz | **Ellenőrzött** – típustábla-fotó |
| Maximális üzemi nyomás / hőmérséklet | 3 bar / 85 °C | **Ellenőrzött** – típustábla-fotó |
| Víztartalom | 5,9 l | **Ellenőrzött** – típustábla-fotó |
| Tömeg | 28 kg | **Ellenőrzött** – típustábla-fotó |
| Védettség | IP40 | **Ellenőrzött** – típustábla-fotó |
| Kijelzőn korábban látható „26” | Jelentése nincs azonosítva | **Ellenőrizetlen** – korábbi fotó |

A gyártói telepítési és kezelési dokumentációt a pontos típushoz kell társítani, és abból kell azonosítani a vezérlőkapcsokat, a bemenetek villamos jellemzőit és a kazán védelmi funkcióit. A típustábla önmagában nem igazolja a bekötés módját.

## Meglévő fűtési igény és vezérlés

- **Felhasználói pontosítás, 2026-10-27 13:23 Europe/Budapest:** a kazán közvetlen ON/OFF vezérlője a „Nappali & Konyha” Tado termosztát, amely két eres vezetékkel kapcsolódik a kazánhoz. A termosztát kazánoldali kimenetének villamos jellemzői és a tényleges kapcsok továbbra sincsenek ellenőrizve.
- **Kazán előremenő hőmérsékletének beállítása:** 32 °C — felhasználói közlés, rögzítve 2026-10-27 13:23 Europe/Budapest; **nem ellenőrzött élő beállítás**, és nem mért tényleges előremenő vízhőmérséklet.
- A fürdőszobai Tado termosztát adata a Tado felhőbe jut, és a felhasználó leírása szerint a felhőn keresztül a „Nappali & Konyha” termosztát vezérlése történik. Így a fürdőszobai hőigény a nappali termosztáton keresztül jut el a kazán ON/OFF bemenetéhez; a pontos Tado-konfigurációt és az adatút részleteit külön nem ellenőriztük.
- A felhasználó korábbi leírása szerint bármelyik termosztát hőigénye fűtési igényt eredményez. Ezt a most pontosított felhőn keresztüli jelúttal együtt kell értelmezni, nem két külön közvetlen kazánbekötésként.
- A Home Assistantban felhőalapú Tado-integráció működik. Ez önmagában nem bizonyítja, hogy a Home Assistant közvetlenül vezérli a kazán fűtési bemenetét.
- Nem igazolt, hogy a kazán ON/OFF vezérlőbemenete pontosan milyen villamos jelet vár, és hogy a nappali termosztát és a kazán között van-e további köztes elem. A felhasználó ON/OFF-os bekötésként írta le a kapcsolatot; ezt a fizikai bekötés vizsgálata nélkül felhasználói közlésként tartjuk nyilván.

## Kapcsolódó villamos védelmi adatok

A felhasználó korábban az alábbi, kazánhoz kapcsolódó villamos elemeket nevezte meg:
- Tracon TFVH4-80100 FI-relé;
- három Schneider Resi9 C32 kismegszakító.

Ezek a felhasználói közlésből átvett adatok; a tényleges bekötési topológia, a védelmi koordináció és a vezetékek méretezése itt nincs függetlenül ellenőrizve. A dokumentum nem villamos felülvizsgálati jegyzőkönyv.


## Gyártói kézikönyv szerinti követelmények

- **Forrás:** Bosch, *Tronic Heat 3500 – Szerelési és karbantartási kézikönyv*, dokumentumazonosító **6720871226**, kiadás **2023/06**. [Hivatalos magyar nyelvű PDF](https://bosch-hu.boschhc-documents.com/download/pdf/file/6720871226).
- **Ellenőrzés dátuma:** 2026-10-27, Europe/Budapest.
- **Bizonyítottság:** a kézikönyvben szereplő gyártói előírások **Ellenőrzöttek**; a meglévő telepítés megfelelősége ettől külön kérdés, **Ellenőrizetlen**.

### Vezérlési módok

A kézikönyv több külső vezérlési módot tárgyal, köztük szobatermosztátos és távoli vezérlési megoldásokat (5.2.3–5.2.9. szakasz, hozzávetőleg 23–26. PDF-oldal). A megfelelő bemenet és paraméterezés az alkalmazott módtól függ. A kézikönyv 7.3.1. szakasza olyan kéttermosztátos működést is leír, amelyben bármelyik termosztát bekapcsolhatja a kazánt, a kazán leállításához pedig mindkét termosztátnak kikapcsolt állapotban kell lennie.

**Fontos korlátozás:** ez a gyártó által dokumentált lehetőség összhangban lehet a felhasználó által leírt működéssel, de önmagában nem bizonyítja, hogy a jelenlegi Tado-rendszer pontosan így van bekötve. A bemeneti kapcsok, a köztes relé esetleges megléte, valamint a paraméterek tényleges értékei nem lettek ellenőrizve. A kézikönyvben szereplő PA00 és SE07 paraméterek szerepét az alkalmazott kapcsolási módhoz kötötten kell értelmezni; jelenlegi értékük ismeretlen.

### Minimális üzemi nyomás

A kézikönyv 6.1. szakasza legalább **0,6 bar** üzemi nyomást ír elő. Ez gyártói követelmény, nem a rendszer jelenlegi nyomásának mérése. A tényleges nyomást a meglévő fotókból nem tekintjük hitelesen megállapítottnak.

### Hatás a későbbi körönkénti szabályozás tervezésére

A későbbi tervezés során meg kell őrizni a kazán gyártó által előírt védelmi és üzemeltetési feltételeit. Különösen nem feltételezhető, hogy a padlófűtési körök lezárása a kazán számára megfelelő vízáramlás mellett is biztonságos; ezt a teljes hidraulikai kialakítás és a gyártói előírások alapján kell értékelni. Jelen felmérési lépésben nem történt beavatkozás, paraméter-lekérdezés, kazánpróba vagy nyomásmérés.

## Nyitott kérdések

1. A Bosch Tronic Heat 3500 H hivatalos telepítési dokumentációjában melyik bemenet és milyen villamos jellemzőkkel alkalmas külső fűtési igény fogadására?
2. A fürdőszobai termosztát Tado-felhőn át a „Nappali & Konyha” termosztátot vezérli a felhasználó leírása szerint; a pontos konfiguráció és az esetleges további köztes elem még nincs ellenőrizve.
3. Melyik kazánvédelmi és minimális áramlási követelményeket kell megőrizni, ha később a padlófűtési köröket külön szabályozzuk?
4. A kijelzőn korábban látható „26” milyen állapotot vagy értéket jelölt?

## Következő megfigyelési lépések

- A korábban megosztott kazánfotók és a gyártói kézikönyv összevetése.
- A gyártói dokumentáció releváns, vezérlőbemenetre és védelmekre vonatkozó részének rögzítése.
- A meglévő Tado-vezérlés képernyőképeinek és a korábbi kapcsolati információknak az eredeti forrásuk szerinti felhasználása.

Új adattábla-fotót nem kérünk be ismételten, mert az korábban már meg lett osztva és át lett tekintve.

## Biztonsági korlát

Nem bontunk burkolatot, nem végzünk feszültség alatti mérést, nem vizsgálunk vezetékeket, nem indítunk kazánpróbát és nem módosítunk beállítást. Bármely ilyen művelet külön, konkrét felhasználói jóváhagyást és szükség esetén szakképzett szakembert igényel.


## Felhasználó által közölt kazánbeállítások

**Rögzítés dátuma:** 2026-10-27, Europe/Budapest  
**Forrás:** felhasználói közlés a kazán üzemi paramétereiről és előremenő-beállításáról.  
**Bizonyítottság:** **Felhasználói közlés / részben ellenőrzött** — a közölt értékeket nem olvastuk le élő kazánkijelzőről vagy szervizmenüből ebben a felmérési lépésben; a paraméterek funkcióját és a megadott értékek helyességét a pontos modell dokumentációjával még össze kell vetni.

| Paraméter | Közölt érték | Megjegyzés |
|---|---:|---|
| PA00 | 01 | A felhasználó által megadott üzemi paraméter |
| PA01 | 03 | A felhasználó által megadott üzemi paraméter |
| PA02 | 06 | A felhasználó által megadott üzemi paraméter |
| PA03 | 02 | A felhasználó által megadott üzemi paraméter |
| PA09 | 20 | A felhasználó által megadott üzemi paraméter |
| Kazán előremenő-hőmérséklet beállítása | 32 °C | Beállított érték; nem igazolja a tényleges előremenő vízhőmérsékletet |

A paraméterek funkcióját és azt, hogy az adott vezérlési módhoz megfelelőek-e, csak a gyártói kézikönyv alapján szabad értelmezni. A PA00 aktuális értéke a felhasználó közlése szerint 01; a korábbi „ismeretlen” státusz erre az értékre már nem érvényes, de a helyszíni leolvasás és a paraméter jelentésének ellenőrzése továbbra is hiányzik. Az SE07 értékét a felhasználó nem közölte, ezért az továbbra is ismeretlen. Nem történt beállításmódosítás vagy élő rendszerpróba.


## SE paraméterek hozzáférhetősége — felhasználói pontosítás

**Rögzítés dátuma:** 2026-10-27, Europe/Budapest  
**Forrás:** felhasználói közlés.  
**Bizonyítottság:** **Felhasználói közlés; a szervizmenü értékei nem hozzáférhetők a felhasználó számára.**

A felhasználó tájékoztatása szerint az SE paraméterek alapértelmezettek, és azokhoz nem fér hozzá. Emiatt az SE07 egyedi aktuális értékét nem tekintjük leolvasott vagy ellenőrzött adatnak. Az alapértelmezett érték pontos számszerű értékét és funkcióját a gyártói dokumentáció vagy jogosult szerviz tudja megerősíteni. A felmérés nem próbálja megkerülni a hozzáférési korlátozást, és nem javasol jogosulatlan paramétermódosítást.


## Fizikai termosztátbekötés és kapcsolási rajz — 2026-10-30

**Ellenőrzés:** 2026-10-30, Europe/Budapest. **Forrás:** a most feltöltött kazán- és termosztátfotók, a felhasználó vezetékazonosítása és a megosztott Bosch kapcsolási rajz.

| Adat | Megállapítás | Bizonyítottság |
|---|---|---|
| Kazánoldali kapocspár | **B5–B6**; a felhasználó a világoskék–barna érpárt azonosította termosztátvezetékként | **Ellenőrzött** a fotók, kapocsjelölések és felhasználói azonosítás együttesével |
| Termosztátoldali bekötés | Tado fali alaplap: **barna → NO**, **világoskék → COM**; NC, parkoló- és digitális kapcsok a képen üresek | **Ellenőrzött**, 7690.jpg |
| Kapcsolási rajz | 21. ábra: Tronic Heat 3500 (15–24 kW), 3×400/230 V AC; PT = szobatermosztát, kapcsolóérintkező B5 és B6 között; látható rajzazonosító 0010010251-002 | **Ellenőrzött** a megosztott rajzkivágás tartalmára; a teljes kiadás és készülékrevízió egyezése külön nincs igazolva |
| Azonosított kapcsolási út | Tado NO–COM ↔ kazán B5–B6, relés ON/OFF igénykapcsolat | **Ellenőrzött** a hozzáférhető végpontok és a felhasználó kábelazonosítása alapján; nem folytonosságmérés vagy teljes rejtett kábelút-ellenőrzés |
| Bemenet villamos előírásai | A pontos termosztátköri feszültség, áram és megengedett külső illesztés nem szerepel egyértelműen a megosztott ábrán | **Ellenőrizetlen**; a rajz 24 V DC tápegységjelölése önmagában nem elegendő ezek megadásához |

A vezeték színéből nem következtetünk a kapocs villamos funkciójára. A relés bekötés nem jelent digitális buszos kazánvezérlést. A rejtett kábelút és esetleges köztes elem hiányát nem állítjuk függetlenül ellenőrzöttnek.

### Termosztátok és már rögzített működés

- **Nappali & Konyha:** Tado Smart Thermostat **RU02**, **DRU02-TA-14**; a hátlap típuskódja **Ellenőrzött** (7691.jpg). A V3+ megnevezés a korábbi felhasználói azonosításból származik.
- **Fürdőszoba / háztartási helyiség átjáró:** **Hager EK960, Typ RU01**, ZR0516 jelöléssel; a típustábla és a 3 AAA elem **Ellenőrzött** (7692.jpg). Nem történt eszközcsere: az eredeti fürdőszobai készülék Hager volt; a korábbi általános „fürdőszobai Tado” megnevezés ezt az eszközt jelentette.
- A Hager vezeték nélküli hőmérséklet-érzékelőként való használata a Tado-rendszerben, valamint mindkét készülék 3 AAA elemes táplálása a [PF-01.04 korábbi feljegyzéseiből](https://app.notion.com/p/4063e49c5f5f81cf9cc6fad61f53adf6) származik (2026-10-28 23:29–23:39, Europe/Budapest; **Korábbi forrásból átvett**). A Hager elemei a mostani fotón is látszanak; a Tado aktuális elemei ezen a hátlapképen nem láthatók.
- Mindkét helyiségnek saját időprogramja és célhőmérséklete van; bármelyik igénye kezdeményezhet fűtést. A kazánt közvetlenül a nappali Tado kapcsolja; a Hager igénye a Tado-rendszeren belül közvetetten jut el ehhez a vezérlőhöz. Ez már korábban megadott működési leírás (**Korábbi forrásból átvett**), nem újra bekérendő adat. A teljes rádiós/felhős jelút és az alkalmazás eszközszerep-konfigurációja nem lett élő teszttel ellenőrizve.
- A Hager és egy konkrét Tado V3/V3+ készülék teljes hardverazonossága nem bizonyított pusztán a hátlap és az alkalmazás alapján.

### A korábbi bejegyzések értelmezése és megmaradó kérdések

Ez a dátumozott kiegészítés pontosítja a korábbi „kapcsok ismeretlenek”, „fizikai bekötés nem látható”, illetve általános „fürdőszobai Tado” megfogalmazásokat. A régi állapotok forrásként megmaradnak, de nem aktuális hiányok: B5–B6, NO–COM, RU02 és Hager EK960/RU01 most azonosítottak. A bemenet teljes villamos specifikációja, a rejtett kábelút, a szivattyú beállításának értelmezése, a bypass/keverőkör teljes körű igazolása és a korábbi tervezési követelmények továbbra is elkülönített nyitott pontok.

A képek és adatok rögzítése nem változtat feladatstátuszt és nem jelent megvalósítási jóváhagyást. Nem történt az asszisztens által végzett működési próba, vezetékezés-, kazán-, termosztát- vagy Home Assistant-módosítás.


### Forrásjegyzék – 2026.10.30-i feltöltések

A dátum a megosztás és az ellenőrzés napja (Europe/Budapest); a készítési idő külön nem ellenőrzött. Az eredeti képek nem kerültek a GitHubra. A hátlapfotók hitelesítési kódjait és QR-kódjait nem másoljuk a műszaki dokumentációba.

| Forrás | Tartalom |
|---|---|
| [image(20261030-184017).png](https://chatgpt.com/library?file_id=libfile_88c2556c2f488191b450a186498a3598&account_id=personal) | Kazán belső áttekintés |
| [image(20261030-184019).png](https://chatgpt.com/library?file_id=libfile_b8fe2f619aa081919dcb15ef5c67baf8&account_id=personal) | Kazán alsó belső része |
| [image(20261030-184025).png](https://chatgpt.com/library?file_id=libfile_1361565658dc81919c316f0562436f6d&account_id=personal) | Vezérlőcsatlakozók |
| [image(20261030-184029).png](https://chatgpt.com/library?file_id=libfile_a014fd06cabc819196d811e44b19d8f1&account_id=personal) | Vezérlőcsatlakozók |
| [image(20261030-184032).png](https://chatgpt.com/library?file_id=libfile_3cd78c8f0b108191a854405bf6d5d24d&account_id=personal) | Vezérlőcsatlakozók |
| [image(20261030-184035).png](https://chatgpt.com/library?file_id=libfile_c5e0f450985c8191aa4e4a0a281f8ba6&account_id=personal) | Szivattyú előlap |
| [image(20261030-184043).png](https://chatgpt.com/library?file_id=libfile_90e34e7a8bbc8191ae32150ea17571f6&account_id=personal) | A oldali csatlakozó |
| [image(20261030-184205).png](https://chatgpt.com/library?file_id=libfile_adb570d45cec8191bf325a8d3e9d1b1c&account_id=personal) | Szivattyú forgókapcsoló közeli kép |
| [image(20261030-194138).png](https://chatgpt.com/library?file_id=libfile_03eae27bf59c8191af4c26507badb7b4&account_id=personal) | Szivattyú adattábla |
| [image(20261030-194153).png](https://chatgpt.com/library?file_id=libfile_1cf0c14235d4819196b6428d9710fc52&account_id=personal) | B kapocssor jelölései |
| [image(20261030-194211).png](https://chatgpt.com/library?file_id=libfile_d5fa4807bad881918b195d21acb976c5&account_id=personal) | B5–B6 közeli nézet |
| [image(20261030-194223).png](https://chatgpt.com/library?file_id=libfile_5b5045355df081919fa4a0c967b255c2&account_id=personal) | Termosztátkábel kazánoldalon |
| [image(20261030-194600).png](https://chatgpt.com/library?file_id=libfile_a1ae9685caf881918a95a2c74e7efdab&account_id=personal) | Bosch kapcsolási rajz, 21. ábra |
| [7692.jpg](https://chatgpt.com/library?file_id=libfile_173a85100e5c8191b32dcf27154cd457&account_id=personal) | Hager EK960 hátoldal |
| [7691.jpg](https://chatgpt.com/library?file_id=libfile_d5ac37b79f68819196c4a043b1409395&account_id=personal) | Tado RU02 hátoldal |
| [7690.jpg](https://chatgpt.com/library?file_id=libfile_2fd66ac668748191bc4556dd93a0b406&account_id=personal) | Tado fali alaplap és NO–COM bekötés |
