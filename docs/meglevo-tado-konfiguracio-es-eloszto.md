# Meglévő Tado-konfiguráció és villamos elosztó – kezdeti dokumentálás

**Rögzítés dátuma:** 2026-10-27, Europe/Budapest  
**Forrás:** a felhasználó által 2026-10-27-én megosztott Tado-app képernyőképek, az elektromos elosztóról megosztott fénykép, valamint a felhasználó írásos közlései.  
**Hatókör:** kizárólag dokumentálás és megfigyelés. Kazánpróba, vezetékezési vizsgálat, fűtési vagy hidraulikai módosítás, illetve Home Assistant-konfiguráció módosítása nem történt.

## Bizonyítottsági szintek

- **Részben ellenőrzött:** a képernyőképen vagy fényképen látható, illetve a felhasználó közlésével alátámasztott, de a helyszíni működés vagy a teljes műszaki összefüggés külön nem igazolt adat.
- **Ellenőrizetlen:** azonosításra vagy további bizonyítékra váró adat.

## 1. Tado-eszközök és elhelyezés

- Két Tado Smart Thermostat eszköz van használatban.
- **Nappali & Konyha:** modell-/eszközazonosítóként megjelenő karakterlánc: `RU2734702592`; firmware: `215.2`; a felhasználó megerősítése szerint V3+ változat. Elhelyezés: az előszoba és a nappali-konyha közötti átjáró.
- **Fürdőszoba:** modell-/eszközazonosítóként megjelenő karakterlánc: `RU1602FT01050584057344`; firmware: `54.20`. A V3 vagy V3+ generáció **Ellenőrizetlen**; a rövid, készülékcímkén feltüntetett modellkód ellenőrzése szükséges.
- Mindkét eszköz képernyőképen látható állapota csatlakoztatott, az akkumulátor állapota „Good”, a Dazzle Mode be van kapcsolva.
- **Tado Internet Bridge:** firmware `92.1`, a képernyőkép szerint csatlakoztatott.
- **Home Assistant:** a felhasználó közlése szerint a Tado-integráció felhőalapú. Az entitások és automatizmusok aktuális konfigurációját ebben a dokumentálási lépésben nem vizsgáltuk.
- **Auto-Assist:** a képernyőkép szerint aktív; megjelenített megújítási dátum: 2026-11-26.

**Bizonyítottság:** a képernyőképen látható alkalmazásadatok **Részben ellenőrzöttek**; az elhelyezés és a bekötés a felhasználó közlésén alapul, ezért **Részben ellenőrzött**.

## 2. A felhasználó által leírt vezérlési logika

A felhasználó közlése szerint a két termosztátnak külön hőmérséklet-időprogramja van, és ha bármelyik termosztát a saját programja szerinti célhőmérsékletnél alacsonyabb hőmérsékletet érzékel, a kazán fűtési igényt kap és elindul.

A Nappali & Konyha termosztát a felhasználó szerint két eres vezetékkel kapcsolódik a kazánhoz, és ez az egyetlen közvetlen, vezetékes termosztát–kazán kapcsolat. A felhasználó a Tado rendszert nevezte meg a jelenlegi vezérlés kizárólagos vezérlőjeként.

**Fontos korlát:** a leírás felhasználói közlésből származik; a kazán tényleges indulását, a termosztátok igényének összegzését, a kazánbemenet típusát, a kapcsolás elektromos módját és az esetleges köztes relé/vezérlő jelenlétét nem ellenőriztük. Ezek nem tekintendők igazolt villamos kapcsolási ténynek.

## 3. Időprogram – Nappali & Konyha

### Hétfő–péntek

| Idősáv | Célhőmérséklet |
| --- | ---: |
| 00:00–05:00 | 21 °C |
| 05:00–08:00 | 22 °C |
| 08:00–15:00 | 22 °C |
| 15:00–17:00 | 24 °C |
| 17:00–23:00 | 23 °C |
| 23:00–24:00 | 21 °C |

