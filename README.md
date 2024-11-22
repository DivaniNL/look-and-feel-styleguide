# Styleguide

Dit project bevat de styleguide voor Red Pers. Deze styleguide bevat HTML-code waarin alle elementen getoond worden. Hierin zit ook het gezamenlijke CSS-stijlenbestand voor Red Pers, ontwikkeld om consistentie en herkenbaarheid in de stijl van de website te waarborgen. De huisstijl maakt gebruik van gedefinieerde kleuren, typografie, en stijlelementen die over verschillende pagina’s en componenten heen toegepast worden.

De stylesheet kan hier worden geraadpleegd: https://divaninl.github.io/redpers-styleguide/redpers.css

## Inhoud

1. [Bestandsstructuur](#bestandsstructuur)
2. [Typografie](#typografie)
3. [Kleuren](#kleuren)
4. [Naamgevingsconventie](#naamgevingsconventie)
5. [Componenten en Gebruik](#componenten-en-gebruik)

---

### Bestandsstructuur
De standaard projectstructuur bestaat uit vier hoofdmappen:
styles: Bevat de CSS-bestanden, inclusief het hoofdhuisstijlbestand.
fonts: Bevat de benodigde lettertypes, zoals Tiempos en Inter.
scripts: Bevat de JavaScript-bestand(en)
assets: Bevat afbeeldingen en overige bestanden

### Typografie

We maken gebruik van drie verschillende fonts voor specifieke doeleinden:

- **Tiempos Headline**: Voor citaten en artikelkoppen.
- **Tiempos Text**: Voor artikeltekst.
- **Inter**: Voor reguliere tekst, kleinere kopteksten en overige tekstfragmenten.

De fonts worden geladen met behulp van `@font-face`, en de juiste fonts worden ingesteld via CSS-variabelen voor eenvoudig hergebruik in de stylesheet.

**Typografie CSS Variabelen**
- `--font-default`: Inter, sans-serif, voor algemene tekst.
- `--font-article`: Tiempos Text, voor artikeltekst.
- `--font-heading-important`: Tiempos Headline, voor belangrijke koppen.
Inter wordt ingeladen via de API van Google Fonts. Tiempos Text en Tiempos Headline zijn lokaal opgeslagen in de map "fonts".
Er zijn standaard lettergroottes, letterafstanden en regelhoogtes gedefinieerd voor verschillende soorten tekst en koppen, die bijdragen aan een leesbare en aantrekkelijke lay-out.

### Kleuren

De kleuren van de huisstijl zijn opgebouwd uit primaire en secundaire kleuren, met een aanvullende set van grijstinten voor contrast en leesbaarheid.

- **Primaire kleur (Rood)**: `--primary-color` en varianten voor lichtere tinten.
- **Secundaire kleur (Groen)**: `--secondary-color` en `--secondary-color-dark` voor een donkerdere versie.
- **Grijstinten**: Inclusief zwart, wit, en verschillende grijstinten zoals `--grey` en `--darkgrey` voor tekst en achtergronden.

Voor toegankelijkheid is er een hoge-contrastmodus toegevoegd met aangepaste kleuren om te voldoen aan WCAG AAA-normen. Dit wordt geactiveerd via een mediaquery voor `prefers-contrast: more`.

### Naamgevingsconventie

Om de CSS-structuur consistent en begrijpelijk te houden, gebruiken we een vaste naamgevingsconventie voor klassen. Klassenamen volgen de structuur:

**`elementtype_functie`**

- **elementtype**: Het HTML-element of de rol, zoals `button`, `heading`, of `link`.
- **functie**: De specifieke stijl of functie die het element vervult, zoals `utility`, `quote`, of `article`.

**Voorbeelden van naamgeving:**
- `button_utility`: Voor standaard utility-knoppen.
- `heading_quote`: Voor koppen die worden gebruikt bij citaten.
- `text_intro`: Voor intro-tekst bij artikelen.
- `form_search`: Voor zoekformulieren.

### Componenten en Gebruik

**Koppen**  
Koppen worden gestileerd met verschillende klassen op basis van hun functie. Bijvoorbeeld, `.heading_article` wordt gebruikt voor artikelkoppen, en `.heading_quote` voor citaten. 

**Knoppen**  
De knoppen in de huisstijl zijn ontworpen voor specifieke functies en bevatten standaardstijlen voor interacties zoals hover en focus. Voorbeelden zijn `.button_play` voor audio-knoppen en `.button_subscribe` voor de aanmeldingsknop voor nieuwsbrieven.

**Formulieren**  
Formulieren bestaan uit verschillende inputvelden en een submit knop. Ook in de searchpopup bevind zich een formulier met een submitknop die een icoon bevat van een vergrootglas. De submitknop op de contactpagina zal hoogstwaarschijnlijk dezelfde stijl krijgen als de "button_menu". Mocht dit veranderen zal ik dit vermelden

---

Met dit stijlenbestand zorgen we voor een professionele en consistente visuele presentatie die gebruikerservaringen verbetert en aansluit bij de identiteit van Red Pers.
