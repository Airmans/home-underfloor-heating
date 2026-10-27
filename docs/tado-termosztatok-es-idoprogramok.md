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

A felhasználó 2026-10-27-én bemásolta a sablon kimenetét. Az alábbi lista **a megosztott kimenet alapján Ellenőrzött**; nem jelent külön, közvetlen lekérdezést a Home Assistantból.

#### Bináris szenzorok

| Entitásazonosító | Megjelenített név |
| --- | --- |
| `binary_sensor.haztartasi_termosztat_ablak` | Háztartási termosztát Ablak |
| `binary_sensor.haztartasi_termosztat_atfedes` | Háztartási termosztát Felülbírálás |
| `binary_sensor.haztartasi_termosztat_bekapcsolva` | Háztartási termosztát Bekapcsolva |
| `binary_sensor.haztartasi_termosztat_csatlakozas` | Háztartási termosztát Csatlakozás |
| `binary_sensor.haztartasi_termosztat_korai_kezdes` | Háztartási termosztát Korai kezdés |
| `binary_sensor.ib0332086528_kapcsolat_allapota` | IB0332086528 Kapcsolat állapota |
| `binary_sensor.nappali_termosztat_ablak` | Nappali termosztát Ablak |
| `binary_sensor.nappali_termosztat_atfedes` | Nappali termosztát Felülbírálás |
| `binary_sensor.nappali_termosztat_bekapcsolva` | Nappali termosztát Bekapcsolva |
| `binary_sensor.nappali_termosztat_csatlakozas` | Nappali termosztát Csatlakozás |
| `binary_sensor.nappali_termosztat_korai_kezdes` | Nappali termosztát Korai kezdés |
| `binary_sensor.ru1602ft01050584057344_elem_akku` | RU1602FT01050584057344 Elem/Akku |
| `binary_sensor.ru1602ft01050584057344_kapcsolat_allapota` | RU1602FT01050584057344 Kapcsolat állapota |
| `binary_sensor.ru2734702592_elem_akku` | RU2734702592 Elem/Akku |
| `binary_sensor.ru2734702592_kapcsolat_allapota` | RU2734702592 Kapcsolat állapota |

#### Klímaentitások

| Entitásazonosító | Megjelenített név |
| --- | --- |
| `climate.haztartasi_termosztat` | Háztartási termosztát |
| `climate.nappali_termosztat` | Nappali termosztát |

#### Választóentitások

| Entitásazonosító | Megjelenített név |
| --- | --- |
| `select.furdo_haztartasi_haztartasi_termosztat_futesi_kor` | Háztartási termosztát Fűtési kör |
| `select.nappali_konyha_nappali_termosztat_futesi_kor` | Nappali termosztát Fűtési kör |

#### Szenzorok

| Entitásazonosító | Megjelenített név |
| --- | --- |
| `sensor.haztartasi_termosztat_futes` | Háztartási termosztát Fűtés |
| `sensor.haztartasi_termosztat_homerseklet` | Háztartási termosztát Hőmérséklet |
| `sensor.haztartasi_termosztat_paratartalom` | Háztartási termosztát Páratartalom |
| `sensor.haztartasi_termosztat_tado_mod` | Háztartási termosztát Tado mód |
| `sensor.kis_otthonunk_automatikus_geofencing` | Kis Otthonunk Automatikus geofencing |
| `sensor.kis_otthonunk_geofencing_helymeghatarozas_mod` | Kis Otthonunk Geofencing (helymeghatározás) mód |
| `sensor.kis_otthonunk_idojarasi_allapot` | Kis Otthonunk Időjárási állapot |
| `sensor.kis_otthonunk_kulso_homerseklet` | Kis Otthonunk Külső hőmérséklet |
| `sensor.kis_otthonunk_napsutes_szazalek` | Kis Otthonunk Napsütés százalék |
| `sensor.kis_otthonunk_tado_mod` | Kis Otthonunk Tado mód |
| `sensor.nappali_termosztat_futes` | Nappali termosztát Fűtés |
| `sensor.nappali_termosztat_homerseklet` | Nappali termosztát Hőmérséklet |
| `sensor.nappali_termosztat_paratartalom` | Nappali termosztát Páratartalom |
| `sensor.nappali_termosztat_tado_mod` | Nappali termosztát Tado mód |

**Egyeztetési megjegyzés:** a bemásolt kimenetben 34 entitásazonosító szerepel, míg a Tado-integráció áttekintő képernyőképe 39 entitást jelez. Az eltérés oka **Ellenőrizetlen**; nem következtetünk arra, hogy hiányzik-e entitás, vagy az összesítés más módon számol. A fenti lista a ténylegesen megosztott kimenetet őrzi meg.


## Nyitott kérdések

1. A fürdőszobai termosztát pontos generációja.
2. A fizikai vezetékezés és a termosztátok fűtési igényének összegzése; lásd a külön kazánvezérlési dokumentumot.
3. A Tado Home Assistant-integráció aktuális entitásai és a kapcsolódó automatizmusok, ha a jóváhagyott felmérés során relevánssá válnak.

## Biztonsági korlát

Ez a dokumentum konfigurációs adatok dokumentálása. Nem történt termosztát- vagy Home Assistant-beállítás módosítása, vezetékezési vizsgálat vagy fűtést befolyásoló teszt.
