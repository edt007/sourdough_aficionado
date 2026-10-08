# AGENTS.md – Sourdough Aficionado

## Formål og niveau

Byg en statisk hjemmeside, som hjælper nybegyndere med at starte og passe en surdej. Brugeren er multimediedesignstuderende på 1. semester. Skriv enkel, overskuelig kode, som brugeren kan forstå og arbejde videre med. Forklar valg kort på dansk.

## Faste rammer

- Brug HTML5 og CSS3. Ingen JavaScript, frameworks, CSS-frameworks eller byggeværktøjer.
- Opret otte selvstændige HTML-sider med fungerende navigation via relative links.
- Saml fælles styles i én genanvendelig CSS-fil. Brug tydelige klassenavne og CSS-variabler til farver og andre fælles værdier.
- Brug semantisk HTML, fx `header`, `nav`, `main`, `section` og `footer`. Hver side skal have én hovedoverskrift og en logisk overskriftstruktur.
- Brug links til navigation og handlinger, der fører til en anden side. FAQ skal bruge HTML-elementerne `details` og `summary`.
- Fremdriftsvisningen viser det aktuelle trin i guiden. Den gemmer ikke brugerens fremskridt.
- Bevar eksisterende arbejde. Undersøg projektet, før du opretter eller ændrer filer.

## Designreference

Figma: https://www.figma.com/design/BQxruClZ9nzh5dqI5DVtAR/Sourdough-Aficionado?node-id=10-18141

Brug Figma MCP som primært opslagsværk. Brug udelukkende designet **HiFi Prototype**. Kontrollér, at node `10:18141` tilhører dette design. Brug ikke andre filer, skitser eller designs som grundlag. Hvis reference eller frame er uklar, spørg brugeren, før implementeringen fortsætter. Hvis Figma MCP ikke er tilgængelig, oplys det og bed om det nødvendige designgrundlag; opfind ikke designdetaljer.

### Designværdier fra den tidligere analyse

Kontrollér værdierne i HiFi Prototype under den første analyse. Ved afvigelser bruges det verificerede design, og forskellen nævnes i planen.

| Egenskab | Værdi |
| --- | --- |
| Desktopreference | 1440 px bred |
| Indhold | Maksimal bredde 1200 px, centreret |
| Baggrund | `#F7F3EB` |
| Primær tekst | `#292822` |
| Sekundær tekst | `#5F5B51` |
| Accent | `#85452F` |
| Kanter | `#CEC5B6` |
| Overskrifter | Lora, Regular |
| Brødtekst | Inter, Regular |
| H1 | 60 px på desktop |
| H2 | 36 px på desktop |
| H3 | 28–32 px på desktop; vælg efter den konkrete komponent |
| Brødtekst | 16 px |
| Navigation | 15 px |
| Knaptekst | 15 px, Semi Bold |

Hent også afstande, linjehøjder, billeder og komponentmål fra designet. Brug passende fallback-skrifttyper, hvis Lora eller Inter ikke kan indlæses.

## Sider og foreslåede filnavne

| Side | Fil |
| --- | --- |
| Forside | `index.html` |
| Start din første surdej | `start-din-foerste-surdej.html` |
| Bland mel og vand | `bland-mel-og-vand.html` |
| Du har blandet din første surdej | `du-har-blandet-din-foerste-surdej.html` |
| Giv din surdej frisk næring | `giv-din-surdej-frisk-naering.html` |
| En lille rutine, morgen og aften | `en-lille-rutine-morgen-og-aften.html` |
| Materialer | `materialer.html` |
| Bliv klogere på surdej | `bliv-klogere-paa-surdej.html` |

Brug designets indhold, siderækkefølge og linkmål. Tilpas filnavnene til en eksisterende projektstruktur, hvis det er nødvendigt, og forklar det i planen.

## Responsivitet og billeder

