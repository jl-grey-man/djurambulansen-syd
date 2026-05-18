# Handoff: Djurambulansen Syd – Webbplats

## Overview
En fullständig landningssida för Djurambulansen Syd, en ideell organisation i Blekinge och Skåne som transporterar husdjur och viltskadade djur till veterinär och rehabilitator. Sidan är designad för att kännas varm, seriös och tillgänglig — inte corporate.

## Om designfilerna
Filerna i detta paket är **HTML-designreferenser** — prototyper som visar avsedd layout, visuell stil och interaktioner. De är **inte** produktionskod att kopiera direkt. Uppgiften är att **återskapa dessa designer i målkodbas** med dess befintliga ramverk och bibliotek (React, Next.js, eller liknande). Använd HTML-filen som visuell specifikation.

## Fidelity
**High-fidelity (hifi)** — pixelperfekta mockups med slutgiltiga färger, typografi, avstånd och interaktioner. Återskapa UI:t noggrant med de bibliotek och mönster som finns i kodbasen.

---

## Sektioner / Vyer

### 1. Navigation (sticky)
- **Layout**: Full-bredd, `height: 66px`, flex row, logo vänster, länkar höger
- **Bakgrund**: `rgba(255,255,255,0.97)` med `backdrop-filter: blur(12px)`
- **Scrollad**: border-bottom + box-shadow aktiveras vid scroll > 20px
- **Logo**: SVG tassavtryck (vinrött) + wordmark "Djurambulansen" (Lora, 15.5px, bold) / "SYD" (guld, 10px, uppercase, letter-spacing 0.13em)
- **Länkar**: 14px, font-weight 500, färg `#6B5F5A`, hover → `#721825`
- **CTA-knapp**: "Bli månadsgivare" — `background: #721825`, vit text, 9px 20px padding, border-radius 8px

### 2. Hero
- **Layout**: Full-bredd, `height: 58vh`, min-height 520px
- **Bakgrund**: `uploads/axel.png` — person bakifrån bär golden retriever, cobblestone-gata
- **Overlay**: Gradient vänster→höger: `rgba(22,10,8,0.60)` → transparent vid 68%
- **Innehåll** (max-width 500px, padding 80px 52px):
  - Badge: "IDEELL ORGANISATION · BLEKINGE & SKÅNE" — guld `#D4A83A`, 11px, uppercase, med 26px linje till vänster
  - H1: "Vi är här när ditt djur behöver oss" — Lora, clamp(28px–48px), vit, font-weight 600, letter-spacing -0.025em
  - Underrubrik: 16px, `rgba(255,255,255,0.82)`, max-width 400px
  - CTA primär: "Ring oss nu" — `#721825`, vit text, 13px 28px padding
  - CTA sekundär: "Bli månadsgivare" — outline light, `rgba(255,255,255,0.42)` border

### 3. Om oss
- **Layout**: Centrerad, `padding: 80px 52px`, bakgrund `#FAF8F5`
- **Innehåll**: max-width 760px, text-align center
- **Text**: 18px, line-height 1.76, `#6B5F5A`
- **Copy**: "Djurambulansen Syd är en ideell organisation som hjälper djurägare och människor som hittar skadade vilda djur..."

### 4. Tre pelare ("Vad vi tror på")
- **Layout**: 3-kolumns grid, gap 20px, `padding: 96px 52px`, vit bakgrund
- **Rubriken**: section-label "VAD VI TROR PÅ" (guld), H2 "Tre saker som gör oss annorlunda" (Lora, 38px)
- **Kort** (`.pillar-card`):
  - Bakgrund: `#FAF8F5`
  - Border-radius: 12px
  - Röd topp-linje: 3px solid `#721825`
  - Hover: translateY(-2px) + box-shadow
  - Ikon-cirkel: 48px, `rgba(114,24,37,0.08)`, SVG-ikon i crimson
  - H3: Lora, 20px, `#2A1E1C`
  - Text: 14.5px, `#6B5F5A`, line-height 1.74
- **Pelare A** – Gratis för alla (gåva-ikon)
- **Pelare B** – Fullständig transparens (öga-ikon)
- **Pelare C** – Medlemsdemokrati (personer-ikon)
- Varje kort har en textlänk med → pil

### 5. Tjänster ("Hur hjälper vi?")
- **Bakgrund**: `#511018` (mörk vinröd)
- **Header-bild**: `uploads/bil3.png`, full-bredd, height 340px, object-fit cover center
- **Innehåll-padding**: `64px 52px 0` inom max-width 1320px
- **Section-label**: guldig, 70% opacity
- **H2**: "Hur hjälper vi?" — vit, Lora
- **Grid**: 2×2, gap 16px
- **Tjänste-kort** (`.service-item`):
  - Bakgrund: `#fff`
  - Border-radius: 12px
  - Hover: box-shadow + translateY(-1px)
  - Layout: flex row, gap 22px
  - Ikon-box: 48px × 48px, border-radius 10px, `rgba(114,24,37,0.07)`, crimson SVG-ikon
  - Nummer: 10.5px, guld, uppercase
  - H3: 19px, Lora, `#2A1E1C`
  - Text: 14.5px, `#6B5F5A`
- **4 tjänster**:
  1. Husdjur till veterinär (transport-ikon)
  2. Vilt till rehabilitator (fågel-ikon)
  3. Stöd för myndigheter (stjärna-ikon)
  4. Samarbete med rehabilitatorcentrum (puls-ikon)

