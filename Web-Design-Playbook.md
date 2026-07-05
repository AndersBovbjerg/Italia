# Web Design Playbook — universelle principper

En løbende samling af designprincipper, gør-og-undgå-regler og tekniske huskeregler
til at bygge hjemmesider der ser professionelle ud og virker. **Ikke** bundet til en
bestemt branche — reglerne gælder bredt (landingssider, virksomhedssider, portfolios,
webshops, SaaS m.m.).

> **Sådan bruger du den:** Vedlæg filen i starten af et nyt projekt. Kør igennem
> "Kerneprincipperne" når du sætter retningen, og "Pre-launch tjeklisten" før du går live.
> Tilføj nye erfaringer nederst under "Log" og flyt dem op i de rette afsnit med tiden.

- **Version:** 1.0
- **Sidst opdateret:** 2026-07-06

---

## Del 1 — De 6 kerneprincipper (fanger 80 % af "wow"-effekten)

### 1. Ankerskrift + støtteskrifter (typografi med hierarki)
Vælg **overskriftsskriften først** — den sætter sidens personlighed (moderne, varm, klassisk...).
Find derefter støtteskrifter der skaber **kontrast uden at ligne** ankeret for meget.

- **Gør:** Giv hver skrift ét fast job — fx *display-serif til overskrifter*, *tekst-skrift til brødtekst*, *neutral sans til UI/knapper/labels/tal*.
- **Gør:** Brug sans-serif med tabular-tal til priser, tider og data — det står skarpt og hopper ikke i bredden.
- **Undgå:** Mere end 3 skriftfamilier. 2 er standard, 3 er loftet.
- **Regel:** Det bliver først "kaos" når skrifter mangler klare roller eller når man rammer 4+. 3 med streng rollefordeling = fint, ikke støj.

### 2. Showets stjerne (ét centralt visuelt element)
Vælg **ét element** der fanger øjet med det samme — et rigtigt foto, en unik gradient, et interaktivt objekt. Resten af designet vokser ud fra det som et "frø".

- **Gør:** Lad stjernen være ægte indhold (et rigtigt produkt-/stemningsbillede), ikke bare dekoration.
- **Gør:** Løft den med subtile virkemidler: glød, ring/ramme, blød skygge, let bevægelse.
- **Undgå:** En "tom" pladsholder eller et generisk stockbillede der ikke betyder noget.
- **Undgå:** Flere konkurrerende stjerner i samme skærmbillede — så er der ingen.

### 3. Visuelt rim (gentag små detaljer)
Gentag former, farver og teksturer på tværs af siden, så alt føles fra samme univers.

- **Gør:** Træk en form fra logoet (fx en oval, en bue, en vinkel) og genbrug den i knapper, mærkater, rammer og ikoner.
- **Gør:** Genbrug ét signaturmønster/-tekstur (fx en stribe eller et gitter) diskret flere steder.
- **Undgå:** At hver sektion har sin egen stil, sine egne hjørneradier og sin egen rytme.

### 4. Skab dybde (tekstur, lag, subtile effekter)
Undgå det flade og upersonlige med **subtil** dybde: fin støj (noise), glas/blur, bløde lagdelte skygger.

- **Gør:** Hold effekterne meget lette (fx støj omkring 5 % opacitet) — de skal *føles*, ikke *ses*.
- **Gør:** Brug en konsistent skygge-/elevationsskala (ikke tilfældige skyggeværdier).
- **Undgå:** Kraftige effekter der stjæler fra stjernen eller gør teksten svær at læse.
- **Undgå:** Blur som ren dekoration — blur betyder "der ligger noget bagved" (modaler, ark).

### 5. Opacitet som hierarki
Styr læserækkefølgen med **gennemsigtighed** i stedet for mange forskellige farver.

- **Gør:** Samme farvetone i teksten, men faldende alpha: overskrift 100 %, brødtekst ~75-80 %, sekundær/meta ~60 %, småtekst/juridisk ~45 %.
- **Gør:** Test kontrast bagefter — nedtonet tekst skal stadig kunne læses (mind. 4.5:1 for brødtekst).
- **Undgå:** Grå-på-grå eller så lav opacitet at teksten forsvinder.

### 6. Prøv noget helt andet (iteration)
Nøjes aldrig med den første idé. Lav bevidst **alternative versioner** for at bryde ud af den første tanke.

- **Gør:** Byg 1-2 drastiske alternativer (fx dark mode ↔ light mode, eller helt nyt layout) som *demoer*, før du binder dig.
- **Gør:** Behandl fx "lys vs. mørk hero" som et *enten/eller*-valg, ikke et tillæg.
- **Undgå:** At bygge videre på den første version bare fordi den allerede er der.

