# VUAdmin Updates

## Week van 13 tot 19 juli 2026

### ✨ Nieuw & Verbeterd

- **Nieuw rapport "Deelnemersgegevens jaarraport"**: Bij Beheer → Rapporten is een nieuw rapport beschikbaar dat een overzicht geeft van alle unieke deelnemers die in een gekozen jaar minstens één lesdag hebben gehad, met hun contactgegevens (ID, voornaam, achternaam, e-mailadres, telefoonnummer, geboortedatum en plaats). Het rapport is te filteren op jaartal.

- **Cursus-tags — Los invoerveld vervangen door tags met suggesties**: Het veld "SEO Zoekwoorden" bij een cursus (tabblad Marketing) is vervangen door een echt tags-veld. In plaats van los tekst met komma's te typen, voeg je nu tags toe die als los te verwijderen "pilletjes" verschijnen; terwijl je typt worden al bestaande tags gesuggereerd, en een tag die nog niet bestaat wordt automatisch aangemaakt. Bestaande zoekwoorden zijn bij deze update automatisch omgezet naar tags, dus er gaat niets verloren. Tags worden nog altijd op dezelfde manier gebruikt voor de zoekfunctie op de cursuspagina en voor de synchronisatie met Cultuurconnectie.

- **Productverkopen — Prijs automatisch ingesteld bij aanmaken**: Bij het aanmaken van een productverkoop wordt de prijs niet langer handmatig ingevuld, maar automatisch overgenomen van de huidige verkoopprijs van het gekozen product. Het prijsveld op het tabblad "Prijzen" is nu alleen-lezen (en blijft, zoals voorheen, bevroren na aanmaken, ook als de productprijs later verandert). Wil je voor een specifieke verkoop een andere prijs, gebruik dan het kortingsbedrag.

- **Tags uitgebreid naar blogartikelen, webpagina's, producten, collecties en docenten**: Het tags-veld dat eerder al bij cursussen was geïntroduceerd (tabblad Marketing) staat nu ook bij blogartikelen, webpagina's, producten, collecties en docenten. Voeg tags toe door te typen en op Enter of komma te drukken; bestaande tags worden gesuggereerd, een nieuwe tag wordt automatisch aangemaakt. Deze tags zijn bedoeld om content beter te categoriseren en vindbaar te maken.

### 🐛 Bugfixes

- **Inschrijven vanuit het buitenland (Breda & Utrecht)**: Het inschrijfformulier, de cursistgegevens en het "extra gegevens invullen"-formulier bij Breda en Utrecht accepteerden alleen een Nederlands telefoonnummer en een Nederlandse postcode, waardoor cursisten met een buitenlands adres of telefoonnummer zich niet konden inschrijven. Beide thema's hebben nu, net als Amsterdam, een land-keuzeveld (standaard Nederland) en accepteren voortaan ook buitenlandse telefoonnummers en postcodes.

## Week van 6 tot 12 juli 2026

### ✨ Nieuw & Verbeterd

- **Cultuurconnectie — Collectie-URL's koppelen aan disciplines**: Cultuurconnectie ondersteunt sinds kort het koppelen van één externe URL per discipline. Collecties die aan een Cultuurconnectie-discipline zijn gekoppeld, worden nu automatisch met hun collectiepagina-URL doorgestuurd naar Cultuurconnectie, zodat bezoekers vanuit Cultuurconnectie direct op de juiste collectiepagina uitkomen. Wanneer meerdere collecties aan dezelfde discipline gekoppeld zijn, wordt de meest recent bewerkte collectie gebruikt. Koppelingen die niet meer kloppen (bijvoorbeeld omdat een collectie niet meer aan een discipline gekoppeld is) worden automatisch weer verwijderd bij Cultuurconnectie. Deze synchronisatie draait elk uur automatisch, alleen wanneer `CC_KEY` is ingesteld.

- **Opschonen van niet-afgeronde bestellingen**: Inschrijvingen en productverkopen die tijdens het bestelproces zijn aangemaakt maar nooit zijn afgerond (geen betaling, geen bevestiging) blijven eerst nog "open" staan, zodat een klant de winkelwagen later kan hervatten. Blijven ze na 14 dagen nog steeds open en onbetaald, dan worden ze automatisch verwijderd, zodat ze niet langer als ruis in het beheerscherm blijven staan. Inschrijvingen met een lopende factuur (bijv. bedrijfsfacturen die handmatig geplaatst moeten worden, of een reeds verstuurde of gedeeltelijk betaalde factuur) worden nooit verwijderd, en ook lopende termijnen van een terugkerend product (bijv. een maandelijks abonnement) blijven staan totdat ze daadwerkelijk in rekening zijn gebracht. Bestellingen die hierdoor volledig leeg achterblijven, worden ook opgeruimd.

- **Facturen — Statuslabel en filters**: Zowel het factuuroverzicht als het tabblad "Facturen" bij een cursist tonen nu een statuslabel per factuur: "Ingepland" (factuurdatum ligt in de toekomst), "Openstaand" (nog niet betaald), "Herinnerd" (betalingsherinnering verstuurd), "Achterstallig" (herinnering meer dan 2 weken geleden verstuurd) of "Betaald". In het factuuroverzicht is hierop ook gefilterd te worden, naast een nieuw filter om facturen te vinden binnen een bepaalde factuurdatum-periode. Daarnaast toont de kolom "Betaalmethode" nu de ingestelde naam van de betaalmethode in plaats van de interne code, en toont de datumkolom in het tabblad "Facturen" voortaan de factuurdatum in plaats van het aanmaakmoment.

- **Financieel dashboard — Openstaande posten gecorrigeerd, nieuw blok voor openstaande credits**: De telling van "openstaande posten" hield voorheen geen rekening met facturen die pas in de toekomst verstuurd worden, en rekende de ouderdom vanaf de vervaldatum in plaats van de factuurdatum. Dit is gecorrigeerd: een post telt nu mee zodra de factuurdatum is verstreken en er nog niet is betaald, en de leeftijdscategorieën ("Dagen") lopen nu automatisch mee met de ingestelde betalingstermijn en het herinneringsritme (eerste herinnering na de betalingstermijn, tweede herinnering 14 dagen later). Lege categorieën worden niet meer getoond. Er is een nieuw blok "Openstaande Credits" toegevoegd onder de openstaande posten, met dezelfde indeling maar dan voor nog niet uitbetaalde tegoeden. In beide overzichten is het factuurnummer nu klikbaar en opent direct de betreffende factuur. De KPI-tegels bovenaan tonen nu ook "Totaal Open" en "Totaal Credit", berekend op dezelfde manier als de blokken eronder (dus onafhankelijk van de gekozen periode).

- **E-maillog — Filter op e-mailsjabloon**: Het e-maillog is nu te filteren op e-mailsjabloon, met de sjabloonnaam als label. Hiervoor slaan alle systeem-e-mails voortaan ook het gebruikte sjabloon op in het log (voorheen deed alleen een klein deel van de e-mails dit).