### 6. Skadade vilda djur (split)
- **Layout**: 50/50 grid, ingen padding
- **Vänster**: `uploads/uggla.png`, height 100%, object-fit cover, object-position center 25%
- **Höger**: bakgrund `#F3EDE3`, padding 88px 64px 88px 60px
- **Innehåll**: section-label, H2 "Skadade vilda djur", två stycken text

### 7. Täckningsområde (kartsband)
- **Layout**: Full-bredd, height 420px, position relative
- **Bakgrund**: `uploads/karta.png` — Google Maps-screenshot av södra Sverige, object-fit cover center
- **Overlay**: Gradient vänster→höger: `rgba(247,243,238,0.92)` → transparent vid 75%
- **Text**: absolut positionerad ovanpå, max-width 480px till vänster
- **Copy**: "Vi kör i Blekinge och Skåne..."

### 8. Statistik (på bil4-bakgrund)
- **Layout**: Full-bredd band, `padding: 80px 52px`, position relative
- **Bakgrundsbild**: `uploads/bil4.png`, ambulans på motorväg, overlay `rgba(81,16,24,0.82)`
- **Grid**: 4 kolumner med dividers
- **Siffror**: Lora 50px, vit, bold
- **Labels**: 13.5px, `rgba(255,255,255,0.55)`
- **Platshållarvärden**: XX+ för alla siffror — ersätt med riktiga

### 9. CTA-sektion ("Du kan hjälpa redan idag")
- **Layout**: 3 kort, gap 18px, bakgrund `#FAF8F5`, `padding: 96px 52px`
- **Kort 1 – Ring oss**: vit bakgrund, border, stort telefonnummer i Lora
- **Kort 2 – Bli månadsgivare**: `background: #721825`, vit text, guldknapp
- **Kort 3 – Läs mer**: `#F3EDE3`, outlined knapp

### 10. Footer
- **Bakgrund**: `#2A1E1C`
- **Layout**: 3 kolumner (2fr 1fr 1fr), padding 68px 52px 36px
- **Logo**: guld tassavtryck + wordmark
- **Kolumner**: Snabblänkar, Kontakt (Tel, Mail, Nöd 24/7, Adress)
- **Bottenkant**: copyright vänster, sociala medier höger

---

## Interaktioner & Beteende

| Element | Beteende |
|---|---|
| Nav | Transparent → solid med shadow vid scroll > 20px |
| Pillar-kort | hover: translateY(-2px) + box-shadow |
| Tjänste-kort | hover: box-shadow + translateY(-1px) |
| Pilar-länk (→) | hover: gap ökar 5px → 8px |
| Btn primary | hover: lightare bakgrund + translateY(-1px) |
| Smooth scroll | `scroll-behavior: smooth` på html-element |

---

## Design Tokens

### Färger
```
--crimson:       #721825   /* Primär brand, djup vinröd */
--crimson-deep:  #511018   /* Tjänster-bakgrund, mörkare */
--crimson-soft:  #8B2535   /* Hover-state */
--gold:          #C4982A   /* Accenter, labels */
--gold-warm:     #D4A83A   /* Hero badge, hover-gold */
--cream:         #FAF8F5   /* Sektion-bakgrund, varm off-white */
--cream-warm:    #F3EDE3   /* Alternerande sektioner */
--dark:          #2A1E1C   /* Primär text, footer */
--mid:           #6B5F5A   /* Brödtext, sekundär text */
--border:        rgba(114,24,37,0.09)
```

### Typografi
```
Rubriker: 'Lora', Georgia, serif
  H1:    clamp(28px, 3.2vw, 48px) / weight 600 / letter-spacing -0.025em
  H2:    clamp(25px, 2.6vw, 38px) / weight 600 / letter-spacing -0.022em
  H3:    19–22px / weight 600

Brödtext: 'Nunito Sans', system-ui, sans-serif
  Body:  14.5–18px / line-height 1.68–1.76
  Small: 10.5–12px / weight 700 / letter-spacing 0.12em (uppercase labels)
```

### Spacing & Radii
```
Section padding:  96px 52px (desktop), 22px (mobil)
Card radius:      12px
Button radius:    8px
Gap (grid):       16–22px
```

### Skuggor
```
Card hover:  0 6px 24px rgba(114,24,37,0.08)
Nav scrolled: 0 2px 20px rgba(0,0,0,0.06)
```

---

## Assets

| Fil | Användning | Sektion |
|---|---|---|
| `uploads/axel.png` | Hero bakgrundsbild — person bär hund | Hero |
| `uploads/bil3.png` | Ambulans på gatsten med folk | Tjänster header |
| `uploads/bil4.png` | Ambulans på motorväg, solnedgång | Statistik-bakgrund |
| `uploads/uggla.png` | Personal räddar uggla på gata | Viltsektion |
| `uploads/karta.png` | Google Maps-screenshot södra Sverige | Täckningsområde |

---

## Platshållare att fylla i

- `0-XXX-XXX` — telefonnummer (3 platser: hero, CTA, footer)
- `info@djurambulansensyd.se` — e-post
- `[Adress]` — gatuadress
- `XXXXXX` — organisationsnummer
- `XX+` i statistiksektionen — ersätt med riktiga siffror

---

## Filer i detta paket

| Fil | Beskrivning |
|---|---|
| `index.html` | Komplett design, alla sektioner, interaktioner, tweaks-panel |
| `uploads/axel.png` | Hero-bild |
| `uploads/bil3.png` | Tjänster header-bild |
| `uploads/bil4.png` | Statistik bakgrundsbild |
| `uploads/uggla.png` | Viltsektion bild |
| `uploads/karta.png` | Kartbild södra Sverige |

Öppna `index.html` i en webbläsare för att se designen. Klicka på tweaks-ikonen (nedre högra hörnet) för att testa varianter.
