# VUAdmin Updates

## Week van 11 tot 17 mei 2026

### 💸 Gespreide betaling (termijnen) — Checkout stap 2

Cursussen kunnen voortaan worden aangeboden met de mogelijkheid om in termijnen te betalen. Dit is per cursus instelbaar via het admin-panel (veld "Termijnbetaling").

- In **stap 2 van het afrekenproces** (deelnemersgegevens) verschijnt automatisch een keuzelijst bij cursussen die termijnbetaling ondersteunen — maar alleen wanneer **niet op factuur** betaald wordt.
- De opties zijn: **"Betaal het volledige bedrag"** of **"Betaal in X delen"** (waarbij X het aantal termijnen is dat voor die cursus is ingesteld).
- De gekozen betaaloptie wordt opgeslagen per inschrijving en werkt door in de **overzichtspagina** (stap 3), waar het te betalen bedrag dienovereenkomstig wordt aangepast.
- Bij betaling via Mollie wordt het correcte termijnbedrag doorgestuurd.
- Bij hernavigatie naar stap 2 wordt de eerder gemaakte keuze automatisch teruggezet.

---

## Week van 4 tot 10 mei 2026

### 🎓 Cursusdetailpagina — Startdatum toont tijd van eerste les

Bij de selectie van een startdatum op de cursusdetailpagina wordt nu naast de datum ook de **begin- en eindtijd van de eerste les** getoond (bijv. `12-05-2026 09:00–11:00`). De programmatitel is verwijderd uit dit overzicht.

### 🃏 Cursuskaarten — Titel toont maximaal 3 regels

De cursustitel op cursuskaarten (aanbodoverzicht) wordt nu afgekapt na **3 regels**, met een ellipsis voor langere titels. Eerder werd 2,5 regel getoond.

### 📧 Footer nieuwsbrieflabels — Betere uitlijning

De labels in de nieuwsbriefinschrijfformulier in de footer waren te laag gepositioneerd. Ze worden nu correct verticaal gecentreerd in het invoerveld.

---

### 🛒 Checkout stap 1 — Verbeterde terugnavigatie en pre-fill

Wanneer een klant terugnavigeerde naar stap 1 (winkelwagen/contactgegevens) nadat er al een bestelling was aangemaakt, werd hij eerder automatisch doorgestuurd naar stap 2. Dat is aangepast:

- **Stap 1 toont nu altijd het formulier**, ook als er al een bestelling bestaat voor deze winkelwagen.
- Alle ingevulde gegevens worden **automatisch teruggezet**: naam, e-mail, geboortedatum, telefoonnummer, adres én alle bedrijfsgegevens inclusief de eerder gekozen betaalwijze.
- Het bedrijfsveld klapt automatisch open als er eerder een bedrijfsnaam was ingevuld.
- Bij opnieuw indienen van stap 1 worden de **bestelling en studentgegevens bijgewerkt** in plaats van een nieuwe bestelling aan te maken.
- De winkelwagen toont een **"Je winkelwagen is leeg"**-melding als er geen items zijn, in plaats van het contactformulier.

### 💳 Betaalwijze — iDEAL / WERO

De betaaloptie "direct betalen" toont nu **iDEAL / WERO** in plaats van alleen iDEAL.

### 🧾 Pro forma factuur — Meerdere deelnemers en correct ordernummer

De pro forma factuur die bij een zakelijke bestelling (op factuur) wordt meegestuurd is herzien:

- **Één factuur per bestelling**: er wordt nu één e-mail met bijlage verstuurd voor de volledige bestelling, in plaats van een aparte e-mail per inschrijving.
- **Ordernummer correct**: de factuur toont nu het juiste ordernummer (`ordernr`) van de bestelling.
- **Deelnemer per regel**: de factuurlijst bevat een extra kolom "Deelnemer" zodat bij elke cursusregel direct zichtbaar is voor wie de inschrijving geldt.
- **"Cursist" uit de aanhef verwijderd**: de cursistnaam in de adresregel staat nu direct onder het bedrijfsadres, zonder apart kopje.
- **Kortingsregels per item**: kortingen worden correct per inschrijvingsregel verwerkt.

---

### 📎 E-maillog — bijlagen zichtbaar en downloadbaar

E-mails die met een bijlage worden verstuurd worden nu ook als zodanig vastgelegd in het e-maillog.

- Het e-maillog slaat het pad naar de bijlage op wanneer een e-mail met bijlage wordt verstuurd.
- Op de detailpagina van een e-maillogbericht verschijnt een **"Bijlage downloaden"**-knop als de e-mail een bijlage had.
- Bij het opnieuw verzenden van een e-mail wordt de bijlage automatisch opnieuw meegestuurd.

Ondersteunde e-mails met bijlagen:
- **Nieuwe cursist** — bijlage uit het e-mailsjabloon (bijv. welkomstbrief)
- **Factuur** — factuur-PDF
- **Gecombineerde factuur** — gecombineerde factuur-PDF
- **Bedrijfsfactuur** — gegenereerde offerte-PDF

---

### 🏢 Bedrijfsfacturatie — Volledig vernieuwd checkout-proces

Bij het afrekenen kunnen bedrijven nu alle facturatiegegevens direct invullen in stap 1, en kiezen hoe ze willen betalen.

**Stap 1 — Bedrijfsgegevens**

- Wanneer een bedrijfsnaam wordt ingevuld, verschijnt automatisch een uitklapblok met aanvullende velden: e-mailadres (voor de factuur), BTW-nummer, contactpersoon, bedrijfsadres (straat, postcode, plaatsnaam), referentie/kostenplaats en PO-nummer/inkoopnummer.
- De gebruiker kiest hier ook de betaalwijze: **direct betalen via iDEAL** of **op factuur**.
- Bij keuze "op factuur" wordt het e-mailadres verplicht (factuur wordt hiernaar verstuurd).
- Alle velden worden opgeslagen bij het aanmaken van de bestelling.

**Stap 2 — Deelnemersgegevens**

- Geen wijzigingen.

**Stap 3 — Overzicht**

- Bedrijfsgegevens worden getoond als alleen-lezen overzicht: naam, e-mail, BTW, contactpersoon, adres, referentie, PO-nummer en betaalwijze.
- Inschrijvingen die op factuur worden betaald tonen een paars **"Betaling: Op factuur"**-label.
- Totaalblok toont een aparte regel **"Op factuur: €XX"** naast het direct te betalen bedrag.

**Betaalrouting**

- **Direct (iDEAL)**: bedrijfsnaam wordt opgeslagen bij de inschrijving, maar betaling verloopt gewoon via Mollie.
- **Op factuur**: factuur wordt automatisch per e-mail verstuurd naar het opgegeven bedrijfse-mailadres. De inschrijving gaat **niet** door Mollie.

**Nieuwe instelling: "Bedrijfsfactuur: plaatsingsstatus"**

Beheerders kunnen via *Instellingen → Betalingen* kiezen wat er gebeurt met inschrijvingen die op factuur worden betaald:

- **Na ontvangst betaling** *(standaard)*: inschrijving blijft op "open" staan totdat een beheerder handmatig bevestigt dat de bankbetaling is ontvangen.
- **Direct geplaatst**: inschrijving wordt direct als bevestigd beschouwd; de factuur dient dan puur als boekhoudkundig document.

---

## Week van 27 april tot 3 mei 2026

### 🧹 Opruimen achter de schermen

- **Producten krijgen altijd een unieke webadres**: Twee producten met dezelfde naam kregen soms hetzelfde webadres, waardoor één van de twee niet bereikbaar was. Dit wordt nu automatisch voorkomen.
- **Verouderde en ongebruikte onderdelen verwijderd**: Een aantal velden en opties die nooit in gebruik zijn genomen zijn opgeruimd. Dit heeft geen invloed op de werking van de site, maar houdt het systeem overzichtelijk en sneller.

---

### ✨ Financial Dashboard

Nieuw dashboard op `/admin/financial` voor een financieel overzicht per grootboekrekening.

- **Omzet per Grootboekrekening**: Toont gefactureerde bedragen per grootboek (cursusinschrijvingen én productverkopen), uitgesplitst naar BTW-tarief, met kolommen excl. BTW, BTW-bedrag en incl. BTW.
- **Betalingen per Grootboekrekening**: Toont ontvangen betalingen per betaalmethode/grootboek (op basis van `payment_methods.grootboeknummer`), inclusief terugbetalingen en nettobedrag.
- **BTW Overzicht**: Volledige BTW-splitsing per tarief — zowel gefactureerd als ontvangen, excl./BTW/incl. naast elkaar.
- **Omzet per dag**: Lijndiagram (Chart.js) met dagelijkse ontvangen omzet incl. en excl. BTW.
- **Openstaande Posten**: Overzicht van alle onbetaalde facturen, ingedeeld in leeftijdsbuckets (0–30, 30–60, 60–90, >90 dagen) met kleurcodering.
- **Datumfilter**: Datumkiezer met snelknoppen (7d, 30d, deze maand, vorige maand, dit jaar). Standaard ingesteld op de huidige maand.


---

### 🐛 Bugfixes

- **Eigen profiel kon niet worden opgeslagen**: Beheerders zonder het "Gebruikers"-recht kregen een foutmelding bij het opslaan van hun eigen profiel. Je kunt nu altijd je eigen naam, e-mailadres en wachtwoord aanpassen, ongeacht je rechten. Rollen en permissies blijven uiteraard alleen bewerkbaar voor beheerders met het juiste recht.

- **Fout bij aanmaken nieuw programma**: Bij het aanmaken van een nieuw programma stond de cursus-dropdown automatisch op de eerste cursus uit de lijst. Dit zorgde voor fouten als die selectie niet klopte. De dropdown start nu leeg en je moet bewust een cursus kiezen voordat je het programma kunt opslaan.

- **Verlaten winkelwagen e-mail crashte**: E-mailsjabloon 25 (verlaten winkelwagen) bevatte een verwijzing naar `$order`, maar de verlaten-winkelwagen-mail (`Cartleftmail`) stuurde deze variabele niet mee. Het sjabloon moet `$cart` gebruiken in plaats van `$order`.

- **Marketing Dashboard: fout bij docenten in populaire pagina's**: De kolom `display_name` is eerder verwijderd uit de `teachers`-tabel (samengevoegd met `name`). Het dashboard probeerde die kolom nog op te halen. De query haalt nu `name` én `lastname` op en zet deze samen tot de volledige naam — identiek aan het `fullname`-attribuut op het Teacher-model.

- **Bevestigingse-mail bij directe plaatsing werd dubbel verstuurd (Westvoorne)**: Bij directe plaatsing (geen Mollie-betaling) en na de Mollie-webhook werd de bevestigingse-mail twee keer verstuurd. De dubbele aanroepen zijn verwijderd; de model observer handelt dit nu volledig af.

---

### 🎨 Westvoorne thema — Filters cursusoverzicht en collectiepagina's werken nu correct

- **`beschikbaar` → `available`**: De filterdropdown had de verkeerde parameternaam (`beschikbaar`), waardoor dit filter volledig werd genegeerd door de backend. Hernoemd naar `available`.
- **Geselecteerde categorie blijft zichtbaar**: De collectie-dropdown toonde nooit de actief geselecteerde optie — `selected` attribuut toegevoegd.
- **Locatiefilter toegevoegd**: De `$locations`-variabele werd al door de controller meegegeven maar nooit getoond. Een locatiedropdown (op stad) is nu zichtbaar in het filter.

---

## Week van 20 to 26 april 2026

### 🎨 Amsterdam thema — Diverse fixes en verbeteringen

- **Mobiel zoekformulier**: De zoekbalk in het mobiele menu heeft nu `action="/cursussen"`, `method="GET"` en `name="q"`, identiek aan het desktopformulier. De zoekknop submit het formulier.
- **CTA halfbreed — mobiel**: Complexe flex/negatieve-marge layout vervangen door de normale Bootstrap grid-stacking. `.offers-img` krijgt een expliciete hoogte zodat de achtergrondafbeelding zichtbaar blijft. Cirkel (`.offers-content`) blijft `position: absolute` in de hoek.
- **CTA halfbreed — cirkelgrootte mobiel**: Cirkel vergroot naar 185×185px (was 155px), afbeeldingshoogte naar 220px voor betere proporties en ruimte voor de knop.
- **Sortering cursusoverzicht**: `?sort=` parameter werkt nu correct. Sortering wordt nu toegepast vóór het samenstellen van `$allItems`, zodat beide variabelen de juiste volgorde weerspiegelen.
- **Nieuwsslider — gelijke hoogte**: Alle nieuwskaarten in de slider hebben nu dezelfde hoogte via flexbox op `.slick-track`, `.slick-slide` en `.news-item`. Knop "Lees meer" staat altijd onderaan.
- **`.basic-details p`**: Paragrafen binnen `.basic-details` blokken hebben nu `margin-bottom: 0`.
- **Passieve event listener fout (Slick)**: `EventTarget.prototype.addEventListener` gepatcht zodat `touchstart`/`touchmove` altijd als `passive: false` worden geregistreerd — lost de `preventDefault`-waarschuwing van Slick op.
- **Bloktitel hoogte (`.online-offer-title-block`)**: Inline stijl `min-height: 3em; line-height: 1.5em; overflow: hidden` verplaatst van HTML naar CSS als klasse `.online-offer-title-block`. Op mobiel (`max-width: 767px`) vergroot naar `min-height: 5em`.
- **Statustag cursusblok**: `<a href="#">` vervangen door `<span>` met klasse `.btn-red-border`. `.btn-red-border` gestyled als pill (`border-radius: 50px`, `width: auto`, `min-width: 90px`, `padding: 3px 14px`, `font-size: 11px`).
- **Megamenu mobiel — container breedte**: `.container` binnen het megamenu dropdown krijgt op mobiel (`max-width: 767px`) `max-width: 100%; padding: 0` zodat het dezelfde breedte heeft als de andere menu-items.
- **Megamenu mobiel — driekoloms grid**: Grid op `.list-group-content ul` verplaatst van `@media (min-width: 768px)` naar `@media (min-width: 992px)` zodat het alleen actief is als de `col-lg-*` kolommen ook naast elkaar staan.
- **Megamenu mobiel — lege panelen**: Klik op een item zonder subpagina's toont niet langer een leeg paneel. De click handler controleert nu of het doelpaneel bestaat; zo niet, wordt de link gewoon gevolgd.
- **Megamenu mobiel — lettertypes**: Alle tekst in het mobiele megamenu gebruikt nu consistent `"DM Sans", sans-serif` op `13px`. `.back-btn` gebruikte `'AvenirNextDemiBold'`, `.block-title` en sublinks hadden geen fallback of verkeerde grootte — allemaal gecorrigeerd.

---

### ✨ Zoekresultaten — Producten verschijnen nu ook bij cursuszoekopdrchten

