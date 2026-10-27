# Padlófűtési körök és jelenlegi beszabályozás

**Rögzítés dátuma:** 2026-10-27, Europe/Budapest  
**Állapot:** a körkiosztás és a beállítások a felhasználó által megosztott Excel és alaprajz alapján dokumentálva.  
**Bizonyítottság:** a táblázatban látható értékek forrásból átvéve; a jelenlegi beállításokat a felhasználó 2026-10-27-én kifejezetten megerősítette.

## Források

- Elsődleges forrás: felhasználó által megosztott `Padlófűtés beállítás.xlsx` munkafüzet, benne a körkiosztással, méretekkel, korrekciós tényezőkkel és alaprajzzal.
- A forrásmunkafüzet tervezett, verziókezelt helye: [`evidence/padlofutes-beallitas-20261027.xlsx`](../evidence/padlofutes-beallitas-20261027.xlsx). A fájlt a GitHub-repozitóriumba még fel kell tölteni.
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
- **Ellenőrzött felhasználói megerősítés alapján:** a `Poz` értékek a jelenlegi tényleges beállítások.
- **Korábbi mérési forrásból átvett:** a hőkamerás körazonosítás és az alaprajzi zónakiosztás; a korábbi hőkamerás mérési jegyzőkönyv külön nincs csatolva ebben a dokumentumban.
- **Felhasználói tapasztalat:** a szobák nagyjából azonos hőmérsékletűek a jelenlegi beszabályozással; ehhez itt nincs csatolt, egyidejű hőmérséklet-adatsor.
- A `Poz` oszlop mértékegysége és az értékek pontos fizikai jelentése a munkafüzeten kívüli műszaki dokumentáció nélkül nincs önállóan igazolva; az értékeket változatlanul, a forrás szerinti jelöléssel rögzítettük.

## Tervezési következmény

A jelenlegi beszabályozás a későbbi körönkénti szabályozás tervezésének kiindulási állapota. A tervezés során nem szabad automatikusan megváltoztatni a `Poz` értékeket. Előbb azonosítani kell a szelepek és működtetők kompatibilitását, valamint meg kell tervezni, hogyan marad meg a hidraulikai beszabályozás a zónavezérlés mellett.

## Biztonsági korlát

Ez a dokumentum csak megfigyelési és tervezési célú rögzítés. A körök elzárása/nyitása, a `Poz` értékek módosítása, a hidraulikai beállítások megváltoztatása vagy a fűtést befolyásoló próba külön, konkrét felhasználói jóváhagyást igényel.
