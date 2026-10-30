# PF-01.05 – érzékelő-egyeztetés zárójegyzék

Ellenőrzés: 2026-10-30, Europe/Budapest. Forrás: Home Assistant MCP, ha_search és ha_get_entity, kizárólag olvasási lekérdezés; korábbi PF-01.05 Notion-adatok. Bizonyítottság: Ellenőrzött a HA-regiszterben való jelenlét; a fizikai felszereltség csak korábbi felhasználói közlés.

## Hőmérséklet és páratartalom

A nyolc beltéri és egy kerti Aqara hőmérő regisztrált, engedélyezett ZHA-entitás. A hét megvizsgált hőmérő számszerű állapotot adott. A Dolgozó és Háztartási hőmérő pillanatnyi állapotát a felhasználó kérésére nem dokumentáltuk. A kapcsolódó páratartalom-entitások és két termosztát páratartalom-entitása is megtalálható.

## Nyitásérzékelők

A `binary_sensor` tartományban az `aqara_door_window` azonosítórészre 18 találat volt: Dolgozó 1, Bejárat 1, Fürdő 1, Háztartási 1, Fürdőajtó 1, Háló bal/jobb 2, Konyha bal/jobb 2, Nappali bal/jobb 2, teraszajtó bal/jobb 2, Zoé bal/jobb 2, Zsombi bal/jobb 2, WC-ajtó 1. Az entitások a HA-regiszterben szerepelnek. A Háló bal és a Fürdőajtó entitásai nem tartalmazzák a `nyilik` névrészt; a korábbi szűk keresés emiatt nem találta meg őket.

## Mozgásérzékelők

A `binary_sensor` tartományban a `mi_motion` azonosítórészre 18 találat volt: Bejárat, Előszoba, Dolgozó, Fürdő, Háló, Konyha, Nappali, Zoé és Zsombi; mindegyikhez mozgás- és foglaltságjelző entitás tartozik. Ez kilenc név szerint megfeleltetett érzékelőhely, nem 18 külön fizikai érzékelő bizonyítéka.

## Egyéb kapcsolódó HA-adatok

A `climate` tartomány nyolc entitást tartalmazott: két termosztát, négy klíma és két törölközőszárító-szabályozó. Az időjárás-előrejelzés entitása `weather.forecast_otthon`. A szabályozási és automatizmuslogika nem része ennek az egyeztetésnek.

## Eltéréslista és lezárási megjegyzés

1. **WC-ajtó:** `binary_sensor.wc_ajto_aqara_door_window_wc` szerepel a HA-ban, miközben a felhasználó korábban jelezte, hogy a WC-ajtón nincs már felszerelt érzékelő. Státusz: Ellenőrzött HA-nyilvántartás + korábbi felhasználói közlés, fizikai megfeleltetés nyitott. Nem törlünk vagy nevezünk át semmit.
2. **Eltérő névkonvenció:** a Háló bal és Fürdőajtó entitása célzott kereséssel igazolt; nem hiányzó entitás.
3. **Helyiségnevek:** Zoé = Reni szoba, Háló = Bálint szoba; dokumentációs aliasok, HA-átnevezés nélkül.
4. **Előszoba:** nincs helyiségi hőmérő a felhasználó közlése szerint; nem kezeljük hiányzó HA-entitásként.
5. **Fizikai felszereltség és tartós működés:** MCP-regiszterből nem bizonyítható; a szabályozási tervezéskor szükség szerint külön vizsgálandó.

A PF-01.05 felmérési hatóköréhez szükséges releváns entitáscsoportok, források, bizonyítottság és ismert eltérések dokumentálva. A nyitott WC-ajtó leltárkülönbség nem igényel most fizikai beavatkozást. Home Assistant és fűtési konfiguráció nem változott.