- **Producten in zoekresultaten**: Bij een zoekopdracht via `?q=` op `/cursussen` worden nu ook actieve producten doorzocht (op `title`, `description` en `intro`). Cursussen en producten worden samengevoegd en alfabetisch gesorteerd getoond.
- **`CourseController`**: importeert nu `Product`, zoekt producten bij een zoekterm, tagt elk item met `item_type` (`course` of `product`), en geeft `$allItems` en `$products` mee aan de view.
- **`course_index.blade.php` (Amsterdam)**: loopt nu over `$allItems`, controleert `item_type`, en toont `<x-horizontal_product_block>` voor producten en `<x-horizontal_course_block>` voor cursussen — identiek aan `collection_show.blade.php`.

---

### ✨ Marketing Dashboard — Verwijzende domeinen

- **Nieuw: Verwijzende domeinen-kaart**: Toont de top 25 externe domeinen die bezoekers naar de site stuurden, met het aantal bezoeken. Het eigen domein (via `APP_URL`) en IP-adressen worden automatisch uitgesloten.
- Domeinen zijn klikbaar als link naar `https://{domein}`.

---

### ✨ Marketing Dashboard — Docenten in populaire pagina's

- **Docentnamen in populaire pagina's**: `/docent/*`-URLs tonen nu de naam van de docent in plaats van de URL. De `display_name` wordt gebruikt, met `name` als fallback.
- `TrackPageVisit`-middleware herkent `/docent/{slug}` voortaan als `page_type = 'teacher'`.
- De controller haalt docenten op via `teachers.slug → display_name / name`.

---

### ✨ Marketing Dashboard — Collectietitels in populaire pagina's

- **Collectietitels correct**: `/collectie/{slug}`-URLs tonen nu de collectienaam in plaats van de URL. Opgeslagen als slug (niet ID), zowel in de middleware als de controller.
- Titel-JSON wordt gedecode naar `nl` als de waarde een JSON-object is.

---

### ✨ Marketing Dashboard — Links in populaire pagina's

- **Klikbare titels**: Elke rij in de "Populaire pagina's"-tabel is nu een klikbare link (`<a target="_blank">`) naar de volledige opgeslagen URL.

---

### ✨ Marketing Dashboard — Cursustitels via slug-fallback

- **Cursussen zonder `program_id`**: Bezochte cursuspagina's zonder `?program_id=` in de URL worden nu alsnog correct op naam getoond via een slug-opzoeking in de `courses`-tabel.

---

### ✨ Marketing Dashboard — E-mailstatistieken verwijderd

- De "Verstuurde e-mails per sjabloon"-kaart is verwijderd uit het Marketing Dashboard.

---

### ✨ Marketing Dashboard — UTM-filterrij als Bootstrap-grid

- De vier UTM-filterdropdowns (bron, medium, campagne, zoekterm) zijn opgemaakt als een Bootstrap `row g-2` met elk een `col-3` kolom, zodat ze netjes naast elkaar staan.

---

### 🐛 Bugfix — `TrackAttribution`: array-naar-string-conversie

- **Oorzaak**: Bij URL's met `?utm_source[]=foo` retourneerde `$request->get($param)` een array. De `"$param=$value"` string-interpolatie crashte met *Array to string conversion* op regel 27.
- **Fix**: Beide loops (UTM en Matomo/MTM-parameters) slaan de waarde nu over met `continue` als `is_array($value)` geldt.

---

### 🐛 Bugfix — E-mailsjabloon: `action_link` te lang voor kolom

- **Oorzaak**: `action_link` was gedefinieerd als `VARCHAR(255)`. Lange URLs met Matomo- én UTM-parameters overschreden deze limiet.
- **Fix 1**: Nieuwe migratie `2026_04_25_140000_alter_emailtemplates_action_link_to_text.php` wijzigt de kolom naar `TEXT`.
- **Fix 2**: `Emailtemplate::autoTagActionLink()` herkent nu ook Matomo-URL's (`mtm_source=`, `mtm_campaign=`) als reeds getagd en voegt geen extra UTM-parameters toe.

---

- **Preset datumbereiken**: Naast de vrije datumkiezer zijn zes snelkoppelingen toegevoegd: **7 d**, **30 d** (standaard actief), **90 d**, **Deze maand**, **Vorige maand** en **Dit jaar**. Klikken op een preset stelt de datumvelden automatisch in en laadt de data. Er kan nog gekozen worden voor custom data.

- **Nieuw: 404-pagina's kaart**: Een nieuwe kaart toont de top 25 URLs die een 404-fout veroorzaakten in de geselecteerde periode. Gebaseerd op een nieuwe `not_found_logs`-tabel die bij elke `NotFoundHttpException` de oorspronkelijke URL vastlegt (vóór de redirect naar `/404`).
  - Nieuwe migratie: `2026_04_25_100002_create_not_found_logs_table.php`.
  - `App\Exceptions\Handler` logt voortaan de originele URL naar `not_found_logs` bij elke 404.
  - Nieuw model: `App\Models\NotFoundLog`.

- **Nieuw: Zoekopdrachten op de site**: Een nieuwe kaart toont de top 25 zoektermen ingevoerd via `?q=` op de publieke website. De termen worden live opgehaald uit de reeds bijgehouden `page_visits.url`-kolom (geen extra database-opslag nodig).

- **`/404` uitgesloten van populaire pagina's**: De `/404`-redirect-URL wordt niet meer getoond in de "Populaire pagina's"-tabel, net als de bestaande uitsluiting van `cart/*`.

- **Controller volledig herwerkt voor array-filters**: Alle dashboard-methoden (`getKpis`, `getVisitorsOverTime`, `getSourceSplit`, `getDeviceSplit`, `getCampaigns`, `getKeywords`, `getPopularPages`, `getConversionStats`) accepteren nu een `array $filters` met `sources`, `mediums`, `campaigns` en `terms` in plaats van een enkele `string $source`.
  - Nieuw: `scopeForUtmFilters()` scope op `PageVisit`-model voor efficiënte DB-filtering op alle vier UTM-dimensies.
  - Nieuw: `filterItemsByUtm()` helper voor filteren van geattribueerde `OrderItem`-collecties.
  - Nieuw: `getFilterOptions()` haalt unieke UTM-waarden op voor de dropdownopties.

---

### ✨ E-mailsjablonen — Automatisch UTM-tagging van knoplinks

- **Auto-tagging bij opslaan**: Wanneer een e-mailsjabloon wordt opgeslagen en de `action_link` nog geen `utm_source`-parameter bevat, worden automatisch de volgende UTM-parameters toegevoegd:
  - `utm_source=VUadmin`
  - `utm_medium=email`
  - `utm_campaign=<action_description van het sjabloon>`
  - `utm_term=<action_text zonder Blade-tags en HTML>`
- De logica staat in `Emailtemplate::boot()` via een `saving`-event en werkt voor alle bronnen (beheerinterface, artisan, enz.).
- Uitzonderingen: lege `action_link`, links die al getagd zijn (idempotent), en pure Blade-expressies zoals `{{ $evaluationUrl }}` (onveranderd gelaten).

---

### ✨ Marketing Dashboard — Verbeteringen

- **E-mails gegroepeerd op sjabloon-ID**: E-mails in het dashboard worden nu correct gegroepeerd op `emailtemplate_id` (één rij per sjabloon). Als naam wordt de `action_description` van het sjabloon getoond in plaats van het onderwerp.

- **`cart/*`-pagina's uitgesloten van populaire pagina's**: URLs die beginnen met `cart/` worden niet meer meegenomen in de "Populaire pagina's"-tabel.

- **Populaire pagina's: filter op type**: De "Populaire pagina's"-kaart heeft filterknoppen gekregen: **Alle / Pagina's / Cursussen / Collectie**. Klikken filtert de lijst direct zonder nieuwe API-aanroep.

- **Cursustitels correct weergegeven**: Meertalige cursustitels (opgeslagen als `{"nl": "..."}`) worden nu altijd als leesbare Nederlandse naam getoond.

- **UTM én MTM (Matomo) parameters correct verwerkt**:
  - `TrackPageVisit`-middleware slaat nu ook `mtm_source`, `mtm_medium`, `mtm_campaign`, `mtm_term` en `mtm_content` op als fallback op de UTM-kolommen.
  - Verkeersbronnen, campagnes en zoektermen in het dashboard herkennen beide parameterformaten.
  - `utm_medium = cpc` wordt als enige definitie van betaald verkeer gebruikt — overige media-waarden zijn verwijderd.

- **Bronfilter correct**: De `scopeForSource`-scope in `PageVisit` werkte niet correct door losstaande `orWhereIn`-aanroepen die buiten de datumrange vielen. Alle condities zijn nu verpakt in sluitingen zodat de AND/OR-logica correct is.

- **Nieuwsbrief niet als betaald kanaal**: `utm_source = newsletter` wordt nooit als betaald verkeer geclassificeerd, ook niet bij `utm_medium = cpc`.

---

### ✨ Marketing Dashboard — Eerste versie

- **Nieuw: Marketing Dashboard** (`/admin/marketing`): Een apart beheer-dashboard met basisstatistieken voor marketeers. Zichtbaar voor gebruikers met de rechten `Marketing Dashboard`.

  - **Bezoekers & paginaweergaven**: Aantal unieke bezoekers (per sessie) en totale paginaweergaven over de gekozen periode.
  - **Conversies & omzet**: Aantal inschrijvingen (order items) met de bijbehorende omzet, afgeleid uit `order_items.attribution_data`.
  - **Conversieratio & mobiel %**: Verhouding conversies/bezoekers en aandeel mobiele bezoekers.
  - **Bezoekers per dag**: Lijngrafiek met dagelijks bezoekaantal over de geselecteerde periode.
  - **Verkeersbronnen**: Doughnut-grafiek met verdeling over Paid, Social, Nieuwsbrief, Organisch, Direct en Overig.
  - **Apparaat**: Doughnut-grafiek Desktop / Mobiel / Tablet.
  - **Campagnes**: Tabel met `utm_campaign`, conversies en omzet — gefilterd op bron.
  - **Zoektermen**: Tabel met `utm_term` en conversies.
  - **Populaire pagina's**: Top 15 bezochte URL's met bezoekcount en percentage.
  - **Populaire cursussen**: Top 10 cursuspagina's op bezoekcount, inclusief cursusnaam.
  - **E-mails per sjabloon**: Overzicht van alle verstuurde e-mails gegroepeerd op sjabloon (onderwerp), met aantal verstuurd, geopend en open rate.
  - **Tijdfilter**: Aangepaste datumkiezer (van/tot) met "Toepassen"-knop.
  - **Bronfilter**: Knoppengroep — Alles / Organisch / Betaald / Social / Nieuwsbrief / Direct. Klikken op een bron filtert alle statistieken, campagnes, zoektermen en conversies naar die bron.

- **Nieuw: paginabezoeken bijhouden** (`page_visits`-tabel + middleware): Een nieuwe `TrackPageVisit`-middleware registreert elke paginabezoek op de publieke website.

  - Slaat per bezoek op: sessie-ID, IP-adres, volledige URL, pagina-type (`home`, `course`, `program`, `page`), pagina-ID (bijv. program_id), referrer, user agent, apparaattype en UTM-waarden uit de sessie.
  - Dedupliceert: dezelfde sessie + URL wordt maximaal één keer per 30 minuten geregistreerd.
  - Sluit bots en crawlers automatisch uit (Google, Bing, Yandex, curl, etc.).
  - Slaat admin-, API- en asset-verzoeken over.
  - Migratie: `2026_04_25_000001_create_page_visits_table.php`.

- **Nieuw: `emailtemplate_id` in e-maillogboek**: De tabel `emaillogs` heeft een nullable foreign key `emailtemplate_id` gekregen, zodat e-mails gekoppeld kunnen worden aan het gebruikte sjabloon. Maakt groepering per sjabloon in het Marketing Dashboard mogelijk. Migratie: `2026_04_25_000002_add_emailtemplate_id_to_emaillogs.php`.

- **Nieuw: `Marketing Dashboard`-rechten via migratie**: De permissie `Marketing Dashboard` wordt automatisch aangemaakt bij `php artisan migrate` (`2026_04_25_000003_add_marketing_dashboard_permission.php`). Wijs de rechten daarna toe aan de gewenste rollen via het beheer (Gebruikers & Rollen).

- **Verbeterd: attributie-opslag als sleutel-waarde object**: Nieuwe bestellingen slaan `attribution_data` voortaan op als een gestructureerd object (`{"utm_source": "meta", "utm_campaign": "zomer"}`) in plaats van de vroegere array van strings (`["utm_source=meta"]`). Bestaande data in de database blijft ongewijzigd en wordt nog steeds correct weergegeven in het inschrijvingenbeheer. De nieuwe `AttributionHelper::parse()` herkent automatisch beide formaten.

- **Bugfix: Marketing Dashboard geladen zonder Alpine.js**: Het dashboard-scherm bleef vastzitten op de laad-spinner omdat de Backpack CoreUI v4-thema Alpine.js niet laadt. De volledige view is herschreven naar vanilla JavaScript (geen Alpine.js-afhankelijkheid meer). Chart.js wordt nu ingeladen via CDN in de `after_scripts`-stack. De werking is identiek: AJAX-call via de native `fetch()` API, bronfilter via data-attributen, grafieken via Chart.js 4.

## Week van 20–26 april 2026

### ✨ Nieuw & Verbeterd

- **Dashboard globaal zoeken**: Op het beheer-dashboard is een real-time zoekbalk toegevoegd waarmee direct in meerdere objecttypen gezocht kan worden. Resultaten verschijnen terwijl je typt; klikken op een resultaat gaat direct naar de beheerpagina van het object.

  - **Zoekt in**: Cursisten (naam, e-mail), Programma's (code, titel), Cursussen (titel), Inschrijvingen (naam/e-mail cursist én programmacode), Facturen (factuurnummer, Mollie-betalingskenmerk), Pagina's (titel, slug), Collecties, Producten, Locaties, Docenten, Productverkopen (naam cursist), Blog artikelen (titel).
  - Per objecttype worden maximaal **10 meest recent bijgewerkte** resultaten getoond.
  - **Meerdere zoekwoorden**: Bij cursussen en pagina's kunnen meerdere woorden worden ingevoerd (volgorde maakt niet uit) — alle woorden moeten voorkomen in de titel.
  - **Voornaam + achternaam**: Cursisten zijn ook vindbaar door voor- én achternaam te combineren.
  - **Hoofdletterongevoelig**: Zoeken op "jan" vindt ook "Jan" en "JAN".
  - **Alleen objecten waartoe je toegang hebt**: De zoekresultaten houden rekening met je rechten — je ziet alleen objecttypen die je ook in het menu kunt beheren.
  - De zoekbalk staat bovenaan het dashboard, boven de KPI-widgets.


- **CMS contentblokken: configureerbare velden per bloktype**: Aan `ContentBlockType` zijn drie nieuwe vlaggen toegevoegd waarmee per bloktype ingesteld kan worden welke velden beschikbaar zijn bij blokken van dat type.

  - **`has_video`**: Schakel de videolink-invoer (YouTube/Vimeo) in of uit.
  - **`has_text`**: Schakel de rich-text editor (Jodit) in of uit.
  - **`has_order`**: Schakel het volgordeveld in of uit.

  In het beheer (`ContentBlockType`-bewerken) zijn de checkboxes zichtbaar onder "Beschikbare velden voor dit bloktype". In `BlockCrudController` worden de velden conditioneel getoond op basis van het gekoppelde bloktype.

