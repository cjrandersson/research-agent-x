HUR ?
Bygger vi detta?
Verifierar vi data?
Validerar vi data?
Visualiserar vi data, gör det läsbart och jämförtbart över tid?
Simplifierat/kortfattat:

Ett litet research-system i fyra lager, där varje lager bara gör det som behövs just då. Det gör prompten lättare att köra, lättare att förstå och mycket bättre för återkommande research.

1. Grundtanken
Tänk så här:

Core Scan hittar signaler. 🛜

Deep Dive verifierar signaler. 🔃

Evaluation avgör om signalen är värd att följa. 🟢

Report gör fynden läsbara och jämförbara över tid. 🟢

Allt behöver alltså inte hända i varje körning.

Layer 1: Research Scope
Det här är filtret innan researchen börjar.

Här definierar vi sådant som sällan ändras:

Sectors & Topics
Geographic Scope
Research Languages
Founder Constraints
Budget
Available Time
Exclusions
Preferred opportunity types
Detta lager svarar på:

Vad är vi intresserade av och vad är realistiskt för oss?

Det ska ligga i production-prompten, men ganska komprimerat.

Exempel:

Focus on Nordic/EU B2B software opportunities in legacy modernization, AI automation, vertical SaaS, climate/energy infrastructure, resilience and embedded fintech. Favor opportunities feasible for 1–2 founders, <$25k initial capital and ~20h/week.

Inte tre sidor text varje gång.

Den långa versionen vi byggt fungerar istället som master specification.

Layer 2: Core Scan
Det här är motorn som körs regelbundet.

Målet är inte att bevisa en startup-idé. Målet är:

Hitta avvikelser, problem och förändringar som förtjänar mer research.

Jag skulle använda sju signalgrupper.

A. Pain
Leta efter:

complaints
negative reviews
missing features
frustration
broken workflows
expensive software
bad integrations
Fråga:

Vad verkar människor återkommande ha problem med?

B. Manual Work
Leta efter:

Excel
email workflows
copy/paste
reconciliation
manual validation
manual data transfer
repetitive support work
people coordinating between systems
Fråga:

Var fungerar människor fortfarande som middleware?

Detta är särskilt viktigt för vår research.

C. Demand
Leta efter:

search growth
“alternative to”
“how to automate”
“API for”
job openings
procurement
explicit requests for tools
Fråga:

Finns det tecken på att någon faktiskt söker efter en lösning?

D. Technology Shift
Leta efter förändringar som gör nya produkter möjliga:

MCP
agents
cheaper inference
new APIs
new open-source tooling
interoperability standards
new data availability
Fråga:

Har något blivit möjligt nu som var svårt eller dyrt för två år sedan?

E. Market / Regulatory Catalyst
Leta efter:

new EU requirements
compliance deadlines
labor shortages
energy costs
security requirements
ERP migration
new industry standards
Fråga:

Finns det något som tvingar marknaden att förändras?

F. Competitor / Incumbent Weakness
Leta efter:

poor reviews
outdated UX
expensive incumbents
acquisitions causing dissatisfaction
poor APIs
slow product development
excessive consulting
Fråga:

Finns det ett problem som existerande leverantörer inte verkar lösa väl?

G. Startup / Market Activity
Leta efter:

new startups
funding
accelerator companies
acquisitions
new product categories
Men detta används som signal, inte som bevis.

Fråga:

Börjar flera aktörer röra sig mot samma problem?

Resultatet från Core Scan
Core Scan ska inte producera långa startup-analyser.

Den ska exempelvis kunna returnera:

| Signal | Evidence | Sector | Strength | Action | | --- | --- | --- | --- | --- | | Manual EDI exception handling | 6 independent complaints | Supply chain | High | Deep dive | | AI compliance tooling for NIS2 | Regulation + startup activity | Cybersecurity | Medium | Watch | | Agent checkout protocols | Lots of media, little buyer evidence | Commerce | Low | Ignore for now |

Idealt kanske 10–20 signaler scannas, men bara 2–5 går vidare.

