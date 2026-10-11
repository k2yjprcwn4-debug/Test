# ATLET 105 · Opdatering V3 — gem historikken og se videoer

## Vigtigst: Du HAR allerede appen i GitHub

**Opret ikke et nyt repository, og slet ikke appikonet på iPhonen.** Opdater i det eksisterende `Test`-repository på GitHub, hvor Pages allerede virker.

1. **Sikkerhedskopiér først dine data.** Åbn ATLET 105 i den installation, hvor dine gamle træningsresultater vises (Safari eller hjemmeskærmsapp). Vælg **Indstillinger → Eksportér data**, og gem JSON-filen i *På min iPhone*. Hvis dine gamle data kun ses i Safari, skal du eksportere i Safari. Safari-fanen og hjemmeskærmsappen deler ikke altid lager.
2. På din Windows-pc: pak V3 ZIP-filen ud.
3. Åbn dit GitHub-repository **Test**. Upload **index.html** og **sw.js** som erstatning for de eksisterende filer. Hvis GitHub ikke tilbyder overskrivning ved upload, kan du åbne filen i GitHub, vælge redigering (blyant) og indsætte hele indholdet fra den nye fil, eller slette den gamle fil i repositoryet og derefter uploade en ny (det påvirker ikke din lokale browserlagring, så længe URL'en er den samme).
4. Upload også opdateret `START-HER.md`, hvis du ønsker vejledningen liggende i repositoryet. `manifest.webmanifest` og de to appikoner er uændrede.
5. Klik **Commit changes**. Vent 1–3 minutter til GitHub Pages er blevet opdateret. Åbn appen fra det **samme** iPhone-ikon, ikke fra en ny adresse. Mens du er online, luk og genåbn appen (eventuelt to gange), så service worker kan skifte til V3.
6. Du skal **ikke** vælge "Føj til hjemmeskærm" igen; hold fast i det eksisterende ikon. Tjek, at der står **V3** øverst i appen.
7. Kontrollér under **Udvikling**, at din gamle historik stadig er der. Hvis den mangler, så **importér den JSON-backup, du tog i trin 1**, i den appinstallation du vil bruge fremover.

## Hvorfor forsvandt mine opdateringer?

V2 lagrede afsluttede træninger og dagens valg i localStorage, men ikke et påbegyndt pas. V3 gemmer derfor også uafsluttede pas, automatisk hvert ca. 5. sekund når timeren kører, og når appen går i baggrunden. V3 forsøger desuden at gemme en ekstra kopi i IndexedDB og viser en synlig gemmestatus. Alt dette ligger på telefonen.

Særligt på iPhone kan Safari og en installeret PWA have separate datalagre. Vælg helst at åbne **hjemmeskærmsikonet** hver gang; eksportér/importér, hvis du vil flytte data fra Safari.

Lokalt webapp-lager er ikke en garanteret, permanent databasetjeneste. iOS kan slette data efter lagerpres, hvis du rydder webstedsdata, eller ved sletning af webappen. Tag derfor jævnligt backup i JSON. Ingen login og ingen serverdatabase bruges.

## Videoer

V3 indeholder **indbyggede videofelter til armbøjninger og squats**, hentet fra frit tilgængelige kilder på Wikimedia Commons. De skal åbnes med internetforbindelse og er endnu **ikke** pakket offline ind i ZIP-filen. Teknikteksten under videoen bestemmer den valgte variant; en demonstration af gulvarmbøjning svarer ikke til vægarmsbøjning. De øvrige øvelser bruger fortsat skitser.

Klipkilder og ophav:
- Armbøjninger: US Centers for Disease Control and Prevention, public domain (US federal government). https://commons.wikimedia.org/wiki/File:Muscle_Strengthening_at_Home_-_Push-ups.webm
- Squat: CRiles23, CC BY-SA 3.0. https://commons.wikimedia.org/wiki/File:Squats_Wikipedia.webm

Afspilning fra eksterne videokilder afhænger af kildernes drift og browserens videounderstøttelse. Ved fejl falder visningen tilbage til en lokal skitse. Det er en første opgradering, **ikke et komplet offline videobibliotek endnu**. Vi bør bruge konsistente, licenserede og teknikvaliderede clips til alle varianter inden denne del er færdig.

## Det der skal testes på din iPhone

1. Åbn fra hjemmeskærmsikonet, markér fx "Styrketræning i dag".
2. Luk appen helt. Åbn fra **samme ikon**: markeringen skal stadig være der.
3. Start Morgen, tryk "Næste" to gange. Luk og genåbn: det ufærdige pas skal vende tilbage fra det trin, du nåede.
4. Registrér en vejning under Udvikling. Luk og genåbn: vejningen skal stadig fremgå.
5. Tag backup: Indstillinger → Eksportér data.

## Om privatliv

GitHub Pages hoster appens **offentlige statiske kildekode** gratis. Ingen vægt-, styrke- eller træningsdata sendes til GitHub. Videoer hentes direkte fra deres eksterne kilde, som kan registrere normale netværksmetadata ved videoafspilning. Selve træningsappen og data fungerer uden video og internet, når PWA-filerne er installeret og cachelagret.