- **Account aanmaken zonder bestelling (alle thema's)**: Bezoekers kunnen nu een cursistaccount aanmaken zonder direct een cursus te boeken. Op de inlogpagina staat naast het inlogformulier voortaan ook een registratieformulier (voornaam, achternaam, e-mailadres). Na registratie ontvangt de nieuwe cursist een welkomstmail en een tijdelijke inlogcode waarmee een wachtwoord kan worden ingesteld; daarna kan altijd worden ingelogd om cursussen te bekijken en zich in te schrijven. Waar de nieuwsbriefkoppeling (Mailchimp/MailerLite) is ingesteld, staat er ook een aanmeldvinkje voor de nieuwsbrief bij het registratieformulier.

### 🐛 Bugfixes

- **BTW-rapport — Productverkopen ontbraken**: Het BTW-rapport bouwde de omzet per cursus alleen op uit inschrijvingen; betalingen voor productverkopen werden overgeslagen, waardoor productomzet niet in het rapport verscheen. Het rapport neemt nu ook betaalde productverkopen mee, gegroepeerd per product met het btw-percentage van dat product.

- **Herinnering "cursus start over 1 week" — Verstuurde soms niet**: Deze herinnering werd gekoppeld aan een exacte datum-match, terwijl de onderliggende startdatum van een programma tussentijds kan verschuiven (bijv. door een verplaatste les). Schoof de datum ook maar één dag, dan werd de herinnering voor die groep cursisten stilzwijgend en blijvend overgeslagen. De check is verbreed naar een venster van enkele dagen rond de 1-weekgrens, met een controle op het e-maillog om dubbel versturen te voorkomen.

- **Marketingdashboard — Campagnes en zoektermen gesorteerd op omzet**: De tabellen "Campagnes" en "Zoektermen" waren gesorteerd op aantal conversies. Beide zijn nu gesorteerd op omzet, van hoog naar laag; bij "Zoektermen" is hiervoor ook een omzetkolom toegevoegd.

## Week van 29 juni tot 5 juli 2026

### ✨ Nieuw & Verbeterd

- **GA4 E-commerce tracking (alle thema's)**: Bezoekersgedrag in het afrekenproces wordt nu gedetailleerd bijgehouden via Google Analytics 4. Wanneer GA4 tracking is ingeschakeld via Beheer → Instellingen → Scripts, worden automatisch events verstuurd op het moment dat een bezoeker een cursus- of productpagina bekijkt, een item toevoegt of verwijdert uit de winkelwagen, de winkelwagenpagina bekijkt, stap 2 of stap 3 van het bestelproces doorloopt, en de betaling afrond. Op de bedankpagina wordt een aankoopgebeurtenis geregistreerd met het ordernummer, het totaalbedrag en alle losse artikelen. Elk event wordt maar één keer verstuurd — ook bij een paginaverversing. Beschikbaar voor alle thema's: Amsterdam, Utrecht, Breda, Westvoorne, Gouda en Demo.

- **Standaard sortering cursusoverzicht (alle thema's)**: Nieuwe instelling "Standaard sortering cursusoverzicht" (Beheer → Instellingen → Cursussen) waarmee per site gekozen kan worden welke sortering standaard wordt toegepast op het cursusoverzicht en de collectiepagina's, zolang een bezoeker zelf nog geen sortering heeft gekozen. Beschikbaar voor alle thema's; voor Westvoorne staat deze instelling standaard op "Datum".

- **Bezettingsrapport — Kolom "Doorgang"**: Het bezettingsrapport heeft een nieuwe kolom "Doorgang". Per programma staat hier "ja" als de doorgang definitief is bevestigd, "nee" als het programma is geannuleerd, en "onbepaald" in alle overige gevallen.

- **Collectiepagina — Producten zichtbaar (Amsterdam)**: Producten die aan een hoofdcollectie zijn gekoppeld, worden nu ook getoond op de collectiepagina — na de cursussen, gesorteerd op de ingestelde volgorde.

- **Productverkopen — Zoeken op naam en e-mail**: In het beheerscherm van productverkopen werkt de zoekfunctie nu ook op productnaam, voor- en achternaam van de cursist en diens e-mailadres.

- **E-Boekhouden-synchronisatie — Ook productverkopen**: De dagelijkse synchronisatie van betalingen naar e-Boekhouden (Westvoorne) nam voorheen alleen betaalde cursusinschrijvingen mee. Betaalde productverkopen worden nu op dezelfde manier meegenomen: per grootboek en btw-tarief van het product gegroepeerd en samengevoegd in dezelfde dagomzet-mutatie als de cursusbetalingen. Daarnaast wordt bij het opbouwen van de synchronisatie nu ook de instelling "Synchroniseer naar boekhouding" per betaalmethode gerespecteerd; deze schakelaar was al aanwezig in het beheerscherm van betaalmethoden maar had voorheen geen effect.

- **Kortingscode/-pas — Dubbele toewijzing voorkomen**: Kortingscodes en kortingspassen met een maximaal aantal toepassingen worden nu al geweigerd als het limiet al volledig in gebruik is in andere openstaande winkelwagens. Dit voorkomt dat meer deelnemers dan toegestaan tegelijk met dezelfde code door het bestelproces gaan.

- **E-maillog — Inhoud opgeslagen in database**: De volledige tekst van via het systeem verstuurde e-mails wordt nu opgeslagen in de database, zodat e-mails later zijn in te zien en opnieuw te versturen vanuit het e-maillog.

- **Cursistdashboard — Direct inloggen op leeromgeving (Moodle)**: Bij een inschrijving met een actieve plaatsing verschijnt in het dashboard nu een knop "Naar leeromgeving" zodra de bijbehorende cursus in Moodle beschikbaar is. Dit volgt dezelfde beschikbaarheidsregels als de Moodle-synchronisatie: de knop verschijnt pas als de cursus in Moodle is aangemaakt, zichtbaar is met inhoud, en de cursist een gekoppeld Moodle-account heeft. De cursist wordt via een eenmalige, kortlevende inlogsleutel automatisch ingelogd en direct naar de betreffende cursus gebracht, zonder zelf Moodle-inloggegevens te hoeven invoeren. Mislukt het automatisch inloggen (bijv. door een storing aan Moodle-zijde), dan wordt de cursist teruggevallen op het normale Moodle-inlogscherm voor die cursus, en wordt de fout gelogd voor onderzoek. Beschikbaar voor alle thema's: Amsterdam, Utrecht, Westvoorne, Gouda en Demo.

- **Docentensynchronisatie met Moodle**: Docenten kunnen nu per docent worden aangemeld voor synchronisatie naar de leeromgeving via een nieuwe schakelaar "Synchroniseer naar Moodle" in het beheerscherm (alleen zichtbaar als Moodle is gekoppeld). Voorheen probeerde de synchronisatie bij elke ronde een docent te herkennen op e-mailadres; voor docenten met de schakelaar aan die nog geen Moodle-account hebben, wordt nu automatisch een nieuw account aangemaakt. Docenten die al eerder gekoppeld waren, zijn bij deze update automatisch op "synchroniseren" gezet.

- **Beheerpaneel — Logo compacter in zijbalk**: Het logo bovenin de zijbalk van het beheerpaneel is kleiner gemaakt, zodat het beter past bij de beschikbare ruimte.

### 🐛 Bugfixes

- **Moodle-synchronisatie — Docenten en cursisten steeds opnieuw aangemeld**: Docenten en cursisten die al als docent/cursist aan een cursus gekoppeld waren in Moodle, werden bij elke synchronisatieronde opnieuw aangemeld op die cursus. De synchronisatie controleert nu eerst wie al gekoppeld is aan de Moodle-cursus en slaat die over.

- **Evaluatieformulier — Dubbel cijferveld verwijderd** (Amsterdam, Utrecht, Breda, Westvoorne): Bovenaan het evaluatieformulier stond een extra keuzelijst "Geef een algemeen cijfer (1-10)". Dit veld stond los van de vragen in het formulier en kon overlappen met een vraag die hetzelfde vroeg. Het vaste cijferveld is verwijderd; cijfers worden voortaan uitsluitend via de ingestelde vragen in het formulier gevraagd.

- **Checkout Amsterdam stap 2 — Naam en e-mail van deelnemer verplicht**: De velden voor voornaam, achternaam en e-mailadres van de deelnemer in stap 2 van het bestelproces misten het verplicht-attribuut, waardoor het formulier kon worden ingediend zonder dat de deelnemersgegevens waren ingevuld. Dit is gecorrigeerd.

- **Inschrijvingen — Programma verplicht bij aanmaken en bewerken**: Het veld voor het programma bij het aanmaken of bewerken van een inschrijving in het beheer stond per ongeluk als optioneel ingesteld. Er moet nu altijd een programma worden geselecteerd.

- **Marketing — Zoekterm niet meer gevuld bij Google-omleidingslinks**: Wanneer een bezoeker via een Google-omleidingslink  op de website terechtkwam, werd de volledige omleidings-URL onterecht opgeslagen als zoekwoord in de statistieken. Zoektermen worden nu alleen opgeslagen als de waarde daadwerkelijk een zoekwoord betreft en geen URL is.

- **Productverkopen — Zoeken op naam gaf foutmelding**: De nieuwe zoekfunctie op cursistnaam in het productverkopenoverzicht (zie hierboven) verwees per abuis naar een niet-bestaande kolom `name`, waardoor zoeken een foutmelding gaf. De zoekfunctie gebruikt nu het juiste veld `firstname` en werkt weer correct.

### 🎨 Thema-updates Westvoorne

- **Winkelwagen — Waarschuwing bij bestaand account**: Als een bezoeker bij het afrekenen een e-mailadres invult waarvoor al een cursistaccount bestaat, verschijnt nu een melding met een link om eerst in te loggen. Zo wordt voorkomen dat iemand per ongeluk een dubbele bestelling los van zijn bestaande account plaatst.
- **Cursuspagina — Programma-specifieke prijzen**: De leden- en reguliere prijs op de cursuspagina tonen nu de prijs van het gekozen programma (indien ingesteld), in plaats van altijd de algemene cursusprijs. Zo kunnen programma's binnen dezelfde cursus eigen prijzen hebben.
- **Bestelproces — Ledenkorting direct zichtbaar**: Wanneer het e-mailveld van een deelnemer al vooringevuld is (bijvoorbeeld met het e-mailadres van de besteller), wordt nu direct bij het laden van de pagina gecontroleerd of ledenkorting van toepassing is. Voorheen moest de bezoeker eerst het veld aanklikken en weer verlaten voordat de juiste prijs verscheen.
- **Deelknoppen cursuspagina — Iconen laadden niet**: Op de cursuspagina ontbrak het FontAwesome-stijlbestand in de pagina-header, waardoor de iconen van de deelknoppen (Facebook, WhatsApp, LinkedIn, e-mail) niet zichtbaar waren. Dit is hersteld.
- **Winkelwagen — Losse blok voor direct meebestellen**: De voorgestelde extra producten ("upsell") stonden voorheen tussen het cursusoverzicht in de winkelwagen. Deze staan nu in een eigen, duidelijk herkenbaar blok onder het totaalbedrag, met productfoto, korte omschrijving en prijs. Een klik op de foto of titel opent de productpagina; de knop "+" voegt het product direct toe aan de winkelwagen, zoals voorheen.
- **Homepage — Slider beheerbaar via blokken**: De slider op de homepage was hardcoded en kon alleen door een ontwikkelaar worden aangepast. Deze wordt nu, net als bij Utrecht, opgebouwd uit "hero-banner"-blokken die in het beheer aan de pagina zijn gekoppeld (met afbeelding, titel en optionele knop). De stijl en werking van de slider blijven ongewijzigd; afbeeldingen van niet-actieve slides laden pas kort na het inladen van de pagina, zodat de eerste weergave niet vertraagd wordt.
- **Cursuskaarten — Herbruikbare component**: De cursuskaart is omgezet naar een herbruikbaar component  en wordt nu op dezelfde manier gebruikt op de homepage, het cursusoverzicht en bij "gerelateerde cursussen" op de cursusdetailpagina, net als de productkaart  die al eerder herbruikbaar was gemaakt. Wijzigingen aan de kaartweergave hoeven zo nog maar op één plek te worden doorgevoerd.
- **Cursuskaarten — Knop "Meer info" op gelijke hoogte**: Bij een langere cursustitel (2 regels) werd de kaart hoger dan de kaarten ernaast, waardoor de knop "Meer info" niet meer op één lijn stond binnen dezelfde rij. Titels worden nu begrensd tot maximaal 2 regels en de knop wordt onderaan de kaart uitgelijnd, zodat de knoppen binnen een rij altijd op dezelfde hoogte staan.
- **Cursusoverzicht en collecties — Sorteren op datum**: Aan de sorteeropties op het cursusoverzicht en de collectiepagina's is "Datum" toegevoegd. Cursussen worden dan gesorteerd op de eerstvolgende startdatum van een beschikbaar programma; cursussen zonder (aankomend) programma en producten staan onderaan. Voor Westvoorne staat dit standaard geselecteerd, ook zonder dat een bezoeker zelf een sortering kiest.


### 🎨 Thema-updates Amsterdam

- **GA4 tracking ingebouwd**: Cursuspagina's, productpagina's, winkelwagen, alle stappen van het bestelproces en de bedankpagina sturen nu automatisch GA4 ecommerce events via de dataLayer. In te schakelen via de site-instellingen.
- **Collectiepagina — Producten getoond**: Gekoppelde producten worden nu ook op de hoofd-collectiepagina weergegeven.
- **Evaluatieformulier — Dubbel cijferveld verwijderd**: Zie bugfixes.
- **Checkout stap 2 — Deelnemersvelden verplicht**: Zie bugfixes.

### 🎨 Thema-updates Utrecht, Breda & Westvoorne

- **GA4 tracking ingebouwd**: Winkelwagen, bestelproces, cursus- en productpagina's sturen nu GA4 ecommerce events.
- **Evaluatieformulier — Dubbel cijferveld verwijderd**: Zie bugfixes.

### 🎨 Thema-updates Utrecht

- **Cursistdashboard — Vernieuwde opzet**: Het cursistdashboard is visueel vernieuwd en overzichtelijker gemaakt, vergelijkbaar met de opzet van het Amsterdam-thema. Bovenaan staat nu een gebruikerskaart met avatar, naam en e-mailadres en een directe uitlogknop. De tabbladen "Mijn Gegevens", "Wachtwoord", "Mijn Inschrijvingen", "Mijn Facturen" en "Mijn Favorieten" zijn omgezet naar ruimere, afgeronde tabknoppen in de huisstijlkleur. De inhoud heeft meer witruimte gekregen en de lijsten met inschrijvingen, facturen en favorieten tonen nu gestileerde kaarten met statuslabels in plaats van een kale tabel. Functioneel is er niets veranderd: alle formulieren, de wachtwoordsterkte-indicator en de Moodle-koppeling werken op dezelfde manier als voorheen.

---

## Week van 22 tot 28 juni 2026 

### ✨ Nieuw & Verbeterd

- **Facturen — Drie aparte datumvelden**: Het factuurproces is uitgebreid van één datumveld naar drie: **Factuurdatum** (wanneer de factuur is aangemaakt/verstuurd), **Vervaldatum** (wanneer betaling verwacht wordt) en **Betaaldatum** (wanneer betaling is ontvangen). Dit maakt onderscheid mogelijk tussen wanneer een factuur wordt verstuurd, wanneer de betaaltermijn verloopt en wanneer het geld daadwerkelijk is binnengekomen. Alle bestaande facturen zijn automatisch bijgewerkt: betaalde facturen krijgen `betaaldatum = factuurdatum`, creditfacturen en toekomstige termijnen krijgen `betaaldatum = leeg`.

- **Facturen — Termijnfacturen vooraf aanmaken**: Bij een termbetaling (partpayment > 1) worden alle toekomstige termijnen direct als factuurrecord aangemaakt nadat de eerste termijn is betaald — één maand per termijn. Wanneer een volgende Mollie-betaling binnenkomt wordt het bijbehorende vooraf-aangemaakte record bijgewerkt in plaats van een nieuw record aangemaakt. Dit voorkomt dubbele facturen bij herhaalde termijnbetalingen.

- **Facturen — Verstuurd op (sent_at)**: Er wordt bijgehouden wanneer een factuur-PDF daadwerkelijk per e-mail is verstuurd. Dit is anders dan de factuurdatum: de factuurdatum bepaalt wanneer de factuur verstuurd moet worden; `verstuurd op` registreert het moment dat de e-mail daadwerkelijk is afgegaan. Facturen worden alleen verzonden als ze nog niet verstuurd zijn.

- **Facturen — Overdue herinneringen via factuurcommando**: De overdue-herinnering is verplaatst van de dagelijkse mail naar het `vu:invoices`-commando. Zodra de vervaldatum is verstreken, de factuur al verstuurd is en de betaling nog niet is ontvangen, verstuurt het commando automatisch een herinnering (e-mailsjabloon #6) inclusief de originele factuur-PDF als bijlage en een betaalknop. Er wordt per factuur één herinnering verstuurd (`reminder_sent_at` voorkomt herhaling).

- **Facturen — Handmatig opnieuw versturen**: In de facturen-tab van een inschrijving staat naast de downloadknop een **"Verstuur"-knop** voor facturen die nog niet zijn betaald. Als de factuurdatum al verstreken is wordt de factuur opnieuw verstuurd as-is. Als de factuurdatum nog in de toekomst ligt (vroeg versturen) wordt de factuurdatum naar vandaag verschoven voor het versturen.

- **Facturen — PaymentLink e-mail met PDF**: De betalingslink-e-mail (sjabloon 5, verstuurd bij `payment_moment = plaatsing`) bevat nu de factuur-PDF als bijlage. De PDF wordt direct aangemaakt als die nog niet beschikbaar is, en de factuur wordt meteen als "verstuurd" gemarkeerd zodat het `vu:invoices`-commando deze niet nogmaals verstuurt.

- **Programma bevestigen — Facturen aanmaken bij plaatsing**: Wanneer `betaalmoment = plaatsing` en een programma wordt bevestigd via de knop "Bevestigen", worden factuurrecords aangemaakt voor alle ingeschreven deelnemers. Bij termbetaling worden alle termijnen direct vooraf-aangemaakt met datums één maand per termijn. Daarna wordt de betalingslink-e-mail mét PDF verstuurd.

- **Factuuroverzicht — Nieuwe kolommen**: In de factuurlijst zijn de kolommen **Vervaldatum**, **Betaaldatum** en **Verstuurd op** toegevoegd. Het label "Betaaldatum" (dat voorheen de factuurdatum toonde) heet nu correct **Factuurdatum**.

- **Inschrijvingen — Facturen-tab uitgebreid**: De facturen-tab bij een inschrijving toont nu ook **Vervaldatum**, **Betaaldatum** en **Verstuurd op** per factuur.

- **Factuur bewerken — Alleen betaalgegevens bewerkbaar**: In het bewerkscherm van een factuur zijn alleen **Betaalmethode** en **Betaaldatum** bewerkbaar. Alle overige velden (factuurnummer, factuurdatum, vervaldatum, bedrag) zijn readonly. Gebruik de betaaldatum om handmatig een bankoverschrijving te registreren.

- **Factuur-PDF — Factuurdatum en vervaldatum**: De factuur-PDF toont nu zowel de **Factuurdatum** als de **Vervaldatum** in de header. De "voldaan op"-regel onderaan gebruikt voortaan de werkelijke betaaldatum in plaats van de aanmaakdatum.

- **Financieel dashboard — Openstaande posten op vervaldatum**: De openstaande posten in het financieel dashboard tonen nu alleen facturen die al verstuurd zijn maar nog niet betaald. De aging-buckets zijn gebaseerd op de **vervaldatum** (niet meer op de factuurdatum). Buckets: nog niet vervallen, 0–30 dagen, 30–60 dagen, meer dan 60 dagen.

- **E-boekhouden — Synchronisatie op betaaldatum**: De e-boekhoudensynchronisatie groepeert mutaties nu op **betaaldatum** (wanneer geld is ontvangen) in plaats van op de aanmaakdatum van de factuur. Alleen betaalde facturen (`betaaldatum IS NOT NULL`) worden gesynchroniseerd.

- **Rapportage Betalingen — Kasbasis op betaaldatum**: Het betalingenrapport filtert en sorteert nu op **betaaldatum** (wanneer geld is ontvangen) in plaats van op factuurdatum. Het BTW-rapport blijft op factuurdatum (accrual basis).

- **Kortingspassen — Automatisch factuur bij goedkeuring subsidie**: Wanneer een kortingspas het veld "Maak de korting aan als betaalmethode" ingevuld heeft (bijv. voor U-PAS/gemeentesubsidie), wordt bij het goedkeuren van de kortingspas automatisch een betaalde factuur aangemaakt met betaaldatum = goedkeuringsdatum en betaalmethode = de ingestelde subsidie-methode. De beheerder hoeft dit niet meer handmatig te doen.

- **Programma groepse-mail — Deeloptie docent**: De optie "Geplaatst" in het groeps-e-mailvenster is gesplitst in twee opties: **Geplaatst incl. docent** (standaard, stuurt ook naar de docent) en **Geplaatst excl. docent** (stuurt alleen naar de deelnemers). De optie "Seintje" is verwijderd.

- **Kortingen — Ledenprijs via product (kortingsmodus)**: In het kortingenbeheer is een derde kortingsvorm toegevoegd naast het vaste bedrag en het percentage: de **ledenprijs**. Via het nieuwe keuzeveld "Kortingstype" (radio-knoppen: Vast bedrag / Percentage / Ledenprijs) in het tabblad Financieel kies je per korting welke berekening gebruikt wordt. Bij "Ledenprijs" wordt het kortingsbedrag automatisch berekend als: reguliere prijs − ledenprijs van het programma. Onder het tabblad Toepassing kunnen daarnaast één of meerdere **vereiste producten** worden ingesteld via een multi-select. Dit vereiste-productencheck werkt onafhankelijk van de kortingsmodus: ook een vaste korting of percentage kan worden beperkt tot deelnemers die een bepaald product hebben gekocht. De check werkt op het e-mailadres van de deelnemer (niet de betaler), zodat de korting persoonlijk is. Op sites met niet-unieke e-mailadressen (zoals Westvoorne) wordt de korting alleen toegepast als precies één student met dat e-mailadres het product heeft gekocht; bij meerdere overeenkomsten wordt de korting overgeslagen. De geldigheidsperiode wordt bepaald door de begin- en einddatum van de korting zelf. Hiermee vervangt het kortingenmoduul het voormalige abonnementenmoduul voor locaties die lidmaatschap als product verkopen.

- **Kortingen — Beschikbaarheidsfilter per site instelbaar**: Via de nieuwe instelling **"Beschikbaarheidsfilter standaard aan"** (beheer → Instellingen → Cursussen) kan per site worden ingesteld of het beschikbaarheidsfilter standaard ingeschakeld is op de cursus- en collectiepagina's. Staat de instelling op "Uit", dan worden ook niet-beschikbare cursussen standaard getoond. Standaard staat de instelling op "Aan" (bestaand gedrag voor Amsterdam en Utrecht).

### 🐛 Bugfixes

- **Beveiliging — Persoonsgegevens niet meer zichtbaar voor niet-ingelogde bezoekers**: In stap 1 van de checkout werden de naam, het adres, het telefoonnummer en de geboortedatum van een bestaande cursist automatisch ingevuld zodra iemand een bekend e-mailadres intikte — zonder dat die persoon ingelogd was. Dit is een datalek: onbevoegden konden zo profielgegevens van anderen inzien. Persoonsgegevens worden nu uitsluitend vooringevuld voor ingelogde gebruikers. Geldt voor Amsterdam, Utrecht en Breda.

- **Facturen — Factuurnummer pas bij verzending**: Geplande facturen (toekomstige termijnen) kregen bij aanmaak al een factuurnummer toegewezen. Factuurnummers worden nu pas gegenereerd op het moment dat de factuur daadwerkelijk wordt verstuurd. Zolang een termijnfactuur nog niet verzonden is, heeft deze geen factuurnummer en geen PDF.

- **Checkout — Status "controle" pas na bevestiging in stap 3**: Bij inschrijvingen waarbij een kortingspas of voucher met goedkeuringsvereiste werd gebruikt, stond de status van de inschrijving al op "controle" zodra stap 2 (deelnemersgegevens) was ingevuld — nog vóór de bestelling definitief werd afgerond. Dit is hersteld: de inschrijving blijft op "open" staan totdat de bestelling in stap 3 daadwerkelijk wordt bevestigd. Pas op het moment van definitieve afronding wordt de status "controle" toegekend.

- **Rapportages — Docentgegevens: kolom Functie toegevoegd**: Het docentgegevensrapport bevatte geen kolom voor de functietitel van de docent, terwijl dit veld wel wordt bijgehouden. De kolom "Functie" is toegevoegd, direct na de naamvelden.

- **Kortingen — Cursusselectie toont alle cursussen**: In het kortingenbeheer werden niet alle cursussen getoond in de cursusselectie. De lijst was beperkt tot 500 cursussen en de sortering werkte niet correct door de meertalige opzet van cursustitels. Alle cursussen worden nu getoond, gesorteerd op naam.

- **Annuleringscredits — Correcte datum en zichtbaarheid**: Creditnota's bij annulering kregen voorheen een factuurdatum +1 jaar in de toekomst (een tijdelijke oplossing om te voorkomen dat ze meegerekend werden als betaald). Nu krijgt een creditnota factuurdatum = vandaag en betaaldatum = leeg. De berekening van "betaald" werkt op `betaaldatum IS NOT NULL`, waardoor de truc niet meer nodig is. Cursisten zien de creditnota direct op hun dashboard.

- **Betaald-berekening — Consequent op betaaldatum**: Alle berekeningen van "betaald bedrag" (in inschrijvingen, factuurmodel, rapportages en missingdata-commando) gebruiken nu consequent `betaaldatum IS NOT NULL` in plaats van `factuurdatum <= vandaag`. Hierdoor tellen vooraf-aangemaakte toekomstige termijnen en openstaande creditnota's niet meer mee als betaald.

- **Checkout — Ongeldige kortingscode blokkeert betaling**: Als een kortingscode of pasnummer is ingevoerd maar nog niet is gevalideerd (het groene vinkje is niet zichtbaar), kan de checkout niet worden voortgezet. Er verschijnt een foutmelding "Controleer de code voordat u verdergaat." Dit geldt voor Utrecht, Breda en Amsterdam. Een leeg veld blokkeert de checkout niet.

- **Rapportages — Dagplanning: cursuscode, locatiespelling en lesvorm**: In het Dagplanningrapport zijn drie verbeteringen doorgevoerd: de kolom "Lokatie" heet nu "Locatie" (met een C), de kolom "Cursuscode" toont voortaan de echte cursuscode in plaats van een intern ID, en er is een nieuwe kolom "Lesvorm" toegevoegd die aangeeft of een les online, hybride of offline plaatsvindt.

- **Statistieken — UTM-tracking strenger**: De UTM-velden "term" en "content" worden voortaan alleen opgeslagen wanneer ze expliciet als zodanig in de link zijn meegegeven. Links afkomstig van Mailchimp worden niet langer automatisch gevuld met interne Mailchimp-trackingwaarden. Daarnaast wordt "term" niet meer opgeslagen wanneer de waarde identiek is aan de campagnenaam — wat bij Meta/Instagram-advertenties standaard het geval was. Alle UTM-waarden worden afgekapt op maximaal 150 tekens.

- **Exportrapport Kortingen — Pasnummers volledig zichtbaar**: Lange pasnummers (zoals stadspasnummers van 19 cijfers) werden in Excel en Google Sheets afgerond of in wetenschappelijke notatie weergegeven, waardoor het originele nummer niet meer te herstellen was. Pasnummers worden nu altijd als tekst opgeslagen in het exportbestand, zodat het volledige nummer zichtbaar en kopieerbaar blijft.

### 🎨 Thema-updates Amsterdam, Utrecht & Breda

- **Checkout stap 1 — Nieuwe volgorde contactgegevens**: De volgorde en indeling van de contactgegevensvelden in stap 1 van het bestelproces is aangepast voor Amsterdam, Utrecht en Breda. De velden staan nu in de volgende volgorde: e-mail, dan aanhef/voornaam/achternaam naast elkaar, straatnaam + huisnummer naast plaatsnaam, land naast postcode (Amsterdam) of postcode op een aparte rij (Utrecht/Breda), telefoonnummer, en tot slot de drie geboortedatumvelden. Het adres staat daarmee niet langer in een apart blok.

- **Checkout Amsterdam — Stijl keuzelijsten**: De keuzelijsten voor geboortedag, geboortemaand, geboortejaar en land hadden een andere stijl dan de overige keuzelijsten in het formulier. Ze zien er nu hetzelfde uit als de aanhef-keuzelijst.

### 🎨 Thema-updates Breda

- **Checkout — Migratie naar nieuw bestelproces (3 stappen)**: Het Breda-thema is overgezet naar het nieuwe bestelproces, gelijk aan Amsterdam en Utrecht. De checkout bestaat nu uit drie stappen: (1) persoonsgegevens inclusief optionele bedrijfsfacturatie, (2) deelnemersgegevens per cursusitem met kortingscode/Breda Pas-invoer en live validatie, (3) bestellingsoverzicht met betaalstatussen, kortingen en bedrijfsfactuurgegevens. De "Breda Pas"-korting werkt via het algemene vouchersysteem in stap 2.

- **Succespagina — Bestellingsoverzicht na betaling**: Na een succesvolle betaling toont de succespagina van Breda nu een volledig bestellingsoverzicht: inschrijvingen met status en eventuele korting, factuurgegevens en het totaalbedrag. Bij een nog lopende betaling wordt de pagina automatisch ververst totdat de status bekend is.

### 🎨 Thema-updates Westvoorne

- **Checkout — Migratie naar nieuw bestelproces (3 stappen)**: Het Westvoorne-thema is overgezet naar de nieuwe `OrderControllerNew`. De checkout bestaat nu uit drie stappen: (1) persoonsgegevens met lidmaatschapsnummer-validatie en e-mailcheck via `/api/check-email-id`, (2) deelnemersgegevens per item met automatische kortingstoepassing (ledenprijs wordt hier berekend en getoond als groene melding), (3) bestellingsoverzicht. Westvoorne is hiermee de laatste live-site die is overgezet van het oude bestelproces.

- **Betaalmoment "plaatsing" — Bevestiging zonder directe betaling**: Westvoorne gebruikt `payment_moment = plaatsing`. Inschrijvingen krijgen direct de status "geplaatst"; er wordt geen Mollie-betaling aangemaakt. De bevestigingsknop in stap 3 heet "BEVESTIG INSCHRIJVING". Facturen worden aangemaakt zodra de beheerder het programma bevestigt.

- **Overzichtspagina (stap 3) — Nieuw bestand**: Een nieuwe `order_overview.blade.php` is aangemaakt voor stap 3 in Westvoorne-stijl. Toont een twee-kolomlayout met items links en een sticky prijsoverzicht rechts. Betaalstatussen worden weergegeven als gekleurde badges; bij `geplaatst` verschijnt "Betaling bij doorgang activiteit". De algemene voorwaarden-checkbox staat in de linkerkolom.

- **Productpagina — Nieuw bestand**: Een nieuwe `product_index.blade.php` is aangemaakt met zoekbalk, kaartweergave per product (afbeelding, titel, intro, prijs, "Meer info"-link) en ondersteuning voor de `?q=`-zoekparameter.

- **Cursusoverzicht — Beschikbaarheidsfilter standaard uit**: Op de cursus- en collectiepagina's van Westvoorne staat het beschikbaarheidsfilter standaard uitgeschakeld. Alle cursussen worden getoond, ook niet-beschikbare. Beheer → Instellingen → Cursussen → "Beschikbaarheidsfilter standaard aan" → Uit.

- **Checkout — Winkelwagen leeg na succesvolle betaling**: Na een geslaagde betaling bleef het product in de winkelwagen staan. Oorzaak: `Cart::findOrCreateBySession()` retourneerde bij een dubbele sleutelfout de oude, reeds afgerekende winkelwagen. Opgelost door vóór het aanmaken van een nieuwe winkelwagen het `session_id` van niet-actieve winkelwagens vrij te geven.

- **Checkout — Geboortedatum optioneel en overdraagbaar**: De geboortedatum was ten onrechte verplicht; het veld is nu gelabeld als "(optioneel)". Daarnaast werd de geboortedatum uit stap 1 niet overgenomen naar stap 2 bij de eerste deelnemer — opgelost door in `create_student()` de geboortedatum altijd bij te werken als er een waarde is ingevuld.

- **Routes — Altijd via OrderControllerNew**: De routelogica gebruikte nog een voorwaardelijke check om te bepalen welke controller gebruikt moest worden, waardoor `/cart/add-more/{id}` een fout gaf voor Westvoorne. Alle routes gebruiken nu altijd `OrderControllerNew`.

- **Rijke tekst — `.wv-prose`-stijlen**: Pagina's, cursussen, docenten, FAQ-antwoorden en producten toonden CMS-inhoud als platte tekst zonder opmaakhiërarchie. Een nieuwe CSS-klasse `.wv-prose` is toegevoegd met stijlen voor koppen (h1–h6), lijsten, links, blockquotes en tabellen, toegepast op alle sjablonen waar CMS-inhoud wordt weergegeven.

- **Succespagina — Volledig breedte bestellingsoverzicht**: Het overzicht op de succespagina werd in een smalle kolom getoond. Aangepast naar `col-12` voor volledige breedte.

- **Docentpagina — Cursusblok verborgen bij geen cursussen**: Op de docentdetailpagina werd altijd een cursusblok gerenderd, ook als de docent geen actieve cursussen heeft. Het blok is nu omsloten met een `@if`-check op `$courses->isNotEmpty()`.

- **Cursus- en docentkaarten — Volledig klikbaar met zoom-effect**: Alle cursuskaarten en docentblokken zijn nu volledig klikbaar via Bootstrap `stretched-link`. Cursuskaarten tonen een zoom-effect op de afbeelding bij hover.

- **Paginasjabloon — Extra ruimte onder h1**: De h1-wrapper op de normale paginasjabloon heeft nu `mb-4` voor meer witruimte onder de paginatitel.

- **Cursuskaarten — Verbeterde prijsweergave**: De twee kale oranje prijsregels zijn vervangen door een `.wv-price-block`: de reguliere prijs groot en vetgedrukt, de ledenprijs ernaast met een oranje pill-badge "LEDENPRIJS". Toegepast op cursusoverzicht, homepagina, docentpagina, collectiepagina en gerelateerde cursussen.

- **Cursusdetailpagina — Prijstabel**: De prijsweergave is vervangen door een gestileerde tabel met twee rijen: "Ledenprijs" en "Reguliere prijs", gescheiden door een dunne lijn en omsloten door een kadrering.

- **Cursusdetailpagina — Aantalknop voor inschrijven**: Naast de "Inschrijven"-knop staat nu een +/−-stappenregelaar voor het inschrijven van meerdere deelnemers tegelijk. Het maximum is het aantal nog beschikbare plaatsen (max. 10). De controller verwerkt de `qty`-parameter en maakt het juiste aantal `CartItem`-records aan.

- **Cursusdetailpagina — Programmaselectie en inschrijfknop opgemaakt**: De datum-radiogroep is vervangen door gestileerde kaarttjes met rand en oranje hover-/geselecteerde staat. De "Inschrijven"-knop is vergroot.

- **Checkout — Lettergroottes verkleind**: Labels, alinea's en invoervelden in de checkout erfden de 22px body-lettergrootte. Binnen de checkout-containers zijn deze teruggebracht naar 16px; sectietitels (`.faq-title`) zijn gestileerd als 20px PoppinsSemiBold. Bootstrap-alerts zijn ook op 16px gezet.

- **Afbeeldingen — Lazy loading**: Alle `/storage/`-afbeeldingen in de Westvoorne-sjablonen hebben nu `loading="lazy"`, zodat afbeeldingen buiten beeld pas worden geladen wanneer de bezoeker ernaartoe scrolt.

- **Lettertypen — Sneller laden en betere fallback**: `PoppinsLight.woff2` en `PoppinsSemiBold.woff2` worden nu via `<link rel="preload">` in de `<head>` vooraf geladen. Alle `font-family`-declaraties hebben `Arial, sans-serif` als fallback, zodat bij het laden een schreefloze systeemlettertype wordt getoond in plaats van Times New Roman.

---

## Week van 15 tot 21 juni 2026

### ✨ Nieuw & Verbeterd

- **Checkout — Internationaal telefoonnummer en landkeuze**: Het telefoonnummer in de checkout (stap 1), op de cursuspagina (wachtlijst / seintje-formulieren) en in het cursistenprofiel is vervangen door een internationaal telefoonnuminvoerveld. Er verschijnt een vlaggetje met de landcode; de vlag en de landcode worden automatisch gesynchroniseerd. Standaard staat het veld op Nederland (+31). Bij het indienen wordt het volledige internationale nummer (E.164-formaat) opgeslagen. De validatie is aangepast: voor Nederlandse nummers geldt de bestaande 10-cijfercontrole, voor overige landen wordt gevalideerd via de intl-tel-input bibliotheek.

- **Checkout — Postcode-validatie versoepeld**: De strikte Nederlandse postcode-validatie (verplicht formaat 1234AA) is vervangen door een flexibele controle. Voor een Nederlands adres wordt de postcode automatisch opgemaakt naar het standaardformaat met spatie (bijv. "1234 AA"), zowel bij het verlaten van het veld als bij het laden van het formulier. Voor adressen in andere landen wordt elk formaat geaccepteerd.

- **Evaluaties — Locatiecijfer en -opmerking**: In het evaluatieformulierenbeheer kunnen vragen nu worden gekoppeld aan twee nieuwe marketingvelden: "Cijfer locatie" en "Opmerking locatie". Bij het indienen van een evaluatie worden deze waarden automatisch opgeslagen in vaste kolommen op de evaluatierespons. In het beheerscherm is het locatiecijfer zichtbaar (niet bewerkbaar) en de locatie-opmerking redactioneel aanpasbaar. Het evaluatierapport bevat twee nieuwe vaste kolommen: "Cijfer locatie" en "Opmerking locatie".

- **Productverkopen — Betaler en ontvanger (zoals bij inschrijvingen)**: Productverkopen werken nu net als cursusinschrijvingen: er is een aparte betaler (de persoon die betaalt, via de bestelling) en een ontvanger (de persoon die het product ontvangt). In de checkout kan de ontvanger afwijken van de besteller; standaard is de ontvanger gelijk aan de besteller. De ontvanger wordt aangemaakt als cursist als dat account nog niet bestaat. In het beheer worden betaler en ontvanger naast elkaar getoond, inclusief bedrijfsgegevens bij de betaler. De bevestigings- en verwerkingsmail gaan naar de ontvanger; de factuur gaat naar de betaler (gecombineerd per bestelling). Het productverkopenrapport bevat nu aparte kolommen voor betaler en ontvanger. Bestaande productverkopen zijn bijgewerkt zodat ontvanger gelijk is aan betaler.

- **Cursisten — Tab productverkopen**: In het cursistprofiel is een nieuw tabblad "Productverkopen" toegevoegd. Dit tabblad toont een leesbaar overzicht van alle productverkopen van de cursist met datum, product, prijs, status en betaaldatum, en een directe link naar de verkoop. Het tabblad is alleen zichtbaar voor gebruikers met het recht "Product verkopen".

- **Productverkopen — Betaler en ontvangerblok in bewerkscherm**: In het bewerkscherm van een productverkoop worden betaler en ontvanger naast elkaar getoond als leesbare informatieblokken. De betaler toont naam, e-mail, telefoon en eventuele bedrijfsgegevens uit de bestelling. De ontvanger toont naam, e-mail en geboortedatum. Beide blokken bevatten een directe link naar het cursistprofiel. Wanneer ontvanger en betaler dezelfde persoon zijn wordt dit aangegeven.

- **Marketing Dashboard — Productverkopen**: Het marketing dashboard toont nu ook productverkopen. Twee nieuwe KPI-kaarten tonen het aantal productverkopen (betaald + verwerkt) en de productomzet (ex BTW) in de geselecteerde periode. Een nieuwe tabel "Populaire producten" rangschikt producten op aantal verkopen, met producttype, aantal en omzet ex BTW. De tabel is verborgen wanneer er geen verkopen zijn in de periode.

- **Rapportages — Dagplanning**: Nieuw rapport "Dagplanning" op basis van lessen (lections). Kolommen: Cursuscode, Cursusnaam, les nummer, Lesdatum (Y-m-d), Lesdag(en) (Nederlandse dagnaam), Starttijd, Eindtijd, Lokatie, Lokaal, Docent en Status. Status toont "definitief" wanneer het programma definitief is, anders de programamstatus (open/wachtlijst/gesloten/geannuleerd/voorinschrijving). Filteropties: van/tot op lesdatum, locatie en docent. Actief op alle sites.

- **Rapportages — Productverkopen**: Nieuw rapport "Productverkopen" met kolommen Besteldatum, Klantnaam, Klantemail, Klanttelefoon, Product, Prijs, Betaalstatus, Betaalmethode en Verwerkt. Filterbaar op besteldatum. Actief op alle sites.

- **Checkout Amsterdam — Aparte dag/maand/jaar velden voor geboortedatum**: In het Amsterdam-thema zijn de geboortedatumvelden in zowel stap 1 (contactgegevens) als stap 2 (deelnemersgegevens) omgezet van een vrij tekstinvoerveld naar drie losse keuzelijsten voor dag, maand en jaar — gelijk aan het Utrecht-thema. De geboortedatum is optioneel: wanneer niets is ingevuld wordt `NULL` opgeslagen en blokkeert de validatie de checkout niet.

- **Kortingen — Automatisch toepassen zonder vouchercode**: In het kortingenbeheer kan per korting de schakelaar "Korting automatisch berekenen" worden ingeschakeld. Wanneer actief, wordt de korting bij het openen van stap 2 van de checkout automatisch toegepast op elk product in de winkelwagen — zonder dat de klant een code hoeft in te voeren. Alle selectiemethoden (producten, cursussen, programma's, deelnemers en veldvoorwaarden) worden wel gecontroleerd. De korting wordt getoond met dezelfde groene melding als bij vouchercodes. In rapporten en bevestigingen verschijnt de kortingsnaam met type "Automatisch".

- **Kortingen — Cursusselectie: uitsluitmodus**: Naast de bestaande modus "Beperken tot geselecteerde cursussen" is een tweede modus beschikbaar: "Alle cursussen behalve deze". Via het nieuwe dropdownveld "Cursusselectie modus" in het tabblad Toepassing kan per korting worden gekozen of de cursusselectie als inclusie- of exclusielijst werkt. Alle bestaande kortingen zijn automatisch op de inclusiemodus gezet — er is geen gedragswijziging voor bestaande instellingen.

### 🐛 Bugfixes

- **Cursisten — Tab productverkopen toont ook ontvangen producten**: Het tabblad "Productverkopen" in het cursistprofiel toonde eerder alleen verkopen waarbij de cursist de betaler was. Nu worden ook verkopen getoond waarbij de cursist de ontvanger is. Een nieuwe kolom "Rol" geeft aan of de cursist betaler of ontvanger is.

- **Productverkopen — Verwerkingsmail bij bedrijfsfactuur**: Bij een bestelling via bedrijfsfactuur werden productverkopen niet verwerkt: ze bleven op status "open" staan en er werd geen factuurrecord aangemaakt. Productverkopen worden nu ook bij de bedrijfsfactuurflow gefactureerd en op "betaald" gezet.

- **Productverkopen — Verwerkingsmail naar betaler én ontvanger**: De "verwerkt"-mail (`ProductProcessed`) werd per abuis verstuurd naar zowel de betaler (via `Mail::to()`) als de ontvanger (via de mailable zelf). De mail gaat nu uitsluitend naar de ontvanger, of bij ontbrekende ontvanger naar de betaler.

- **Checkout — Ontvangernaam in besteloverzicht**: In het besteloverzicht (stap vóór betaling) werd bij productverkopen de naam van de besteller getoond achter "Ontvanger" in plaats van de naam die in de ontvangersvelden is ingevuld. Dit is opgelost voor zowel het Amsterdam- als het Utrecht-thema.

- **Checkout Utrecht/Amsterdam — Geboortedatum niet verplicht**: De JavaScript-validatie behandelde een lege geboortedatum als fout en blokkeerde daardoor onterecht de checkout. Geboortedatum is optioneel: een lege invoer passeert de validatie nu zonder foutmelding.

- **Checkout Utrecht — Dag onder 10 gaf validatiefout**: Bij een geboortedatum met een dag onder 10 (bijv. 5 januari) werd de validatie niet goed gedaan voor de dag werd gecombineerd in het verborgen veld. Dit is opgelost door het verborgen veld direct bij te werken zodra een keuzelijst wijzigt, zodat de validatie altijd de actuele waarde controleert.

- **Facturenverwerking — Plaatsingsstatus bedrijfsfactuur**: Bij het verwerken van facturen via de cron (`vu:invoices`) en bij een directe bankoverschrijving in de checkout werd de instelling "Bedrijfsfactuur: plaatsingsstatus" (handmatig/direct) niet gerespecteerd. Inschrijvingen bij sites met de instelling op "handmatig" worden nu pas op "geplaatst" gezet nadat de beheerder dit handmatig bevestigt.

- **Betaallinks — Stille fouten bij ontbrekende deelnemergegevens**: De `vu:paymentlinks`-cron sloeg inschrijvingen zonder student-id en e-mailadres stilzwijgend over. Er worden nu waarschuwingen gelogd, en inschrijvingen met een e-mailadres maar zonder gekoppeld account krijgen automatisch een nieuw studentaccount aangemaakt.

- **Bedrijfsfactuur — E-mail naar verkeerd adres**: De gecombineerde bedrijfsfactuur werd verstuurd naar het e-mailadres van de contactpersoon in plaats van het bedrijfsfaktuure-mailadres van de bestelling. Dit is gecorrigeerd.

- **Beveiliging — Kortingscode-validatie tegen programma-startdatum**: Kortingen worden gevalideerd op basis van de startdatum van het programma (niet de huidige datum). Hierdoor wordt een korting die pas ingaat bij aanvang van de cursus correct geaccepteerd, en wordt een korting met een einddatum vóór de startdatum van het programma correct geweigerd — ook als die korting vandaag nog geldig lijkt.

- **Beveiliging — Chrome User-Agent Reduction onterecht geblokkeerd**: Chrome heeft sinds versie 113 (mei 2023) standaard "User-Agent Reduction" ingeschakeld, waardoor echte Chrome-browsers `Chrome/MAJOR.0.0.0` rapporteren (met nullen voor minor/build/patch). Dit patroon werd onterecht als botverkeer geblokkeerd. Chrome/113 t/m Chrome/147 zijn verwijderd uit de blokkeerlijst. Eerder door deze regel geblokkeerde IP-adressen worden automatisch gedeblokkeerd via een migratie.

- **Beveiliging — FacebookBot geblokkeerd waardoor OG-previews faalden**: De crawler van Facebook (`FacebookBot` en `facebookexternalhit`) stond op de blokkeerlijst, waardoor link-previews op Facebook en Instagram niet meer werkten wanneer een pagina werd gedeeld. Beide crawlers staan nu op de toegestane lijst.

### 🎨 Thema-updates Utrecht

- **Checkout — Kortingscode-invoer per deelnemer**: In stap 2 van het checkout-proces (deelnemersgegevens) kan per cursusinschrijving een kortingscode of stadspasnummer worden ingevoerd. De code wordt direct gevalideerd via een asynchroon verzoek en de korting wordt zichtbaar verwerkt in het winkelwaagenoverzicht. De validatie gebruikt dezelfde regels als het Amsterdam-thema.

- **Evaluaties — Redactionele bewerking van antwoorden**: In het evaluatie-antwoordbeheer kunnen nu per antwoord een quote voor bij de cursus en een quote voor bij de docent worden ingevuld. Deze worden bij het indienen automatisch gevuld vanuit de antwoorden die als "Opmerking cursus" of "Opmerking docent" zijn gemarkeerd. Beheerders kunnen de tekst daarna inkorten of aanpassen voor publicatie.

- **Evaluaties — Interne notitie en statistiekenuitzondering**: Per evaluatie-antwoord kan een interne notitie worden toegevoegd (alleen zichtbaar in het beheer). Via een vinkje "Uitsluiten van statistieken" kan een antwoord buiten de KPI-berekeningen op het dashboard worden gehouden — handig voor test- of uitzonderingsgevallen.

- **Evaluaties — Publicatieschakelaars per antwoord**: In het overzicht van evaluatie-antwoorden staan twee schakelknoppen per rij: "Publ. cursus" en "Publ. docent". Deze zijn direct in de lijst te bedienen zonder de rij te openen — een klik slaat de keuze meteen op. Dezelfde schakelaars zijn ook beschikbaar in het bewerkscherm.

- **Dashboard — Uitgesloten antwoorden tellen niet mee in KPI's**: Evaluatie-antwoorden waarop "Uitsluiten van statistieken" is ingeschakeld, tellen niet meer mee bij de gemiddelde cijfers en responspercentages op het dashboard.

- **Evaluaties — Cijfers opgeslagen als eigen veld**: Bij het indienen van een evaluatie worden de cijfers voor cursus en docent nu direct als afzonderlijke velden opgeslagen. Dit maakt sorteren op cijfer mogelijk in het overzicht, en de dashboardberekeningen zijn hierdoor een stuk sneller — er hoeft niet langer per antwoord door de JSON-antwoordenlijst te worden gezocht. Bestaande ingediende antwoorden zijn automatisch bijgevuld. De cijfers zijn zichtbaar (maar niet bewerkbaar) in het bewerkscherm.

- **Evaluaties — Zoeken op cursusnaam**: In het overzicht van evaluatie-antwoorden werkt de zoekfunctie nu ook op cursusnaam.

---

## Week van 8 tot 14 juni 2026

### ✨ Nieuw & Verbeterd

- **Rapportages — Vernieuwd rapportage-overzicht**: Het rapportage-overzicht is volledig heringericht:
  - Zoek snel een rapport door te typen in het zoekveld — de omschrijving van het gekozen rapport verschijnt direct als toelichting.
  - De filteropties verschijnen alleen wanneer je een rapport hebt gekozen.
  - De knop "Uitvoeren" is uitgeschakeld totdat alle verplichte filteropties zijn ingevuld.
  - Rapporten die direct klaar zijn geven een groene melding "Rapport gereed!" met een downloadknop.
  - Rapporten die op de achtergrond worden aangemaakt, ververst de pagina automatisch totdat ze klaar zijn.
  - Rapporten kunnen nu per site worden aan- of uitgezet. Uitgeschakelde rapporten zijn niet meer zichtbaar in het overzicht.

- **Rapportages — Daglijst Docent**: Nieuw rapport als uitbreiding op de Daglijst. De "Daglijst Docent" toont alle kolommen van de gewone Daglijst, aangevuld met: sessienummer ("Les X van Y"), locatie, het aantal betalende deelnemers en het aantal niet-betalende deelnemers (deelnemers die gratis deelnemen of 100% korting hebben gekregen). Beide rapporten gebruiken dezelfde filters: periode en optioneel locatie.

- **Beheerpaneel — Kolominstellingen per gebruiker**: Per lijstpagina kun je kolommen zichtbaar of verborgen zetten via de kolomknop rechtsboven. De keuze wordt automatisch onthouden — ook na het sluiten van de browser of inloggen op een ander apparaat. Zo ziet elke beheerder precies de kolommen die voor hem of haar relevant zijn.

- **Beheerpaneel — Eigen logo uploaden via site-instellingen**: In de site-instellingen (tabblad "Algemeen") is een veld toegevoegd waarmee het logo in de linkerbovenhoek van het beheerpaneel en op de inlogpagina vervangen kan worden door een eigen afbeelding. Wanneer er geen logo is geüpload, blijft het standaard VUAdmin-logo zichtbaar.

- **Programma bericht — Via e-mailsjabloon**: Het vrije bericht dat vanuit een programma naar deelnemers en de docent gestuurd kan worden, loopt nu via het sjabloonsysteem (sjabloon #35 — "Vrij bericht aan deelnemer / docent vanuit programmaoverzicht"). De aanhef, tekst en opmaak zijn daarmee aanpasbaar via het e-mailsjablonenbeheer, net als alle andere e-mails in het systeem.

- **Amsterdam certificaat — Nieuw lettertype en opmaak**: Het certificaat van het Amsterdam-thema gebruikt nu het DM Sans lettertype. Naam en cursustitel zijn vetgedrukt in het blauw van de huisstijl; overige tekst is in grijs. Bij een cursus van één dag toont het certificaat "Op DD-MM-JJJJ" in plaats van een datumreeks "Van … tot …".

- **Beveiliging — Verbeterde detectie en blokkering van botverkeer**: De beveiliging tegen geautomatiseerde aanvallen is aangescherpt en uitgebreid. Bekende aanvalspatronen worden sneller herkend en automatisch geblokkeerd, ook terugkijkend in de geschiedenis.

- **Statistieken — Spamverkeer telt niet meer mee**: De foutpagina van de website werd vroeger door bots massaal bezocht en telde daardoor onterecht mee als gewoon bezoek. Bezoekers, paginaweergaven, conversieratio en populaire pagina's in het marketing dashboard zijn nu gebaseerd op uitsluitend echte bezoekers.

- **Marketing Dashboard — Sneller en nauwkeuriger**: Spam- en aanvalsverkeer wordt nu al bij het ophalen van de gegevens uitgefilterd in plaats van achteraf per rapport. Dit maakt alle dashboardpagina's sneller en zorgt ervoor dat de cijfers overal consistent zijn.

- **Marketing — Zoekverkeer van Google en andere zoekmachines automatisch herkend**: Wanneer iemand via een zoekmachine op de website terechtkomt, wordt dit nu automatisch geregistreerd als "organisch" bezoek — inclusief de zoekmachine (Google, Bing, DuckDuckGo, enzovoort) en, wanneer beschikbaar, het gebruikte zoekwoord. Dit werkt alleen als er geen betaalde campagnelink is gebruikt, zodat advertentieverkeer altijd de juiste bron houdt.

- **Marketing Dashboard — Filteren op verwijzende website**: Naast filteren op bron, medium en campagne is het nu ook mogelijk om alle dashboardcijfers te filteren op de website waar een bezoeker vandaan kwam. Selecteer een verwijzend domein in het nieuwe dropdown-filter om te zien hoeveel bezoekers, paginaweergaven en aankopen er uit die bron kwamen. De cijfers kloppen ook echt: de koppeling loopt via de winkelwagen, zodat ook conversies correct worden toegeschreven aan de juiste verwijzer.

### 🐛 Bugfixes

- **Winkelwagen / Bestelling — Sessie-synchronisatie**: Bij het openen van een bestellingslink via een e-mail terwijl er al een andere browsersessie actief was, konden de winkelwagen en de bestelling door elkaar lopen. Drie samenhangende oorzaken zijn opgelost zodat de winkelwagen altijd correct gekoppeld blijft aan de bijbehorende bestelling — ook bij het wisselen van browser of apparaat.

- **Beveiliging — Aangescherpte beveiliging nieuwsbriefinschrijfformulier**: De beveiliging van het nieuwsbriefinschrijfformulier is aangescherpt. Geautomatiseerde aanmeldingen en misbruik worden nu sneller tegengehouden, terwijl normaal gebruik niet wordt gehinderd.

- **Moodle-koppeling — Verbeterde betrouwbaarheid**: De koppeling met Moodle werkt nu ook correct wanneer de URL op een niet-standaard manier was geconfigureerd. De "Bekijk in Moodle"-knop verschijnt alleen nog wanneer de koppeling actief is.

---

## Week van 1 tot 7 juni 2026

### ✨ Nieuw & Verbeterd

- **FAQ-categorieën — Actief/Inactief**: FAQ-categorieën hebben nu een "Actief"-vinkje in het beheer. Inactieve categorieën worden niet meer getoond op de FAQ-pagina en op CMS-pagina's met het FAQ-blok. Nieuwe categorieën staan standaard op actief.

- **Lessen genereren — Eén les zonder dagkeuze**: Bij programma's met precies één les hoeft geen dag van de week geselecteerd te worden. Vul de startdatum in en de les wordt direct ingepland. Bij meerdere lessen blijven dagen verplicht. Programma's met een startdatum maar nog geen aangemaakte lessen worden nu ook automatisch herkend en aangevuld.

- **SEO — Gestructureerde data gecorrigeerd**: De gestructureerde data in de paginakop (voor zoekmachines) bevatte een opmaakfout waardoor zoekmachines die niet correct konden lezen. Dit is hersteld.

- **Zoeken — Geen beschikbaarheidsfilter bij zoekopdrachten**: Op de cursus- en collectiepagina's staat het filter "Alleen beschikbare cursussen" standaard aan. Bij het zoeken wordt dit filter automatisch uitgeschakeld zodat alle overeenkomende cursussen — ook gesloten of toekomstige — in de zoekresultaten verschijnen. Het filter blijft actief bij gewoon bladeren zonder zoekopdracht.

- **Zoekresultatenpagina — Paginatitel**: De cursusoverzichtspagina toont nu een duidelijke paginatitel: "Zoekresultaten voor: [zoekterm]" bij een actieve zoekopdracht, en "Onze cursussen" bij gewoon bladeren.

- **Productpagina — Paginatitel**: De productdetailpagina miste een paginatitel. De productnaam staat nu correct als hoofdtitel op de pagina.

- **Homepage sliders — Alleen beschikbare cursussen**: De vier collectiesliders op de homepage (online cursussen, cursussen op locatie, tips & inspiratie, populaire cursussen) toonden alle cursussen uit een collectie, ook cursussen zonder open programma. De sliders tonen nu alleen cursussen waarvoor je je daadwerkelijk kunt inschrijven.

- **GA4 — Aankoopregistratie op bedankpagina**: Na een succesvolle bestelling wordt op de bedankpagina een GA4-aankoopgebeurtenis geregistreerd met het ordernummer, het totaalbedrag en alle cursusinschrijvingen en productverkopen. Het event wordt pas geregistreerd nadat de betaling volledig is verwerkt, zodat het niet meerdere keren wordt geteld bij een paginaverversing.

- **Alt-teksten — Afbeeldingen Amsterdam-thema**: Alle afbeeldingen in het Amsterdam-thema zonder zinvolle omschrijving zijn gecorrigeerd. Decoratieve iconen zijn als decoratief gemarkeerd; locatie-, docent- en contentblokafbeeldingen tonen nu de juiste naam als alt-tekst. Dit verbetert de toegankelijkheid en is conform de WCAG-richtlijnen.

### 🐛 Bugfixes

- **Nieuwsbriefinschrijving — Foutmelding opgelost**: Het nieuwsbriefinschrijfformulier gaf bij sommige bezoekers een foutmelding. Er bleken meerdere samenhangende problemen te zijn in de beveiligings- en spamdetectie-instellingen. Alle oorzaken zijn opgelost; het formulier werkt nu betrouwbaar.

- **Kortingspas — Fouten bij cursus die volgend jaar start**: Bij het toepassen van een kortingspas op een cursus die volgend jaar start, traden meerdere fouten op. De kortingscode werd niet correct herkend en er werd soms een pas aangemaakt voor de verkeerde periode. Alle oorzaken zijn opgelost.

- **Redirects — Werkt nu voor alle pagina's**: Voorheen werkten doorverwijzingen (redirects) alleen voor CMS-pagina's. Ze werken nu ook voor cursuspagina's, collecties, blogposts, productpagina's en alle andere publieke pagina's op de website.

- **Cursus-beheer — Certificaattemplate gebaseerd op actief thema**: De keuzelijst voor de certificaattemplate bij een cursus toont nu alleen de templates die beschikbaar zijn voor het actieve thema. Eerder werden templates van alle thema's door elkaar getoond.

- **Cursusfilter — "Beschikbaar" standaard aan (Amsterdam)**: Op de cursus- en collectiepagina's van het Amsterdam-thema staat het filter "Alleen beschikbare cursussen" nu standaard ingeschakeld. Bij het eerste bezoek worden automatisch alleen cursussen met een open programma getoond. De bezoeker kan het filter uitschakelen via het filterpaneel; die keuze wordt correct bewaard.

- **Kortingen — Begindatum**: Naast een einddatum kan nu ook een begindatum worden ingesteld voor een korting. Is geen begindatum opgegeven, dan geldt de korting altijd vanaf het begin. De geldigheidscheck gebruikt — net als bij de einddatum — de startdatum van het programma als referentiedatum, zodat een korting die pas ingaat bij aanvang van de cursus correct wordt gevalideerd.

- **Kortingen validiteit**: Kortingen worden nu gecheckt of ze valide zijn bij aanvang cursus, niet bij inschrijving.

- **Logging — Recaptcha-fouten onderdrukt**: Foutmeldingen van de reCAPTCHA-beveiliging worden niet meer gelogd of als melding verstuurd.

- **Factuur-e-mail — Juiste PDF-bijlage**: De factuure-mail die naar het bedrijf wordt verstuurd bevatte altijd de proforma-PDF, ook nadat de definitieve factuur al was aangemaakt. Nu wordt de definitieve factuur meegestuurd zodra die beschikbaar is.

- **Moodle-koppeling — URL-configuratie verbeterd**: De Moodle-koppeling werkt nu ook correct wanneer de URL niet volledig was ingesteld.

- **Menuvolgorde — Fout bij het opslaan**: Bij het gebruik van de sorteerfunctie in het menu-beheer kon een fout optreden waardoor de volgorde niet werd opgeslagen. Dit is opgelost.

- **Factuurmail overgeslagen bij geïmporteerde betalingen**: Facturen die via een bulk-import zijn aangemaakt, krijgen geen automatische e-mail meer.

- **Productverkopen — Snellere dropdowns**: De dropdowns voor product, cursist en bestelling in het aanmaak-/bewerkscherm van productverkopen laden nu efficiënter, ook bij grote aantallen records.

- **Nieuwsbriefformulier — reCAPTCHA-beveiliging**: Het nieuwsbriefinschrijfformulier (footer en nieuwsbrief-pagina) is beveiligd met Google reCAPTCHA.

- **Marketing Dashboard — Bestelproces-funnel**: Het marketing dashboard toont nu een overzichtskaart "Bestelproces" met drie stappen: **Winkelwagen** (bezoekers met minstens één item), **Verlaten** (niet-afgeronde winkelwagens ouder dan 30 minuten) en **Afgerond** (bestellingen die zijn doorgegaan in de geselecteerde periode). Per stap worden het absolute aantal en het percentage ten opzichte van de start getoond.

---

## Week van 25 tot 31 mei 2026

### ✨ Nieuw & Verbeterd

- **Checkout stap 1 — Formulier voorgevuld vanuit ingelogd studentprofiel**: Wanneer een student ingelogd is, worden de contactgegevens in stap 1 van de checkout (naam, e-mail, geboortedatum, aanhef, telefoon, adres, postcode, plaatsnaam) automatisch voorgevuld vanuit zijn of haar studentprofiel. Dit gebeurt alleen als er nog geen eerdere bestelling is voor de winkelwagen — is die er wél, dan worden de al ingevulde gegevens van die bestelling gebruikt. Het e-mailveld is alleen-lezen wanneer de student ingelogd is. De "bestaat al een account"-waarschuwing en de bijbehorende API-check worden alleen getoond aan niet-ingelogde bezoekers.
- **Checkout stap 2 — Kortingsvelden verborgen bij factuurbetalingen (Amsterdam)**: Bij een zakelijke bestelling waarbij gekozen is voor betaling op factuur (Bankoverschrijving), worden de invoervelden voor kortingscode, stadspasnummer en loyalty card niet meer getoond in stap 2. Deze velden zijn niet relevant bij facturatie.
- **Bedrijfsfacturatie — Directe orderverwerking (Amsterdam)**: Bij betaling op factuur worden bestellingen nu direct volledig verwerkt:
  - Alle inschrijvingen worden direct op **"Geplaatst"** gezet en de deelnemers ontvangen hun bevestigingsmail.
  - De gecombineerde factuur-PDF en de e-mail naar het bedrijf worden automatisch verstuurd.
  - De betaler wordt direct doorgestuurd naar de bestellingsbevestigingspagina.
  - De instelling "Bedrijfsfactuur: plaatsingsstatus" is hiermee vervallen — inschrijvingen worden altijd direct geplaatst bij zakelijke facturatie.
- **Bevestigingsmails — Controle per inschrijving**: Een deelnemer ontvangt nu altijd zijn bevestigingsmail, ook als de bestelling al eerder bevestigd werd (bijv. bij een gecombineerde bestelling met meerdere deelnemers).
- **Programma-beheer — Inschrijvingen-tab: links naar student en inschrijving**: In de tab "Inschrijvingen" op de programmapagina zijn twee verbeteringen doorgevoerd:
  - De **studentnaam** is nu een klikbare link naar de studentpagina.
  - Achter het statusveld staat nu een **"✎ Open"**-knop die direct naar de bewerkpagina van de inschrijving navigeert.

### 🐛 Bugfixes

- **Winkelwagen leeg na inloggen**: Na het inloggen was de winkelwagen leeg, ook al waren er voor het inloggen items toegevoegd. Oorzaak: na `Auth::guard('student')->attempt()` wordt de sessie-ID door Laravel geregenereerd. De code vond de winkelwagen op het oude sessie-ID en paste het nieuwe sessie-ID toe op het model, maar sloeg dit nooit op (`$cart->save()` ontbrak). De winkelwagen kon daarna niet meer gevonden worden op het nieuwe sessie-ID.

### 🎨 Thema-updates Amsterdam

- **Knop `.btn-sky` nu centreerbaar**: De klasse `.btn-sky` gebruikte `display: flex` (blokniveau), waardoor `text-align: center` op de bovenliggende container geen effect had. Gewijzigd naar `display: inline-flex`, zodat de knop correct gecentreerd wordt. De bestaande `max-width: max-content` zorgt ervoor dat het visuele gedrag op alle andere plekken ongewijzigd blijft.
- **Filteroverlay mobiel — label naast checkbox**: In het filterpaneel op mobiel (`max-width: 575px`) werden labels onder de checkbox geplaatst door `flex-direction: column`. Gecorrigeerd naar `flex-direction: row` met `align-items: center`.
- nieuwsbrief inschrijven block voor nieuwsbrief pagina
- typeform embed blok


---

## Week van 18 tot 24 mei 2026

### ✨ Nieuw & Verbeterd

- **Frontend validatie — Nederlandse telefoon, postcode en geboortedatum**: In alle thema's is client-side validatie toegevoegd voor `phone1`, `zip` en geboortedatumvelden op checkout-, dashboard- en formulieren zoals wachtlijst/seintje. Inhoud wordt genormaliseerd naar Nederlandse formaten, ongeldige invoer wordt geblokkeerd en er verschijnen foutmeldingen in het Nederlands.
- **Course-level certificaattemplate**: Cursusbeheer heeft nu een optioneel veld voor een certificaattemplate en kan per cursus geselecteerd of leeg gelaten worden wanneer er geen certificaat verstuurd moet worden.


### 🎨 Thema-updates 
- **Utrecht certificaten aangepast**: Voor Utrecht zijn de certificaten templates aangapast, deze kunnen worden geselecteerd  in de Basiscursus instellingen.
- **Amsterdam badrijfsfactuur aanpassing**: De facturen tonen nu "Factuur" in plaats van Proforma Factuur.

## Week van 11 tot 17 mei 2026

### ✨ Nieuw & Verbeterd


- **Frontend zoekfunctie — Relevantiesortering**: De zoekfunctie op de cursuspagina (`/cursussen`) is uitgebreid met relevantiesortering en slimmere queryverwerking:
  - **Stop-word filtering**: Veelgebruikte Nederlandse woorden (de, het, een, van, voor, cursus, …) worden automatisch uit de zoekterm gefilterd zodat ze geen irrelevante hits veroorzaken.
  - **Speciale tekens worden gestript**: Leestekens en andere niet-alfanumerieke tekens (bijv. `?`, `!`, `-`, `.`) worden verwijderd uit elk zoekwoord vóór de verwerking. `yoga!` en `yoga` worden dus identiek behandeld.
  - **Multi-word zoeken**: De zoekterm wordt opgesplitst in losse woorden. Elk woord wordt afzonderlijk gezocht, waardoor "schilderen aquarel" resultaten vindt die *beide* woorden bevatten en die hoger scoren.
  - **Gewogen relevantiescore**: Elk resultaat krijgt een score op basis van waar het zoekwoord gevonden wordt:
    | Veld | Punten per woord |
    |---|---|
    | Exacte titelmatch | +100 bonus |
    | Titel begint met zoekwoord | +30 bonus |
    | `seo_keywords` | +40 |
    | `title` | +20 |
    | `intro` | +8 |
    | `text` / `description` | +3 |
  - **`intro`-veld nu doorzocht**: De `intro`-kolom van cursussen werd voorheen niet meegenomen in zoekopdrachten — dit is nu hersteld.
  - **Producten via DB gezocht**: Productzoekacties werden eerder gedaan via PHP `stripos()` na alle producten op te halen. Dit is vervangen door DB LIKE-queries per zoekwoord.
  - **Relevantie als standaard sortering**: Alle themes tonen zoekresultaten standaard op relevantie (hoogste score bovenaan). breda, utrecht, westvoorne en demo hadden al "Relevantie" in hun sorteer-dropdown — het backend-equivalent ontbrak alleen. Amsterdam toont nu contextgevoelig "Relevantie" bij zoeken en "Alfabetisch" bij bladeren.


- **Route `/favorieten` opent Favorieten-tab in dashboard**: De route `/favorieten` toont niet langer een aparte pagina, maar stuurt ingelogde studenten door naar `/student/dashboard?tab=favorieten`. Het Amsterdam-dashboard leest de `?tab=`-parameter uit de URL en activeert de bijbehorende tab automatisch bij het laden van de pagina.
- **Amsterdam dashboard — Uitgebreide inschrijvingskaarten**: De "Mijn Inschrijvingen"-tab toont nu per inschrijving aanvullende details naast de cursustitel:
  - **Statusbadge** kleurgecodeerd (groen = Ingeschreven, geel = Openstaand, blauw = Betaling, rood = Gestopt).
  - **Programmacode** (met code-icoon).
  - **Startdatum** (opgemaakt uit `c_startdate`, met fallback naar `planner_start`).
  - **Locatie** uit het `c_location`-veld (ruimte + locatienaam).

- **Admin — `seo_complete`-kolom sorteerbaar**: De kolom "SEO Compleet" in de cursuslijst is nu sorteerbaar via `orderable(true)` + een `orderByRaw CASE`-expressie. `searchLogic(false)` voorkomt dat Backpack probeert op het accessor-veld te filteren.
- **Checkout — Producten altijd gekoppeld aan besteller**: In stap 2 van de checkout (deelnemersgegevens) worden producten niet meer met invulbare naam/e-mail/aanhefvelden getoond. In plaats daarvan staat er een read-only kaart met de naam en het e-mailadres van de besteller. `OrderControllerNew::post_payment()` koppelt de `ProductSale` direct aan `$order->student` in plaats van via `find_or_create_participant()`.


### 🐛 Bugfixes

- **Admin — "Deblokkeer"-knop geeft JSON-fout op productie**
- **Amsterdam checkout — dubbele bevestigingsknop consistent gemaakt**: In stap 3 van het Amsterdam-theme is de linker bevestigingsactie vervangen door een echte submit-knop, zodat beide kolommen dezelfde `btn btn-pay`-actie gebruiken.
- **Utrecht theme — locatieblok gecontroleerd op een lege locatie**: Het programma geeft nu geen fout meer als `selected_program->location` ontbreekt in `themes/utrecht/course_show.blade.php`.

### ✨ Nieuw & Verbeterd

- **Security Dashboard — Actieve sessies**: Het Security Dashboard toont nu een overzicht van alle actieve sessies. Per sessie is zichtbaar: gebruikersnaam (beheerder, student of gast), type, IP-adres, browser/user-agent en tijdstip van laatste activiteit. Bij de standaard bestandssessie-driver (`SESSION_DRIVER=file`) zijn IP-adres en user-agent niet beschikbaar; bij de database-driver zijn deze wel zichtbaar. De kaart heeft een "Vernieuwen"-knop voor realtime updates zonder de volledige pagina te herladen. Sessies verlopen automatisch na de ingestelde `SESSION_LIFETIME`.

- **Security, Marketing & Financial Dashboard — Paginering in tabellen**: Alle lange lijsten in de drie dashboards worden nu gepagineerd weergegeven met maximaal 25 items per pagina, met een pager die het huidige bereik toont ("X–Y van Z") en knoppen om te navigeren. Geldt voor: 404-pagina's, aanvalspaden, geblokkeerde IPs, mislukte inlogpogingen, campagnes, zoektermen, populaire pagina's, verwijzende domeinen en openstaande posten.
- **Theme — 500-fout bij ontbrekend menu**: Wanneer een menu-slug (bijv. `top1` of `top2`) niet bestaat in de database, gaf het theme een 500-fout (`Attempt to read property "rootItems" on null`). `VuMenuService::get()` geeft nu een leeg `VuMenu`-object terug als er geen menu gevonden wordt, zodat alle themes hier automatisch tegen beschermd zijn.
- **Theme — 500-fout in `<head>` zonder paginaelement**: De `Head`-component had `$element = ''` als standaardwaarde, waardoor de nullsafe `?->` operatoren in de blade werden omzeild en PHP probeerde een property op een string te lezen (`Attempt to read property "seo_title" on string`). Standaardwaarde is nu `null`, waardoor alle themes correct werken wanneer geen element meegegeven wordt.

### ✨ Nieuw & Verbeterd

- **Beveiliging — Geblokkeerde IPs ook geblokkeerd in de beheeromgeving**

- **Bedrijfsfactuur — Betaallink via Mollie**: De proforma factuur die naar het bedrijf wordt verstuurd bevat nu een **"Betaal factuur"**-knop die direct linkt naar een betaalpagin.
  - De knop leidt naar Mollie, waar het totale openstaande bedrag voor alle inschrijvingen in de bestelling in één keer betaald kan worden.
  - Na succesvolle betaling worden automatisch per inschrijving facturen aangemaakt en verstuurd naar het bedrijfse-mailadres.
  - De betaallink is altijd actief zolang er nog openstaande inschrijvingen (`open` / `betaling`) in de bestelling staan. Als alles al betaald is, wordt doorverwezen naar de bevestigingspagina.

- **Beschikbaarheidscheck bij zakelijke betaallink**: Wanneer een bedrijf de betaallink volgt (die soms weken na de aanmelding verstuurd of gebruikt wordt), controleert het systeem eerst of de cursussen nog beschikbaar zijn.
  - **Programma volgeboekt**: de inschrijving wordt verplaatst naar de wachtlijst (`wachtlijst`) en uitgesloten van de betaling.
  - **Programma gesloten**: de inschrijving wordt gemarkeerd als `seintje` (wachtlijst ook vol) en uitgesloten.
  - Als alle inschrijvingen in de bestelling niet meer beschikbaar zijn, wordt de betaling geblokkeerd met een duidelijke foutmelding.
  - Beschikbare inschrijvingen gaan gewoon door; het Mollie-bedrag wordt automatisch aangepast op alleen de nog beschikbare items.

- **Bevestigingse-mail — Termijninformatie**: De bevestigingse-mail die naar de koper wordt verstuurd toont nu duidelijk de termijninformatie wanneer voor gespreide betaling is gekozen.
  - Per cursusregel wordt het termijnbedrag getoond (1e termijn) met ondertitel "1e termijn van N · totaalprijs €X".
  - In het totaalblok onderaan: "Nu betaald: €X" en "Resterend te betalen: €Y (wordt later gefactureerd)".


### 🎨 Thema-updates (alle thema's)

- **Proforma factuur — Schrijfwijze gecorrigeerd**: "Pro forma" is aangepast naar de correcte Nederlandse schrijfwijze "Proforma" in alle PDF-templates (amsterdam, utrecht, breda, westvoorne, demo).

- **Proforma factuur — Starttijd eerste les toegevoegd**: Op de proforma factuur wordt nu achter de startdatum ook de start- en eindtijd van de eerste les getoond (bijv. `start 15-09-2026 09:30–12:30`).

- **Filter — Alle filteropties zichtbaar**: In het filterpaneel op collectie- en cursuspagina's werden na 6 items de overige opties verborgen (overblijfsel van een oude "Meer tonen"-functionaliteit). Alle filteritems in elk accordion-blok worden nu altijd getoond.

- **Backend — Wachtwoord-reset geeft 500-fout**: De wachtwoord-reset in de beheeromgeving mislukte omdat `config/auth.php` nog verwees naar de tabel `password_resets`, terwijl die via een eerdere migratie hernoemd was naar `password_reset_tokens`. Config is bijgewerkt.

- **Student-portaal — Wachtwoordsterkte-indicator en -afdwinging** (alle thema's): Op de pagina's "Nieuw wachtwoord instellen" (`/student/codelogin`) en "Wachtwoord wijzigen" in het accountdashboard is een wachtwoordsterkte-indicator toegevoegd, bestaande uit vier gekleurde segmenten (rood → oranje → geel → groen) met een tekstlabel (Zwak / Matig / Redelijk / Sterk). De score is gebaseerd op lengte (≥ 8 tekens), een hoofdletter, een cijfer en een speciaal teken. Indienen wordt client-side geblokkeerd als de score onder "Redelijk" ligt. Server-side wordt hetzelfde beleid afgedwongen via Laravel's `Password::min(8)->mixedCase()->numbers()->symbols()`-regel.

### 🎨 Thema-updates Amsterdam

- **Agenda — Gebaseerd op startdatum programma**: De agenda op de homepage toont nu cursussen op basis van de **startdatum van het programma** (de eerste les), in plaats van de eerstvolgende les die nog in de toekomst ligt. Zo ziet een bezoeker altijd de programma's waarvan de cursus nog niet begonnen is, gesorteerd op wanneer ze starten.
- **Checkout stap 2 — Cursusinfo onder de cursustitel**: Onder de naam van de cursus in stap 2 (deelnemersgegevens) staan nu de **programmacode**, de **startdatum** en de **locatie** van het programma, zodat de deelnemer meteen ziet om welk specifiek programma het gaat.
- **Checkout stap 3 — Betaalwijze bij termijnbetaling duidelijker**: Wanneer voor een cursus gekozen is voor gespreide betaling, toont de badge bij de cursus nu **"Betaling: in X delen"** in plaats van "Betaling: Direct". Bovendien wordt rechts in het besteloverzicht naast "Nu te betalen" ook een extra regel **"Later te betalen (termijnen)"** getoond met het totale bedrag dat nog in latere termijnen verschuldigd is.
- **Bestellingsbevestiging — Termijninformatie bij gespreide betaling**: Op de bevestigingspagina na betaling wordt per cursus nu getoond hoeveel de eerste termijn is en wat er later nog betaald moet worden (bijv. "Termijn 1 van 3: €100,00 — later: €200,00"). Onderaan verschijnt een extra regel **"Later te betalen (resterende termijnen)"** als er nog toekomstige termijnen zijn.
- **Nieuwsbriefcheckbox — Seintje & Wachtlijst (Amsterdam)**: Bij alle drie de formulieren op de cursuspagina (wachtlijst, seintje "inschrijving gesloten", seintje "geen startdata") verschijnt een **"Schrijf mij in voor de nieuwsbrief"**-checkbox. De checkbox wordt alleen getoond als `MAILCHIMP_TOKEN`/`MAILCHIMP_LISTID` (of MailerLite) geconfigureerd zijn in `.env`. `HomeController::sendToMailchimp()` geeft nu netjes `false` terug als de env-sleutels ontbreken.
- **Nieuwsbriefcheckbox — Checkout (Amsterdam)**: In de laatste betalingsstap van de checkout verschijnt de checkbox **"Schrijf mij in voor de nieuwsbrief"** boven de akkoordverklaring met de algemene voorwaarden. De checkbox is alleen zichtbaar als de Mailchimp- of MailerLite-sleutels geconfigureerd zijn. `OrderControllerNew::post_overview()` verwerkt de keuze en roept de nieuwe `sendToNewsletter()`-methode aan (Mailchimp of MailerLite, gebaseerd op `config('app.mijnvu')`).
- **Nieuwsbriefcheckbox — Seintje & Wachtlijst zonder conditie (Amsterdam)**: De `@if`-bewakers zijn verwijderd; de nieuwsbrief-checkbox verschijnt nu altijd in de drie formulieren op de cursuspagina (wachtlijst, seintje "gesloten", seintje "geen startdata") — het Amsterdam-thema hoeft hier geen configuratiecheck te doen.
- **Cursuskaart — "Gesloten"-label verborgen (Amsterdam)**: De label "Gesloten" wordt niet meer getoond op cursuskaarten (`course_block` en `horizontal_course_block`). Programma's met status `gesloten` of `Vol` krijgen nu geen badge.
- **Cursuspagina — Favorieten-icoontje bij de cursustitel (Amsterdam)**: Op de cursusdetailpagina (`course_show`) staat nu het hartje-icoontje naast de cursustitel. Klikken togglet de `active`-klasse via het bestaande JS-script.

- **Student-portaal — Volledig herontwerp van inlog- en accountpagina's**: De vier pagina's van het studentportaal zijn volledig heronworpen in de stijl van het Amsterdam-thema.
  - **Inlogpagina** (`/student/login`): Gecentreerde `checkout-block`-kaart met `form-floating`-invoervelden, correcte `breadcrumb-top-wrp`-navigatie en links naar wachtwoord aanmaken/vergeten gestyled als `.btn-sky-link`. De ontbrekende `method="POST"` en `action` op het formulier zijn hersteld.
  - **Code opvragen** (`/student/code`): Hetzelfde kaartlayout met beschrijvende tekst, knoplabel gecorrigeerd naar "Code versturen" en een hulpblok voor gebruikers die al een code ontvangen hebben.
  - **Nieuw wachtwoord instellen** (`/student/codelogin`): Titel verduidelijkt naar "Nieuw wachtwoord instellen", `autocomplete="one-time-code"` toegevoegd aan het codeveld en navigatielinks naar code opnieuw aanvragen en terugkeren naar inloggen.
  - **Accountdashboard** (`/student/dashboard`): Volledig herschreven. Verouderde Bootstrap-tabs en kale formulierlabels vervangen door:
    - Gebruikers-headerkaart met avatar-initialen (blauw cirkel), naam, e-mailadres en uitlogknop.
    - Pill-stijl tabbladennavigatie (`.vu-tab-btn`) passend bij de rest van het thema — actief tab in blauw (`#297d99`), hover in lichtblauw.
    - Alle formuliervelden gebruiken nu `form-floating`, consistent met de checkout-pagina's.
    - E-mailveld vervangen door een alleen-lezen `#e1f2f7`-infoblok.
    - Inschrijvingen en facturen worden nu getoond als stijlvolle kaarten met `#fef3ee`-achtergrond in plaats van kale Bootstrap-tabellen.
    - Lege staten met vriendelijke melding en call-to-action naar het cursusaanbod.

- **Cursusblok — Hartje-favorietenknop werkt nu**: De hart-SVG in het horizontale cursusblok was puur decoratief (geen `<a>`-tag). De SVG is nu omsloten met een link naar `/favorieten/add/{id}`, zodat klikken op het hartje de cursus aan de favorieten toevoegt.

- **Student-portaal — Tab "Mijn Favorieten" toegevoegd aan accountdashboard**: Het accountdashboard toont nu een vierde tab met de opgeslagen favorieten van de student. Per favoriet wordt het cursusafbeelding (indien aanwezig), de cursustitel als link en een "Bekijken"-link getoond, plus een knop om de favoriet te verwijderen. Bij geen favorieten verschijnt een lege staat met een call-to-action naar het cursusaanbod.

- **Type- en marketinglabels als pill-badges**: De cursusvorm (`type`) en marketingtekst (`highlight_text`) worden nu getoond als stijlvolle pill-badges naast de cursustitel, op alle plekken waar cursussen worden weergegeven (cursusblok, horizontaal blok, cursuspagina). Het type-label heeft een oranje stijl (`#D16941` tekst, `#FEF3EE` achtergrond), het highlight-label een blauw-groen stijl (`#297D99` tekst, `#EBF6FA` achtergrond). De labels zijn niet klikbaar.
- **Programma-keuzelijst — Meer ruimte tussen opties**: Tussen de radio-knoppen voor programmaselectie op de cursuspagina is nu een marge van 8px toegevoegd voor betere leesbaarheid.
- **Hoofdcollectie — Cursussen gesorteerd op volgorde**: In de hoofdcollectie-weergave worden de cursussen per subcollectie (max. 4) nu gesorteerd op de ingestelde volgorde uit de `collection_items` pivottabel, in plaats van alfabetisch op titel.
- **Online/Locatie-badges — Nieuwe kleuren**: De "Online"-badge heeft nu kleur `#297D99` (was `#37a7cc`) en de "Locatie"-badge heeft nu kleur `#B9542D` (was `#F58357`). De inline stijlen zijn vervangen door CSS-klassen.
- **Programma-statuslabels — Nieuwe prioriteitslogica en stijl**: De statuslabels in de programma-keuzelijst op de cursuspagina zijn volledig vernieuwd. In plaats van generieke knopstijlen worden nu gekleurde pill-badges getoond op basis van de volgende prioriteitsvolgorde: **Laatste kans** (start binnen 7 dagen), **Laatste plekken** (≤ 2 plekken over), **Instromen** (al gestart), **Wachtlijst**, **Verwacht** (voorinschrijving), **Start zeker** (definitief), **Open**, **Gesloten**. Elke status heeft een eigen kleurstelling.
- **Checkout stap 3 — "Later te betalen €0" bij factuurbetalers**: In het besteloverzicht werd de regel "Later te betalen" ook getoond bij klanten die volledig op factuur betalen, met een bedrag van €0. Deze regel wordt nu alleen getoond wanneer er daadwerkelijk een resterend bedrag te betalen is.
- **Checkout stap 1 — Zakelijke bestelling verplichte velden**: Bij het aanvinken van "Dit is een zakelijke bestelling" zijn de volgende velden nu verplicht: Bedrijfsnaam, E-mailadres, Bedrijfsadres, Postcode en Plaatsnaam. De velden tonen een `*` zodra het checkbox wordt aangevinkt en worden automatisch verplicht/niet-verplicht bij het aan- en uitvinken.
- **Checkout stap 2 — Cursusinformatie in rechterkolom**: In de rechterkolom van stap 2 (deelnemersgegevens) wordt per inschrijving nu de **startdatum**, **start- en eindtijd van de eerste les** en de **locatienaam** getoond in plaats van de programmacode en startdatum
- **Header — Gebruikersicoon naar student-dashboard**: Het gebruikersicoon in de header linkt nu naar `/student/dashboard` wanneer de bezoeker al ingelogd is als student, en naar `/student/login` wanneer dat niet het geval is.
- **Header — Mobiel menu: hoofdcategorieën klikbaar**: In het mobiele menu waren de hoofdcategorieën (niveau 2) niet klikbaar als link — een klik opende direct de subcategorieën. Nu zijn de categorienamen volwaardige links, en is er een apart pijl-icoontje toegevoegd om de subcategorieën te openen. Op desktop is het gedrag ongewijzigd.
- **Labels — Lettergrootte verhoogd naar 14px**: De font-size van alle pill-badge labels is verhoogd van 12px naar 14px. Dit geldt voor de programma-statuslabels (`.program-label`), de type- en highlight-tags (`.tags ul li span`) en de Online/Locatie-badges (`.online-block`).
- **Programma-keuzelijst — Blauwe container ook bij één programma**: De blauwe omlijsting rondom de programmaselectie werd eerder alleen getoond bij meer dan één programma. De conditie is aangepast naar `>= 1`, zodat de container ook getoond wordt wanneer er precies één programma is.
- **Programma-keuzelijst — Geen marge onder laatste rij**: Op mobiel had het laatste programma-item nog een `padding-bottom` vanwege de flex-column layout. Dit is gecorrigeerd: het laatste item heeft nu `padding-bottom: 0` en `margin-bottom: 0`.
- **Cursus- en collectiepagina's — Extra marge boven titel op kleine schermen**: Op schermen smaller dan 430px had de paginatitel te weinig ruimte boven zich. Het `@media (max-width: 430px)` blok in `responsive.css` geeft nu `margin-top: 50px` aan zowel `.modern-course-detail-wrp .main-title` (cursuspagina) als `.about-course-details .main-title` (collectiepagina's).
- **Nieuws, docenten en locaties — Afbeeldingen klikbaar**: De kaartafbeeldingen op de nieuws-, docenten- en locatiepagina's zijn nu aanklikbaar als link, net als bij cursussen. Nieuws en docenten linken naar de detailpagina; locaties linken naar Google Maps. Aangepast in `blog_post.blade.php`, `teacher_index.blade.php`, `includes/teacher_index.blade.php`, `location_index.blade.php` en `includes/location_index.blade.php`.
- **Cursuskaarten — Programma-statuslabel op index en sliders**: Op cursuskaarten (slider-blok en horizontaal blok in de cursusoverzichtspagina) wordt nu rechts van de prijs een statuslabel getoond — exact dezelfde pill-badge stijl als de programma-statuslabels op de cursuspagina. Logica: bij één actief programma wordt het programma-statuslabel overgenomen ("adopt program-status"). Bij meerdere actieve programma's geldt een marketingprioriteit: **Laatste kans** (start binnen 7 dagen) → **Laatste plekken** (≤ 2 plekken vrij) → **Start zeker** (definitief gepland) → **Wachtlijst** (enkel wachtlijst beschikbaar). "Gesloten" en "Open" worden bewust niet getoond op kaarten.
- **Header — Megamenu JavaScript herschreven**: Het ingebedde script in de megamenu-component bevatte een JavaScript-syntaxfout (niet-afgesloten `forEach`- en `DOMContentLoaded`-callbacks), waardoor het volledige script faalde. Bijkomende problemen: de uitklap-knop toonde het doelpaneel niet, en de "Terug"- en dropdown-reset-listeners werden bij elke klik opnieuw geregistreerd. Alle callbacks zijn nu correct afgesloten, de paneel-wisseling (toon niveau 3, verberg niveau 2) zit in de expand-handler, en de back-/reset-listeners worden eenmalig geregistreerd bij `DOMContentLoaded`. Op mobiel wordt de `list-group-wrp` ook direct bij het laden verborgen zodat altijd het juiste niveau 2 zichtbaar is.
- **Bedrijfsfactuur e-mail (template 12) — Besteloverzicht toegevoegd**: De e-mail naar het bedrijf bevat nu automatisch een overzichtstabel met alle inschrijvingen (cursus, deelnemer, bedrag) en eventuele producten, inclusief het totaalbedrag. Bij termijnbetalingen wordt het eerste termijnbedrag getoond met een toelichting. Daarnaast zijn extra variabelen beschikbaar voor de e-mailtemplates in Backpack: `$order` (het volledige order), `$order->total`, `$order->totalpaid` en `$payment_url` (de betaallink).
- **Collectie- & cursuspagina's — Actieve filterpills zichtbaar op mobiel**: Op mobiel werden de actieve filterpills (geselecteerde cursusvorm, dagdeel, dag, maand, locatie, enz.) alleen getoond binnen het filteroverlay-paneel. Ze zijn nu ook zichtbaar buiten het overlay, direct onder de "Filteren"-knop. Op desktop zijn de pills ongewijzigd zichtbaar in het vaste filterpaneel links.

---

## Week van 4 tot 10 mei 2026

### ✨ Nieuw & Verbeterd

- **Beveiligingssysteem — Automatische IP-blokkering bij aanvalspogingen**: Het platform detecteert nu bekende kwetsbaarheidsscans en hackaanvallen en blokkeert aanvallende IP-adressen automatisch.
  - **Aanvalspatronen**: ruim 70 bekende aanvalspaden worden herkend
  - **Auto-blokkering**: een IP-adres dat binnen 60 minuten 5 of meer aanvalspogingen doet, wordt automatisch permanent geblokkeerd.
  - **Marketing Dashboard — Beveiligingsoverzicht**: het marketing dashboard toont nu een beveiligingssectie met aanvalsstatistieken (totaal, unieke IPs, auto-geblokkeerd in de periode), de lijst van alle geblokkeerde IP-adressen met reden, type (auto/handmatig) en status, en een formulier om IPs handmatig te blokkeren of deblokkeren.
  - **Marketing Dashboard — 404-pagina's**: aanvalsverzoeken in de 404-tabel worden rood gemarkeerd met een ⚠-icoon en een badge met het totaal aantal aanvalsverzoeken in de geselecteerde periode.
- **Gespreide betaling (termijnen) — Checkout stap 2**: Cursussen kunnen voortaan worden aangeboden met de mogelijkheid om in termijnen te betalen. Dit is per cursus instelbaar via het admin-panel (veld "Termijnbetaling").
  - In **stap 2 van het afrekenproces** (deelnemersgegevens) verschijnt automatisch een keuzelijst bij cursussen die termijnbetaling ondersteunen — maar alleen wanneer **niet op factuur** betaald wordt.
  - De opties zijn: **"Betaal het volledige bedrag"** of **"Betaal in X delen"** (waarbij X het aantal termijnen is dat voor die cursus is ingesteld).
  - De gekozen betaaloptie wordt opgeslagen per inschrijving en werkt door in de **overzichtspagina** (stap 3), waar het te betalen bedrag dienovereenkomstig wordt aangepast.
  - Bij betaling via Mollie wordt het correcte termijnbedrag doorgestuurd.
  - Bij hernavigatie naar stap 2 wordt de eerder gemaakte keuze automatisch teruggezet.


### 🐛 Bugfixes

- **Blog-pagina geeft 404 bij thema zonder blogweergaven**: Op thema's die geen blogweergaven bevatten (zoals Utrecht) gaf de blog-index en detailpagina een 500-fout (`View [blog_index] not found`). De `BlogController` controleert nu eerst of de view bestaat en retourneert een nette 404 als dat niet het geval is.

- **Menuitems met pad als waarde gaven 500-fout**: Menuitems van het type `internal` waarbij de waarde een URL-pad is (bijv. `collectie/zomerweken`) in plaats van een routenaam veroorzaakten een `RouteNotFoundException` en crashten de pagina. `VuMenuItem::url()` vangt deze uitzondering nu op en behandelt de waarde als een URL-pad.

- **Betaallink-command crasht bij verwijderde cursus**: Het `vu:paymentlinks` Artisan-commando crashte met `Attempt to read property "firstname" on null` wanneer een orderregel verwees naar een cursus die niet meer bestaat. Het commando slaat zulke orderregels nu over en logt een waarschuwing.

### 🎨 Thema-updates Amsterdam

- **Cursuskaarten — Titel toont maximaal 3 regels**: De cursustitel op cursuskaarten (aanbodoverzicht) wordt nu afgekapt na **3 regels**, met een ellipsis voor langere titels. Eerder werd 2,5 regel getoond.

- **Footer nieuwsbrieflabels — Betere uitlijning**: De labels in de nieuwsbriefinschrijfformulier in de footer waren te laag gepositioneerd. Ze worden nu correct verticaal gecentreerd in het invoerveld.

- **Cursusdetailpagina — Startdatum toont tijd van eerste les**: Bij de selectie van een startdatum op de cursusdetailpagina wordt nu naast de datum ook de **begin- en eindtijd van de eerste les** getoond (bijv. `12-05-2026 09:00–11:00`). De programmatitel is verwijderd uit dit overzicht. 


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

### ✨ Nieuw & Verbeterd

- **Financial Dashboard**: Nieuw dashboard op `/admin/financial` voor een financieel overzicht per grootboekrekening.
  - **Omzet per Grootboekrekening**: Toont gefactureerde bedragen per grootboek (cursusinschrijvingen én productverkopen), uitgesplitst naar BTW-tarief, met kolommen excl. BTW, BTW-bedrag en incl. BTW.
  - **Betalingen per Grootboekrekening**: Toont ontvangen betalingen per betaalmethode/grootboek (op basis van `payment_methods.grootboeknummer`), inclusief terugbetalingen en nettobedrag.
  - **BTW Overzicht**: Volledige BTW-splitsing per tarief — zowel gefactureerd als ontvangen, excl./BTW/incl. naast elkaar.
  - **Omzet per dag**: Lijndiagram (Chart.js) met dagelijkse ontvangen omzet incl. en excl. BTW.
  - **Openstaande Posten**: Overzicht van alle onbetaalde facturen, ingedeeld in leeftijdsbuckets (0–30, 30–60, 60–90, >90 dagen) met kleurcodering.
  - **Datumfilter**: Datumkiezer met snelknoppen (7d, 30d, deze maand, vorige maand, dit jaar). Standaard ingesteld op de huidige maand.

- **Opruimen achter de schermen**:
  - **Producten krijgen altijd een unieke webadres**: Twee producten met dezelfde naam kregen soms hetzelfde webadres, waardoor één van de twee niet bereikbaar was. Dit wordt nu automatisch voorkomen.
  - **Verouderde en ongebruikte onderdelen verwijderd**: Een aantal velden en opties die nooit in gebruik zijn genomen zijn opgeruimd. Dit heeft geen invloed op de werking van de site, maar houdt het systeem overzichtelijk en sneller.

### 🐛 Bugfixes

- **Eigen profiel kon niet worden opgeslagen**: Beheerders zonder het "Gebruikers"-recht kregen een foutmelding bij het opslaan van hun eigen profiel. Je kunt nu altijd je eigen naam, e-mailadres en wachtwoord aanpassen, ongeacht je rechten. Rollen en permissies blijven uiteraard alleen bewerkbaar voor beheerders met het juiste recht.

- **Fout bij aanmaken nieuw programma**: Bij het aanmaken van een nieuw programma stond de cursus-dropdown automatisch op de eerste cursus uit de lijst. Dit zorgde voor fouten als die selectie niet klopte. De dropdown start nu leeg en je moet bewust een cursus kiezen voordat je het programma kunt opslaan.

- **Verlaten winkelwagen e-mail crashte**: E-mailsjabloon 25 (verlaten winkelwagen) bevatte een verwijzing naar `$order`, maar de verlaten-winkelwagen-mail (`Cartleftmail`) stuurde deze variabele niet mee. Het sjabloon moet `$cart` gebruiken in plaats van `$order`.

- **Marketing Dashboard: fout bij docenten in populaire pagina's**: De kolom `display_name` is eerder verwijderd uit de `teachers`-tabel (samengevoegd met `name`). Het dashboard probeerde die kolom nog op te halen. De query haalt nu `name` én `lastname` op en zet deze samen tot de volledige naam — identiek aan het `fullname`-attribuut op het Teacher-model.

- **Bevestigingse-mail bij directe plaatsing werd dubbel verstuurd (Westvoorne)**: Bij directe plaatsing (geen Mollie-betaling) en na de Mollie-webhook werd de bevestigingse-mail twee keer verstuurd. De dubbele aanroepen zijn verwijderd; de model observer handelt dit nu volledig af.

### 🎨 Thema-updates

- **Westvoorne — Filters cursusoverzicht en collectiepagina's werken nu correct**:
  - **`beschikbaar` → `available`**: De filterdropdown had de verkeerde parameternaam (`beschikbaar`), waardoor dit filter volledig werd genegeerd door de backend. Hernoemd naar `available`.
  - **Geselecteerde categorie blijft zichtbaar**: De collectie-dropdown toonde nooit de actief geselecteerde optie — `selected` attribuut toegevoegd.
  - **Locatiefilter toegevoegd**: De `$locations`-variabele werd al door de controller meegegeven maar nooit getoond. Een locatiedropdown (op stad) is nu zichtbaar in het filter.

---

## Week van 20 tot 26 april 2026

### ✨ Nieuw & Verbeterd

- **Dashboard globaal zoeken**: Op het beheer-dashboard is een real-time zoekbalk toegevoegd waarmee direct in meerdere objecttypen gezocht kan worden. Resultaten verschijnen terwijl je typt; klikken op een resultaat gaat direct naar de beheerpagina van het object.

  - **Zoekt in**: Cursisten (naam, e-mail), Programma's (code, titel), Cursussen (titel), Inschrijvingen (naam/e-mail cursist én programmacode), Facturen (factuurnummer, Mollie-betalingskenmerk), Pagina's (titel, slug), Collecties, Producten, Locaties, Docenten, Productverkopen (naam cursist), Blog artikelen (titel).
  - Per objecttype worden maximaal **10 meest recent bijgewerkte** resultaten getoond.
  - **Meerdere zoekwoorden**: Bij cursussen en pagina's kunnen meerdere woorden worden ingevoerd (volgorde maakt niet uit) — alle woorden moeten voorkomen in de titel.
  - **Voornaam + achternaam**: Cursisten zijn ook vindbaar door voor- én achternaam te combineren.
  - **Hoofdletterongevoelig**: Zoeken op "jan" vindt ook "Jan" en "JAN".
  - **Alleen objecten waartoe je toegang hebt**: De zoekresultaten houden rekening met je rechten — je ziet alleen objecttypen die je ook in het menu kunt beheren.
  - De zoekbalk staat bovenaan het dashboard, boven de KPI-widgets.

- **Marketing Dashboard — Uitbreidingen**:
  - **Verwijzende domeinen**: Top 25 externe domeinen die bezoekers naar de site stuurden, met het aantal bezoeken. Het eigen domein en IP-adressen worden automatisch uitgesloten. Domeinen zijn klikbaar.
  - **Docentnamen in populaire pagina's**: `/docent/*`-URLs tonen nu de naam van de docent in plaats van de URL.
  - **Collectietitels in populaire pagina's**: `/collectie/{slug}`-URLs tonen nu de collectienaam in plaats van de URL. Meertalige titels (JSON) worden als Nederlandse naam getoond.
  - **Klikbare titels in populaire pagina's**: Elke rij is nu een klikbare link naar de volledige URL.
  - **Cursustitels via slug-fallback**: Bezochte cursuspagina's zonder `?program_id=` worden nu alsnog op naam getoond via slug-opzoeking.
  - **E-mailstatistieken verwijderd**: De "Verstuurde e-mails per sjabloon"-kaart is verwijderd.
  - **Preset datumbereiken**: Zes snelkoppelingen toegevoegd: **7 d**, **30 d** (standaard actief), **90 d**, **Deze maand**, **Vorige maand** en **Dit jaar**.
  - **404-pagina's kaart**: Top 25 URLs die een 404-fout veroorzaakten. Gebaseerd op een nieuwe `not_found_logs`-tabel (`2026_04_25_100002`). `App\Exceptions\Handler` logt voortaan de originele URL; nieuw model `NotFoundLog`.
  - **Zoekopdrachten op de site**: Top 25 zoektermen ingevoerd via `?q=` op de publieke website, live uit `page_visits.url`.
  - **`/404` uitgesloten van populaire pagina's**: naast de bestaande uitsluiting van `cart/*`.
  - **UTM-filterrij als Bootstrap-grid**: De vier UTM-filterdropdowns zijn opgemaakt als `row g-2` met elk een `col-3` kolom.
  - **Array-filters**: Alle dashboard-methoden accepteren nu `array $filters` met `sources`, `mediums`, `campaigns` en `terms`. Nieuw: `scopeForUtmFilters()`, `filterItemsByUtm()` en `getFilterOptions()`.
  - **E-mails gegroepeerd op sjabloon-ID**: Één rij per sjabloon; naam is de `action_description`.
  - **`cart/*`-pagina's uitgesloten van populaire pagina's**.
  - **Populaire pagina's: filter op type**: Filterknoppen Alle / Pagina's / Cursussen / Collectie.
  - **UTM én MTM (Matomo) parameters correct verwerkt**: `TrackPageVisit` slaat ook `mtm_*`-parameters op als fallback; `utm_medium = cpc` is de enige definitie van betaald verkeer; `utm_source = newsletter` nooit als betaald.
  - **Bronfilter correct**: `scopeForSource` condities verpakt in sluitingen zodat AND/OR-logica klopt.

- **Marketing Dashboard — Eerste versie**: Nieuw dashboard op `/admin/marketing` voor marketeers (recht `Marketing Dashboard`), met bezoekers, paginaweergaven, conversies, omzet, verkeersbronnen, apparatuur, campagnes, zoektermen, populaire pagina's, populaire cursussen en e-mailstatistieken. Paginabezoeken worden bijgehouden via nieuwe `TrackPageVisit`-middleware en `page_visits`-tabel (`2026_04_25_000001`). E-mails koppelbaar aan sjabloon via `emailtemplate_id` op `emaillogs` (`2026_04_25_000002`). Permissie aangemaakt via migratie (`2026_04_25_000003`). Attributie-opslag als gestructureerd object; `AttributionHelper::parse()` herkent beide formaten. Dashboard herschreven naar vanilla JS (geen Alpine.js).

- **E-mailsjablonen — Automatisch UTM-tagging van knoplinks**: Bij opslaan worden `utm_source=VUadmin`, `utm_medium=email`, `utm_campaign` en `utm_term` automatisch toegevoegd aan `action_link` als deze nog geen UTM-parameters bevat. Idempotent; pure Blade-expressies worden niet gewijzigd.

- **Zoekresultaten — Producten in cursuszoekresultaten**: Bij `?q=` op `/cursussen` worden nu ook actieve producten doorzocht (titel, beschrijving, intro). Cursussen en producten worden samengevoegd en alfabetisch getoond via `item_type`-tag.

- **CMS contentblokken: configureerbare velden en crop-verhouding per bloktype**: Drie nieuwe vlaggen (`has_video`, `has_text`, `has_order`) bepalen welke velden beschikbaar zijn. Per bloktype instelbare crop-verhouding voor afbeeldingen (bijv. `1.78` voor 16:9).

- **Winkelwagen bericht bij producten**: Veld toegevoegd op producten (tabblad "Basis"); getoond in de winkelwagen bij toevoeging.

- **Cultuurconnectie: meerdere disciplines per collectie**: Enkelvoudige kolom vervangen door pivot-tabel `collection_discipline`; select2-meervoudige keuzelijst in het beheer.

- **Statusmails bij checkout nu volledig werkend**: Wachtlijst-mail (template #1) en nieuwe controle-mail (template #32, migratie `2026_04_21_000001`) worden nu correct verstuurd.

- **Aparte koper-bevestigingsmail (template #33)**: Na Mollie-bevestiging ontvangt de koper een eigen overzichtsmail (`SendBuyerConfirmation`, migratie `2026_04_21_000002`) met alle inschrijvingen en producten. Deelnemers ontvangen nog steeds de individuele `SendConfirmation`-mail.

- **Productbestelling verwerkt-mail (template #34)**: Bij status "Verwerkt" op een productverkoop ontvangt de student automatisch een bevestigingsmail (`ProductProcessed`, migratie `2026_04_21_000003`).

- **Uitnodigingen ook verstuurd aan studenten met toekomstige inschrijving**: Beperking verwijderd uit `vu:dailymails`.

- **Winkelwagen-teller correct bij gecached menu**: Badge dynamisch bijgewerkt via `GET /cart/count` bij elke paginalading (alle thema's).

- **Mobiel submenu Utrecht — navigatie en uitklappen gesplitst**: Aparte `<button class="submenu-toggle">` naast menu-items met submenu; link navigeert, knop klapt open.

- **Inactieve docenten uitgesloten van docentenrapportage**.

- **Productverkopen-beheer verbeterd**: Preview-knop en "Aangemaakt"-kolom verwijderd; kolomselectie en exportknoppen (CSV/Excel/PDF) toegevoegd.

### 🐛 Bugfixes

- **`TrackAttribution`: array-naar-string-conversie**: Bij `?utm_source[]=foo` retourneerde `$request->get()` een array; string-interpolatie crashte. UTM- en MTM-loops slaan array-waarden nu over.

- **E-mailsjabloon `action_link` te lang voor kolom**: Kolom vergroot naar `TEXT` via migratie `2026_04_25_140000`. `autoTagActionLink()` herkent nu ook Matomo-URL's als reeds getagd.

- **Typefout in `SendBuyerConfirmation` en `ProductProcessed`**: Property-typedeclaraties verwijderd; `Queueable` en `SerializesModels` traits toegevoegd.

- **"Alle cursussen"-link rechts uitgelijnd (Amsterdam)**: Link op collectie-overzichtspagina via Bootstrap `text-end`.

### 🎨 Thema-updates

- **Amsterdam — Diverse fixes**:
  - Mobiel zoekformulier: correcte `action`, `method` en `name`.
  - CTA halfbreed — mobiel: Bootstrap grid-stacking; cirkel vergroot naar 185×185px.
  - Sortering cursusoverzicht: `?sort=` nu correct toegepast vóór `$allItems`.
  - Nieuwsslider: gelijke hoogte via flexbox; "Lees meer"-knop altijd onderaan.
  - `.basic-details p`: `margin-bottom: 0`.
  - Passieve event listener fout (Slick) opgelost.
  - `.online-offer-title-block`: inline stijl naar CSS; op mobiel `min-height: 5em`.
  - Statustag cursusblok: `<a href="#">` vervangen door `<span class="btn-red-border">`.
  - Megamenu mobiel: container breedte, grid-breakpoint, lege panelen en lettertypes gecorrigeerd.

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



### Voor gebruikers (kort en eenvoudig)

- Je winkelwagen blijft nu behouden wanneer je inlogt — items die je als gast toevoegt blijven staan na inloggen.
- Wachtlijst- en "seintje"-formulieren op de cursuspagina werken betrouwbaar en tonen direct een bevestiging nadat je je hebt aangemeld.
- Collecties en producten tonen nu consequent dezelfde gekoppelde items; als een product in een collectie staat, zie je dat overal terug.
- Bij grote importen van cursisten worden niet per ongeluk welkomsmails naar iedereen gestuurd — e-mails worden alleen verzonden bij echte inschrijvingen.


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

