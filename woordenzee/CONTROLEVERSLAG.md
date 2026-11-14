# Controleverslag

Datum: 14 november 2026

## Samenvatting

- 162 geautomatiseerde controles uitgevoerd, 162 geslaagd.
- Alle tests zijn gedaan in **Chromium (headless) met scherm- en aanraaksimulatie**.
- **Er is niets op een fysiek toestel getest.** Geen echte iPhone, iPad, Android-toestel of Windows-pc, en ook niet in echte Safari of Edge.

## Aangeleverd materiaal: woordenlijst en audio

- Bij de opdracht zat **geen woordenlijst en geen audio**. De repository bevatte alleen een niet-verwant `index.html`.
- Daarom bevat de app een **startlijst van 72 woorden** (6 eilanden × 12), zelf samengesteld rond spellingcategorieën van groep 5/6, elk met betekenis en voorbeeldzin.
- Controle van de startlijst: geen dubbele woorden, geen spaties voor of na, één schrijfwijze per woord. Er zijn geen aangeleverde woorden aangepast, want die waren er niet.
- Audio: de app gebruikt de Nederlandse voorleesstem van het toestel. Er zijn dus ook geen fragmenten gekoppeld of gecontroleerd.
- De eigen lijst kan via Ouders › Woorden › Woordenlijst plakken worden toegevoegd; audio per woord via opname of bestand.

## Wat is getest (gesimuleerd)

### Functionaliteit (desktop-venster 1366×768)
| Onderdeel | Resultaat |
|---|---|
| Zes eilanden op de kaart; 2 t/m 6 op slot bij de start; gesloten eiland opent niet | geslaagd |
| Eiland ontgrendelt na alle missies van het vorige; crewlid komt erbij | geslaagd |
| Woord wordt voorgelezen bij start; knoppen Luister, Langzaam, Hoor de zin | geslaagd (met nagebootste stem) |
| Goed antwoord, ook met hoofdletters of spaties eromheen | geslaagd |
| Hint 1 (aantal letters), hint verbergen/tonen | geslaagd |
| Hint 2 (eerste letter + goede letters groen) | geslaagd |
| 3e fout toont het woord; typen geblokkeerd tot het woord verborgen is | geslaagd |
| Met hulp opgelost komt op herhaallijst; zonder hulp is beheerst | geslaagd |
| Herhaalwoorden komen terug in volgende missie en in de Herhaal-missie; daarna beheerst | geslaagd |
| "Later nog eens" (overslaan), Stop-knop | geslaagd |
| Munten, schat per nieuwe missie, eindscherm | geslaagd |
| Bibliotheek: 72 woorden, zoeken, filters, betekenis, luisteren, eigen zin bewaren | geslaagd |
| Ouderslot (fout antwoord geweigerd, goed antwoord opent) | geslaagd |
| Woord toevoegen, aanpassen, verwijderen; dubbel woord geweigerd; lijst plakken | geslaagd |
| Audiobestand koppelen aan een woord (wav) en na herladen terugvinden | geslaagd |
| Voortgangsoverzicht en moeilijke woorden | geslaagd |
| Export als bestand (inhoud gecontroleerd, inclusief audio) en als tekst | geslaagd |
| Alles wissen, daarna import: woorden, voortgang en audio hersteld | geslaagd |
| Voortgang blijft na herladen | geslaagd |
| Offline herladen via de service worker | geslaagd |
| Openen als los bestand (`file://`) | geslaagd |
| Geen Nederlandse stem: kijk-verberg-schrijf als alternatief | geslaagd |
| Geen JavaScript-fouten tijdens de hele doorloop | geslaagd |

### Schermformaten (simulatie)
Op elk profiel zijn startscherm, kaart, eiland, oefenscherm, bibliotheek, crew, ouderslot en de vier oudertabbladen doorlopen. Gecontroleerd: geen horizontaal scrollen, alle knoppen minstens 44 px hoog, geen fouten.

| Profiel | Simulatie | Fysiek getest |
|---|---|---|
| iPhone 13 (staand en liggend) | geslaagd | nee |
| iPad 9e generatie, 810×1080 (staand en liggend) | geslaagd | nee |
| Android-telefoon (Pixel 5) | geslaagd | nee |
| Android-tablet (Galaxy Tab S4) | geslaagd | nee |
| Windows-pc 1366×768 en 1920×1080 | geslaagd | nee |

### Bestanden
- ZIP uitgepakt en geïntegreerd getest met `unzip -t`: geen fouten.
- `index.html` uit de ZIP opent en start.

## Niet getest

- Echte Safari (iOS, iPadOS, macOS) en echte Edge. De simulatie gebruikt de Chromium-engine met de schermmaten van die toestellen.
- De echte voorleesstemmen van iOS, Android en Windows (uitspraak, snelheid, beschikbaarheid). In de test is de stem nagebootst.
- Opnemen met de microfoon.
- Installeren op het beginscherm en het gedrag van de geïnstalleerde app.
- Delen via het deelmenu van iOS/Android.
- Toetsenbordgedrag op echte telefoons (schuiven van het scherm bij het typen).

## Bekende beperkingen en de praktische oplossing

| Beperking | Oplossing |
|---|---|
| iPhone/iPad opent een los HTML-bestand niet als werkende app. | Zet de map op een https-adres (README: Netlify Drop of GitHub Pages) en open dat in Safari. |
| Offline werken en installeren op het beginscherm werkt alleen vanaf https, niet vanaf een los bestand. | Idem. Op pc werkt het losse bestand wel gewoon, ook zonder internet. |
| De voorleesstem verschilt per toestel; sommige Android-toestellen hebben geen Nederlandse stem geïnstalleerd. | Stem installeren in de toestelinstellingen, eigen opnames koppelen, of de kijk-knop gebruiken. De app schakelt zelf over als er geen Nederlandse stem is. |
| Een voorleesstem kan klankgelijke woorden niet onderscheiden (bv. ei/ij). | Knop "Hoor de zin" leest de voorbeeldzin voor; eigen opname is het duidelijkst. |
| Hint 2 vergelijkt letters per positie. Bij een vergeten letter schuift alles op en worden weinig letters groen. | Hint 3 toont daarna het hele woord. |
| Opnemen in de app vraagt https en microfoontoestemming. | "Kies audiobestand" werkt overal. |
| Voortgang staat alleen lokaal; geen synchronisatie. Safari kan gegevens van weinig gebruikte websites na enkele weken wissen als de app niet op het beginscherm staat. | App op het beginscherm zetten en geregeld een back-up exporteren. |
| Downloaden van de back-up kan in een geïnstalleerde app op iOS mislukken. | "Deel" of "Toon als tekst" gebruiken. |
| Emoji-pictogrammen zien er per platform iets anders uit. | Geen actie nodig. |
