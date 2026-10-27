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
