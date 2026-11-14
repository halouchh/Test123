# Woordenzee: Grand Adventure Crew

Een spellinggame voor kinderen van ongeveer 9 jaar. De speler is kapitein, ontdekt zes eilanden en verdient munten, schatten en crewleden door woorden goed te schrijven. Geen tijdsdruk, geen straffen.

## Wat zit er in deze map?

| Bestand | Waarvoor |
|---|---|
| `index.html` | De complete app in één bestand. Dit is alles wat u nodig hebt om te spelen. |
| `manifest.webmanifest`, `sw.js`, `icon-*.png` | Maken de app installeerbaar en offline bruikbaar wanneer hij op een https-adres staat. |
| `HANDLEIDING-OUDERS.md` | Korte handleiding voor ouders. |
| `CONTROLEVERSLAG.md` | Wat getest is, hoe, en wat de bekende beperkingen zijn. |

## Snelste manier per toestel

### Windows-pc of Mac
1. Pak de ZIP uit (rechtermuisknop › Alles uitpakken).
2. Dubbelklik op `index.html`. De app opent in uw browser (Chrome, Edge of Safari).
3. Klaar. De voortgang wordt in die browser bewaard.

### iPhone en iPad (belangrijk)
iOS kan een los HTML-bestand uit de app Bestanden **niet** als werkende app openen (u ziet alleen een voorbeeldweergave zonder werkende knoppen). Op iPhone en iPad moet de app daarom op een **https-adres** staan. Dat is eenmalig vijf minuten werk, zie "Online zetten" hieronder. Daarna:
1. Open het adres in **Safari**.
2. Tik op de deelknop (vierkant met pijl) › **Zet op beginscherm**.
3. Start de app voortaan via het icoon. Hij werkt dan ook zonder internet.

### Android-telefoon en -tablet
Ook hier is een https-adres de betrouwbare weg:
1. Open het adres in **Chrome**.
2. Tik op de drie puntjes › **App installeren** of **Toevoegen aan startscherm**.
3. Start de app via het icoon. Hij werkt dan ook zonder internet.

(Een los HTML-bestand openen via een bestandsbeheer-app lukt op sommige Android-toestellen, maar niet op alle. Reken er niet op.)

## Online zetten (https), zonder programmeren

Kies één van de twee:

**A. Netlify Drop (geen account nodig om te proberen)**
1. Ga op een pc naar `https://app.netlify.com/drop`.
2. Sleep de uitgepakte map `woordenzee` in het venster.
3. U krijgt een https-adres. Open dat adres op telefoon of tablet.
   Maak een gratis account aan om het adres blijvend te houden.

**B. GitHub Pages (als de bestanden al in een GitHub-repository staan)**
1. Open de repository op github.com › **Settings** › **Pages**.
2. Kies bij "Branch" de branch waarin de map `woordenzee` staat en klik **Save**.
3. Na een paar minuten staat de app op `https://<gebruikersnaam>.github.io/<repository>/woordenzee/`.
   Let op: bij een gratis GitHub-account moet de repository hiervoor openbaar zijn.

## Voortgang en meerdere toestellen

- Alles wordt **lokaal** bewaard: op dat ene toestel, in die ene browser.
- Er is **geen automatische synchronisatie** tussen toestellen.
- Overzetten gaat via **Ouders › Back-up**: exporteren op toestel A, importeren op toestel B.
- Wie de browsergegevens wist (of op iPhone de app lang niet gebruikt in Safari zonder hem op het beginscherm te zetten), kan de voortgang kwijtraken. Maak af en toe een back-up.

## Geluid

- Er zijn geen audiofragmenten meegeleverd. De app leest woorden voor met de **Nederlandse voorleesstem van het toestel** (nl-NL of nl-BE).
- Ouders kunnen per woord een **eigen opname of audiobestand** koppelen. Dat gaat dan vóór de voorleesstem.
- Heeft een toestel geen Nederlandse stem, dan schakelt de app over op **kijk, verberg en schrijf**.
- Staat het toestel op stil (schuifje op iPhone), dan hoort u de voorleesstem mogelijk niet.

## Ondersteunde browsers

Recente versies van Safari (iOS/iPadOS/macOS), Chrome (Android/Windows/Mac) en Edge (Windows).
