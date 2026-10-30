# Padlófűtés – meglévő hidraulikai rendszer és körök

**Dokumentumállapot:** folyamatban lévő helyszíni felmérés.  
**Utolsó frissítés:** 2026-10-30, Europe/Budapest.  
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

## Kapcsolódó dokumentum – körök, helyiségek és alaprajzi bizonyítékok

A körök helyiségekhez rendelése, a nyitott légterek, a felhasználó által közölt csővezetési útvonalak és a lehetséges hőhatás-relációk a [Padlófűtési körök és beszabályozás](padlofutesi-korok-es-beszabalyozas.md) dokumentumban szerepelnek.

A verziókezelt tervrajzok:
- [PF-AL-00 – Eredeti építészeti alaprajz, É-01, 1:100 (PDF)](evidence/PF-AL-00-epiteszeti-alaprajz-eredeti-E-01.pdf)
- [PF-AL-01 – Nyitott légtér: nappali és konyha (PNG)](evidence/PF-AL-01-nyitott-legterek-nappali-konyha.png)
- [PF-AL-02 – Nyitott légterek és helyiségkapcsolatok (PNG)](evidence/PF-AL-02-nyitott-legterek-es-kapcsolatok.png)
- [PF-AL-03 – Padlófűtési körök és helyiségek (PNG)](evidence/PF-AL-03-padlofutesi-korok-es-helyisegek.png)

A felhasználó 2026-10-28-i GitHub-képernyőképe a négy fájl jelenlétét és a fájlneveket alátámasztja. A körökhöz rendelt helyiségek és területek a felhasználó korábbi hőkamerás azonosításából és az általa megadott alaprajzi értelmezésből származnak; a színezett ábrák nem méretezett csőfektetési tervek.


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


## Csővezetési nyomvonalak és helyiségek közötti hőhatások (2026-10-28, Europe/Budapest)

Forrás: felhasználói közlés az osztó-gyűjtő és a helyiségek elrendezéséről, valamint a megosztott áttekintő fénykép és alaprajz. A nyomvonalak a háztartási helyiségből induló csövek megadott útját rögzítik; a teljes csőhossz és a padlón belüli pontos fektetési útvonal továbbra sem ismert.

| Kör | Felhasználó által közölt nyomvonal |
|---:|---|
| 1 | A fürdő/WC/előszoba fűtési zónája; a háztartási helyiségtől induló pontos átvezetés még nincs részletezve |
| 2 | A fürdőn (az 1-es kör helyiségcsoportján) keresztül vezet |
| 3 | A fürdőn (az 1-es kör helyiségcsoportján) keresztül vezet |
| 4 | A fürdőn (az 1-es kör helyiségcsoportján) keresztül vezet |
| 5 | Közvetlenül a háztartási helyiségből érkezik |
| 6 | Közvetlenül a háztartási helyiségből érkezik |
| 7 | A 8-as kör felső helyiségén, a dolgozón keresztül vezet |
| 8 | A dolgozó és gardrób fűtési köre; a 7-es kör dolgozón keresztüli nyomvonala mellett a teljes saját nyomvonal nincs külön feltérképezve |

A helyiségen keresztül vezetett csőszakasz hőt adhat le az átvezetett helyiségnek akkor is, ha a kör a helyiségen csak áthalad. Ennek mértéke a cső szigetelésétől, a fektetés módjától, a csőhossztól és a kör üzemi állapotától függ; ezekre jelenleg nincs elegendő adat, ezért a hatás nagysága ellenőrizetlen.

## Helyiségkapcsolatok és 7. kör lezárása (felhasználói közlés, 2026-10-28)

- A háló (7. kör) és a gardrób (a 8. kör része) között jellemzően nyitott kapcsolat van.
- A dolgozó, amely szintén a 8. körhöz tartozik, jellemzően nyitott a háló felé.
- A felhasználó tapasztalata szerint a háló–gardrób–dolgozó blokk túl meleg volt, ezért lezárta a 7. kört.
- A dolgozóban napközben rendszeres a tartózkodás, és az ablak gyakori nyitása miatt a 8. kör működése fontos a komforthoz.
- A 2. és 3. kör helyiségei a felhasználó tapasztalata szerint a többihez képest 4–5 °C-kal hűvösebbek voltak; ezért e körök térfogatáramát korábban növelte.