- **CMS contentblokken: configureerbare crop-verhouding voor afbeeldingen**: Per bloktype kan een **afbeeldingverhouding (crop)** worden ingesteld als decimaal getal (bijv. `1.33` voor 4:3, `1.78` voor 16:9, `1` voor vierkant). Wanneer een beheerder een afbeelding selecteert bij een blok, wordt de cropper automatisch ingesteld op deze verhouding. Laat leeg voor vrij bijsnijden.

- **Winkelwagen bericht bij producten**: Aan producten is het veld **"Winkelwagen bericht"** toegevoegd (tabblad "Basis"). Dit bericht wordt getoond in de winkelwagen wanneer het product is toegevoegd, vergelijkbaar met het bestaande winkelwagen bericht bij kortingscodes.

- **Cultuurconnectie: meerdere disciplines per collectie**: Een collectie kan nu aan meerdere Cultuurconnectie disciplines tegelijk worden gekoppeld. De enkelvoudige kolom `cultuurconnectie_discipline_id` is vervangen door een pivot-tabel `collection_discipline`. In het beheer van collecties (tabblad "Marketing") is het veld vervangen door een select2-meervoudige keuzelijst. De synchronisatie van cursussen naar Cultuurconnectie (`CourseObserver`, `cultuurconnectie:sync-courses`) leest de disciplines nu via de nieuwe relatie.

