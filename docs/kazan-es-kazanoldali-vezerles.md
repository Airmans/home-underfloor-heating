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

- A felhasználó közlése szerint a fűtési igény a két Tado V3 termosztát közül bármelyik igénye esetén megjelenik.
- A „Nappali & Konyha” termosztát két eres vezetékkel kapcsolódik a kazánhoz; a felhasználó ezt nevezte meg egyetlen közvetlen vezetékes termosztát–kazán kapcsolatként.
- A másik, fürdőszobai termosztát kazán felé vezető jelútja nem tisztázott.
- A vezérlés Tado V3 rendszerhez kötött; a Home Assistantban felhőalapú Tado-integráció működik. Ez az integráció önmagában nem bizonyítja, hogy a Home Assistant közvetlenül vezérli a kazán fűtési bemenetét.
- Nem igazolt, hogy a kazán vezérlőbemenete potenciálmentes kontaktust, buszos vezérlést vagy más jelet vár-e, illetve hogy van-e köztes relé vagy vezérlő.

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
2. A két Tado termosztát igénye pontosan hogyan jut el a kazánhoz; van-e köztes relé vagy más vezérlő?
3. Melyik kazánvédelmi és minimális áramlási követelményeket kell megőrizni, ha később a padlófűtési köröket külön szabályozzuk?
4. A kijelzőn korábban látható „26” milyen állapotot vagy értéket jelölt?

## Következő megfigyelési lépések

- A korábban megosztott kazánfotók és a gyártói kézikönyv összevetése.
- A gyártói dokumentáció releváns, vezérlőbemenetre és védelmekre vonatkozó részének rögzítése.
- A meglévő Tado-vezérlés képernyőképeinek és a korábbi kapcsolati információknak az eredeti forrásuk szerinti felhasználása.

Új adattábla-fotót nem kérünk be ismételten, mert az korábban már meg lett osztva és át lett tekintve.

## Biztonsági korlát

Nem bontunk burkolatot, nem végzünk feszültség alatti mérést, nem vizsgálunk vezetékeket, nem indítunk kazánpróbát és nem módosítunk beállítást. Bármely ilyen művelet külön, konkrét felhasználói jóváhagyást és szükség esetén szakképzett szakembert igényel.
