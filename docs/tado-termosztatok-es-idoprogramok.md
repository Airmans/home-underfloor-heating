# Tado-termosztátok és időprogramok

**Rögzítés dátuma:** 2026-10-27, Europe/Budapest  
**Forrás:** a felhasználó által megosztott Tado-app képernyőképek és írásos közlések.  
**Bizonyítottság:** a képernyőképeken látható beállítások Részben ellenőrzöttek; a fizikai bekötés és a tényleges működés külön nem lett vizsgálva.

## Eszközök és elhelyezés

- **Nappali & Konyha:** Tado Smart Thermostat; megjelenített azonosító: `RU2734702592`; firmware `215.2`. A felhasználó megerősítése szerint V3+. Elhelyezés: az előszoba és a nappali-konyha közötti átjáró.
- **Fürdőszoba:** Tado Smart Thermostat; megjelenített azonosító: `RU1602FT01050584057344`; firmware `54.20`. V3 vagy V3+ generációja **Ellenőrizetlen**; a készülék hátoldali modellkódja szükséges az azonosításhoz. Elhelyezés: a fürdőszoba és a mosókonyha/gépészeti helyiség közötti átjáró.
- Mindkét eszköz képernyőképen látható állapota csatlakoztatott, akkumulátorállapota „Good”, Dazzle Mode bekapcsolva.
- **Tado Internet Bridge:** firmware `92.1`, a képernyőkép szerint csatlakoztatott.
- A felhasználó közlése szerint a Home Assistant Tado-integrációja felhőalapú. Az aktuális HA-entitásokat és automatizmusokat itt nem vizsgáltuk.
- **Auto-Assist:** a képernyőkép szerint aktív; megjelenített megújítási dátum: 2026-11-26.

## Felhasználó által leírt vezérlési logika

A felhasználó közlése szerint a két termosztát külön időprogrammal rendelkezik, és bármelyik termosztát fűtési igénye elindíthatja a kazánt. A kazánoldali részleteket külön dokumentum rögzíti: [Kazán és kazánoldali fűtésvezérlés](./kazan-es-kazanoldali-vezerles.md).

## Időprogram – Nappali & Konyha

### Hétfő–péntek

| Idősáv | Célhőmérséklet |
| --- | ---: |
| 00:00–05:00 | 21 °C |
| 05:00–08:00 | 22 °C |
| 08:00–15:00 | 22 °C |
| 15:00–17:00 | 24 °C |
| 17:00–23:00 | 23 °C |
| 23:00–24:00 | 21 °C |

A 05:00–08:00 és 08:00–15:00 idősávokat a képernyőképen látható bontás megőrzése érdekében külön sorban tartjuk.

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

## Időprogram – Fürdőszoba

A képernyőkép szerint hétfőtől vasárnapig azonos program érvényes.

| Idősáv | Célhőmérséklet |
| --- | ---: |
| 00:00–05:00 | 19 °C |
| 05:00–07:30 | 22 °C |
| 07:30–18:00 | 19 °C |
| 18:00–21:00 | 22 °C |
| 21:00–24:00 | 19 °C |

## További Tado-beállítások

| Beállítás | Nappali & Konyha | Fürdőszoba |
| --- | --- | --- |
| Minimum távolléti hőmérséklet | Engedélyezve, 20 °C | Engedélyezve, 19 °C |
| Érkezés előtti előfűtés | Balance | Balance |
| Nyitottablak-érzékelés | Bekapcsolva | Kikapcsolva |

A pillanatnyi mért szobahőmérsékleteket nem rögzítjük, mert ehhez a felmérési feladathoz nem relevánsak.


## Home Assistant-integráció – eszközleltár

A 2026-10-27-én megosztott Home Assistant képernyőkép szerint a Tado-integráció összesítése **7 eszközt és 39 entitást** jelez. A képernyőképen látható eszközök:

| Home Assistant-eszköznév | Megjelenített terület / zóna | Entitások száma | Bizonyítottság |
| --- | --- | ---: | --- |
| Háztartási termosztát | Fürdő & Háztartási · Zone | 11 | **Ellenőrzött** – képernyőkép |
| IB0332086528 | IB01 · Gépészet | 1 | **Ellenőrzött** – képernyőkép; Tado Internet Bridge |
| Kis Otthonunk | Home · Gépészet | 0 | **Ellenőrzött** – képernyőkép |
| Kis Otthonunk | Home | 6 | **Ellenőrzött** – képernyőkép; az eszköz pontos szerepét külön nem azonosítottuk |
| Nappali termosztát | Nappali & Konyha · Zone | 11 | **Ellenőrzött** – képernyőkép |
| RU1602FT01050584057344 | RU01 · Gépészet | 2 | **Ellenőrzött** – képernyőkép; fürdőszobai termosztát |
| RU2734702592 | RU02 · Gépészet | 2 | **Ellenőrzött** – képernyőkép; nappali-konyhai termosztát |

**Megjegyzés:** a képernyőképen szereplő integrációs összesítés 39 entitást mutat, miközben a felsorolt eszközsoroknál látható darabszámok összege ettől eltér. Ezt az eltérést nem oldjuk fel feltételezéssel; az egyedi entitások listáját a Home Assistantból kell lekérni és ellenőrizni.

### Entitásazonosítók lekérése

A Home Assistantban a **Fejlesztői eszközök → Sablon** oldalon az alábbi Jinja-sablon listázza a Tado-integrációhoz rendelt entitásazonosítókat és a hozzájuk tartozó megjelenített neveket:

```jinja
{% for entity_id in integration_entities('tado') | sort %}
{{ entity_id }} — {{ state_attr(entity_id, 'friendly_name') }}
{% endfor %}
```

A sablon eredménye még nincs rögzítve ebben a dokumentumban. A lekért lista alapján lehet majd véglegesíteni a Tado-hoz tartozó HA-entitások leltárát.


## Nyitott kérdések

1. A fürdőszobai termosztát pontos generációja.
2. A fizikai vezetékezés és a termosztátok fűtési igényének összegzése; lásd a külön kazánvezérlési dokumentumot.
3. A Tado Home Assistant-integráció aktuális entitásai és a kapcsolódó automatizmusok, ha a jóváhagyott felmérés során relevánssá válnak.

## Biztonsági korlát

Ez a dokumentum konfigurációs adatok dokumentálása. Nem történt termosztát- vagy Home Assistant-beállítás módosítása, vezetékezési vizsgálat vagy fűtést befolyásoló teszt.