---

## Del 2 — Indhold & tekst

- **Skriv til den faktiske læser.** Hvis målgruppen allerede kender afsenderen, så drop lange intro-tekster og "fakta om os". Kom til sagen.
- **Skær fyldtekst væk.** Generiske fraser ("vi tilbyder kvalitet og hygge") tilfører intet. Er en sætning sand for *enhver* konkurrent, så slet den.
- **Opfind ikke påstande** (årstal, historie, antal kunder) for at fylde ud. Det er utroværdigt og kan være direkte forkert.
- **Én tydelig primær handling (CTA) pr. skærmbillede.** Sekundære handlinger skal være visuelt underordnede.
- **Undgå at gentage samme information i flere sektioner.** Hvis kontakt/åbningstider/adresse står to steder, så saml det ét sted. Dubletter forvirrer og ser ufærdige ud.

---

## Del 3 — Brand & billeder (assets)

### Logo & brand
- **Brug de rigtige, officielle brand-assets** i høj opløsning — gæt aldrig på et logo eller genskab det.
- **Gør logoet transparent** (PNG med alfa) så det virker på alle baggrunde. Ved baggrundsfjernelse: flood-fill fra hjørnerne så indvendige lyse detaljer bevares.
- **Placer et mørkt/farvet logo på en lys plade** hvis baggrunden ellers er mørk (og omvendt) — undgå lav kontrast.
- **Gentag ikke logoet unødigt.** Ét sted i toppen (menuen) er nok — det behøver ikke også fylde i hero og footer.

### Billeder
- **Optimér altid før upload.** Store PNG'er (2-3 MB) gør siden langsom. Komprimér til JPEG (kvalitet ~80) og skalér til den viste størrelse → typisk 100-250 KB.
- **Behold originalerne** urørt ved siden af de optimerede versioner.
- **Angiv `width`/`height`** (eller `aspect-ratio`) på billeder for at reservere plads og undgå layout-hop (CLS).
- **`loading="lazy"`** på alt under folden / tunge medier.
- **Brug `object-fit: cover` + `object-position`** til at styre beskæringen, så det vigtige i billedet ikke skæres væk i faste formater.
- **Beskrivende `alt`-tekst** på meningsbærende billeder; tomt `alt=""` på rent dekorative.
- **Brug SVG-ikoner** (fx Heroicons, Lucide) — aldrig emojis som strukturelle ikoner.

---

## Del 4 — Teknik: performance, responsivt design & tilgængelighed

### Performance
- Moderne billedformater (WebP/AVIF når muligt), responsive billeder, lazy loading.
- `font-display: swap` og `preconnect` til fontudbyder, så tekst ikke bliver usynlig ved load.
- Reservér plads til alt asynkront indhold (undgå CLS).

### Responsivt
- **Mobile-first.** Design til smal skærm først, skalér op.
- **Systematiske breakpoints** (fx 375 / 768 / 1024 / 1440) og en 4/8px spacing-skala.
- **Ingen horisontal scroll** på mobil — tjek altid at `scrollWidth <= viewport`.
- **Min. 16px brødtekst** på mobil (undgår auto-zoom på iOS).
- Skjul/forenkl dekorative elementer på mobil (fx store hero-grafikker) frem for at mase dem ind.

### Tilgængelighed (minimum)
- **Kontrast** mind. 4.5:1 for brødtekst, 3:1 for store elementer.
- **Synlige fokus-tilstande** på interaktive elementer (fjern aldrig fokus-ringen uden erstatning).
- **Touch-mål mind. 44×44px** med luft imellem.
- **Respektér `prefers-reduced-motion`** — sluk/dæmp animationer. (Nem global regel: `@media (prefers-reduced-motion:reduce){ *{animation:none!important;transition:none!important} }`.)
- **Farve må ikke være eneste betydningsbærer** (tilføj ikon/tekst).
- Semantisk HTML, korrekt overskrifts-hierarki (h1→h6 uden spring), labels på formfelter.

### Kode-hygiejne
- **Semantiske farve-tokens / CSS-variabler** (`--primary`, `--surface`...) frem for rå hex spredt i koden.
- **Giv ikoner i knapper eksplicit størrelse.** En inline-`<svg>` uden `width`/`height` render­er kæmpestor og sprænger layoutet — sæt altid fx `width:18px;height:18px`.
- **Vær varsom med "lige høje kolonner" via flex/grid-stretch** — det kan give uventet strukne knapper eller tomme huller. Ofte er en fast/responsiv højde eller top-justering mere robust.
- Ryd ubrugt CSS/HTML væk når du fjerner en sektion (ingen forældreløse klasser).

