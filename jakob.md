### Dag 1 19-10
* Aftalte arbejdsgange og metoder, vi kom frem til at køre "documentation driven udvikling" Som egentligt bare betyder at vi fokusere på det skriftige og for styr på det og er på samme side omkring funktionaliteten og krav inden der bliver udviklet noget på en feature.
* Derefter brainstormede vi vores produkt og skabte et overblik over hvilke features det krævede og nice to have udvidelser dertil. 
* Vi semi enige om sprog og frameworks.
* Opsatte github organization og repositories.


### Dag 2 20-10
* Videre brainstorming af produkt samt aftale på tech stack og UI library


### Dag 3 21-10
* Mere planlægning.
* Sparing ift set-up af ASP.NET project.
* Scaffold af Frontend project og opsætning af diverse libraries. Tilføjede DaisyUI og tailwind til UI. Og Pinia som et driftsikkert store til SSR Nuxt.


### Dag 4 22-10
* Start på default authenticated layout i frontend project. Tilføjede icon package, og har som udgangspunkt valgt at bruge (Material Symbols Light)[https://icon-sets.iconify.design/material-symbols-light/]
* Skrev Krafspecifikation
* Lavede noget pair programming med Sebastian, for at få ham introduceret til frontend udvikling i Nuxt & Vue.
* Lavede en generel opdeling for at Sebastian og jeg er "owners" på frontend, og Nicklas og Tobias er "owners" af backend. Alle følger naturligvis med på begge platforme. Og har mulighed for at tage opgaver begge steder hvis der er brug for at de får noget gjort for at komme videre med noget andet. 


### Dag 5 23-10
* Se ind i Rapport krav og Lav en indledende struktur vi kan arbejde ud fra. Vi snakkede om at lave et krav om at i alle vores pull requests skal der være en reference til vores rapport, enten til et nyt afsnit eller afsnit der er skrevet mere på, så vi er sikre på at arbejdet er inkluderet i vores rapport. 
* Færdiggjorde responsivt authenticated Layout. Mangler at skrive rapport til det, men næsten klar til pull request. 

### Dag 6 24-10
* Fridag :)

### Dag 7 25-10
* Skabte kort et overblik over libraries vi har i brug på frontend projektet, og lavede lidt noter til det i raporten.
* Review a Sebastians kode, endte med at tilføje lidt til hans pull request med unauthenticated layout.
* Skrev Rapport til standart layout og indhold af det. For at kunne lave en pull request. 
* Så på lidt backend kode og commits :)

### Dag 8 26-10
* Undervisning, snak om krav til rapporten. 
* Ugentligt sprint, gennemgik hvad vi nåede sidste uge ift produktet og opdaterede vores projekt board iteration 1 for at kunne få alle features vi har nået under vores sprints i Rapporten.
* Møde med Flemming angående vores nuværende omstilling og vision for rapporten. 
* Cleanup og implementering af naming standart på vores projekt board
* Implementeret Nuxt open fetch generation på vores frontend imod lokal backend.


### Dag 9 - 27-10
* Startede med at skrive rapport ift open-fetch i vores nuxt project. Blev lidt side tracked og skrev en masse noter til andet relevant og skrive også
* Lavede open-fetch integrationen færdig, og fik efterspurgt at vi tilføjet /api som prefix på hele api'en så vi kunne generere en enkelt client nemmere via open-fetch.
* Arbejdede på Kravspecification.
* Eslint implementering med workflow
* Mere arbejde på kravspec og skriv noget eslint ind i rapporten.
* Code review, og lidt arbejde på github workflows på vores egne runners.

### Dag 10 - 28-10 
* Implementation af test i frontend og pull request dertil, mangler noget i rapporten dertil
* Skrev Kravspecification
* Review af api jwt refactor
* Scope nye tickets for frontend og andre epics som api tickets også kan laves på.

### Dag 11 - 29-10
* Skrev noget Rapport til vores integration med Pinia stores
* Sikkerheds research og hvordan vi bedst håndtere og beskytter vores tokens client side.
* lavede AuthStore til håndtering af login, registration og refresh. Og i fremtiden andre auth endpoints. Med håndtering af tokens der for nu.
* Fortsat arbejde på auth store, håndtering af refresh token i httpOnly cookie i stedet, lidt udfordringer for at få middleware til at redirecte væk fra login ruter for brugere der er logget ind.