Det är själva tratten.

Layer 3: Deep Dive
Deep Dive körs endast på de starkaste signalerna.

Här byter frågan från:

“Finns något här?”

till:

“Kan detta faktiskt bli en bra business?”

Jag skulle dela Deep Dive i sex steg.

1. Verify the Problem
Bekräfta att problemet verkligen finns.

Hitta:

flera oberoende användare
olika företag
olika datum
konkreta exempel
Försök också motbevisa hypotesen.

2. Current Workflow
Förstå exakt vad användaren gör idag.

Exempel:

Order fails
↓
EDI specialist checks VAN
↓
Downloads XML
↓
Compares against ERP
↓
Emails customer
↓
Mapping team investigates
↓
Transaction resent
Det är mycket mer värdefullt än:

“EDI automation is a growing market.”

Här hittar vi själva produkten.

3. Commercial Evidence
Undersök:

Vem äger problemet?
Finns budget?
Vad kostar problemet?
Betalar företag redan för människor/software/consultants?
Finns procurement?
Finns jobbannonser för att hantera problemet?
Vi behöver inte kunna räkna TAM.

Vi behöver kunna säga:

“Companies clearly spend money on this problem.”

4. Existing Solutions
Kartlägg:

incumbents
startups
internal tools
consultants
spreadsheets
manual workflows
Sedan frågar vi:

Vad löser de inte?

Det är “gapet”.

5. Startup Wedge
Nu får research-agenten tänka produkt.

Inte:

“Build an AI platform for supply chains.”

Utan exempelvis:

“AI investigation layer for failed EDI transactions that reads mapping logs, ERP state and partner-specific rules, then proposes resolution.”

Och sedan:

V1

Upload failed transaction + mapping log → root-cause diagnosis + recommended fix.

Det ska vara mycket smalare än slutvisionen.

6. Founder Fit
Sista filtret:

Kan vi:

bygga det med 1–2 personer?
testa för <$25k?
komma framåt med ~20h/week?
hitta 5–10 potentiella customers?
köra concierge MVP först?
få någon att betala innan vi byggt hela plattformen?
Om svaret är nej:

försök hitta en mindre wedge.

Layer 4: Evaluation & Opportunity Log
Här skulle jag undvika att göra någon avancerad “AI investment score” i början.

Använd istället ett enkelt system.

Evidence
Low / Medium / High

Founder Fit
Low / Medium / High

Commercial Signal
Low / Medium / High

Competition Gap
Low / Medium / High

Status
NEW
STRENGTHENING
WATCH
UNCHANGED
WEAKENING
INVALIDATED
Det räcker långt.

Opportunity Log
Alla bra fynd får ett stabilt ID.

Exempel:

OPP-EDI-004

AI-assisted EDI exception investigation

Nästa vecka kanske vi hittar ytterligare tre datapunkter.

Då skapar vi inte:

“New opportunity: AI for EDI errors.”

Vi uppdaterar:

OPP-EDI-004 → STRENGTHENING

Det är där det börjar bli riktig venture intelligence istället för en hög länkar.

Hur vi visualiserar resultaten
Jag skulle ha tre nivåer.

1. Weekly Radar
Snabb överblick.

Exempel:

| Opportunity | Status | Evidence | Commercial | Founder Fit | | --- | --- | --- | --- | --- | | EDI Exception Agent | 🟢 Strengthening | High | High | High | | NIS2 Supplier Compliance | 🟡 Watch | Medium | Medium | High | | Agent Checkout Infrastructure | 🟡 Watch | Low | Medium | Medium | | BESS Optimization SaaS | 🔴 Weakening | Medium | High | Low |

Detta är dashboarden.

2. Opportunity Card
Klickar man mentalt in på en opportunity får man:

OPP-EDI-004
AI-assisted EDI exception investigation

Problem

EDI specialists manually investigate failed transactions across multiple systems.

Buyer

Integration Manager / EDI Manager

Current workflow