Ezek felhasználói tapasztalatok, nem egyidejű, naplózott helyiséghőmérséklet-mérések. A tervezésben a zónák közötti légkapcsolatot és a dolgozó változó szellőztetési hőterhelését figyelembe kell venni. A 7. kör automatikus újranyitása vagy bármely hidraulikai beállítás módosítása nem része ennek a dokumentálásnak, és külön jóváhagyás nélkül nem végezhető.

## Épület szerkezeti adatai és alaprajzi forrás (2026-10-28)

A felhasználó feltöltötte az É-01 alaprajz.pdf fájlt (1 oldal; földszinti alaprajz, m=1:100, 2022. január). A rajz helyiséglistája az eredeti építészeti terv szerinti neveket és alapterületeket tartalmazza; a fűtési körökhöz rendelt területek ettől eltérhetnek, mert a körök több helyiséget is lefednek, illetve a felhasználó külön fűtési zónatérképet adott.

A felhasználó által megadott építészeti műszaki leírás szerint:
- könnyűszerkezetes, ROTAREX galvanizált acélvázas fal;
- a falvázban 8 cm kőzetgyapot, kívül 15 cm EPS hőszigetelés;
- a padlóban 10 cm EPS100;
- a tetőben 30 cm Rockwool Multirock kőzetgyapot;
- a homlokzati nyílászárókra Uw ≤ 0,8 W/m²K szerepel a leírásban;
- megadott belmagasság: 2,55 m.

Bizonyítottság: az alaprajz mint feltöltött forrás ellenőrzött; a rétegrendek és belmagasság a felhasználó által idézett műszaki leírásból származnak, helyszíni rétegrend-feltárás nem történt. A helyiségek tényleges hővesztesége és a szükséges körönkénti térfogatáram ezekből az adatokból önmagában nem számítható ki.


## Körönkénti leolvasások és helyiségek közötti kapcsolatok – 2026-10-28

A részletes, körönkénti táblázatot, a felhasználó által leolvasott áramlásértékeket, a csővezetési nyomvonalakat, a nyitott légtereket és a tervezési hőhatás-relációt a [Padlófűtési körök és jelenlegi beszabályozás](padlofutesi-korok-es-beszabalyozas.md) dokumentum tartalmazza.

A 2026-10-28-i felhasználói leolvasások:
- 1. kör: 3,55 L/min
- 2. kör: 3,20 L/min
- 3. kör: 2,68 L/min
- 4. kör: 2,72 L/min
- 5. kör: 2,50 L/min
- 6. kör: 3,12 L/min
- 7. kör: 0 L/min – a felhasználó közlése szerint lezárt kör
- 8. kör: 2,95 L/min

A leolvasások fényképek és felhasználói értelmezés alapján részben ellenőrzöttek; nem kalibrált mérések, és nem tekintendők automatikus beszabályozási célértéknek.

A felhasználó által jelzett nyitott légterek:
- nappali–konyha egybefüggő tér, részben nyitott kapcsolattal az előszoba felé;
- háló–gardrób ajtó nélküli kapcsolat, a dolgozó jellemzően nyitott a háló felé;
- fürdő–háztartási helyiség ajtó nélküli kapcsolat.

A felhasználó szerint a 2. és 3. kör helyiségei korábban 4–5 °C-kal hűvösebbek voltak a többi helyiségnél; a 7. kört a háló–gardrób–dolgozó blokk túlmelegedése miatt zárta le. A 4. és 5. kör a felhasználó szerint egyaránt fűti a konyhát. Ezek felhasználói tapasztalatok és közlések, nem egyidejű, naplózott helyiséghőmérséklet-mérések.