- Gengiv desktopdesignet så præcist som muligt ved 1440 px. Brug en fleksibel indholdscontainer med maksimal bredde 1200 px og plads langs kanterne.
- Der findes kun et desktopdesign. Lav derfor en enkel mobiltilpasning: stabl kolonner, tilpas overskrifter og afstande, og lad kort og billeder følge skærmbredden.
- Vælg media queries efter indholdets behov. Undgå vandret scrolling. Navigationen skal fungere på mobil uden JavaScript; lad fx links ombryde.
- Brug billeder og illustrationer fra Figma, når de kan eksporteres. Gem dem lokalt, og brug relative billedstier.
- Brug tydelige placeholders i passende proportioner, når billeder mangler. Oplys, hvilke billeder der senere skal udskiftes.
- Giv informative billeder meningsfuld `alt`-tekst og dekorative billeder tom `alt`-tekst.
- Sørg for synligt tastaturfokus, læsbar tekst og tilstrækkeligt store klikområder.

## Arbejdsproces og godkendelse

### Etape 1 – Undersøgelse og plan, uden filændringer

1. Undersøg projektmappen, eksisterende filer og eventuelle projektinstruktioner.
2. Kontrollér adgang til Figma MCP og den korrekte HiFi Prototype-reference.
3. Skab overblik over de otte sider, navigationen og de fælles komponenter.
4. Undersøg farver, typografi, layout og billeder. Notér mangler og nødvendige mobiltilpasninger.
5. Fremlæg en kort dansk plan med mappestruktur, sider, fælles komponenter, etaper og eventuelle afklaringer.
6. **Stop og afvent brugerens godkendelse, før du opretter eller ændrer projektfiler.**

### Etape 2 – Grundstruktur

Efter godkendelse: Opret en enkel struktur med de otte HTML-filer, `css/style.css` og `images/`, medmindre projektet allerede har en passende struktur. Giv endnu ikke implementerede sider en tydelig midlertidig overskrift. Opret fælles navigation og footer, så links mellem siderne virker fra starten.

### Etape 3 – Fælles styles og komponenter

Implementér farver, typografi, indholdscontainer, header, footer, links, CTA-links, kort, informationsbokse og fremdriftsvisning. Genbrug CSS-klasser på tværs af sider. Hold HTML og CSS enkelt; gentag fælles HTML, når statisk HTML kræver det.

### Etape 4 – Forside

Implementér forsiden efter HiFi Prototype. Kontrollér desktop og mobil, før siden meldes færdig.

### Etape 5 – Øvrige sider, én ad gangen

Implementér hver af de resterende sider som en separat etape. Undersøg kun de relevante Figma-frames, genbrug fælles styles og kontrollér sidens links og layout. Implementér FAQ med `details` og `summary` på siden Bliv klogere på surdej.

Efter hver implementeringsetape: Rapportér kort, hvad der er færdigt, hvad der er kontrolleret, og hvad næste etape indeholder. Afvent godkendelse til næste etape, medmindre brugeren allerede har godkendt flere etaper samlet. Gentag ikke spørgsmål om allerede godkendt arbejde.

## Ressourcebevidst brug af Figma MCP

- Hent først et overblik og derefter kun detaljer for den aktuelle etape.
- Genbrug allerede hentede designværdier og fælles komponentoplysninger.
- Undgå gentagne kald for uændrede frames og unødvendige fulde udtræk af designet.
- Hent nye oplysninger, når de er nødvendige for at løse en konkret usikkerhed eller kontrollere en afvigelse.

## Kontrol og kort rapportering

Kontrollér efter hver relevant etape:

- At relative links, billedstier og CSS-stier virker, og at alle otte sider kan åbnes.
- At HTML har sidetitel, `lang="da"`, tegnsæt og viewport samt korrekt semantik og overskriftstruktur.
- At navigation, CTA-links og FAQ kan bruges med tastaturet, og at fokus er synligt.
- At layoutet følger Figma på desktop og fungerer på mobil uden vandret scrolling.
- At fælles komponenter fremstår ens, og at placeholders er tydelige.

Brug de tilgængelige browser- og valideringsværktøjer uden at tilføje unødvendige afhængigheder. Lav en samlet kontrol af hele hjemmesiden, når alle sider er implementeret.

Rapportér på dansk i få punkter: ændrede filer, færdigt arbejde, udførte kontroller, eventuelle mangler og næste etape. Skeln mellem kontroller, der faktisk er udført, og kontroller, brugeren selv skal udføre. Forklar kun tekniske detaljer, når de hjælper brugeren med at forstå arbejdet.
