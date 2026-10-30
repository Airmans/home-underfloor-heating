# Tado-termosztátok és időprogramok

**Rögzítés dátuma:** 2026-10-27, Europe/Budapest  
**Forrás:** a felhasználó által megosztott Tado-app képernyőképek és írásos közlések.  
**Bizonyítottság:** a képernyőképeken látható beállítások Részben ellenőrzöttek; a fizikai bekötés és a tényleges működés külön nem lett vizsgálva.

## Eszközök és elhelyezés

- **Nappali & Konyha:** Tado Smart Thermostat; megjelenített azonosító: `RU2734702592`; firmware `215.2`. A felhasználó megerősítése szerint V3+. Elhelyezés: az előszoba és a nappali-konyha közötti átjáró.
- **Fürdőszoba:** Hager EK960, Typ RU01; a Tado alkalmazásban Smart Thermostat néven szerepel, megjelenített azonosító: `RU1602FT01050584057344`; firmware `54.20` a korábbi képernyőkép szerint. A Hager EK960/RU01 típus a 2026-10-30-i hátlapfotó alapján **Ellenőrzött**; a teljes V3/V3+ hardverazonosság nincs külön igazolva. Elhelyezés: a fürdőszoba és a mosókonyha/gépészeti helyiség közötti átjáró. Nem történt csere; a korábbi Tado-megnevezést a 2026-10-28-i Notion-feljegyzés már helyesbítette.
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

**Egyeztetési megjegyzés:** a 39-es integrációs összesítés eltérésének okát a felhasználó 2026-10-27-én tisztázta: a Tado-integráció frissítés előtti változata még támogatta a telefonokhoz kapcsolódó entitásokat, ezért létrehozta azokat. A frissítés után ezek már nem szerepeltek az integráció által szolgáltatott entitások között. A korábbi összesítés és a jelenlegi leltár ezért nem feltétlenül hasonlítható össze közvetlenül.

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

**Egyeztetési megjegyzés:** a bemásolt kimenetben 33 entitásazonosító szerepel. A korábbi 39-es integrációs összesítés eltérésének okát a felhasználó a korábbi integrációs változat telefonentitás-támogatásával magyarázta; lásd a következő ellenőrzési bejegyzést. A fenti lista a ténylegesen megosztott kimenetet őrzi meg.



### Megszűnt Tado-telefonentitások törlésének ellenőrzése

- **Ellenőrzés dátuma:** 2026-10-27, Europe/Budapest.
- **Státusz:** **Ellenőrzött**.
- **Forrás:** a Home Assistantban megjelenő „Ezt az entitást már nem szolgáltatja a(z) tado integráció” figyelmeztetés, a törlés utáni, felhasználó által bemásolt entitáslista és a felhasználó 2026-10-27-i magyarázata.
- **Megállapítás:** a Tado-integráció frissítés előtti változata még támogatta a telefonokhoz kapcsolódó entitásokat, ezért létrehozta azokat. A frissítés után ezeket az entitásokat az integráció már nem szolgáltatta.
- **Eltávolított elavult entitások:** hét entitás a következő telefonokhoz kapcsolódóan: Bálint telefon (3), Reni telefon (1), Zoé telefon (1), Zsombi telefon (2). A felhasználó mind a hét elavult entitást törölte a Home Assistantból.
- **Lezárás:** a telefonentitások eltérésének oka és a törlés indokoltsága **Ellenőrzött**. Ez a bejegyzés a korábbi integrációs állapot magyarázatát rögzíti; nem állítja, hogy a Home Assistant aktuális állapotát közvetlenül lekérdeztük.

## Nyitott kérdések

1. A fürdőszobai termosztát pontos generációja.
2. A rejtett kábelút és a teljes Tado jelút független ellenőrzése; a kazánoldali B5–B6, valamint a Tado NO–COM végpontbekötés már fotóval dokumentált. A két helyiség igénylogikája korábban rögzített, nem újra bekérendő adat.
3. A Tado Home Assistant-integráció aktuális entitásai és a kapcsolódó automatizmusok, ha a jóváhagyott felmérés során relevánssá válnak.

## Biztonsági korlát

Ez a dokumentum konfigurációs adatok dokumentálása. Nem történt termosztát- vagy Home Assistant-beállítás módosítása, vezetékezési vizsgálat vagy fűtést befolyásoló teszt.


## Hátlapfotók és vezérlési kapcsolat pontosítása — 2026-10-30