---

## Del 5 — Tredjeparts-integrationer (kort & embeds)

### Google Maps (indlejret kort)
- **Den nøglefrie `?output=embed`-variant er upålidelig:** den kan blive frame-blokeret og udløser EU-cookiesamtykke — den kan time-out / ikke vise noget for besøgende.
- **Brug i stedet den officielle "Del → Indlejr et kort"-kode** (`.../maps/embed?pb=...`). Den er lavet til iframes, er stabil og kræver **ingen API-nøgle**. (Man skal blot hente koden fra Google Maps-UI'en én gang.)
- **API-nøgle-varianten** (`/maps/embed/v1/place`) er mest robust men kræver opsætning.
- **GDPR-alternativ:** OpenStreetMap-embed loader altid i iframes og sætter ingen tredjeparts-cookies — vælg den hvis du vil undgå samtykke helt (men det er ikke Google).
- **Generel lære:** Test enhver ekstern iframe reelt. Loader OSM men Google ikke, er det tjenesten (framing/consent) — ikke din kode.

### Generelt om embeds
- Antag aldrig at et embed "bare virker" — verificér at det faktisk loader i en rigtig browser.
- Overvej cookie-/samtykke-konsekvenser (især i EU) før du indlejrer tredjepartsindhold.

---

## Del 6 — Arbejdsgang (iteration & verifikation)

- **Byg demoer før du ændrer det rigtige.** Lav varianter i en separat mappe, sammenlign, og bind dig først når valget er truffet.
- **Verificér altid i browseren efter en ændring** — antag ikke at det virker:
  - Tjek konsollen for fejl.
  - Tjek mobil (smal viewport) + at der ikke er horisontal scroll.
  - Tjek at billeder/embeds faktisk loader (`complete`, netværk).
  - Tjek med reduced-motion slået til.
- **Rapportér ærligt.** Hvis noget ikke kan verificeres (fx et værktøj kan ikke se under folden), så sig det — pynt ikke på resultatet.

---

## Del 7 — Anti-mønstre (AI-klichéer & "det ringe" — undgå)

Ting der får en side til at ligne en generisk skabelon eller et hurtigt AI-udkast:

- ❌ **Altid-centreret hero** med en stor overskrift midt på og to knapper under. (Prøv asymmetriske/venstrestillede layouts.)
- ❌ **Generisk fyldtekst** og opdigtet historie/fakta.
- ❌ **Emojis som ikoner.**
- ❌ **Selvtegnede/AI-genererede "maskot"-SVG'er** i stedet for rigtige assets eller ægte fotos.
- ❌ **"Prototype/Demo/Lorem ipsum"-rester** der bliver liggende.
- ❌ **Samme information gentaget** i flere sektioner.
- ❌ **Uskarpe/pixelerede eller enorme uoptimerede billeder.**
- ❌ **Grå-på-grå tekst** og manglende hierarki.
- ❌ **For mange skrifttyper** uden klare roller.
- ❌ **Dekorative animationer uden mening** eller effekter der overdøver indholdet.
- ❌ **Tilfældige skygge-/radius-/spacing-værdier** uden system.

---

## Pre-launch tjekliste

- [ ] Der er én tydelig "stjerne" og én primær CTA pr. skærmbillede.
- [ ] Maks. ~3 skrifttyper, hver med en klar rolle.
- [ ] Tekst-hierarki er tydeligt (størrelse/vægt/opacitet), ingen grå-på-grå.
- [ ] Ingen dubleret information; ingen fyldtekst eller opdigtede påstande.
- [ ] Rigtige, skarpe brand-assets og optimerede billeder (<~250 KB, korrekt beskåret, alt-tekst, lazy).
- [ ] `width`/`height`/`aspect-ratio` sat → ingen layout-hop.
- [ ] Alle embeds (kort m.m.) loader reelt; samtykke/GDPR er overvejet.
- [ ] Mobil: ingen horisontal scroll, læsbar tekst, touch-mål ≥44px, dekoration forenklet.
- [ ] Tilgængelighed: kontrast, fokus-tilstande, reduced-motion, semantisk HTML, labels.
- [ ] Ingen konsol-fejl.
- [ ] Ubrugt CSS/HTML ryddet væk.
- [ ] Mindst ét alternativt design er overvejet, ikke bare den første idé.

---

## Log (tilføj nye erfaringer her, flyt op i afsnittene med tiden)

- **2026-07-06 — v1.0:** Første version. Samler de 6 tips + brand/logo, billedoptimering,
  Google Maps-embed-faldgruber, tekst/indhold, teknik/tilgængelighed, arbejdsgang og anti-mønstre.