### Dag 12 - 30-10
* Skrev noget rapport til sikkerhed og system
* færdiggjorde authStore branch klar til review og passer checks

### Dag 13 - 31-10
* Lavede starten på Users table, prøvede at simplificere koden lidt i forhold til hvordan det så ud på connections table. kunne evt lave et komponent for at opnå lean ensartede tables. 


### dag 14 - 01-11
* Færdiggjorde users table og edit modal. 
* lavede review på sebastians pull request.

### Dag 15 - 02-11
* Ugentligt sprint, vi gennemgik hvad vi har lavet den forrige uge og fik sørget for at sprint var korrekt up to data ift hvad den forrige uge indeholdte. 
* lavede nogle nye tickets med ideer fra mødes og flere ift audit logs
* Sparring med Sebastian angående form input komponent og andre spørgsmål.
* lavede users table under organisations settings i navigationen
* forbedrede lidt ift at arbejde med tables so det bliver mere effektivt og nemmere at arbejde med tables og holde dem ens.
* Begyndte på at lave en forbedret composable til at håndtere forms på resourcer der hurtigt skal opdateres

### Dag 16 - 03-11
* tilføjede statistikker til user og /settings/roles 
* forsøgte forgæves at få et nice collapsible transition op at køre på forms i tables
* implementerede nogle nye komponenter på tværs af appen også
* review a pull request fix tests

### Dag 17 - 04-11
* Brugte starten af dagen på at skrive rapport. Punkter omrking vores brugerflade og værktøjer samt users og roles manangement i frontend.
* startede på audit logging - planlægning af struktur og generel onboarding af mig selv til C# igen.

### Dag 18 - 05-11
* Lavede klasse diagram af audit logs, imens jeg researchede standart strukture for audit log systemer.
* Scaffoldede klasser, child klasser og interceptors.
* Vores møde i dag, fik vi lavet lidt gode fremskridt på strukturen af vores rapport. Indtil videre har det været lidt bare at smide ting ind under punkter vi syntes giver mening, men nu har vi ændret strukturen lidt, sådan den forhåbenligt får en lidt bedere introduktion og generel indledning. 
* arbejde på audit logs, fandt bug hvor rolle navn var unikt index.
* begyndte at fixe bug på roles, men det index jeg ville skulle fjerne på normalized name, bruges af mange af hjælpefunctionerne, så jeg tror vi ville skulle overwrite en del af base Identitys role system. 
* Færdiggjorde POC på vores audit log system.

### Dag 19 - 06-11
* Arbejde på audit logs, virkede ikke på added da organization ikke fandes endnu, men fandt fix,
* Fik scaffolded og implementeret alt base scaffolding. startede på controller,service og repository. 
* lavede Controller Service og Repository med functionalitet, og er ved at få DTOer og dynamiske ting på plads

### Dag 20 - 07-11
* Oprydning af kode til audit logs for at få det mere in line med resten af kode basen, og bedre genbrugelighed og læsbarhed.
* Lavede resterende endpoints til at få resource specifikke audit logs.

### Dag 21 - 08-11
* Skrev rapport til audit log
* Begyndte på implementering af Organisationer i frontend, lidt løsninger og tilføjelser til backend for at understøtte hvad jeg gerne vil i frontend.

### Dag 22 - 09-12
* Sprint møde
* Planlægning og overblik af hvad vi mangler for at have produktet i en stabil state med must have funktionalitet 
* Vejledning med Flemming, for at få noget feedback på vores nuværende rapport struktur
* Tilføjede lang TODO liste til Rapporten, som kan fungere som løbende todo, og reminders om hvad vi skal huske at holde ensartet og up to date. 
* fik lavet ændringer på adudit log fra review
* review a tobias branch
* Refactors af organization form i frontend for at genbrude til edit og create

### Dag 23 - 10-11 
* Skrev rapport for, Fronend modules, Pinia, eslint + libaries DaisyUI og tailwind CSS
* Hjalp med at blive færdig med UserOrganization CRUD pull request.