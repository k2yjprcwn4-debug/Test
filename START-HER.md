# ATLET 105 · Gratis PWA til iPhone

**Ingen abonnement, ingen database, ingen login.** Dette er en personlig træningsapp udviklet som fem statiske filer. Den kræver en HTTPS-webadresse til installation på iPhone, men de personlige trænings- og vægtdata bliver **kun gemt lokalt** i iPhonens webapp-lager.

## Kom i gang gratis via GitHub Pages (Windows-PC + iPhone)

1. Pak ZIP-filen ud på din Windows-PC. Mappen indeholder `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png` og `icon-512.png`.
2. Log ind eller opret en gratis konto på https://github.com/.
3. Åbn https://github.com/new og opret et **public** repository med navnet `atlet-105` (andet navn virker også). På GitHub Free kræver Pages et public repository.
4. Åbn repository, vælg **Add file → Upload files**, og upload **de fem filer til roden** af repository. Klik **Commit changes**. Upload ikke selve ZIP-filen.
5. Under **Settings → Pages → Build and deployment** vælg **Deploy from a branch**, `main` og `/ (root)`, og tryk **Save**. Vent på at GitHub viser din Pages-adresse.
6. Åbn den oplyste adresse i **Safari på din iPhone**. Brug **Del → Føj til hjemmeskærm**. Behold **Åbn som webapp** slået til, hvis valget vises.
7. Åbn **ATLET 105** fra hjemmeskærmen mens du er online første gang. Vent et øjeblik, så alle appfiler kan cachelagres. Prøv dernæst flytilstand: appen bør åbne og kunne bruges uden internet.

Typisk Pages-adresse: `https://DIT-BRUGERNAVN.github.io/atlet-105/` (erstat med adressen GitHub giver dig). Webhostingen er gratis på GitHub Free for public repositories. Du behøver hverken eget domæne, kreditkort eller Netlify.

## Hvordan fungerer appen?

- **I dag:** Vælg morgen (fokus på man/ons/fre, ellers lettere), aften eller minimumsdag. Marker, hvis du allerede styrketræner, løber eller har gener fra lænd/forfod, så intensiteten tilpasses.
- **Under et pas:** Trinvis skitse, teknikforklaring, lettere variant, timer, pauser og mulighed for at gå til næste trin manuelt.
- **Efter et pas:** Vurder passet som let, passende eller hårdt. To lette fokuspas giver et lille ekstra tillæg; et hårdt fokuspas reducerer den ekstra belastning. Dette er simple træningsregler, ikke en medicinsk optimeringsalgoritme.
- **Udvikling:** Log vægt, armbøjnings-test på samme støtteniveau samt planke-tid. Se vægtkurven og dine gennemførte pas.
- **Indstillinger:** Justér vægtmål og niveau, og eksporter/importer JSON-backup.

Det personlige udgangspunkt er cirka 120 → 105 kg og mere atletisk fysik. De 12 uger er den første træningsblok; appen lover ikke 15 kg vægttab på 12 uger. Pas er korte supplementer til målrettet styrketræning, løb og kost.

## Privatliv og datasikkerhed

- **Din træningshistorik, vægt, tests og indstillinger sendes ikke til GitHub eller nogen anden server.** De ligger i iPhones lokale webapp-lager (`localStorage`). Ingen analyser, cookies, tredjepartsbiblioteker eller eksterne kald er indbygget.
- **GitHub Pages er offentligt for appens kode og standardindstillinger.** Andre kan se selve appen og dens udgangsmål, men **ikke dine faktiske indtastninger**. Som ved andre websites kan hostingudbyderen registrere IP-adresse og normale tekniske adgangsoplysninger.
- Appen kan bruges offline, efter at Safari har hentet den og serviceworkeren har cachelagret filerne. Hvis du sletter appen/webstedsdata eller iOS rydder webappens lagring, kan historikken forsvinde.
- Tag derfor en **manuel backup** via Indstillinger → Eksportér data og gem JSON-filen i *På min iPhone*. Gem den ikke i iCloud Drive, hvis du ønsker, at også backupfilen kun ligger lokalt.
- Ingen påmindelser sendes, mens appen er lukket: det ville normalt kræve en push-server. Du kan oprette tidsbestemte påmindelser i iPhones Påmindelser-app uden at dele ATLET-data.

## Opdatering

Opdater de samme fem filer i repository, når du får en ny version. For ændret serviceworker-cache bør versionsnummeret i `sw.js` skiftes, så offline-cachen fornyes. Dine lokalt gemte data bevares normalt på samme webadresse. Hvis du skifter GitHub-brugernavn eller repository-navn, bliver det en anden adresse/lager; eksportér fra den gamle app og importér i den nye.

## Testet / begrænsninger

Brugerflow med træningspas, timertrin, feedback, vejning og styrketest er gennemtestet med mobilbredde i Chromium. Koden er statisk og JavaScript-syntaksen er verificeret. **Installationen på en fysisk iPhone og offline-caching i Safari er ikke testet i denne leverance**, så en faktisk enhedstest anbefales. Øvelsesillustrationer er enkle animerede skitser, ikke videooptaget teknikundervisning.

**Forsigtighed:** Brug kontrolleret teknik og cirka 2–3 gentagelser i reserve. Stop ved smerter, og vurder langvarige/forværrede lænde- eller forfodsgener med sundhedsfaglig rådgivning. Appen er ikke en medicinsk vurdering.