VAN → logs → ERP → XML → email → mapping specialist.

Evidence

8 independent examples across 5 sources.

Why now

LLM context handling + MCP + better enterprise agent tooling.

Wedge

Diagnostic assistant before automatic remediation.

Business model

B2B SaaS / transaction volume.

Founder fit

High.

Biggest risk

Enterprise system access and security.

Next validation

Interview 5 EDI specialists.

Det ska gå att läsa på någon minut.

3. Deep Dive Report
Endast för de kanske 1–2 starkaste opportunities.

Där får vi:

evidence
competitors
workflow
pricing signals
market
founder fit
MVP
validation plan
risks
sources
Detta kan vara några sidor.

Vi ska alltså inte producera fem sådana varje gång.

Hur en research-körning faktiskt går till
Jag skulle rekommendera en återkommande loop:

        DEFINE SCOPE
             ↓
         CORE SCAN
             ↓
      Detect 10–20 signals
             ↓
         FILTER
             ↓
       2–5 candidates
             ↓
         DEEP DIVE
             ↓
       0–3 opportunities
             ↓
      UPDATE OPPORTUNITY LOG
             ↓
        WEEKLY RADAR
             ↓
     NEXT RESEARCH CYCLE
Det fina är att researchen blir kumulativ.

Vecka 1:

Interesting complaint.

Vecka 2:

More complaints + job postings.

Vecka 3:

Procurement evidence.

Vecka 4:

Startup enters market.

Då går signalen från:

WATCH → NEW → STRENGTHENING

Hur production-prompten bör struktureras
Här tycker jag vi ska vara ganska brutala med komprimeringen.

Den behöver egentligen bara ha sex huvudsektioner.

1. ROLE
Typ:

Act as a venture intelligence researcher focused on identifying evidence-backed, bootstrappable B2B software opportunities.

2. SCOPE
Kort sammanfattning av:

sectors
geography
founder profile
exclusions
Kanske 15–25 rader totalt.

3. CORE SCAN
De sju signalerna:

pain
manual work
demand
technology
catalyst
incumbent weakness
market activity
4. DEEP DIVE TRIGGER
Instruktion:

Do not fully investigate every signal. Escalate only signals supported by multiple independent sources or unusually strong commercial evidence.

Detta är superviktigt.

5. DEEP DIVE METHOD
De sex frågorna:

Problem?
Customer?
Current workflow?
Commercial evidence?
Existing alternatives/gap?
Feasible wedge?
6. OUTPUT
Returnera:

Executive summary
Opportunity radar
Max 3–5 opportunities
Watchlist
Coverage
Sources
Klart.

Master Spec vs Production Prompt
Jag skulle alltså behålla allt vi har byggt.

Men använda det så här:

Master Research Specification
Den långa versionen.

Innehåller:

alla källor
alla sectors
regler
definitions
evaluation framework
exclusions
edge cases
Detta är vår manual.

Production Prompt
Kanske 20–30 % av längden.

Den refererar till principerna men innehåller bara det som behövs för den aktuella körningen.

Deep Dive Template
Separat prompt/template som bara används när ett fynd kvalificerar.

Det gör hela systemet mycket smidigare.

Och till sist: hur vi bör tolka resultaten
En viktig mental modell:

Core Scan = radar blips.

Inte startup-idéer.

Deep Dive = targets.

Fortfarande inte automatiskt bra businesses.

Validation = reality check.

Först när vi har pratat med människor, sett faktisk spending eller kanske till och med fått en design partner börjar vi kunna säga:

“Det här är något vi faktiskt borde bygga.”

Det är också därför jag skulle undvika att låta research-agenten bli för entusiastisk. Dess uppgift bör vara att hitta bra frågor att undersöka vidare, inte att varje vecka uppfinna fem “billion-dollar opportunities”. 🛰️

Nästa logiska steg är att vi tar allt vi nu definierat och bygger Production Prompt v1, med ungefär den här lagerstrukturen och kanske 60–70 % mindre text än master-specifikationen.
