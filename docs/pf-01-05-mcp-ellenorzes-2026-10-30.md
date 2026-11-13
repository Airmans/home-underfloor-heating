> **TÖRTÉNETI PF-FORRÁS – 2026-11-13:** ez a fájl a dokumentációs migráció előtti állapotot őrzi, nem párhuzamosan karbantartott HA-dokumentum. **Központi, egyetlen szerkesztési hely:** [Home-Assistant-Main / pf-01-05-mcp-ellenorzes-2026-10-30.md](https://github.com/Airmans/Home-Assistant-Main/blob/main/docs/pf-01-05-mcp-ellenorzes-2026-10-30.md). A forrásszöveg és annak eredeti ellenőrzési időpontja/bizonyítottsága változatlan; az alábbi tartalmat a PF-repóban tovább már ne módosítsuk. [PF → HA forrástérkép](https://github.com/Airmans/Home-Assistant-Main/blob/main/docs/pf-heating-source-map.md) · [migrációs jegyzőkönyv](https://github.com/Airmans/Home-Assistant-Main/blob/main/migration/2026-11-13/REPORT.md).

# PF-01.05 – MCP-ellenőrzés, 2026-10-30

Forrás: Home Assistant MCP, olvasási célú entitásregiszter- és állapotlekérdezések. Bizonyítottság: Ellenőrzött az adott lekérdezés időpontjában.

A korábban dokumentált nyolc beltéri és egy kerti hőmérő mind megtalálható a HA entitásregiszterében, engedélyezett ZHA-entitásként. A Dolgozó és Háztartási érzékelők állapotát a felhasználói kérésre nem dokumentáltuk. A további hét hőmérő számszerű értéket adott.

A HA-ban nyolc climate entitás, egy weather entitás és a helyiségi páratartalom-entitások azonosíthatók. A nyilik kifejezésre 15 nyitásérzékelő-entitás szerepelt. Ez nem teljes fizikai eszközleltár.

Nyitott eltérések: a WC-ajtóérzékelő entitása továbbra is szerepel a HA-ban, bár a felhasználó szerint nincs már felszerelve; a Háló bal ablak érzékelője a nyilik keresésben nem szerepelt, további ellenőrzést igényel. A regiszteradat önmagában nem bizonyítja a fizikai felszereltséget.

A részletes relevancia- és eltéréslista véglegesítése szükséges a PF-01.05 lezárásához. A Home Assistant és a fűtési rendszer nem módosult.
