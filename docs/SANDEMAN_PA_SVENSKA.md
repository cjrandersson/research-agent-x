# Sändeman på svenska

Det här dokumentet förklarar Sändeman så enkelt som möjligt.

Målet är att en ny person i projektet snabbt ska förstå **vad vi bygger, varför vi bygger det och hur det fungerar** utan att först behöva läsa den tekniska dokumentationen.

---

## Sändeman på 30 sekunder

**Sändeman är ett research-system som letar efter små förändringar i marknaden innan de blivit uppenbara för alla andra.**

Det kan till exempel handla om:

- samma problem som börjar dyka upp hos flera företag
- ovanligt många nya jobb inom ett tekniskt område
- nya open-source-projekt som plötsligt börjar växa
- nya regler som tvingar företag att förändras
- företag som fortfarande löser viktiga arbetsflöden manuellt
- flera oberoende tecken på att en ny marknad håller på att bildas

Sändeman samlar inte bara länkar och sammanfattar nyheter.

Systemet försöker avgöra:

> **Är det här bara brus, eller börjar flera oberoende signaler peka åt samma håll?**

De starkaste signalerna undersöks vidare för att hitta verkliga problem och möjliga affärsmöjligheter.

---

## Den enkla bilden

Vanliga trendverktyg fungerar ofta som en strålkastare:

> De visar det som redan fått mycket uppmärksamhet.

Sändeman ska fungera mer som perifer syn eller radar:

> Det letar efter svaga rörelser längre ut i synfältet och försöker se när flera små förändringar tillsammans börjar betyda något.

Det är det vi menar med **Peripheral Market Research Vision**.

---

## Vad är problemet vi försöker lösa?

Det finns enormt mycket information på internet:

- nyheter
- jobbannonser
- GitHub
- företagsregister
- finansieringar
- produktlanseringar
- forum och användarklagomål
- regler och myndighetsdata
- open-source-paket
- forskningspublikationer

Problemet är inte att informationen saknas.

Problemet är att nästan allt är brus när man tittar på varje datapunkt för sig.

Sändemans jobb är därför inte:

> "Hitta så mycket information som möjligt."

Utan:

> **"Hitta ovanliga förändringar, koppla ihop oberoende bevis och visa vilka saker som faktiskt är värda att undersöka."**

---

## Ett enkelt exempel

Anta att Sändeman ser följande under några veckor:

1. Flera företag börjar anställa personer med samma nya tekniska kompetens.
2. Nya GitHub-projekt inom samma område växer snabbt.
3. Ett par nya bolag registreras inom området.
4. Företag börjar diskutera samma problem i forum.
5. Det dyker upp en upphandling där någon faktiskt vill köpa en lösning.

Varje observation för sig kan vara ointressant.

Tillsammans kan de vara en tidig signal om att något håller på att förändras.

Sändeman grupperar därför dessa datapunkter till en **signal** och följer den över tid.

---

## Hur systemet fungerar

Den tekniska motorn kan förenklas till:

```text
RÅDATA
  ↓
OBSERVATIONER
  ↓
HÄNDELSER
  ↓
RELATERADE SIGNALER
  ↓
CORE SCAN
  ↓
DEEP DIVE
  ↓
HYPOTES
  ↓
MÖJLIGHET
  ↓
FÖLJ / TESTA / MOTBEVISA
```

### 1. Rådata

Dokument eller datapunkter från exempelvis GitHub, jobbannonser, företagsregister eller myndigheter.

### 2. Observation

Ett konkret faktum extraheras.

Exempel:

> "Fem nya inference-engineer-roller publicerades av företag X."

### 3. Händelse

Observationen översätts till ett standardiserat format som datorn kan jämföra med historiska data.

Exempel:

`HIRING_EXPANSION → AI INFRASTRUCTURE → +5 JOBS`

### 4. Signal Cluster

Relaterade händelser grupperas.

Exempel:

- fler jobb
- fler GitHub-projekt
- fler investeringar
- fler användarklagomål

inom samma område.

### 5. Core Scan

Sändeman frågar:

> "Är detta tillräckligt ovanligt och väl underbyggt för att vi ska bry oss?"

### 6. Deep Dive

Om signalen är stark går systemet djupare:

- Är problemet verkligt?
- Vem upplever det?
- Hur löser de problemet idag?
- Kostar problemet pengar?
- Finns redan bra lösningar?
- Varför händer detta just nu?

### 7. Hypotes / möjlighet

Först här börjar Sändeman formulera något som kan vara en faktisk affärsmöjlighet.

---

## Vad gör Sändeman annorlunda?

Tre saker är särskilt viktiga.

### 1. Flera oberoende bevis

Fem artiklar som kopierar samma pressmeddelande är inte fem bevis.

Sändeman försöker förstå var informationen egentligen kommer ifrån och räknar **oberoende källor**, inte bara antal länkar.

### 2. Förändring över tid

Sändeman tittar inte bara på hur stort något är.

Det tittar på hur snabbt något förändras.

Exempel:

`5 → 8 → 17 → 41`

kan vara mer intressant än:

`500 → 505 → 510 → 515`

### 3. Systemet försöker motbevisa sig självt

När Sändeman hittar något intressant ska det också leta efter bevis som talar emot hypotesen.

Målet är inte att generera spännande idéer.

Målet är att minska risken att vi lurar oss själva.

---

## Vad bygger vi först?

Sändeman V1 är först och främst **vårt eget venture-discovery-system**.

Vi använder det för att hitta och följa möjliga startupmöjligheter som är realistiska för ett litet team.

Den första research-domänen är:

### Enterprise infrastructure & emerging B2B software

med fokus på:

- AI infrastructure
- developer tooling
- integration / interoperability
- vertical operational software

Vi börjar smalt för att kunna mäta om systemet faktiskt fungerar.

Senare kan samma kärna användas för exempelvis:

- VC scouting
- corporate strategy
- market intelligence
- technology monitoring

---

## Vad Sändeman inte ska bli

Sändeman ska inte vara:

- en trendgenerator som hittar på fem "heta marknader" varje vecka
- en samling AI-agenter som pratar med varandra utan mätbar nytta
- ett nyhetsbrev med snygga sammanfattningar
- en gigantisk dashboard som gömmer svag data bakom grafik
- ett system som automatiskt antar att finansiering eller hype betyder en bra marknad

Sändemans värde måste komma från **bättre signaler och bättre timing**, inte mer text.

---

## Hur vet vi om det fungerar?

Vi ska kunna testa systemet historiskt.

Exempel:

> Om Sändeman hade körts med endast information som fanns den 1 mars 2022, hade systemet då kunnat upptäcka en marknadsförändring innan den blev allmänt uppmärksammad?

Detta kallas **backtesting**.

Vi mäter bland annat:

- hur många relevanta signaler Sändeman hittar
- hur många falska signaler det producerar
- hur tidigt det upptäcker förändringar
- om signalerna stärks eller försvinner över tid

---

# En mening

> **Sändeman letar efter flera små, oberoende förändringar som tillsammans kan avslöja ett viktigt marknadsskifte innan det blivit uppenbart.**

# En ännu kortare mening

> **Sändeman försöker se vad som håller på att hända, inte bara vad alla redan pratar om.**
