# VUAdmin Updates

## Week van 27 januari - 2 februari 2026

### ⚙️ Basis Platform Functionaliteiten
- **🏗️ Type Systeem Herstructurering**: Een fundamentele refactoring van het type systeem! Cursustypes, contracttypes, en andere type tabellen zijn samengevoegd tot één generiek Types systeem. Dit maakt het platform schaalbaar en eenvoudiger te beheren. Product types, locatie types, korting types en docent types zijn allemaal gestandaardiseerd.

- **📊 Evaluatie Systeem**: Een compleet nieuw evaluatie systeem is gelanceerd! U kunt nu evaluaties aanmaken, versturen en responses ontvangen. Inclusief:
  - Email template ondersteuning voor gepersonaliseerde evaluatie uitnodigingen
  - Automatische evaluatie generatie via scheduled commands
  - Frontend formulieren voor cursisten om evaluaties in te vullen
  - Response tracking in admin panel voor analyse
  - Hash-based veilige links voor anonieme evaluaties

- **📧 Rapport Notificaties**: Wanneer een rapport klaar is, ontvangt u nu automatisch een email met een download link. Geen handmatig checken meer of uw export klaar is! De email bevat directe toegang tot het gegenereerde bestand.

- **🔍 Email Verificatie API**: Nieuwe API endpoints toegevoegd voor email verificatie. Perfect voor integraties met externe systemen die moeten checken of een email al bestaat in het systeem.

- **📈 Export Verbeteringen**:
  - Null checks toegevoegd aan alle exports om crashes te voorkomen bij ontbrekende data
  - Nederlandse vertalingen worden nu gebruikt voor cursus titels in alle exports
  - Betere error handling in rapporten voor robuustere exports

- **🔗 Collectie Beheer Fixes**: Meerdere fixes voor het collectie systeem - 500 errors opgelost, betere weergave van cursussen en producten in de selector, en verbeterde array access voor properties.

- **🗑️ Database Opruiming**: Ongebruikte tabellen verwijderd (contract_types, course_types) na migratie naar het nieuwe Type systeem. Dit houdt de database schoon en performant.

- **🔄 Pivot Table Refactoring**: De course_product pivot table gebruikt nu een generiek 'type' veld in plaats van 'required', wat veel flexibeler is voor toekomstige uitbreidingen.

### 🎨 Theme Updates
- **Utrecht Theme**:
  - Evaluatie formulieren toegevoegd met submitted pagina
  - Late inschrijving optie voor al gestarte cursussen
  - NRTO keurmerk logo update
  - Vertalingsproblemen opgelost voor cursus weergave

- **Amsterdam Theme**:
  - "Seintje" (interesse) formulier toegevoegd - bezoekers blijven nu op dezelfde pagina na verzending
  - Wachtlijst formulier verbeterd - blijft ook op dezelfde pagina
  - Product weergave verfijnd met nieuwe type kolom
  - CSS updates voor betere styling van product relaties

- **Westvoorne Theme**:
  - Aangepast voor nieuwe teacher type structuur

---

## Week van 19-26 januari 2026

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
- **Breda Theme**: Nieuw menu systeem geïmplementeerd in de header voor betere navigatie en gebruikerservaring.

- **Amsterdam Theme**:
  - Volledig nieuwe betalingsformulier interface met moderne styling
  - Winkelwagen interface aangepast voor meerdere producten van hetzelfde type
  - Statspas korting verwijderd uit checkout stap 1 voor duidelijkere flow
  - Collectie filters volledig herzien met verbeterde UX
  - Nieuwe DM Sans lettertype familie toegevoegd voor een modernere uitstraling
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