Az egymás melletti 05:00–08:00 és 08:00–15:00 idősávokat a képernyőképen szereplő bontás megőrzése érdekében külön sorban tartjuk.

### Szombat

| Idősáv | Célhőmérséklet |
| --- | ---: |
| 00:00–06:00 | 21 °C |
| 06:00–16:00 | 22 °C |
| 16:00–23:00 | 23 °C |
| 23:00–24:00 | 21 °C |

### Vasárnap

| Idősáv | Célhőmérséklet |
| --- | ---: |
| 00:00–06:00 | 21 °C |
| 06:00–16:00 | 22 °C |
| 16:00–23:00 | 23 °C |
| 23:00–24:00 | 21 °C |

## 4. Időprogram – Fürdőszoba

A képernyőkép szerint hétfőtől vasárnapig azonos program érvényes.

| Idősáv | Célhőmérséklet |
| --- | ---: |
| 00:00–05:00 | 19 °C |
| 05:00–07:30 | 22 °C |
| 07:30–18:00 | 19 °C |
| 18:00–21:00 | 22 °C |
| 21:00–24:00 | 19 °C |

## 5. További Tado-beállítások

| Beállítás | Nappali & Konyha | Fürdőszoba |
| --- | --- | --- |
| Minimum távolléti hőmérséklet | Engedélyezve, 20 °C | Engedélyezve, 19 °C |
| Érkezés előtti előfűtés | Balance | Balance |
| Nyitottablak-érzékelés | Bekapcsolva | Kikapcsolva |

A pillanatnyi mért szobahőmérsékletek szándékosan nem kerülnek rögzítésre, mert ehhez a felmérési feladathoz nem relevánsak.

**Bizonyítottság:** a táblázat a 2026-10-27-én megosztott képernyőképek alapján **Részben ellenőrzött**.

## 6. Elektromos elosztó – a fényképen látható feliratok

A megosztott fényképen az alábbi jelölések olvashatók:

- **Áram-védőkapcsoló (FI-relé):** Tracon `TFVH4-80100`; a készüléken látható jelölések: `In 80 A`, `IΔn 0.1 A` (100 mA), `Un 400 V~`, `EN 61008-1`.
- **Kismegszakítók:** három Schneider Electric Resi9 készülék, `R9F14132`, `C32`, `230 V~`, `4500/3` jelöléssel.
- A fényképen látható egyéb Tracon készülék pontos funkcióját ebből a képből nem azonosítottuk.

**Bizonyítottság:** a fényképen olvasható készülékfeliratok **Részben ellenőrzöttek**; ez nem teljes elosztófelmérés, nem bekötési rajz, és nem villamos biztonsági minősítés.

**Fontos pontosítás:** a felhasználó a Tado kizárólagos vezérlő szerepét említette az elosztóval kapcsolatos megjegyzésben, de a megfogalmazás nem teszi egyértelművé a Tado és a fényképen látható FI-relé/kismegszakítók kapcsolatát. Nem rögzítjük tényként, hogy a Tado a FI-relét vezérli. A Tado és a kazán vezérlési kapcsolatát a fenti, külön szakasz dokumentálja.

## 7. Nyitott kérdések

1. A fürdőszobai termosztát pontos generációja: V3 vagy V3+ (a készülék hátoldali címkéjén szereplő rövid modellkód alapján azonosítandó).
2. A kazán termosztátbemenetének típusa és a két termosztát fűtési igényének elektromos összegzése.
3. Van-e köztes relé vagy külön fűtésvezérlő a termosztát és a kazán között.
4. Az elosztóban látható egyéb Tracon készülék pontos típusa és szerepe, illetve a Tado és az elosztó elemei közötti tényleges kapcsolat.

## 8. Biztonsági korlát

Ez a dokumentum kizárólag a rendelkezésre bocsátott képernyőképek és fénykép, valamint a felhasználói közlés dokumentálása. Nem történt elektromos szerelés, fűtési teszt, kazánpróba, hidraulikai módosítás vagy Home Assistant-konfigurációváltoztatás. Bármely ilyen művelet külön, konkrét felhasználói jóváhagyást igényel.