**Ellenőrzés:** 2026-10-30, Europe/Budapest. Forrás: a most feltöltött 7692.jpg, 7691.jpg, 7690.jpg; a korábbi működési leírás forrása a [PF-01.04 Notion-feladat](https://app.notion.com/p/4063e49c5f5f81cf9cc6fad61f53adf6), 2026-10-28 23:29–23:39, Europe/Budapest.

- Nappali Tado: **RU02, DRU02-TA-14** – **Ellenőrzött**, hátlapfotó; a V3+ változat korábbi felhasználói azonosítás.
- Fürdőszobai Hager: **EK960, Typ RU01, ZR0516** – **Ellenőrzött**, hátlapfotó; a 3 db AAA elem látható. A Tado 3 AAA táplálása a korábbi felhasználói közlésből származik (**Korábbi forrásból átvett**).
- Tado fali alaplap: **barna → NO, világoskék → COM**, NC és a digitális/parkoló kapcsok a képen üresek – **Ellenőrzött**. A kazánoldali érpárt a felhasználó azonosította: **B5–B6**; ezt a kazán kapocsfotói és a megosztott rajz PT szobatermosztát-jelölése támasztja alá.
- A Hager eredetileg is a fürdőszobában volt; nem csere és nem pusztán egy régi/tartalék készülék. A felhasználó szerint a Tado-rendszerben vezeték nélküli érzékelőként használja (**Korábbi forrásból átvett**); az app pontos eszközszerepe és a teljes hardverazonosság nincs függetlenül igazolva.
- A helyiségeknek saját időprogramjuk és célértékük van; bármelyik igénye kezdeményezheti a kazán fűtését. Közvetlen kazánkapcsoló a nappali Tado; a Hager igénye közvetetten, a Tado-rendszeren át érvényesül (**Korábbi forrásból átvett**). Ez a már dokumentált működés nem új nyitott kérdés, élő teszt nem történt.

A bekötés részletei és az összes mostani fénykép név szerinti, eredeti elérhetőséget megőrző forrásjegyzéke: [Kazán és kazánoldali fűtésvezérlés](kazan-es-kazanoldali-vezerles.md). A hátlapok hitelesítési kódjait és QR-kódjait nem másoljuk a dokumentációba. Nem történt beállításmódosítás vagy működési teszt.


## Kiegészítő Tado-útmutató — 2026-10-30

**Forrás:** [a felhasználó által megadott PDF](https://m.media-amazon.com/images/I/A1UoSRX8RDL.pdf). **Ellenőrzés:** 2026-10-30, Europe/Budapest.

A 11 oldalas fájlban a tado° Wireless Smart Thermostat V3+ nemzetközi szerelői útmutatója (3.2 változat), továbbá radiátortermosztát-útmutató található. A fő útmutató Wireless Receiver és Wireless Temperature Sensor készülékekre vonatkozik, nem közvetlenül a lefotózott RU02 vezetékes termosztátra.

A PDF 5. oldalán (4. lépés) a COM–NO relékapcsolat potenciálmentes és 230 V-os alkalmazását külön ábra mutatja; az alapértelmezett relékonfiguráció R01. **Ellenőrzött** kizárólag az útmutatóban tárgyalt vevőre; a helyszíni RU02 konfigurációjának R01 értéke ebből nem állapítható meg.

A relés kapcsolási elv összhangban van a már fotózott NO–COM bekötéssel (**Részben ellenőrzött**, összevetés). A PDF nem igazolja a Bosch B5–B6 teljes villamos specifikációját, a Hager EK960–Tado hardverazonosságot, a meglévő zónakonfigurációt vagy a szivattyú üzemmódját. Nem történt konfigurációmódosítás vagy működési teszt.


## Vezetékes Tado szerelői útmutató — 2026-10-30

**Forrás:** [tado° Starter Kit – Wired Smart Thermostat V3+, English International, Manual version 3.2, dokumentum 104210 V3](https://cdn.brandfolder.io/607DGEMS/as/7k4rssnm8hbmr6mjf94qmck/104210-DIGITAL-ST01IB01-INSTALLER_MANUAL-TA-EN-00-V3.pdf). **Ellenőrzés:** 2026-10-30, Europe/Budapest. A felhasználó által megadott eredeti PDF letöltve és szövegként, valamint a 4. oldal renderelt ábráján ellenőrizve; 8 oldal. A fájlnév V3 jelölése dokumentumjelölés, nem a felhasználó készülékgenerációjának önálló bizonyítéka.

### Megállapítás és alkalmazhatóság

- A 4. PDF-oldal (4. lépés) a **vezetékes Smart Thermostat** NO–NC–COM / P1–P3 / A–−–+ kapocskiosztását mutatja. Ez a lefotózott nappali Tado alaplap kapocskiosztásával egyezik (**Ellenőrzött**, dokumentum és fotó összevetése); a dokumentum nem nevezi meg külön az RU02/DRU02-TA-14 kódot.
- A **COM–NO** a relés kapcsolás két használt kapcsa; az útmutató külön potenciálmentes és 230 V-os relés alkalmazást ismertet. Relés konfigurációazonosító: **R01**; gyári alapmód: Relay (**Ellenőrzött**, gyártói útmutató). A helyszíni menü tényleges értékét nem olvastuk le, ezért az aktuális R01 beállítást nem minősítjük ellenőrzöttnek.
- A fotón barna → NO és világoskék → COM csatlakozik. A felhasználó által azonosított érpár a kazán B5–B6 kapcsára vezet; a Bosch-rajz itt PT szobatermosztát-érintkezőt mutat. A relés ON/OFF kapcsolási elvhez így már a vezetékes termosztát gyártói útmutatója is rendelkezésre áll; új bekötési fotó nem szükséges.
- A dokumentum 5–6. oldala más, digitális és analóg interfészeket is felsorol. A Bosch név ottani előfordulása **nem bizonyítja**, hogy a konkrét Tronic Heat 3500 ezeket támogatja; a lefotózott bekötés relés.
- Ez az útmutató az előző Wireless Receiver kézikönyvnél közvetlenebb forrás a nappali termosztát bekötési elvéhez. Nem igazolja a Hager EK960 teljes hardverazonosságát vagy a teljes Tado-zónakonfigurációt. A B5–B6 kör pontos villamos specifikációját továbbra is a megfelelő Bosch előírásból kell azonosítani.

A kézikönyv konfigurációs és működési tesztlépéseit nem hajtottuk végre. Ez kizárólag dokumentációs ellenőrzés, nem beállításmódosítás vagy rendszerpróba.