- **Statusmails bij checkout nu volledig werkend**: In het bestelproces worden nu voor alle relevante statussen bevestigingsmails verstuurd naar de deelnemer direct na het indienen van de bestelling.

  - **Wachtlijst-mail (template #1) gekoppeld**: Wanneer een inschrijving de status `wachtlijst` krijgt, ontvangt de deelnemer automatisch de wachtlijst-bevestigingsmail (`App\Mail\Waitinglist`).

  - **Controle-mail (template #32) aangemaakt en gekoppeld**: Bij de status `controle` (bijv. bij gebruik van een kortingscode of voucher die gecontroleerd moet worden) ontvangt de deelnemer nu een bevestigingsmail (`App\Mail\Controle`). De mail legt uit dat de inschrijving is ontvangen maar nog gecontroleerd wordt. Migratie `2026_04_21_000001_seed_emailtemplate_controle.php` voegt het template toe.

- **Aparte koper-bevestigingsmail (template #33)**: Na betaalbevestiging via Mollie (of bij gratis/volledig-gekorteerde bestellingen) ontvangt de **koper** voortaan een eigen overzichtsmail (`App\Mail\SendBuyerConfirmation`) in plaats van dezelfde mail als de deelnemer.

  - De koper-mail toont een volledige tabel met alle inschrijvingen (cursus, startdatum, deelnemer, status, bedrag), alle producten en het totaalbedrag van de bestelling.
  - Statuslabels worden leesbaar weergegeven: "Geplaatst", "Intakegesprek vereist", "Wachtlijst", "In controle".
  - De mail wordt nog steeds slechts één keer verstuurd per bestelling (bewaakt door `order.confirmed_at`).
  - Deelnemers die niet de koper zijn ontvangen nog steeds de individuele `SendConfirmation`-mail (template #2).
  - Migratie `2026_04_21_000002_seed_emailtemplate_buyer_confirmation.php` voegt het template toe.

- **Productbestelling verwerkt-mail (template #34)**: Wanneer een productverkoop in het beheer op "Verwerkt" wordt gezet, ontvangt de gekoppelde student automatisch een bevestigingsmail (`App\Mail\ProductProcessed`). De mail meldt dat de bestelling is verwerkt. Bij terugzetten naar "Betaald" wordt geen mail verstuurd. Migratie `2026_04_21_000003_seed_emailtemplate_product_processed.php` voegt het template toe.

- **Uitnodigingen ook verstuurd aan studenten met toekomstige inschrijving**: De beperking waarbij `vu:dailymails` uitnodigingen oversloeg voor studenten die al een actieve inschrijving in de toekomst hebben, is verwijderd. Uitnodigingen worden nu altijd verstuurd als aan de overige voorwaarden is voldaan.

- **Winkelwagen-teller correct bij gecached menu**: Het menu wordt gecacht maar hierdoor stond het aantal artikelen in de winkelwagen-badge bij ingelogde of terugkerende bezoekers soms op nul. De badge wordt nu bij elke paginalading dynamisch bijgewerkt via een lichtgewicht API-aanroep (`GET /cart/count`). Van toepassing op alle thema's: Utrecht, Breda, Demo, Amsterdam en Westvoorne.

- **Mobiel submenu Utrecht: koppeling navigatie en uitklappen gesplitst**: In het mobiele menu van het Utrecht-thema was klikken op een menu-item met submenu geblokkeerd door `e.preventDefault()`, waardoor de link nooit volgde. Er is nu een aparte `<button class="submenu-toggle">`-knop naast elk menu-item met submenu geplaatst. Klikken op de link navigeert naar de pagina; klikken op de knop klapt het submenu open of dicht met een slide-animatie. De pijl-indicator (chevron) is verplaatst naar de nieuwe knop en draait mee bij openen.

- **Inactieve docenten uitgesloten van docentenrapportage**: In het rapport "Docentgegevens" en de bijbehorende filterdropdown werden eerder ook inactieve docenten meegenomen. Het filter en de export-query zijn aangepast zodat alleen docenten met `actief = ja` worden opgenomen.

- **Productverkopen-beheer verbeterd**:
  - De preview-knop (Show) is verwijderd uit de lijst.
  - De kolom "Aangemaakt" is verwijderd uit de lijst.
  - Kolomselectie en exportknoppen (CSV/Excel/PDF) toegevoegd aan de lijstweergave.

### 🐛 Bugfixes

- **Typefout in `SendBuyerConfirmation` en `ProductProcessed` opgelost**: De mailables `App\Mail\SendBuyerConfirmation` en `App\Mail\ProductProcessed` declareerden properties met een expliciet type (`string`, modelklasse), wat conflicteert met de untypede declaraties in Laravel's `Mailable`-basisklasse. Alle property-typedeclaraties zijn verwijderd en de ontbrekende `Queueable` en `SerializesModels` traits zijn toegevoegd, in lijn met alle andere mailables in het project.

- **"Alle cursussen"-link rechts uitgelijnd (Amsterdam, collectie-overzichtspagina)**: De link "Alle cursussen in de categorie …" onderaan een subcollectieblok werd links weergegeven. De link is nu rechts uitgelijnd via Bootstrap `text-end`.

---

## Week van 13–19 april 2026

### 🐛 Bugfixes

- **Null-fout bij cursuspagina opgelost (Breda)**: Wanneer een programma geen locatie had gekoppeld, crashte de cursuspagina met de melding "Attempt to read property 'title' on null". Dit is opgelost door nullsafe operators te gebruiken voor de locatievelden.

- **Null-fout bij orderhistorie opgelost**: In het beheerscherm van studenten kon een fout optreden ("Call to a member function max() on null") bij het weergeven van de inschrijvingshistorie. Dit trad op wanneer een programma geen lesdagen had. Opgelost met nullsafe operators.

### ✨ Verbeterd

- **Programma automatisch gesloten na twee weken zonder sluitingsdatum**: Wanneer er geen sluitingsdatum is ingesteld voor een programma, wordt de status automatisch op "gesloten" gezet als de eerste lesdag meer dan twee weken geleden was. Dit voorkomt dat verlopen programma's zonder sluitingsdatum open blijven staan.

- **Dashboard-melding voor programma's zonder lesdagen**: De dagelijkse cleanup-taak controleert nu of toekomstige programma's geen lesdagen hebben. Als dat het geval is, verschijnt er een melding op het dashboard met een directe link naar het programma.

## Week van 6–12 april 2026

### ✨ Nieuw & Verbeterd

- **🔗 Cultuurconnectie (CursusPro) integratie**: Cursussen worden nu automatisch gesynchroniseerd met de CursusPro API (`https://api.volksuniversiteit.nl/`) van Cultuurconnectie. De integratie is alleen actief wanneer `CC_KEY` is ingesteld in `.env`.

  - **Disciplines lokaal opgeslagen**: Disciplines en subdisciplines worden opgehaald via de API en lokaal opgeslagen. Dit hoeft slechts eenmalig uitgevoerd te worden en kan daarna herhaald worden wanneer Cultuurconnectie nieuwe disciplines toevoegt.

  - **Discipline-koppeling op collecties**: Per collectie kan in het beheer (tabblad "Marketing") een Cultuurconnectie-discipline worden geselecteerd. De disciplines zijn gegroepeerd als "Parentnaam — Subnaam".

  - **Automatische sync via observer**: Bij het aanmaken, bewerken of verwijderen van een cursus in het beheer wordt automatisch de juiste API-aanroep gedaan. De disciplines worden afgeleid van de collecties waaraan de cursus gekoppeld is. Het Cultuurconnectie-ID wordt opgeslagen en is zichtbaar (read-only) in het beheer onder het tabblad "Marketing".

  - **Handmatige bulksync**: Alle bestaande cursussen kunnen in één keer worden gesynchroniseerd via een beheerdersopdracht. Er is ook een optie om reeds gesynchroniseerde cursussen opnieuw te versturen.

  - **SEO Zoekwoorden**: Aan cursussen is het veld **"SEO Zoekwoorden"** toegevoegd (tabblad "Marketing"). De waarde wordt als `zoekwoorden` meegestuurd bij elke synchronisatie naar Cultuurconnectie.

- **🔍 Zoekwoorden meegenomen in cursuszoekfunctie**: Bij het zoeken op de cursuspagina worden de SEO Zoekwoorden van een cursus nu ook doorzocht, naast de titel, tekst en programmacode.

### 🐛 Bugfixes

- **Fout in cursusfilter opgelost (Breda)**: Bij het gebruik van het dagfilter in het cursusoverzicht kon een foutmelding optreden. Dit is verholpen.

- **Moodle-synchronisatie: opnieuw ingeschreven deelnemers worden niet meer uitgeschreven**: Bij de Moodle-synchronisatie kon het voorkomen dat een deelnemer die zich had afgemeld en daarna opnieuw had ingeschreven, alsnog werd uitgeschreven. De sync controleert nu eerst of er een actieve inschrijving bestaat voor dezelfde cursus; zo ja, wordt de uitschrijving overgeslagen.

- **Fout bij aanmaken nieuwe student opgelost**: Het aanmaakscherm voor studenten in het beheer gaf een fout. Dit is verholpen.

### ✨ Verbeterd

- **Rapportage Omzet Boekjaar: ook gestopte deelnemers meegeteld**: Deelnemers met de status "gestopt" worden nu meegenomen in de omzetberekening. Voorheen telden zij niet mee, waardoor de omzet in de rapportage te laag uitkwam.

- **Tweestapsverificatie: apparaat onthouden**: Na het invoeren van de verificatiecode kan een gebruiker aanvinken "Onthoud dit apparaat (7 dagen)". Het apparaat wordt dan 7 dagen onthouden en de code wordt niet opnieuw gevraagd. Bij elke login wordt de 7 dagen automatisch verlengd. Na 7 dagen zonder gebruik vervalt het apparaat vanzelf.

- **Tweestapsverificatie: vertrouwde apparaten beheren**: In de gebruikersinstellingen is een overzicht toegevoegd van alle apparaten waarvoor de code onthouden is. Per apparaat zijn de naam (browser + besturingssysteem), het IP-adres, de datum van laatste gebruik en het aantal resterende dagen zichtbaar. Apparaten kunnen handmatig worden verwijderd.

- **Beheertabblad "SEO" hernoemd naar "Marketing"**: Het tabblad "SEO" in het beheer van cursussen, collecties, pagina's, blogberichten en docenten heet voortaan **"Marketing"**. Alle bestaande velden staan op dezelfde plek, alleen de naam is gewijzigd.

- **Extra marketinglabel voor cursussen**: Het veld voor een extra label bij een cursus (bijv. "i.s.m. Het Filmhuis") is verplaatst naar het tabblad "Marketing" en heet nu **"Extra marketinglabel"**.

- **Marketingnotitie voor cursussen**: Aan cursussen is het veld **"Marketingnotitie"** toegevoegd in het tabblad "Marketing". Dit is een intern tekstveld dat niet op de website wordt getoond en bedoeld is voor aantekeningen voor het marketingteam.

---

## Week van 30 maart – 5 april 2026

### ✨ Nieuw & Verbeterd

- **� E-mailopt-out gerespecteerd bij evaluaties**: Studenten met `no_email = true` worden nu op alle drie niveaus overgeslagen: bij het aanmaken van evaluatieresponses (`vu:generateevaluations`), bij het versturen van uitnodigingen (`vu:mailevaluations`) en bij het versturen van herinneringen (`vu:evaluationreminders`). Bij de mail- en herinneringstap wordt de response direct als verzonden gemarkeerd zodat ze niet opnieuw worden opgepikt.

- **�🚫 Cursus-uitsluiting voor evaluatieformulieren**: In het beheer van evaluatieformulieren (tabblad "Verzending") is een nieuw veld **"Uitgesloten cursussen"** toegevoegd. Hiermee kunnen specifieke cursussen worden uitgezonderd van evaluatiegeneratie. De uitsluiting geldt ook wanneer "Versturen naar alle cursussen" actief is. De koppeling wordt opgeslagen in de nieuwe `evaluation_course_exclusion`-pivot-tabel. De `vu:generateevaluations`-opdracht filtert programma's van uitgesloten cursussen automatisch weg vóór het aanmaken van evaluatieresponses.

---

## Week van 23-29 maart 2026

### ✨ Nieuw & Verbeterd

- **🔁 Lokale opslag aanmaken van orderitems bij stap 2 (Amsterdam)**: Bij het opnieuw indienen van stap 2 (deelnemersgegevens) worden bestaande `OrderItem`- en `ProductSale`-records nu bijgewerkt in plaats van opnieuw aangemaakt. Hiervoor zijn twee nullable kolommen toegevoegd aan `cart_items`: `orderitem_id` en `product_sale_id`. Bij de eerste indiening worden de ID's opgeslagen op het cart-item; bij herindienen worden de bestaande records bijgewerkt met de nieuwe deelnemersgegevens, status, prijs, korting en bedrijfsgegevens. Dit voorkomt dubbele inschrijvingen bij terugnavigatie. De deelnemersformulieren in stap 2 worden voortaan voorgevuld met de eerder opgeslagen deelnemergegevens.

- **🔍 Docentenzoekfunctie op de docenten-pagina (Amsterdam)**: Op pagina's met het type `teacher` in het CMS verschijnt nu een zoekveld boven het docentenrooster. Zoeken filtert op voor- en achternaam. De zoekterm wordt bewaard in het invoerveld na verzending. De bestaande `PageController` ondersteunde `?q=` al; alleen de include-template is uitgebreid.

- **🔍 Docentenzoekfunctie op de losse docenten-indexpagina (Amsterdam)**: Hetzelfde zoekveld is toegevoegd aan `teacher_index.blade.php` voor sites die `/docent` via de `TeacherController` serveren in plaats van via een CMS-pagina.

- **🧾 Productfacturen verwerkt door de factuurverzendopdracht**: De `vu:invoices`-opdracht sloeg facturen met alleen een `product_sale_id` (en geen `orderitem_id`) over. De query is aangepast om facturen te includeren die een orderitem *of* een product sale hebben. `processSingleInvoice` en `processCombinedInvoices` zijn uitgebreid om productfacturen correct te verwerken: geen orderitem-check, geen lectionsdatumcontrole, betaler wordt opgehaald via `productSale->student`.

- **🧾 Stap 3 in het checkout-proces: besteloverzicht vóór betaling (Amsterdam)**: Tussen het invullen van de deelnemersgegevens (stap 2) en de Mollie-betaling is een nieuw betalingsoverzicht toegevoegd (`/order/{ordernr}/overview`). De pagina toont per inschrijving en product: afbeelding, titel, prijs, cursusCode + startdatum, type, locatie en deelnemer. Elk item krijgt een gekleurde badge die het betaalmoment aangeeft: **Betaling: Direct** (plaatsingsinstelling = direct of programma is final), **Betaling: Na bevestiging startdatum** (plaatsingsinstelling ≠ direct), **Betaling: Na intake** (cursus vereist intake/approval), of **Betaling: Na controle korting** (kortingspas met `requires_approval`). Rechts staat een totaalblok met splitsing *Nu te betalen* / *Later te betalen*. Als de betaler een bedrijfsnaam heeft opgegeven in stap 1, verschijnt er bovenaan de rechterkolom een extra blok voor een optionele referentie en een PO-nummer/inkoopnummer. Deze gegevens worden opgeslagen op de order en doorgezet naar alle orderitems.

- **🔀 Mollie-initiatie verplaatst van stap 2 naar stap 3**: De orderitems worden nog steeds aangemaakt na stap 2 (inclusief statusbepaling, intake-mails en admin-remarknotificatie), maar de redirect naar Mollie, de bankoverschrijving-afhandeling en het no-payment-pad zijn verplaatst naar de POST van het nieuwe overzichtsscherm. Het Mollie-bedrag wordt opnieuw berekend op basis van de reeds aangemaakte orderitems, zodat het bedrag op het overzicht exact overeenkomt met wat Mollie in rekening brengt.

- **🛡️ Overzichtsroutes alleen actief in de nieuwe flow**: De routes `GET|POST /order/{id}/overview` zijn geregistreerd in de vaste `OrderControllerNew`-routegroep, niet in de dynamische groep die op andere sites de oude `OrderController` gebruikt. De oude betaalflow blijft daardoor volledig ongewijzigd.

### 🐛 Bugfixes

- **🖼️ Ontbrekende `product_index`-view toegevoegd (Amsterdam)**: De pagina `/producten` op de Amsterdam-site brak met een "View [product_index] not found"-fout omdat er in geen enkel thema een `product_index.blade.php` bestond. Het bestand is aangemaakt voor het Amsterdam-thema met standaard zoek-/sorteerformulier, productkaarten (afbeelding, titel, intro, prijs) en de gebruikelijke layout-componenten (`<x-head>`, `<x-header>`, `<x-footer>`, `<x-pagefooter>`). Variabelen `$products`, `$collections`, `$element` en `$searchterm` worden volledig ondersteund.

- **🔢 "Non-numeric value encountered" in collectiefilter (Utrecht)**: De template `collection_filter.blade.php` van het Utrecht-thema berekende de dagnaaam met `$dutchDays[$val - 1]`, wat een PHP-waarschuwing (gedegradeerd tot exception) opleverde zodra `startday` of `startmonth` een niet-numerieke URL-parameter bevatte (bijv. van een crawler of misgevormde link). De berekening is vervangen door directe opzoektabel-lookups op de al meegegeven `$days`- en `$months`-props met een `(int)`-cast als veiligheidsnet: `$days[(int)$val] ?? $val`.

---

## Week van 16-22 maart 2026

### ✨ Nieuw & Verbeterd

- **🎯 Kortingsvoorwaarden op basis van deelnemersgegevens**: Bij een korting kunnen nu één of meer voorwaarden worden ingesteld op velden van de deelnemer (bijv. woonplaats, postcode, geslacht). Elke voorwaarde bestaat uit een veldkeuze, een vergelijkingstype ("is exact" of "bevat") en een waarde. Alle voorwaarden moeten gelden (AND-logica). Vergelijkingen zijn hoofdletterongevoelig. De instelling staat in het tabblad "Toepassing" van het kortingsbeheer.

- **👤 Kortingsberekening op de deelnemer, niet de betaler**: Bij het toepassen van een vouchercode of kortingspas in de checkout wordt de korting voortaan gevalideerd op de persoon die daadwerkelijk deelneemt, niet op de persoon die betaalt. Als een deelnemer is opgegeven via een uitnodigings-e-mailadres maar niet als cursist in het systeem bestaat, kan de korting niet worden toegepast. Er is geen terugval op de betaler.

- **🗑️ Ongebruikt veld `remark` verwijderd uit deelnemerstabel**: Het kolom `remark` in de `students`-tabel (toegevoegd december 2023) had geen enkel gebruik in de applicatie. Het veld is verwijderd via een migratie. Het actieve notitieveld is `remarks`.

- **🛍️ Upsell producten in de winkelwagen (Amsterdam)**: In het rechterkolom van de winkelwagenpagina (`/cart`) verschijnt nu een apart blok "Direct meebestellen" als er actieve producten zijn gekoppeld aan de cursussen in de winkelwagen (via de `course_product`-koppeltabel). Producten die al in de winkelwagen zitten worden niet nogmaals getoond. Het blok heeft dezelfde stijl als het winkelwagenoverzicht en toont per product de naam, prijs en een `+`-knop. Klikken op de knop voegt het product direct toe aan de winkelwagen en keert terug naar de winkelwagenpagina. Eerder ingevulde formuliervelden worden via `sessionStorage` bewaard zodat de gebruiker niet opnieuw hoeft te beginnen.

- **📄 Gecombineerde factuur-PDF voor multi-product bestellingen**: Bij bestellingen via de nieuwe checkout waarbij meerdere cursussen of producten in één Mollie-betaling zijn afgerekend, ontvangen deelnemers nu één gecombineerde factuur-PDF in plaats van losse mails per factuur. De `vu:invoices`-opdracht groepeert openstaande facturen op `mollie_id`: bij één factuur verloopt het proces zoals voorheen; bij meerdere facturen worden alle regels in één PDF gezet (`invoice_combined.blade.php`) en in één e-mail verstuurd. Om een race condition te vermijden waarbij de webhook nog bezig is facturen aan te maken, worden groepen met een factuur jonger dan 5 minuten overgeslagen tot de volgende ronde.

- **🔢 Factuurnummering bij gecombineerde facturen**: Facturen binnen een gecombineerde betaling krijgen nu een gedeeld basisnummer met volgnummer-suffix (bijv. `20260322-000023-1`, `-2`, `-3`). Het basisnummer is het nummer van de eerste factuur, aangemaakt door de webhook.

- **📬 Gecombineerde en losse facturen verstuurd naar de betaler**: Alle factuurmails (enkelvoudig en gecombineerd) worden nu verstuurd naar de betaler van de order — de persoon die de bestelling heeft geplaatst — in plaats van de eerste deelnemer. Terugval op de deelnemer of de factuurstudent blijft behouden voor oudere records zonder `order_id`.

- **👁️ Kolom "Contact" in factuuroverzicht toont de betaler**: In het beheeroverzicht van facturen is de kolom "Student" hernoemd naar "Contact" en toont nu de betaler van de order (met directe link naar de cursistenpagina) in plaats van de deelnemer. Zoeken werkt eveneens op de naam van de betaler.

- **🔒 Deelnemer-velden op inschrijving worden live geladen uit de studentenrecord**: In het beheerscherm van `Inschrijvingen` worden de velden Deelnemer, E-mailadres en Telefoonnummer nu altijd live ingeladen uit het gekoppelde `Student`-model en zijn ze alleen-lezen. Wijzigingen in het studentprofiel zijn daardoor direct zichtbaar. De naamkolom bevat een linkknop naar de cursistenpagina. Voor achterwaartse compatibiliteit wordt teruggevallen op de opgeslagen veldwaarden als er geen `student_id` is.

- **⚡ Accessors voor `student_name`, `student_email`, `student_phone1` op OrderItem**: De drie gedenormaliseerde velden op het `OrderItem`-model zijn omgezet naar accessors die altijd de live waarde uit de `Student`-relatie teruggeven. Alle consumers — exports, console-opdrachten, bladetemplates — profiteren hiervan automatisch zonder codewijzigingen. Terugval op de opgeslagen kolomwaarde blijft behouden voor legacy-records.

- **👤 Factuuradres op naam van de betaler**: Het factuuradres in de factuurtemplate (Amsterdam) toont nu de gegevens van de betaler van de order — de persoon die de bestelling heeft geplaatst — in plaats van altijd de cursist. Als betaler en cursist verschillen en er geen bedrijf op de factuur staat, wordt de cursist apart vermeld onder "Cursist". Zo klopt het factuuradres ook bij bedrijfsinschrijvingen of inschrijvingen door derden.

- **👤 Deelnemer zichtbaar op factuurregels**: Elke factuurpost (volledige betaling, deelbetaling en creditnota) toont nu in de omschrijvingscel de naam van de deelnemer/cursist als subtext. Dit maakt het gelijk duidelijk voor wie de inschrijving geldt, ook als de betaler iemand anders is.

- **🎨 Achtergrondafbeelding op certificaten (Amsterdam)**: De certificaattemplate van het Amsterdam-thema gebruikt nu dezelfde techniek als de factuurtemplate: een volledige achtergrondafbeelding (`assets/certificate.png`) wordt ingeladen via absolute positionering zonder paginamarges, en de inhoud staat in een `content`-div met padding.

- **⬜ Certificaatinhoud gecentreerd**: Alle tekst en de handtekening op het certificaat zijn nu horizontaal gecentreerd, inclusief de datum, docentnaam, naam van de directeur en de handtekeningafbeelding.

- **⏰ Achterstallige betalingen in dagelijkse admin mail**: De dagelijkse admin-overzichtsmail bevat nu een sectie met inschrijvingen die ouder zijn dan 6 weken, de status "geplaatst" hebben, en waarbij het betaalmoment op "direct" staat maar het volledige bedrag nog niet ontvangen is. Per regel staan het orderitem-ID (als directe link), de studentnaam, het e-mailadres, de programmacode en het openstaande bedrag — dezelfde logica als de OpenstaandePosten-export.

- **🔀 Admin mail losgekoppeld van dagelijkse mailopdracht**: De verzending van de dagelijkse admin-mail is verplaatst naar een aparte opdracht `vu:adminmail`. Deze draait elke werkdag om 07:30 via de scheduler. De `vu:dailymails`-opdracht verstuurt de admin-mail niet meer.

- **🧪 Dry-run modus voor admin-mail**: Met `php artisan vu:adminmail --dry-run` wordt de volledige inhoud van de admin-mail — inclusief alle databasequery's — afgedrukt in de console zonder dat er een e-mail verstuurd wordt. De weekdag-check wordt tijdens een dry-run overgeslagen zodat het op elk moment getest kan worden.

- **🎨 Admin-mail voorzien van opmaak**: De dagelijkse admin-mail heeft nu een eigen HTML-template (`emails/adminmail.blade.php`) met witte kaart op grijze achtergrond en een subtiele VUAdmin-voettekst — vergelijkbaar met de opmaak van de 2FA-verificatiemail.

- **🔗 Links in admin-mail gebruiken de site-URL**: Alle links in de admin-mail (intake, controle, credit-facturen, teveel betaald, achterstallig) gebruiken nu de URL die in de site-instellingen is geconfigureerd (`$site->url`) als basis. Intake- en controle-vermeldingen hadden voorheen helemaal geen link.

- **📨 Testmodus voor admin-mail**: Met `php artisan vu:adminmail --test` wordt de mail met echte database-inhoud verstuurd naar `info@vuadmin.nl` in plaats van het geconfigureerde admin-adres. De weekdag-check wordt ook hier overgeslagen.

- **💾 Formuliergegevens bewaard bij aanpassen winkelwageninhoud**: Wanneer een gebruiker op de winkelwagenpagina (Amsterdam) op de plus, min of verwijder-knop klikt, worden alle ingevulde contactgegevens nu automatisch opgeslagen in `sessionStorage`. Na de paginaverversing worden de velden hersteld. De opgeslagen gegevens worden gewist zodra het formulier daadwerkelijk verstuurd wordt.

- **🔒 Slug niet meer bewerkbaar in productbeheer**: Het slug-veld is verwijderd uit het productbeheer-formulier. De slug wordt éénmalig automatisch gegenereerd op basis van de titel bij het aanmaken van een product en wordt daarna niet meer overschreven.

### 🐛 Bugfixes

- **🔗 Mollie webhook 500 bij gemengde bestelling (cursus + product)**: Bij bestellingen waarbij zowel een cursus als een product in één Mollie-betaling werden afgerekend, gaf de webhook een 500-fout. Oorzaak: de metadata voor producten miste het veld `'type' => 'product_sale'`, waardoor de webhook het product-ID als cursusinschrijving interpreteerde. Een toevallig overeenkomend record werd op `geplaatst` gezet, wat een bevestigingsmail triggerde die crashte op een ontbrekende cursusrelatie. Opgelost door `'type' => 'product_sale'` toe te voegen aan de metadata van producten in `post_payment`.

- **⏳ Betaalverwerking-overlay bleef staan na succesvolle betaling**: De wacht-overlay op de betalingsbevestigingspagina werd niet verwijderd na een time-out (60 seconden), waardoor het bestellingsoverzicht permanent onzichtbaar was. Opgelost: bij time-out wordt de overlay nu verwijderd zodat de inhoud zichtbaar wordt. Tevens controleert de overlay en het pollingendpoint (`/order/payment-status`) nu ook de status van gekoppelde `ProductSale`-records, zodat combi-bestellingen (cursus + product) ook correct worden afgewacht.

- **💥 `vu:invoices` crashte op null-cursus in bevestigingsmail**: De `vu:invoices`-opdracht zette orderitems op `geplaatst` via `$orderitem->save()`, wat de `booted()`-saving-hook activeerde en een bevestigingsmail probeerde te sturen. Bij items zonder gekoppelde cursus (bijv. gecancelde of verwijderde cursussen) crashte dit op `$course->title`. Opgelost door (1) `saveQuietly()` te gebruiken in `SentInvoices` zodat model-events niet worden getriggerd, en (2) een null-guard toe te voegen op `$orderItem->course` in de `OrderItem::booted()` saving-hook vóór het aanmaken van de bevestigingsmail.

- **🎂 Geboortedatum vooringevuld als 01-01-1970 in betaalformulier**: Op het betaalformulier werd de geboortedatum van een bekende cursist weergegeven als `01-01-1970` wanneer de datum in het systeem `null` was. Opgelost met een `!empty()`-check en `Carbon::parse()`.

- **🐛 Verwijderknop vouchercodes gaf foutmelding**: De verwijderknop in het vouchercode-overzicht bij een korting stuurde het verzoek naar het verkeerde pad (`/admin/...` in plaats van `/management/...`). De URL gebruikt nu de juiste backpack-prefix zodat het verwijderen correct werkt.

### 🎨 Thema (Amsterdam)

- **📐 `small-title` h3 in detailbanner op 1.3rem**: De `h3`-elementen binnen `.details-bnr-content .small-title` (gebruikt op o.a. docent- en blogdetailpagina's) waren te groot door de browser-standaard. Ze worden nu ingesteld op `1.3rem` zonder de overige stijlen van `.small-title` te verstoren.

- **📋 Geordende lijsten gestileerd als ongeordende lijsten in paginainhoud**: In de paginainhoud van het Amsterdam-thema (`workplaces-main`) werden geordende lijsten (`<ol>`) niet dezelfde opmaak meegegeven als ongeordende lijsten. Regelhoogte, letterafstand, links, marges, inspringing en lijststijl zijn nu ook op `ol` van toepassing.

---

## Week van 9-15 maart 2026

### 🛒 Betaalproces

- **🐛 Korting werd op alle items toegepast bij meerdere deelnemers**: Wanneer één deelnemer in een bestelling een vouchercode invulde, werd het kortingsbedrag door een ontwerpfout ook meegenomen voor alle volgende deelnemers in dezelfde bestelling. Het kortingsbedrag wordt nu per orderregel opnieuw ingesteld, zodat een korting alleen geldt voor het item waarvoor deze is ingevoerd.

- **⏳ "Betaling wordt verwerkt"-scherm na Mollie-redirect**: Na terugkeer van de betaalpagina toont de bestellingsbevestiging nu een laadscherm met spinner zolang de Mollie-webhook de betaling nog niet heeft verwerkt. De pagina ververst automatisch zodra de betaalstatus bijgewerkt is. Als dit langer dan 60 seconden duurt, verschijnt een handmatige verversknop.

- **🐛 Groene voucherbevestiging niet altijd zichtbaar**: Het groene blok onder het vouchercodesveld dat aangeeft dat een korting succesvol is toegepast, werd niet getoond wanneer de gebruiker de code voor het eerst invoerde (geen bestaande korting bij paginaladen). Het bevestigingsblok wordt nu altijd in de DOM gerenderd en via JavaScript zichtbaar gemaakt na succesvolle toepassing.

- **👥 Meerdere deelnemers voor dezelfde cursus**: Bij het bestellen van meerdere plekken in dezelfde cursus werd het formulier voor elke deelnemer vooringevuld met de gegevens van de koper. Alleen het eerste deelnemersblok wordt nu vooringevuld; alle volgende blokken starten leeg met een instructietekst zodat de gegevens van de andere deelnemers ingevuld kunnen worden.

- **🏷️ Kortingsregel per item zichtbaar in het betaalformulier**: Het betaalformulier toont nu per besteld item een aparte kortingsregel (in groen) zodra er een vouchercode op dat item is toegepast. De weergave wordt real-time bijgewerkt via JavaScript na het toepassen of verwijderen van een code, zonder dat de pagina hoeft te verversen.

- **📋 Orderregels doorgegeven aan Mollie**: Bij het aanmaken van een iDEAL-betaling worden nu de afzonderlijke bestelregels (cursussen en producten, inclusief kortingen) als `lines`-object meegegeven aan de Mollie API. Zo is in het Mollie-dashboard direct zichtbaar wat er per item betaald is.

- **💶 Nettobedrag na korting in bevestigingsmail en succespagina**: De bevestigingsmail toont nu per cursus en per product de daadwerkelijk betaalde prijs na aftrek van eventuele korting. Op de succespagina wordt bij productverkopen eveneens het nettobedrag getoond in plaats van de originele prijs.


### 🔐 Beveiliging

- **🔑 Tweestapsverificatie (2FA) per beheerder**: Beheerders kunnen nu tweestapsverificatie inschakelen via hun gebruikersprofiel. Wanneer ingeschakeld, ontvangen zij na elke login een eenmalige 6-cijferige code per e-mail die binnen 10 minuten ingevoerd moet worden. De verificatiepagina sluit aan op de stijl van het inlogscherm. Een nieuwe code kan direct aangevraagd worden via de link op de verificatiepagina.

- **🔇 Honey/Recaptcha fouten onderdrukt**: Errors die door het Honey spam-beschermingspakket worden gegenereerd worden niet langer gelogd als systeemfouten.

### 👥 Gebruikersbeheer

- **👤 Uitgebreid gebruikersprofiel via menu**: De "Mijn account" link in de rechterbovenbalk verwijst nu naar het volledige gebruikersbeheer-scherm met rollen en permissies, in plaats van de beperkte standaard Backpack accountpagina.

- **⚙️ Aanpasbaar gebruikersbeheer**: De `UserCrudController` is uitgebreid en overschrijft nu de standaard van het permissie-pakket, zodat extra velden en aanpassingen eenvoudig toegevoegd kunnen worden.

### 🖥️ Admin Schermen

- **🚫 "Opslaan en voorbeeld weergeven" verwijderd**: De onnodige opslaanoptie "Opslaan en voorbeeld weergeven" is verwijderd uit alle beheer-CRUDs.

### ⚙️ Basis Platform Functionaliteiten

- **🎟️ Gebruikslimiet per Vouchercode**: Vouchercodes kunnen nu een maximaal aantal keer instellen dat een code gebruikt mag worden. Bij het genereren van codes is een nieuw veld "Max. gebruik per code" beschikbaar — leeg laten voor onbeperkt gebruik. Codes die hun limiet bereiken worden automatisch als ongeldig beschouwd en zijn niet meer inwisselbaar. In het overzicht van codes is het gebruik zichtbaar als `x / max` (bij een limiet) of rood gemarkeerd wanneer de limiet bereikt is.

### 📊 Rapportages

- **💳 Nieuwe Rapportage: Betaling gegevens Cursusdeelnemers**: Exporteert alle betalingen per student voor programma's waarvan minimaal één les in het opgegeven boekjaar valt — inclusief cursussen die in een ander jaar starten of eindigen. Er wordt geen datumfilter op de betaaldatum toegepast: álle betalingen voor die programma's worden meegenomen. Per betaalregel zijn zichtbaar: Betaal ID, Betaaldatum, Programmacode, Startdatum, Einddatum, Studentnaam, Bedrag incl. BTW, BTW-percentage, Bedrag excl. BTW, Betaalmethode, Omschrijving en Mollie ID.

---

## Week van 2-8 maart 2026

### ⚙️ Basis Platform Functionaliteiten
- **🔔 Directe Meldingen bij Fouten via Slack**: Het systeem stuurt nu automatisch een bericht naar Slack wanneer er een fout of ongewone situatie plaatsvindt op het platform. Zo bent u als beheerder direct op de hoogte, zonder zelf te hoeven controleren.

- **🤖 Bescherming Tegen Bots en AI-Scrapers**: Bekende kwaadaardige bots en AI-scrapers worden nu automatisch geblokkeerd voordat ze de website kunnen belasten. Bij een geblokkeerde toegangspoging ontvangt u een Slack-melding.

- **👨‍🏫 Docent Ontvangt Bericht bij Gestopt Programma**: Wanneer een cursusorder wordt gestopt, krijgt de bijbehorende docent nu automatisch een e-mailmelding. Zo is de docent altijd tijdig op de hoogte en hoeft u dit niet meer handmatig door te geven.

- **💳 Korting als Betaalmethode**: Kortingen kunnen nu worden geconfigureerd als volwaardige betaalmethode. Dit geeft meer flexibiliteit bij het inrichten van promotionele acties. Ook is er een optie toegevoegd om betalingen te synchroniseren met de boekhouding.

- **📧 E-mailvalidatie bij Betaallinks**: Voordat een betaallink wordt verstuurd, controleert het systeem nu of het e-mailadres geldig is. Ongeldige adressen worden apart afgehandeld zodat er geen verloren e-mails zijn.

- **🔒 Betere Controle bij Volle of Gesloten Programma's**: Tijdens het betaalproces wordt nu correct gecontroleerd of een programma inmiddels vol of gesloten is geraakt. Dit voorkomt dat iemand toch kan betalen voor een cursus waar geen plek meer is.

- **📋 Extra Marketinggegevens in Evaluatieresponses**: Bij ingevulde evaluaties worden nu ook extra marketingvelden bijgehouden, zodat u beter kunt analyseren via welk kanaal of welke doelgroep de feedback binnenkomt.

- **🔧 Stabiliteit en Foutafhandeling Verbeterd**: Meerdere fouten zijn opgelost in de dagelijkse processen, de evaluatieformulieren en de verwerking van orders en cursussen. Daarnaast zijn aanvullende fixes doorgevoerd in het nieuwe betaalproces: het systeem werkte niet correct wanneer een winkelwagen uitsluitend producten bevatte (geen cursussen), en de Mollie webhook werd op Amsterdam door een verkeerde controller afgehandeld. Beide problemen zijn opgelost.

- **📨 E-mailsjablonen Gecentraliseerd**: E-mails voor locatielogins zijn samengevoegd in één centraal sjabloon in plaats van losse versies per thema. Dit maakt aanpassingen eenvoudiger en consistenter.

- **🗂️ Admin Menu Opgeschoond**: De "Cache legen" optie is verplaatst naar een logischere plek in het beheermenu.

- **✏️ Teksteditor Volledig Bijgewerkt naar Jodit**: Alle rich-text invoervelden in het beheerpanel gebruiken nu de Jodit-editor met consistente instellingen (hoogte 400px, Nederlandse taal). De laatste drie velden die nog de oude Summernote-editor gebruikten (berichtvelden in cursus-, programma- en studentenbeheer) zijn omgezet. Alle velden gebruiken nu ook de correcte configuratiemethode met vaste hoogte en taalinstellingen.

- **🛒 Producten Verkoopbaar via het Betaalproces (Amsterdam)**: Producten uit de webshop kunnen nu volledig via het nieuwe betaalsysteem worden afgerekend. Bij aankoop worden de gegevens van de deelnemer (naam, e-mail, geslacht) opgevraagd en wordt er een productverkoop-record aangemaakt dat aan de bestelling is gekoppeld. Vouchercodes en kortingspassen worden ook bij producten ondersteund.

- **🧾 Elke Betaling Wordt per Orderregel Vastgelegd**: Iedere Mollie-betaling resulteert nu in een aparte factuurvermelding per orderregel — zowel voor cursussen als voor producten. Zo is exact terug te zien wat er wanneer betaald is, ook bij gespreide betalingen. Dubbele verwerking van dezelfde betaling wordt automatisch voorkomen.

- **✅ Betalingsstatus Automatisch Bijgewerkt per Item**: Zodra een betaling bevestigd is, wordt de status van elke betrokken orderregel of productverkoop automatisch bijgewerkt. Een cursusorder gaat van "open" of "in afwachting van betaling" naar "geplaatst"; een productverkoop krijgt de status "betaald" inclusief tijdstip. De statusupdate werd eerder via een indirecte koppeling gedaan die afhankelijk was van een nog niet uitgevoerde migratie — dit is nu rechtstreeks in de webhook verwerkt zodat het altijd betrouwbaar werkt.

- **🎟️ Voucher & Kortingspas Gebruik Bijgehouden bij Productverkopen**: Na een succesvolle betaling voor een product wordt het gebruik van de ingewisselde vouchercode of kortingspas nu ook correct geregistreerd, net zoals dat al het geval was bij cursusinschrijvingen.

- **🧹 Verouderde Subsidiecontrole Verwijderd**: De hardgecodeerde NT2-subsidiecontrole specifiek voor Utrecht is volledig verwijderd uit het betaalsysteem. Subsidieverwerking verloopt voortaan via de algemene kortings- en betaalmethodenlogica.

- **🧹 Abonnementenlogica Opgeruimd**: Alle resterende code rondom abonnementen is verwijderd uit het nieuwe afrekensysteem. Het systeem is daarmee overzichtelijker en eenvoudiger te onderhouden.

- **🏷️ Pagina Types Systeem Uitgebreid**: Het types-systeem (Instellingen → Types) ondersteunt nu ook pagina's als entiteit. Pagina's kunnen een type krijgen dat hun gedrag of weergave bepaalt. Beschikbare pagina types worden centraal beheerd en zijn direct beschikbaar in de paginabeheerder zonder code-aanpassingen. Standaard meegeleverde types: `checkout_success`, `teacher`, `location`, `faq`.

### 💳 Betaalflow 2.0
> *Betaalflow 2.0 is een generieke module die in elk thema geïmplementeerd kan worden. Voor implementatie op een nieuw thema zijn aanpassingen aan de thema-templates vereist (winkelwagen, betaalformulier en succespagina).*

- **✅ Betaalproces Afronding**: Meerdere verbeteringen aan het nieuwe multi-item betaalproces:
  - Na betaling wordt een gecombineerde bevestigingsmail gestuurd naar de besteller (`SendOrderConfirmation`) met alle cursussen en producten in één overzicht
  - Deelnemers die niet de koper zijn ontvangen een eigen bevestigingsmail per inschrijving
  - Een handmatige herbevestiging is mogelijk per orderregel via de admin
  - De succespagina na betaling is nu een CMS-pagina met type `checkout_success` — het bestellingoverzicht (cursussen, producten, totaalbedrag) wordt automatisch onder de paginatekst getoond
  - Omleiding na betaling gebruikt het `?o=order_{id}` formaat; het oude `?o={nummer}` formaat (Utrecht/andere sites) blijft volledig werken

- **🔐 Bestellingsoverzicht Niet Langer Raadbaar via URL**: De succespagina na betaling toont het bestellingoverzicht nu via het ordernummer in de URL (bijv. `?o=2026-R4VSS-YKUB`) in plaats van het interne database-ID. Zo kan niemand bestellingen van anderen raden door nummers te verhogen.

- **🧾 Factuurgegevens Boven het Bestellingoverzicht**: De succespagina toont nu direct boven de overzichtstabel wie er op de factuur staat — naam, adres, e-mailadres, betaalwijze en orderdatum. Bij bedrijfsfacturering worden ook bedrijfsnaam, contactpersoon, BTW-nummer, kostenplaats en inkoopnummer getoond.

- **🗂️ Één Succespagina voor Alle Ordertypen**: Intake-inschrijvingen, kortingspas-controles en bankoverschrijvingen leiden nu allemaal naar de centrale succespagina met het bestellingoverzicht. De aparte `/intake`, `/controle-korting` en `/factuur` omleidingen zijn vervangen. De statusbadges per orderregel (Bevestigd, Intake vereist, In controle, Wachtlijst) tonen direct de situatie per cursus.

- **🛒 Volle Cursus Stopt Betaalproces Niet Meer bij Gemengde Bestellingen**: Een volle of gesloten cursus zorgde eerder voor een onmiddellijke redirect die de rest van de winkelwagen negeerde. Nu worden alle items doorverwerkt: de volle cursus krijgt de status `wachtlijst` of `seintje` en de andere items worden gewoon afgerekend. Intake-, controle-, wachtlijst- en seintje-items worden automatisch uitgesloten van het te betalen bedrag.

- **💡 Totaal Betaald Stond Altijd op € 0,00**: Op de succespagina toonde het "Totaal betaald" altijd nul. De oorzaak was dat `Order::invoices()` zocht naar een `order_id` kolom in de factuurentabel, maar facturen worden opgeslagen met `orderitem_id` of `product_sale_id`. De relatie is gecorrigeerd en het totaal telt nu correct op via beide koppelingen.

- **🍞 Breadcrumb Winkelwagen Volledige Breedte**: De breadcrumb bovenaan de winkelwagenpagina was ingesloten in de flexibele lay-out van het formulier. Deze staat nu in een eigen volbrede sectie, gelijk aan alle andere pagina's.

- **📬 Verlaten Winkelmand E-mail ook bij Gestrand bij Mollie**: Winkelwagens met status `payment` — bezoeker bereikte Mollie maar voltooide de betaling niet — worden nu ook meegenomen in de verlaten winkelmand mailing, naast de gewone actieve winkelmanden.

- **🔐 Brute-force Beveiliging op Bestellingsoverzicht**: De succespagina na betaling is beveiligd met een rate limiter. Per IP-adres zijn maximaal 10 verzoeken per minuut toegestaan. Wie dit overschrijdt krijgt een foutmelding. Zo kan niemand snel meerdere ordernummers uitproberen om andermans bestellingen in te zien.

### 📊 Rapportages

- **📈 Nieuwe Rapportage: Omzet Boekjaar**: Er is een nieuwe rapportage beschikbaar: **Omzet Boekjaar**. Deze toont per programma de omzet die toegerekend kan worden aan een opgegeven boekjaar. Per cursusregel zijn zichtbaar: programmacode, cursusnaam, kostenplaats, doorgaan-status, startdatum, startjaar, prijs, BTW-percentage, prijs excl. BTW, totaal aantal lessen, aantal lessen in het boekjaar, aantal geplaatste deelnemers, totale omzet incl. en excl. BTW (inclusief open saldo's), en de specifiek aan het boekjaar toegerekende omzet excl. BTW op basis van de lessenverhouding (totale omzet excl. BTW ÷ totaal lessen × lessen in boekjaar).

- **📅 Nieuw Filtertype: Boekjaar**: In het rapportagesysteem is een nieuw filtertype toegevoegd: **Boekjaar**. Rapporten die dit filter gebruiken tonen een keuzelijst met jaren (huidig jaar +1 t/m 6 jaar terug), standaard ingesteld op vorig jaar. Intern worden de van/tot-datums automatisch afgeleid (1 januari – 31 december van het gekozen jaar), zodat u niet zelf datums hoeft in te vullen. Het gekozen boekjaar is terugzichtbaar in de rapportagehistorie.

- **📐 Nieuwe Rapportage: DCU Boekjaar**: Er is een nieuwe rapportage beschikbaar: **DCU Boekjaar** (Docent Contact Uren). Deze berekent per programma het aantal DCU's voor een opgegeven boekjaar. Een DCU is gedefinieerd als: *aantal lessen × lesduur in decimale uren × geplaatste deelnemers*. De lesduur wordt per les berekend op basis van de start- en eindtijd, zodat wisselende leslengtes correct worden meegenomen. Alleen lessen die letterlijk binnen het kalenderjaar vallen tellen mee. Per programmaregel zijn zichtbaar: Cursuscode, Interne Categorie (kostenplaats), DCU binnen het boekjaar, DCU in het jaar ervoor, DCU in het jaar erna, en de startdatum van het programma (kan een eerder jaar zijn).

- **💳 Nieuwe Rapportage: Betaling gegevens Cursusdeelnemers**: Er is een nieuwe rapportage beschikbaar: **Betaling gegevens Cursusdeelnemers**. Deze exporteert alle betalingen per student voor programma's waarvan minimaal één les in het opgegeven boekjaar valt — inclusief cursussen die in een ander jaar starten of eindigen. Er wordt geen datumfilter op de betaaldatum toegepast: álle betalingen voor die programma's worden meegenomen. Per betaalregel zijn zichtbaar: Betaal ID, Betaaldatum, Programmacode, Startdatum, Einddatum, Studentnaam, Bedrag incl. BTW, BTW-percentage, Bedrag excl. BTW, Betaalmethode, Omschrijving en Mollie ID.

### 🎨 Theme Updates
- **Amsterdam Theme**:
  - Online aanbod slider heeft een verbeterde indeling en weergave gekregen
  - Statusknop verwijderd van cursusblokken voor een cleaner overzicht
  - Linkopmaak binnen titels gecorrigeerd zodat stijlen consistent zijn
  - Type-tags in het cursusoverzicht zijn nu klikbare links die direct filteren op dat type
  - E-mailfooter bijgewerkt met de juiste naam en huisstijl
  - Winkelwagen, cursuspagina, betalingsformulier en studentlogin verfijnd
  - **🛒 Deelnemersformulier Hersteld**: In het betalingsformulier werden de deelnemersvelden voor cursussen niet correct omsloten door een blok met titel. De omsluitende `checkout-block` met cursusnaam ontbrak waardoor de invoervelden los werden weergegeven. Dit is opgelost.
  - **📄 Pagina Types: Docenten, Locaties & FAQ als CMS-pagina**: Het is nu mogelijk om bestaande CMS-pagina's het type "Docenten overzicht", "Locaties overzicht" of "FAQ overzicht" te geven. Het bijbehorende overzicht wordt dan automatisch **onder de paginatekst** weergegeven. Dit maakt het mogelijk dezelfde pagina's op meerdere plekken te hergebruiken en de introductietekst zelf te beheren in het CMS — zonder aparte routes of vaste slugs.
    - Nieuwe partials aangemaakt: `themes/amsterdam/includes/teacher_index.blade.php`, `location_index.blade.php`, `faq_index.blade.php`
    - De hardgecodeerde slug-checks (`$page->slug == "docent"` / `"locatie"`) zijn verwijderd
    - "Populaire cursussen" blok onderaan wordt niet getoond op overzichtspagina's (teacher/location/faq)
    - Pagina types worden beheerd via Instellingen → Types (entity: Pagina) — migratie voegt `teacher`, `location` en `faq` toe
  - **🔍 Complete SEO & Social Media Optimalisatie**: Het thema heeft nu uitgebreide ondersteuning voor Open Graph, Twitter Cards en gestructureerde data (schema.org):
    - **Open Graph Meta Tags**: Links gedeeld op Facebook, LinkedIn en andere platforms tonen nu rijke previews met afbeelding, titel en beschrijving
    - **Twitter Card Meta Tags**: Optimale weergave bij delen op Twitter/X met grote afbeeldingen
    - **Canonical URLs**: Voorkomt duplicate content problemen bij zoekmachines
    - **Article Meta Tags**: Publicatie- en wijzigingsdatums voor blogartikelen voor betere indexering
    - **Theme Color**: Branded browserkleuren op mobiele apparaten
    - **Gestructureerde Data (JSON-LD)**: Rich snippets voor cursussen, producten en artikelen in Google zoekresultaten:
      - Cursuspagina's tonen prijs, provider en beschrijving direct in zoekresultaten
      - Productpagina's kunnen als productkaarten verschijnen met prijsinformatie
      - Blogartikelen tonen auteur, publicatiedatum en afbeelding in zoekresultaten
    - Alle tags zijn dynamisch en gebruiken database-waarden voor maximale flexibiliteit
  - **🎬 Banner Slider Loading Verbeterd**: De homepage banner slider toont nu alleen de eerste afbeelding tijdens het laden, waardoor er geen flits meer is van alle afbeeldingen tegelijk voordat JavaScript actief wordt. Dit zorgt voor een professionelere en rustiger laadervaring. De eerste afbeelding wordt met hoge prioriteit geladen voor optimale LCP (Largest Contentful Paint), terwijl volgende slides lui worden geladen voor snellere initiële laadtijd
  - **⚡ Slimme Lazy Loading voor Cursussliders**: Cursusafbeeldingen in sliders werden nu intelligent geladen - alleen de eerste 4 zichtbare items (afhankelijk van schermgrootte) laden direct, de rest wordt lui geladen wanneer de gebruiker gaat scrollen. Dit versnelt de initiële pagina-laadtijd aanzienlijk zonder de gebruikerservaring te beïnvloeden
  - **🔒 Null Safety Verbeterd**: Collecties die niet bestaan zorgen niet meer voor errors op de homepage - sliders worden gewoon overgeslagen als de collectie niet gevonden kan worden
  - **♿ Toegankelijkheid Sterk Verbeterd (WCAG 2.1)**:
    - **Viewport Zoomen**: Viewport meta tag aangepast om 5x zoomen toe te staan voor gebruikers met slechtziendheid (was user-scalable=no)
    - **Touch Targets Vergroot**: Alle interactieve elementen voldoen nu aan de minimum 48x48px richtlijn voor mobiele apparaten (slider knoppen 44→48px, zoekicoon 31→48px, button padding 12→14px)
    - **Semantische HTML**: <main> landmark toegevoegd aan homepage voor betere navigatie met screenreaders
    - **Aria-labels Toegevoegd**: Alle slider navigatieknoppen, social media links en zoekiconen hebben nu beschrijvende labels voor screenreaders
    - **Formulierlabels Gekoppeld**: Nieuwsbrief en programma selectie formulieren hebben nu correct gekoppelde labels (for/id attributen)
    - **Contrast Verbeterd**: Breadcrumbs en button kleuren aangepast voor WCAG 4.5:1 contrast ratio (breadcrumb opacity 0.6→0.7, btn-sky-link #2c86a3→#267a94)
    - **Font Awesome Zelf Gehost**: Font Awesome icons nu lokaal gehost om third-party cookies te vermijden en GDPR compliance te verbeteren
  - **✨ Hover Zoom Effecten**: Elegante 10% zoom animatie toegevoegd aan afbeeldingen bij hover over cursusblokken, nieuwsitems, waarom-ons blokken, trainingsruimtes en aanbiedingen voor een modernere en interactievere uitstraling
  - **🎯 Slider Performance Optimalisatie**: 
    - Alle sliders beperkt tot maximaal 12 items voor betere mobiele performance en snellere laadtijden
    - Sliders respecteren nu de volgorde zoals ingesteld in de collectie-instellingen in het admin panel (gebruikt `courseItems` relatie met `collection_items.order` sortering)
    - Toegepast op: online-cursussen, cursussen-op-locatie, tips-en-inspiratie, populaire-cursussen sliders op homepage en pagina's

### 🚀 Performance & Caching
- **♻️ Automatische Cache-Busting**: Alle CSS en JavaScript bestanden worden nu automatisch voorzien van een versienummer vanuit het VERSION bestand. Dit betekent:
  - Browsers laden altijd de nieuwste versie van styling en scripts bij een update
  - Geen handmatige `?v=X` parameters meer nodig in templates
  - Optimale caching: 1 jaar cache voor static assets met automatische vernieuwing bij updates
  - Wijzig simpelweg het VERSION bestand en alle assets worden ververst in één keer
  - Implementatie in alle themes: Amsterdam, Utrecht, Breda, Demo en Westvoorne
- **🎯 Nginx Caching Optimalisatie**: Aanbevelingen voor geoptimaliseerde nginx configuratie met:
  - Gzip compressie voor snellere downloads (tekst, CSS, JS, fonts, SVG)
  - Lange cache headers voor static assets (1 jaar voor afbeeldingen, CSS, JS, fonts)
  - Security headers toegevoegd (Referrer-Policy, Permissions-Policy)
  - FastCGI buffer optimalisatie voor betere PHP-FPM performance

---

## Week van 23 februari - 1 maart 2026

### ⚙️ Basis Platform Functionaliteiten
- **🔑 Studenten Kunnen Zelf Wachtwoord Wijzigen**: Cursisten kunnen nu vanuit hun eigen dashboard hun wachtwoord aanpassen. Geen omweg via de beheerder meer — snel, zelfstandig en veilig.

- **⏰ Herinneringsmails voor Evaluaties**: Als een cursist een evaluatie nog niet heeft ingevuld, kan het systeem nu automatisch een herinneringsmail sturen. U stelt zelf in wanneer de herinnering verstuurd wordt en welke tekst erin staat. Zo vergroot u de kans op een volledige respons zonder handmatig na te moeten bellen.

- **🎨 Contentblokken Uitgebreid met Feature Opties**: Per type contentblok kunt u nu instellen welke onderdelen actief zijn — denk aan het al dan niet tonen van een afbeelding, knop, titel of achtergrondkleur. Dit geeft veel meer vrijheid bij het opmaken van pagina's zonder dat u de structuur kwijtraakt.

- **🌈 Achtergrondkleur per Contentblok**: Elk contentblok op een pagina kan nu een eigen achtergrondkleur krijgen. U kiest de kleur zelf via een kleurcode, zodat uw pagina's visueel afwisselender en merkconsistenter worden.

- **❓ FAQ's Koppelen aan Pagina's**: U kunt nu vanuit een pagina direct verwijzen naar een set veelgestelde vragen. Ideaal om informatieve pagina's te verrijken zonder de inhoud dubbel bij te houden.

- **📝 Rijkere Tekstopmaak in Blokken**: De tekstmogelijkheden binnen contentblokken zijn uitgebreid. U heeft meer controle over hoe tekst wordt weergegeven binnen een blok, voor een professionelere en consistentere pagina-opmaak.

- **📋 Documentatie E-mail Sjabloon Variabelen**: Er is een overzichtsdocument toegevoegd met alle beschikbare variabelen voor gebruik in e-mailsjablonen. Handig als naslagwerk bij het opstellen van gepersonaliseerde e-mails.

- **💳 Betaalmethoden Verfijnd**: Betaalmethoden die alleen intern bedoeld zijn worden nu apart gemarkeerd en zijn niet langer zichtbaar als keuze in het orderoverzicht. Dit voorkomt verwarring bij het verwerken van bestellingen.

- **🎟️ Voucher Bijgehouden per Orderregel**: De gebruikte vouchercode wordt nu ook op regelniveau opgeslagen bij een bestelling, zodat u achteraf precies kunt zien welke code bij welk product of welke cursus is ingezet.

- **📦 Volgorde van Contentblokken Instelbaar**: Contentblokken op pagina's kunnen een vaste volgorde krijgen met automatische standaardsortering.

- **🔧 Evaluatie Verwijderknop Slimmer**: De verwijderknop bij een evaluatie verschijnt nu alleen als verwijderen daadwerkelijk mogelijk is. Zo voorkomt u per ongeluk klikken op een knop die toch niets doet.

### 🎨 Theme Updates
- **Amsterdam Theme**:
  - Pagina's tonen achtergrondkleuren en opmaakopties van contentblokken correct
  - FAQ-sectie kan nu worden opgenomen op pagina's en de homepage
  - CTA-blokken hebben een verfijnde indeling gekregen voor een betere visuele balans
  - Mega menu reageert soepeler op hover en klikken
  - Aanbiedingen-sectie heeft CSS-verbeteringen gekregen
  - Footer bijgewerkt
  - Overbodige producttag verwijderd van de productpagina

- **Amsterdam, Breda, Utrecht, Westvoorne & Demo Themes**:
  - Wachtwoord wijzigen beschikbaar voor studenten via het persoonlijke dashboard

---

## Week van 16-22 februari 2026

### ⚙️ Basis Platform Functionaliteiten
- **🃏 Kortingspas (Loyalty Card)**: Een gloednieuwe kortingspas-functie! U kunt nu loyaliteitskaarten aanmaken en koppelen aan kortingsacties. Klanten met een geldige pas krijgen automatisch korting bij het afrekenen — zonder codes of extra stappen. Alle gebruik wordt per bestelling bijgehouden voor een volledig overzicht.

- **📊 Dashboard Uitgebreid met Programma KPI's**: Naast de evaluatiecijfers toont het beheerdashboard nu ook een overzicht van uw programma's: bezettingsgraad, capaciteit en trends van de afgelopen drie maanden — direct zichtbaar zodra u inlogt.

- **📈 Evaluatie KPI Dashboard**: De evaluatiewidget toont de belangrijkste beoordelingscijfers van uw cursussen in één oogopslag, inclusief een grafiek voor snelle inzichten.

- **📊 Evaluatie Export naar Excel**: Ingevulde evaluaties kunnen nu als rapport worden geëxporteerd. Marketingvragen verschijnen als aparte kolommen, zodat u gericht kunt analyseren wat cursisten vonden.

- **✉️ Evaluatie E-mails Automatisch Verstuurd**: Het systeem verstuurt automatisch evaluatie-uitnodigingen naar cursisten op het juiste moment en houdt bij wanneer een e-mail is verstuurd. Zo verstuurt u nooit dubbel.

- **👁️ Evaluatie Voorbeeldweergave voor Beheerders**: U kunt een evaluatie previeuwen precies zoals een cursist die ziet — inclusief de bedanktpagina — voordat u hem verstuurt.

- **💬 Kortingsbericht Zichtbaar bij Betaling**: Wanneer een klant een voucher of kortingspas gebruikt, wordt het bijbehorende bericht duidelijk getoond op de betalingspagina.

- **🔗 Korting Bijgehouden per Bestelling**: Per orderregel wordt vastgelegd welke korting er is toegepast. Dit maakt rapportage en inzicht in kortingsgebruik een stuk nauwkeuriger.

- **🔄 Programma Status Automatisch Berekend**: De status van een programma (actief, vol, afgelopen, etc.) wordt automatisch bepaald op basis van actuele gegevens — consistent door het hele systeem.

- **📋 Evaluatieresponses Overzichtelijker**: Het responsoverzicht toont nu de volledige antwoordtekst per vraag voor een duidelijker beeld van ingevulde feedback.

- **🔒 Evaluaties Beveiligd tegen Verwijderen**: Een evaluatie met bestaande reacties kan niet meer worden verwijderd. Zo raakt u nooit ingevulde feedback kwijt.

- **🌐 Pagina Ondertitel Vertaalbaar**: De ondertitel van een pagina kan nu ook in meerdere talen worden aangeboden.

- **🔍 Zoeken op Pagina's Verbeterd**: Zoeken op paginatitel en URL in het beheer werkt nu ongeacht hoofdlettergebruik.

- **🗂️ Admin Menu Opgeschoond**: De labels en structuur van het beheermenu zijn verduidelijkt voor een overzichtelijker navigatie.

- **🔧 Bugfixes**:
  - Verlaten-winkelwagen e-mails verstuurden soms een foutieve link — opgelost
  - Docentfacturen exporteerden cursustitels niet in het Nederlands — gecorrigeerd
  - Gerelateerde cursussen worden nu altijd in het Nederlands getoond, ook bij meertalige instellingen
  - Winkelwagen status wordt correct bijgewerkt na een betalingsbevestiging
  - Betalingsformulier gebruikt nu altijd de juiste winkelwagen bij een lopende betaling
  - Favorieten verwijderen vereist nu dat de bezoeker ingelogd is

### 🎨 Theme Updates
- **Amsterdam Theme**:
  - Cursusblokken tonen de vertaalde cursustitels correct
  - Gerelateerde cursussen op de cursuspagina worden altijd in het Nederlands getoond
  - Evaluatieformulier en bedanktpagina ondersteunen de nieuwe preview-functionaliteit
  - Kortingsbericht zichtbaar op de betalingspagina bij gebruik van een voucher of pas

- **Breda, Utrecht & Westvoorne Themes**:
  - Evaluatieformulier en bedanktpagina ondersteunen de nieuwe preview-functionaliteit

- **Alle Themes**:
  - Zijbalk navigatie heeft een consistente opmaak gekregen in het admin panel

---

## Week van 9-15 februari 2026

### ⚙️ Basis Platform Functionaliteiten
- **🌐 Pagina's in Meerdere Talen**: U kunt nu al uw pagina's in meerdere talen aanbieden. Beheerders zien in het admin panel direct per veld of er een vertaling beschikbaar is, en bezoekers zien automatisch de pagina in hun eigen taal. Een bugfix zorgde er ook voor dat de vertaalweergave correct werkt na opslaan.

- **🔒 Beheer van Vertalingen Afgeschermd**: Het beheren van vertalingen is nu een aparte bevoegdheid. Alleen medewerkers met de juiste rechten kunnen vertalingen aanpassen voor cursussen, programma's en pagina's. Zo houdt u controle over wie wat mag wijzigen.

- **🌍 Taalinstelling Consistent Door Hele Website**: De taalverwerking werkt nu overal hetzelfde — of een bezoeker nu een cursuspagina, programma of gewone pagina bekijkt. Geen wisselende taalinstellingen meer per pagina.

- **🗑️ Vertalingen Eenvoudiger Verwijderen**: De knop voor het verwijderen van een vertaling werkt nu duidelijker: u krijgt directe bevestiging en wordt automatisch teruggestuurd naar de juiste pagina.

- **📋 Programmaoverzicht Gesorteerd op Datum**: Programma's worden nu automatisch getoond van vroeg naar laat op basis van startdatum, zodat het actuele aanbod altijd bovenaan staat.

- **✏️ Teksteditor Verbeterd**: De teksteditor heeft een extra knop gekregen waarmee u in één klik alle opmaak kunt verwijderen uit geselecteerde tekst. Ook is het vertaalsymbool (🌐) verplaatst naar de labels bij elk veld, zodat u direct ziet welke velden vertaalbaar zijn.

- **⭐ Meer Mogelijkheden voor Evaluatievragen**: Naast de bestaande vraagtypen kunt u nu ook schaalscore-vragen (bijv. 1 t/m 10) en sterrenwaarderingen toevoegen aan evaluaties. Zo verzamelt u op een laagdrempelige manier nuttige feedback van cursisten.

- **🏷️ Evaluaties Indelen in Types**: U kunt evaluaties nu categoriseren per type, zodat u verschillende soorten evaluaties kunt onderscheiden en makkelijker kunt terugvinden in het overzicht.

- **🛡️ Evaluaties Beter Beveiligd**: Een evaluatie waarop al reacties zijn binnengekomen kan niet meer per ongeluk worden verwijderd. Zo gaan ingevulde gegevens nooit verloren.

- **💬 Persoonlijk Bericht bij Kortingsactie**: Bij een korting kunt u nu een eigen tekst instellen die bezoekers te zien krijgen op het moment dat de korting wordt toegepast in het betalingsformulier. Handig om de actie extra te duiden of te bedanken.

- **🎟️ Slimmere Kortingsacties**: Kortingen hebben twee nieuwe opties gekregen: automatisch inschrijven (de klant wordt direct aangemeld zonder extra stappen) en direct naar betaling (de klant gaat meteen naar het betalingsscherm). Dit maakt promotionele acties veel soepeler.

- **🔗 Cursus-Collectie Overzicht**: Vanuit de beheerpagina van een cursus kunt u nu direct zien in welke collecties die cursus voorkomt — en dit ook beheren. Alle bestaande koppelingen zijn automatisch overgezet naar het nieuwe systeem.

### 🎨 Theme Updates
- **Amsterdam Theme**:
  - **Nieuw Mega Menu**: Het navigatiemenu in de header is volledig vernieuwd met een uitgebreid mega menu. De stijl, indeling en het gedrag zijn zorgvuldig afgestemd voor een prettige gebruikerservaring, inclusief een eigen opmaak voor het eerste menu-item.
  - **Betere Terugkeerervaring bij Seintje & Wachtlijst**: Na het invullen van een seintje- of wachtlijstformulier keert de bezoeker nu automatisch terug naar de juiste cursuspagina.
  - **Sortering in Collecties**: Bezoekers kunnen collecties nu sorteren op relevantie, datum of populariteit — zowel op de overzichtspagina als op de detailpagina van een collectie.
  - **Aankomende Cursussen Altijd Gevuld**: De sectie "aankomende cursussen" toont altijd minimaal 4 cursussen, zodat er nooit een lege of schaarse weergave is.
  - **Dynamisch Product Type Label**: In de winkelwagen en op productoverzichten wordt nu het echte producttype getoond in plaats van een vaste tekst.
  - **Taalwisselaar op Pagina's**: Bezoekers kunnen nu ook op gewone pagina's wisselen van taal, mits er een vertaling beschikbaar is.
  - Kortingsbericht zichtbaar in het betalingsformulier wanneer een voucher wordt toegepast.

- **Amsterdam, Breda, Utrecht & Westvoorne Themes**:
  - Evaluatieformulieren ondersteunen nu schaalscore- en sterrenwaarderingsvragen.

---

## Week van 27 januari - 8 februari 2026

### ⚙️ Basis Platform Functionaliteiten
- **🎟️ Vouchercodes voor Kortingen**: U kunt nu unieke vouchercodes aanmaken en koppelen aan kortingsacties. Bezoekers voeren de code in tijdens het afrekenen en krijgen direct de bijbehorende korting. Alles is zichtbaar in een overzichtelijk beheerpaneel. U kunt kortingen ook beperken tot specifieke cursussen, programma's of collecties voor gerichte acties.

- **🛒 Vouchers Zichtbaar in Winkelwagen**: Wanneer een bezoeker een vouchercode invoert, wordt de korting direct getoond in de winkelwagen én op de betalingspagina. Geen verrassingen achteraf — de klant ziet precies wat hij betaalt.

- **📊 Evaluaties Versturen via E-mail**: Het evaluatiesysteem is uitgebreid met e-mailuitnodigingen. U kunt per evaluatie een eigen e-mailtemplate instellen, waarna uitnodigingen automatisch worden verstuurd op het juiste moment. Cursisten ontvangen een persoonlijke link om de evaluatie anoniem in te vullen. Na het indienen zien ze een bedanktekst die u zelf kunt aanpassen.

- **📋 Evaluatie Responses in Beheer**: Alle ingevulde evaluaties zijn nu terug te vinden in het admin panel, inclusief filtermogelijkheden op programmacode. Zo houdt u eenvoudig overzicht over welke feedback er binnenkomt.

- **📦 Volgorde van Collecties Instelbaar**: Collecties en subcollecties kunnen nu handmatig worden gesorteerd. De ingestelde volgorde is direct zichtbaar op de website.

- **🔢 Maximum Deelnemers per Programma Bewaakt**: Wanneer iemand een cursus aan de winkelwagen toevoegt, controleert het systeem of het maximale aantal deelnemers voor dat programma al bereikt is. Overboeking is daarmee niet meer mogelijk.

- **📧 Melding als Rapport Klaar Is**: Na het genereren van een rapport ontvangt u automatisch een e-mail met een directe downloadlink. U hoeft niet meer handmatig te controleren of het klaar is.

- **📈 Exports Stabieler en Nauwkeuriger**: Alle exports (inschrijvingen, subsidies, daglijsten, facturen, etc.) zijn verbeterd: ze crashen niet meer bij ontbrekende gegevens en tonen cursustitels nu in het Nederlands. Een fout in de daglijst bij verwijderde cursussen is ook opgelost.

- **🏷️ Eén Uniform Typesysteem**: Alle types binnen het platform — cursustypes, locatietypes, contracttypes, kortingstypes, docenttypes en producttypes — zijn samengevoegd in één centraal systeem. Dit maakt beheer overzichtelijker en consistenter.

### 🎨 Theme Updates
- **Amsterdam Theme**:
  - Voucherveld toegevoegd aan winkelwagen en betalingspagina
  - Na het invullen van een seintje- of wachtlijstformulier blijft de bezoeker op dezelfde pagina in plaats van te worden doorgestuurd
  - Navigatiepadjes (breadcrumbs) staan nu op een logischere positie in het bestelproces
  - Formuliervelden hebben een verfijnde stijl gekregen voor een prettiger invulervaring

- **Utrecht Theme**:
  - Evaluatieformulier en bedanktpagina toegevoegd
  - Bezoekers kunnen zich nu ook inschrijven voor een cursus die al gestart is (late inschrijving)
  - NRTO keurmerk logo bijgewerkt naar de nieuwste versie

- **Breda, Amsterdam, Utrecht & Westvoorne Themes**:
  - Gepersonaliseerde bedanktpagina toegevoegd na het invullen van een evaluatie

---

## Week van 26 januari 2026

### ⚙️ Basis Platform Functionaliteiten
- **📜 Certificaat Generatie On-Demand**: Certificaten worden nu pas gegenereerd op het moment dat ze nodig zijn, in plaats van vooraf. Dit bespaart diskruimte en zorgt altijd voor up-to-date certificaten. De oude `certificaten` kolom is verwijderd uit de database voor een schonere structuur.

- **🔐 Planbord Permissies**: Nieuwe permissie toegevoegd voor toegang tot het planbord. Alleen gebruikers met de juiste rechten kunnen nu het planbord bekijken en beheren. Dit verhoogt de veiligheid en controle.

- **🔍 Cursus Zoeken Verbetering**: Zoeken naar cursustitels in het programma beheer is nu case-insensitive (hoofdletter ongevoelig), wat betekent dat u makkelijker kunt vinden wat u zoekt ongeacht hoe u het typt.

### 🎨 Theme Updates
- **Breda Theme**:
  - NRTO keurmerk logo vernieuwd met SVG versie voor scherpere weergave
  - Nieuw menu systeem geïmplementeerd in de header

- **Utrecht Theme**:
  - NRTO keurmerk logo vernieuwd met moderne SVG versie
  - Footer aangepast voor betere visuele balans

- **Demo Theme**:
  - NRTO keurmerk verwijderd uit footer (niet van toepassing op demo)

- **Amsterdam Theme**:
  - **Gesloten Cursussen Weergave**: Speciale weergave voor gesloten cursussen met wachtlijst en waarschuwing formulieren
  - **Inschrijfvarianten UI**: Verbeterde gebruikersinterface voor cursus inschrijfopties met checkout area styling
  - **Dynamische Datums**: Cursus datums worden nu dynamisch weergegeven op basis van de huidige datum
  - Typografische verbeteringen en betere spacing in style.css
  - Head component geoptimaliseerd voor snellere laadtijden

---

## Week van 19-25 januari 2026

### ⚙️ Basis Platform Functionaliteiten
- **🌍 Meertaligheid Cursussen & Programma's**: Een complete vertalingssysteem is geïmplementeerd! U kunt nu cursussen en programma's in meerdere talen aanbieden. Alle velden zoals titel, beschrijving en content zijn vertaalbaar. Het systeem ondersteunt tientallen talen met visuele taalwisseling via vlaggen.

- **🎯 Taalwisseling Frontend**: Bezoekers kunnen op de cursuspagina eenvoudig tussen talen schakelen met één klik. De gekozen taal wordt automatisch opgeslagen en toegepast op de hele site. Dit opent de deur naar internationale cursisten!

- **🛒 Winkelwagen Upgrade - Meerdere Producten**: Het winkelwagen systeem is uitgebreid zodat u nu meerdere exemplaren van hetzelfde product kunt toevoegen. Perfect voor wie meerdere boeken of cursussen tegelijk wil bestellen. De database constraints zijn aangepast voor maximale flexibiliteit.

- **💳 Betalingsformulier Vernieuwing**: Het betalingsformulier heeft een complete redesign gekregen met verbeterde gebruikerservaring. Statspas kortingen zijn verplaatst van stap 1 naar een logischere positie in het proces voor minder verwarring.

- **📜 Certificaat Download Fix**: Certificaten hebben nu cache-busting parameters, wat betekent dat u altijd de meest recente versie downloadt zonder browsercache problemen. Geen verouderde certificaten meer!

- **🔧 Collectie Filter Optimalisatie**: De collectie filters zijn volledig herzien. Query parameters worden nu correct bewaard bij navigatie, checkboxes werken perfect voor single-value filters, en de "500 error" bij lege collecties is opgelost. Filtering is nu razendsnel en foutloos.

- **📦 OrderItem Optimalisatie**: Het `transferred_from` veld wordt nu pas ingesteld wanneer nodig (deferred), wat de performance van grote order imports aanzienlijk verbetert.

- **🎨 Basset Asset Management**: De asset pipeline is geoptimaliseerd voor snellere laadtijden van CSS en JavaScript. Errors in de theme scripts zijn opgelost.

- **📊 Versie Beheer Systeem**: Een automatisch versie bump systeem is geïmplementeerd via GitHub Actions. De versie wordt nu prominent weergegeven in het admin menu en op de login pagina, zodat u altijd weet welke versie u gebruikt.

- **📚 Project Documentatie**: README is volledig bijgewerkt met project-specifieke details, installatiehandleiding en een complete TRANSLATIONS.md gids voor het werken met vertalingen.

### 🎨 Theme Updates
- **Breda Theme**:
  - Nieuw menu systeem geïmplementeerd in de header voor betere navigatie en gebruikerservaring

- **Amsterdam Theme**:
  - Volledig nieuwe betalingsformulier interface met moderne styling
  - Winkelwagen interface aangepast voor meerdere producten van hetzelfde type
  - Statspas korting verwijderd uit checkout stap 1 voor duidelijkere flow
  - Collectie filters volledig herzien met verbeterde UX
  - Avenir lettertype vervangen door DM Sans voor modernere uitstraling en betere leesbaarheid
  - Taalwisseling op cursuspagina's met vlaggen en dropdown menu
  - SVG vlaggen iconen voor alle ondersteunde talen (250+ landen/regio's)
  - Style.css updates voor betere typografie en layout

---

## Week van 6-13 januari 2026

### ⚙️ Basis Platform Functionaliteiten
- **Planbord Optimalisatie**: Het planbord interface is grondig herzien voor een beter overzicht van cursusplanning. U kunt nu sneller en efficiënter uw cursusschema's beheren en direct zien waar er nog ruimte is of waar aanpassingen nodig zijn.

- **Menuitem Beheersysteem**: Het beheersysteem voor menu-items is verfijnd, waardoor u makkelijker en intuïtiever de navigatie van uw website kunt aanpassen en structureren.

- **Admin Panel Verbetering**: Alle gecondenseerde tabellen in het admin panel zijn opnieuw uitgelijnd voor een consistente, overzichtelijke weergave. Dit maakt databeheer aanzienlijk eenvoudiger en foutloze.

- **Performance Optimalisatie**: Onder de motorkap hebben we de code geoptimaliseerd, wat resulteert in snellere laadtijden en een responsiever systeem voor alle gebruikers.

- **Permissie Systeem Upgrade**: Het complete permissie systeem is uitgebreid en verfijnd. Hiermee heeft u nog beter controle over wie toegang heeft tot welke functionaliteiten binnen het platform. Dit zorgt voor verhoogde veiligheid en flexibiliteit in gebruikersbeheer. Voor alle gebruikersrollen zijn de rechten opnieuw geëvalueerd en verbeterd, zodat iedereen precies de toegang heeft die nodig is - niet meer, niet minder.

- **🚀 E-Boekhouden Integratie**: Een complete integratie met E-Boekhouden is geïmplementeerd! Mutaties worden nu automatisch gesynchroniseerd, grootboekrekeningen worden automatisch opgehaald en gekoppeld, en de communicatie met de API is volledig geoptimaliseerd. Dit bespaart u uren administratief werk per week.

- **💳 Betaalmethoden Beheer**: Een gloednieuw beheersysteem voor betaalmethoden is toegevoegd. U kunt nu eenvoudig betaalopties toevoegen, bewerken en beheren vanuit één centraal overzicht.

- **💰 Financiële Nauwkeurigheid**: Alle BTW berekeningen in exports en facturen zijn verbeterd voor 100% nauwkeurigheid. Monetaire waarden worden nu correct afgerond volgens de boekhoudkundige standaarden in alle exports (marktinginschrijvingen, subsidies, deelnemerscursussen).

- **📜 Certificaat Functionaliteit**: Een volledige certificaat module is geïmplementeerd! U kunt nu direct vanuit orderitems certificaten genereren en versturen naar deelnemers. Ook zijn annuleer knoppen toegevoegd voor eenvoudig orderitem beheer.

- **Automatische Programma Files**: De generatie van programma bestanden is geoptimaliseerd en werkt nu volledig automatisch op basis van uw cursusgegevens.

- **📋 Vragenlijst Systeem**: Het vragenlijst systeem is volledig herzien met verbeterde afhandeling en een intelligent bezorgsysteem. Vragenlijsten worden nu op het juiste moment naar de juiste deelnemers gestuurd. Uitgebreide tracking functionaliteit toegevoegd zodat u precies kunt zien welke vragenlijsten zijn verstuurd, geopend en ingevuld. Dit maakt gerichte opvolging mogelijk.

### 🎨 Theme Updates
- **Utrecht Theme**: De header navigatie is volledig vernieuwd met een modernere look en betere gebruikerservaring. Ook de homepage lay-out is geoptimaliseerd voor een aantrekkelijkere presentatie van uw cursusaanbod.

- **Breda Theme**: De certificaat PDF template is speciaal aangepast met een professionele handtekening afbeelding en huisstijl elementen, klaar voor directe uitgifte aan uw cursisten.

---

## Week van 23 december 2025

### ⚙️ Basis Platform Functionaliteiten
- **Database Optimalisatie**: De collectie datastructuur is fundamenteel verbeterd voor veel flexibeler content management. Dit vormt de basis voor toekomstige uitbreidingen en zorgt voor snellere queries.
- **Data Migratie**: Alle bestaande collectie data is succesvol gemigreerd naar de nieuwe structuur zonder dataverlies.

### 🎨 Theme Updates
- **Breda Theme**: Favicon probleem definitief opgelost - uw logo wordt nu correct weergegeven in alle browsers. Nieuwe, hoogwaardige afbeeldingen toegevoegd voor een professionelere uitstraling. De homepage heeft meerdere lay-out verbeteringen ontvangen voor betere content presentatie en conversie.

---

## Week van 16-20 december 2025

### ⚙️ Basis Platform Functionaliteiten
- **🎁 Kortingssysteem**: Een volledig nieuw kortingssysteem is gelanceerd! U kunt nu eenvoudig promotionele kortingen aanmaken, beheren en koppelen aan specifieke cursussen of categorieën. Kortingscodes worden automatisch gevalideerd tijdens het bestelproces en zijn direct zichtbaar in het winkelwagentje.

- **📦 Collectie Revolution**: Collecties zijn nu veel krachtiger - u kunt producten én cursussen door elkaar heen gebruiken binnen één collectie. Dit geeft u ongekende flexibiliteit in hoe u uw aanbod presenteert. Items kunnen eenvoudig gesorteerd en gerangschikt worden via drag-and-drop.

- **👨‍🏫 Docenten Beheer Pro**:
  - BSN nummers zijn nu opgenomen in docentenrapporten voor correcte administratie
  - Zoeken op docentnaam werkt nu veel beter en sneller
  - Docentinformatie wordt automatisch getoond bij toekomstige cursussen, zodat cursisten direct weten wie hun docent wordt

- **🎨 Kleurcodering Cursussen**: Cursuscategorieën zijn nu visueel te onderscheiden met hex kleurcodes. U bepaalt zelf welke kleuren bij welke categorieën horen. Dit maakt uw cursusaanbod overzichtelijker en aantrekkelijker voor bezoekers.

### 🎨 Theme Updates
- **Amsterdam Theme**: Collectie weergave volledig aangepast voor de nieuwe product integratie
- **Breda Theme**: Homepage geoptimaliseerd voor de nieuwe collectie structuur met verbeterde kaartweergave
- **Utrecht Theme**: Kortingen worden nu prominent getoond in het betalingsformulier

---

## Week van 2-12 december 2025

### ⚙️ Basis Platform Functionaliteiten
- **🛍️ Product Module**: Een complete product module is gelanceerd! U kunt nu naast cursussen ook fysieke of digitale producten verkopen:
  - Volledig product beheersysteem met categorieën en kenmerken
  - Sales tracking om te zien welke producten het beste verkopen
  - Mogelijkheid om meerdere product afbeeldingen te uploaden
  - Volledige integratie in het bestaande winkelwagen systeem
  - Slimme aanbevelingen voor gerelateerde producten om cross-selling te stimuleren

- **📄 Factuur Systeem**: Docent facturen worden nu automatisch gegenereerd met correcte gegevens en BTW berekeningen. Orderitem afhandeling in de backend is gestroomlijnd voor sneller en foutloos werken.

### 🎨 Theme Updates
- **Amsterdam Theme**: Professionele product detailpagina's gecreëerd met foto's, beschrijvingen en koopknoppen. Producten zijn naadloos geïntegreerd in de winkelwagen interface met duidelijke onderscheid tussen cursussen en producten.

---

## Week van 18-30 november 2025

### ⚙️ Basis Platform Functionaliteiten
- **🛒 Winkelwagen Upgrade**:
  - **Database Migratie**: Winkelwagens worden nu opgeslagen in de database i.p.v. browser sessies. Dit betekent dat klanten hun winkelwagen kunnen terugvinden op elk apparaat en nooit meer items kwijtraken.
  - **Verlaten Winkelwagen**: Automatische tracking van verlaten winkelwagens met intelligente herinneringsmails. Dit helpt conversie te verhogen.
  - **Overboeking Bescherming**: Geavanceerd systeem voorkomt dat cursussen overboekt raken - het systeem checkt real-time beschikbaarheid en blokkeert plaatsen tijdens het bestelproces.
  - **Import/Export**: Verbeterde functionaliteit om winkelwagens te importeren en exporteren voor administratieve doeleinden.
  - **Dual Controller**: Orderverwerking is opgesplitst in legacy en nieuw systeem voor een soepele overgang zonder downtime.

- **🎨 Page Builder Pro**:
  - **Video Integratie**: U kunt nu direct video links toevoegen aan content blokken voor rijkere pagina's
  - **Afbeeldingen**: Volledige ondersteuning voor afbeeldingen op custom pagina's met automatische optimalisatie
  - **Locatie & Docenten**: Voeg automatisch locatie informatie en docent profielen toe aan pagina's
  - **Lange Teksten**: Database aangepast om langere tekstblokken te ondersteunen voor uitgebreidere content

- **📚 Collectie Weergave**: De hoofdcollectie pagina toont nu individuele cursussen in plaats van programma's, wat bezoekers direct een beter overzicht geeft van wat ze kunnen boeken. Locaties kunnen nu per stuk getoond of verborgen worden.

### 🎨 Theme Updates
- **Amsterdam Theme**: Uitgebreide pagina header customisatie opties, nieuwe flexibele content blok types, en verbeterde cursus filters voor sneller zoeken
- **Alle Themes**: Overboeking bescherming toegevoegd aan alle course_show pagina's voor consistente gebruikerservaring
- **Breda & Utrecht**: Betalingsdetails worden nu prominenter en duidelijker weergegeven, winkelwagen pagina verfijnd met betere layout

---

## Week van 11-17 november 2025

### ⚙️ Basis Platform Functionaliteiten
- **📝 Sorteerbare Blokken**: Content blokken kunnen nu via drag-and-drop gesorteerd worden voor intuïtieve pagina organisatie. Dit bespaart u veel tijd bij het maken van pagina's.
- **Content Types**: Meerdere nieuwe content blok types beschikbaar (tekst, afbeeldingen, video's, quotes) voor maximale flexibiliteit
- **"Opslaan en Nieuw"**: Deze tijdbesparende functie is toegevoegd aan alle belangrijke beheer secties - perfect wanneer u meerdere items achter elkaar wilt toevoegen
- **Login Design**: Inlogpagina heeft een moderne, professionele update gekregen

### 🎨 Theme Updates
- **Amsterdam Theme**: Homepage review sectie volledig vernieuwd, geavanceerde slider met meerdere afbeeldingen en smooth animaties, "Waarom Ons" sectie toegevoegd voor betere conversie, header geoptimaliseerd voor mobiel

---

## Week van 4-10 november 2025

### ⚙️ Basis Platform Functionaliteiten
- **💳 Betaalproces**: Het complete checkout proces is geoptimaliseerd met een strakke flow en duidelijke stappen. Order betaling tracking is verbeterd zodat u altijd weet wat de status is van elke betaling.

- **🎓 Moodle Integratie**: Directe integratie met het Moodle leerplatform! Na inschrijving krijgen cursisten automatisch toegang tot hun online leeromgeving. Dit is volledig geautomatiseerd en vereist geen handmatige stappen meer.

- **Order Management**: Post-order verwerking is gestroomlijnd en orderbeheer tijdens checkout is uitgebreid met meer opties en overzicht.

### 🎨 Theme Updates
- **Amsterdam Theme**: Betalingsformulier interface volledig herzien voor een moderne, vertrouwenwekkende uitstraling. Winkelwagen index pagina geoptimaliseerd met betere product/cursus weergave.