**Forrás és ellenőrzés dátuma:** felhasználói fényképek, alaprajzok és leírás, 2026-10-28, Europe/Budapest. A négy tervfájl GitHubon való jelenlétét a felhasználó 2026-10-28-i képernyőképe alátámasztja.


## Fotókkal kiegészített szivattyú- és hidraulikai leltár — 2026-10-30

**Ellenőrzés:** 2026-10-30, Europe/Budapest. **Forrás:** a felhasználó most megosztott kazánbelső-, szivattyúelőlap- és adattábla-fotói; az eredeti forrásjegyzék a [kazánvezérlési dokumentumban](kazan-es-kazanoldali-vezerles.md#forrásjegyzék--20261030-i-feltöltések) található.

| Adat | Megállapítás | Bizonyítottság |
|---|---|---|
| Beépített keringető típusa | Taco Italia Srl / Taco Comfort Solutions **ES2 C 15-60/130**; ES2 INVERTER TECH előlap | **Ellenőrzött**, adattábla és előlap |
| Tápellátás | 230 V, 50 Hz | **Ellenőrzött**, adattábla |
| Felvett teljesítmény P1 | minimum 3 W, maximum 42 W | **Ellenőrzött**, adattábla; nem pillanatnyi fogyasztásmérés |
| Áramfelvétel | minimum 0,03 A, maximum 0,33 A | **Ellenőrzött**, adattábla |
| Jelölések | IP44; TF95; 0,6 MPa; EEI ≤ 0,21 – Part 2; THI003 | **Ellenőrzött**, adattábla; a 0,6 MPa nem a kazán engedélyezett nyomásának adata |
| Forgókapcsoló helyzete | A fehér nyíl a C tartomány I-es jelölése közelében, a P tartomány 2-es jelölése melletti határnál látható | **Részben ellenőrzött**; a pontos üzemmód és beállítás a megfelelő gyártói útmutatóval még összevetendő |
| Bypass | A korábbi PF-01.02 feljegyzés szerint nincs bypass. Az új fotók bemutatott részein külön bypasság nem azonosítható egyértelműen; ez nem igazolja a teljes rendszerben való hiányát | Korábbi állítás: **Korábbi forrásból átvett**; vizuális megerősítés: **Részben ellenőrzött** |
| Keverőkör | A bemutatott kazánbelsőben külön keverőszelep nem azonosítható; a kazánon kívüli teljes rendszer kialakítása ebből nem bizonyítható | **Részben ellenőrzött** |

A pontos szivattyútípushoz és a kazánoldali termosztátbekötéshez a szükséges képek megérkeztek; ezeket nem kell ismételten bekérni. A szivattyú beállításának értelmezése, a bypass/keverőkör teljes rendszerre vonatkozó igazolása és a korábban rögzített működtető-kompatibilitási kérdés nyitott marad. Az osztó pontos altípusát a korábbi döntésnek megfelelően nem emeljük vissza önálló lezárási feltétellé.

A fotókon működő kijelző és panelvilágítás látható; a fotók nem bizonyítják a feszültségmentességet. Az asszisztens csak a megosztott bizonyítékokat értékelte, nem végzett és nem kezdeményezett élő próbát, szerelést vagy beállításmódosítást.


## Bosch-kézikönyv: szivattyúüzemmódok és fotóegyeztetés — 2026-10-30

**Forrás:** [feltöltött Bosch-kézikönyvoldal](https://chatgpt.com/library?file_id=libfile_acc9e18402488191b66e60c38a902982&account_id=personal), nyomtatott 40. oldal; Tronic Heat 3500, 6720871226 (2023/06), 9.1 szakasz, 36–38. ábra, 14–15. táblázat. Összevetett helyszíni kép: [szivattyú forgókapcsolója](https://chatgpt.com/library?file_id=libfile_adb570d45cec8191bf325a8d3e9d1b1c&account_id=personal). **Ellenőrzés:** 2026-10-30, Europe/Budapest.

| Jelölés | Gyártói jelentés | Bizonyítottság |
|---|---|---|
| P1, P2 | Változó nyomáskülönbség-görbék, Δp-v | **Ellenőrzött**, 14–15. táblázat |
| CI, CII | Állandó nyomáskülönbség-görbék, Δp-c | **Ellenőrzött**, 14–15. táblázat |
| min…max | Meghatározott sebességű üzemmód | **Ellenőrzött**, 14. táblázat |
| LED zöld / narancssárga / kék | P / C / min…max üzemmód | **Ellenőrzött**, 15. táblázat |
| LED fehéren villog | Levegő jelenlétének automatikus felismerése | **Ellenőrzött**, 15. táblázat |
| LED piros | Rendeltetésszerű üzemet akadályozó zavar; például blokkolt rotor, elégtelen tápfeszültség, elektromos zavar | **Ellenőrzött**, 15. táblázat |

**Helyszíni állás:** a korábbi közeli fotó fehér nyila a **CI jelölés környezetébe mutat**. A gyártói ábrával összevetve ez **CI, állandó nyomáskülönbségű beállításnak látszik** (**Részben ellenőrzött**, fotóleolvasás). A korábbi „C/P határ közelében” leírás helyett ez a pontosabb értelmezés alkalmazandó. A jelölések jelentése immár tisztázott; az aktuális üzemmód LED-színnel vagy helyszíni leolvasással nem lett külön megerősítve. A fotón a LED színe nem olvasható megbízhatóan; új működési tesztet nem végeztünk.

A 36. ábra szivattyú-jelleggörbét mutat a 4–24 kW kazánokhoz; a 38. ábra a 15–24 kW kazán hidraulikai ellenállását adja meg, ezért a 18 kW-os kazánhoz ez utóbbi a releváns ellenállásgörbe. Ezek gyártói görbék, nem helyszíni munkapontmérések. A diagramokból önmagukban nem következik a tényleges térfogatáram, a CI beállítás megfelelősége vagy a lezárt körök melletti biztonságos üzem.

A gyártói figyelmeztetés szerint a helytelen szivattyúbeállítás a hőcserélő túlmelegedését okozhatja. Beállításmódosítás nem történt és ebből a dokumentálásból nem következik ilyen jóváhagyás. A bypass/keverőkör teljes rendszerre vonatkozó bizonyítottsága és a működtető-kompatibilitás korábbi nyitott pontjai változatlanok. PF-01.02 státuszváltoztatás nem történt.


## Helyszíni megerősítés — CI kapcsolóállás, 2026-10-30

**Forrás:** a felhasználó közvetlen helyszíni megerősítése: „CI álláson van a szivattyú”. **Ellenőrzés/rögzítés:** 2026-10-30, Europe/Budapest.

A beépített Taco ES2 C 15-60/130 szivattyú forgókapcsolója **CI állásban van**. A kapcsolóállás **Ellenőrzött — felhasználói helyszíni megerősítés és a korábbi fotó együttesével**, nem az asszisztens független helyszíni vizsgálatával. A korábbi, pusztán fotóleolvasásból eredő bizonytalanság erre a kapcsolóállásra megszűnt.

A Bosch 6720871226 (2023/06) kézikönyv 40. oldala, 14. táblázata alapján a CI az **állandó nyomáskülönbségű (Δp-c) I-es jelleggörbe**; a jelölés jelentése **Ellenőrzött** gyártói forrásból. Ez nem igazolja önmagában a tényleges térfogatáramot, munkapontot, a beállítás megfelelőségét vagy a körök lezárása melletti üzembiztonságot. LED-szín külön ellenőrzése nem szükséges a már megerősített kapcsolóállás azonosításához.

Nem történt általunk kezdeményezett beállításmódosítás vagy működési próba. Ez a bejegyzés a bizonyítottságot pontosítja; a PF-01.02 feladat státuszát nem változtatja meg.


## Home Assistant előzmények – CI kiinduló értékelése, 2026-10-30

**Forrás és elérés:** Home Assistant MCP, recorder history, közvetlen olvasási lekérdezés. **Időablak:** 2026-10-28 23:08:49 – 2026-10-30 23:08:49, Europe/Budapest (UTC: 2026-10-28T22:08:48.997750Z – 2026-10-30T22:08:48.997750Z). **Ellenőrzés:** 2026-10-30, Europe/Budapest.

Lekért entitások:
- sensor.gepeszet_padlofutes_homero_padlofutes_eloremeno_homerseklet – 1955 rekord;
- sensor.gepeszet_padlofutes_homero_padlofutes_visszatero_homerseklet – 772 rekord;
- sensor.nappali_termosztat_futes – 42 rekord;
- sensor.haztartasi_termosztat_futes – 18 rekord;
- climate.nappali_termosztat – 116 rekord, attribútumokkal;
- climate.haztartasi_termosztat – 112 rekord, attribútumokkal.

Mindegyik lekérdezés teljes: has_more=false; az előremenő második lapja is lekérve, azonos rögzített időablakkal. A hőmérséklet- és százalékszenzorok minimal_response=true, significant_changes_only alapértelmezett; a climate-adatok minimal_response=false, significant_changes_only=false. A hőmérsékletsorokban nincs unknown/unavailable; a két Tado-hőigénysorban 3-3 rövid unknown átmenet volt. A nyers rekorddarabszám nem szabályos mintavételi gyakoriság.

### Módszer

ΔT = előremenő − visszatérő. Egyperces közös időrácson az utolsó ismert recorder-állapot továbbvitelével párosítottuk a sorokat; az eredmények így közelítő, időarányos leíró értékek. Hőigényesnek azt a mintát tekintettük, amelynél valamelyik elérhető Tado Fűtés százalékszenzor >0. Ez nem a kazán reléállapota és nem bizonyít folyamatos fűtőteljesítményt. Az unknown állapotokat nem értelmezzük igazolt nulla hőigényként; a kiemelt délutáni szakaszokban nem volt ilyen átmenet.

### Megfigyelések

| Időszak / mennyiség | Eredmény | Bizonyítottság |
|---|---|---|
| Teljes 48 óra előremenő | 22,3–30,2 °C | **Ellenőrzött**, recorder-adatok |
| Teljes 48 óra visszatérő | 20,5–28,6 °C | **Ellenőrzött**, recorder-adatok |
| Október 29., kb. 14:47–17:53, Tado-hőigényes szakasz | ΔT medián kb. 2,7 °C; előremenő medián kb. 28,6 °C | **Részben ellenőrzött**, párosított adatokból számítva |
| Október 30., kb. 14:34–18:15, Tado-hőigényes szakasz | ΔT medián kb. 2,8 °C; előremenő medián kb. 29,2 °C | **Részben ellenőrzött**, párosított adatokból számítva |
| Tado-hőigény >0 és előremenő ≥28 °C minták, október 29–30. | Mindkét napon ΔT medián kb. 3,1 °C; a két napi 10–90. percentilis együtt kb. 2,0–3,7 °C tartományt fed le | **Részben ellenőrzött**, elemzési szűrés, nem előírt céltartomány |
| Teljes időablak párosított ΔT | kb. −0,1…3,9 °C; a fűtés nélküli és átmeneti időszakokat is tartalmazza | **Részben ellenőrzött**, számított; a kis negatív eltérés nem önmagában áramlási hiba |

A kiolvasáskor (hőmérők utolsó jelentése kb. 23:04) 24,2 °C előremenő, 22,8 °C visszatérő volt. A Tado utolsó, 22:44 körüli frissítése mindkét helyiségnél idle és 0% hőigény állapotot jelzett; a nappali 23,9 °C / 23 °C célértéket, a fürdő 24,5 °C / 19 °C célértéket mutatott. Eltérő frissítési idejű pillanatfelvételek; nem egyidejű közvetlen mérés.

### Értelmezés és korlát

**Előzetes következtetés – Részben ellenőrzött:** a vizsgált adatok alapján nincs elegendő indok pusztán szivattyúelégtelenségre hivatkozva CII-re váltani. A CI optimális voltát, a kazánvédelem megfelelőségét és a körönkénti elegendő térfogatáramot a két csőhőmérséklet nem bizonyítja. Az adatokból nem azonosítható biztosan a kazán tényleges ki-be kapcsolási gyakorisága sem.

A szivattyú CI állását a felhasználó a vizsgálat előtt megerősítette, de nincs olyan automatikus napló, amely bizonyítaná, hogy a teljes 48 órában változatlanul CI álláson működött. A korábbi 20,72 l/min összesített leolvasás nem egyidejű ezzel a méréssel, ezért ebből nem számítottunk igazolt hőteljesítményt. Az érzékelők csőre rögzítése, eltérő hőkontaktusa és késése korlátozza a ΔT értelmezését. A rövid, ismétlődő hőmérsékletváltozások okát nem tulajdonítjuk bizonyíték nélkül a szivattyúnak.

További értékeléshez releváns a tényleges kazán-/szivattyúállapot vagy villamos teljesítmény, egyidejű körátfolyások és helyiségenkénti komfort. A jelenlegi elemzéshez nem kérünk újra korábban már megosztott fotókat, és nem végzünk körzárást vagy beállításpróbát. Élő rendszerbe írás, automatizmus- vagy konfigurációmódosítás nem történt. A feladat státusza nem változott.


## PF-01.02 zárási feltételeinek pontosítása — 2026-10-30

**Forrás:** a felhasználó jelen beszélgetésbeli pontosítása: bypass és külön keverőkör „nem található”; a szelep–működtető illesztést már megbeszéltük. Korábbi forrás: PF-01.02, 2026-10-28, FERRO SN-RZP adatlap és M30×1,5 termoelektromos fej csatlakoztatási lehetősége. **Rögzítés:** 2026-10-30, Europe/Budapest.

- **Bypass és külön keverőkör:** a rendelkezésre álló felmérésben nem találtunk/azonosítottunk ilyen külön elemet; a bypass hiányát a felhasználó korábban is közölte. **Bizonyítottság: Részben ellenőrzött**, felhasználói közlés és hozzáférhető fotók. Ez a megfigyelés a PF-01.02 leltárának eredménye; nem keletkeztetünk új, korlátlan „teljes rendszer végleges igazolása” feltételt a felmérés lezárásához. Nem állítunk rejtett elemekre kiterjedő független vizsgálatot.
- **Szelep–működtető csatlakozás:** a már megadott FERRO-adatlap szerinti **M30×1,5 termoelektromos fej csatlakoztatási lehetősége** rendelkezésre álló tervezési bemenet; ezt nem kérjük újra és nem tesszük ismét önálló PF-01.02-zárási feltétellé. **Bizonyítottság:** a termékcsalád adatára Ellenőrzött gyártói forrás; a beépített darabhoz rendelés a korábbi dokumentáció szerinti Részben ellenőrzött. A jelen pontosítás nem minősít minden M30×1,5 működtetőt automatikusan teljes körűen kompatibilisnek.
- A konkrét működtető kiválasztása és adatlapjának illesztése a meglévő adatokhoz a PF-02.01 rendes tervezési feladata; ez nem az eddigi felmérés megismétlése.
- A szivattyú CI beállításának optimalizálása és a jövőbeni zónazárások melletti minimumáramlás biztosítása a későbbi tervezés tárgya, nem a jelen komponensleltár zárási akadálya.

**Zárási értékelés:** a PF-01.02 a hozzáférhető elemek leltározásának és a bizonyítottság rögzítésének szintjén lezárásra kész. A korábbi asszisztensi válaszban felsorolt bypass/keverőkör „végleges igazolását” és a már megtárgyalt csatlakozási kérdés újranyitását nem kezeljük további kötelező felmérési lépésként. Ez a bejegyzés önmagában nem változtat státuszt, és nem engedélyez élő rendszerbeavatkozást.
