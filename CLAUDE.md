# Djurambulansen Syd — Webbplats

Statisk landningssida (single-page) för Djurambulansen Syd, en ideell organisation i Blekinge och Skåne.

## Failsafe-regler
- All kod och styling lever i `index.html` (CSS inline i `<style>`-blocket). Inga byggsteg, inget ramverk.
- Ändra inte struktur eller styling utöver det användaren uttryckligen ber om.
- Copy finns parallellt i `webbplats_copy.md` — uppdatera **båda** filerna när texten ändras.
- Bilder ligger i två platser: `uploads/` och projektroten. Verifiera alltid sökväg före referens (se Fragile).
- Bevara existerande klasser och idiom — t.ex. `section-h2`, `section-label`, `pillar-card`, `service-item`.

## Struktur
- `index.html` — hela sidan (inline CSS + JS, tweaks-panel längst ned)
- `webbplats_copy.md` — copy-källa, hålls i synk med index.html
- `README.md` — designspec / handoff-dokument
- `uploads/` — primär bildmapp: `axel.png`, `bil3.png`, `bil4.png`, `karta.png`, `uggla.png`
- Projektrot bilder: `bil3.png`, `bil4.png`, `bil5.png`, `hundaxel1.png`, `ugg1.png`, `axel.png` (duplikater + extra)

## Sektionsordning (top → bottom)
1. Nav (sticky)
2. Hero (axel.png)
3. Om oss
4. Täckningsområde (karta.png)
5. Hur hjälper vi? — bil3.png header, 3 tjänstekort vänster + bil5.png höger
6. Wildlife (ugg1.png) — split
7. Vad vi tror på — 3 pelare
8. Statistik (bil4.png bakgrund)
9. CTA — Du kan hjälpa redan idag
10. Footer

## Kör / Förhandsgranska
- Öppna `index.html` direkt i webbläsaren (inga build-kommandon).
- Tweaks-panelen (nedre högra hörnet) tillåter live-justering av designtokens.

## Designtokens
Se `:root` i `index.html` och tabellerna i `README.md`. Färgsystem: crimson `#721825`, gold `#C4982A`, cream `#FAF8F5`.

## Fragile
- **Bildsökvägar är inkonsekventa.** `bil5.png` ligger endast i projektroten (`src="bil5.png"`), `ugg1.png` likaså. De flesta andra ligger under `uploads/`. Verifiera med `ls` före referens — bruten länk är annars enkelt att introducera.
- **Tweaks-panelen** läser/skriver CSS-variabler och utvalda inline-egenskaper (t.ex. `.hero` height). Ändringar av strukturen runt hero/sektionsmått kan bryta panelens hooks (se script längst ned i `index.html`, ~rad 921).
- **Hero-höjd** är `calc(58vh + 100px)` med `min-height: 620px`. Tweaks-panelen sätter `heroHeight` inline och kan därför skriva över beräkningen.
- **`.services-image`** använder absolute positioning för att fylla högerkolumnen i tjänstegriden. Ändra inte parent `position: relative` utan att också justera bilden.
- **`object-position: center 66.67%`** används medvetet på bil3 för att alltid visa fokuspunkten 1/3 från botten oavsett skärm. Ändra inte till `center` utan att kolla med användaren.
