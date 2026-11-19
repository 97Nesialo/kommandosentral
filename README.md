# Kommandosentralen v1.0

Gratis, privat og mobilvennlig PWA (Progressive Web App) med **7 moduler**:

1. Oversikt med nøkkeltall, grafer og fremdrift
2. Økonomi og NAV: budsjett, manuelle NAV-utbetalinger, gjeld og buffer
3. Skole: fag, oppgaver, notater og fremdrift
4. Bilverksted: vedlikehold, reparasjoner, anslåtte kostnader og EU-dato
5. Privatlærer: lokal norsk VG3-quiz med fasit og forklaringer
6. Planlegger: frister og avtaler (ingen bakgrunnsvarsler)
7. Gaming-lab og mål/trening: PS5/FC 27-notater, vaner og mål

## Start uten å betale

**Rask test på PC:** Pakk ut ZIP-filen og dobbeltklikk på `index.html`. Da virker hovedfunksjonene, men installering som app og offline-cache krever en HTTPS-nettside (eller localhost).

**Publiser gratis via GitHub Pages:**

1. Opprett gratis konto på https://github.com/ (om du ikke har konto).
2. Opprett et **public** repository, for eksempel `kommandosentral`. (Det er bare app-koden som er offentlig; lokale data legges ikke inn i repositoryet.)
3. Last opp innholdet fra mappen `kommandosentral/` til roten av repositoryet: `index.html`, `styles.css`, `app.js`, `sw.js`, `manifest.webmanifest` og `icon.svg`.
4. Gå til **Settings → Pages → Build and deployment**, velg **Deploy from a branch**, `main`, `/ (root)` og **Save**.
5. Besøk adressen GitHub viser under Pages. For eksempel `https://BRUKERNAVN.github.io/kommandosentral/` (erstatt BRUKERNAVN med ditt eget).
6. Åpne siden på mobilen og velg **Legg til på Hjem-skjermen** (iOS Safari) eller **Installer app** (Chrome/Edge, avhengig av nettleser).

GitHub Pages er gratis for offentlige repositories på GitHub Free, men tjenestens vilkår og grenser kan endres. Eget domenenavn er ikke nødvendig.

## Personvern og begrensninger

- Ingen backend, konto, bankkobling eller automatisk NAV-synkronisering. Alle registreringer er manuelle.
- Data lagres i nettleserens **localStorage** på enheten. Forskjellige enheter synkroniserer **ikke** automatisk.
- Eksporter JSON-sikkerhetskopi under Innstillinger og importer den ved behov. **JSON er ikke kryptert**. Oppbevar filen sikkert.
- Tømmer du nettleserdata eller bruker privat modus kan data forsvinne.
- Bruk **ikke** appen som lager for hemmeligheter, passord, fødselsnummer eller særlig sensitive helseopplysninger.
- Starter med redigerbare eksempelverdier. De må kontrolleres av brukeren.
- Planleggeren sender **ikke** varsler når appen er lukket. Bruk telefonens kalender til viktige frister.
- Privatlæreren er en fast quiz, **ikke** et AI-system. Dynamiske forklaringer kan gjøres i ChatGPT separat.
- Service worker gjør kjernefilene tilgjengelig offline etter første HTTPS-besøk, men oppdateringer og eventuell nedlasting av nettfonter trenger nett.

## Filene

- `index.html`: appen
- `styles.css`: design og mobiltilpasning
- `app.js`: alle funksjoner og lagring
- `manifest.webmanifest`: appinstallasjon
- `sw.js`: offline-cache
- `icon.svg`: appikon

MIT-lignende fri bruk: Du kan bruke og endre koden til private formål. Ingen betalingsavhengigheter, API-nøkler eller tredjeparts scripts er nødvendige.


## Nytt i versjon 1.1
- Trening: registrer økter, varighet, type, opplevd innsats og øvelser/sett/vekter. Egne treningsplaner og historikk.
- Kosthold: registrer måltider med energi, protein, karbohydrater og fett; valgfri målsetting og handleliste. Tall må legges inn selv.
- Eksisterende lokale appdata fra versjon 1.0 beholdes når filene erstattes på samme adresse og i samme nettleser (samme origin). Gamle JSON-sikkerhetskopier kan importeres.
- For trygg oppgradering: eksporter sikkerhetskopi i gammel app før du åpner den nye. Filer åpnet med file:// kan ha forskjellig/ustabil lagringsområde selv på samme PC; importer sikkerhetskopien i den nye appen om dataene ikke følger med.
