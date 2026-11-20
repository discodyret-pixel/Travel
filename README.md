# Travel

Jakob og Kristians rejser siden 2004 – som animeret verdenskort og Excel-register.


## Indhold

| Fil | Hvad |
|---|---|
| `index.html` | Animeret verdenskort (d3). Tre farver: Fælles, Jakob, Kristian. København er start og slut; rejser med flere stop hopper by for by. Besøgte lande lyser permanent. CO2-tæller og smeltende isbjerg. |
| `data/rejseregister.xlsx` | Selve registret (kilden til sandheden): hvem rejste, byer, indenrigsfly, sammenhængende rejser (Rejse-ID) og opsummering med formler. |

## Kør lokalt

Åbn `index.html` i en browser (kræver internet, da d3, topojson og verdensdata hentes fra CDN).

## Del som link (GitHub Pages)

Repo -> Settings -> Pages -> Deploy from a branch -> `main` / root.
Linket bliver `https://<brugernavn>.github.io/rejsefeber/`.

## Opdater data

Rejserne ligger indlejret i `index.html` som `const J=[...]` med formatet
`{y, m, hvem, name, stops:[[navn, lng, lat, land, fly], ...]}`.
Ret i Excel-filen og opdater `J` tilsvarende.

## Bemærkninger

- CO2 er et grovt estimat: storcirkelafstand pr. ben x 0,15 kg/km. Det er ikke et præcist regnskab.
- Verdenskortet (110m) mangler små områder som Singapore, Hong Kong, Aruba, Curaçao, Gibraltar og St. Maarten; de vises som prikker.
- Manglende årstal i registret: Polen, Schweiz og en Gran Canaria-tur.
