# 19/10/2026 Mandag
* Diskuteret arbejdsgang og projekt med hold
* Brainstormet bedre sikkerhed og håndtering af data i databasen

# 20/10/2026 Tirsdag
* Brainstormet bedre håndtering af SFTP-server tilføjelser

# 21/10/2026 Onsdag
* Scaffold af API-projekt
* Opsætning af Microsoft Identity og Entity Framework

# 22/10/2026 Torsdag
* Skrev kravspecifikation
* Opsætning af logging-modul i API

# 23/10/2026 Fredag
* Database modeller
* Implementation af Unit of Work service

# 26/10/2026 Mandag
* Primært undervisning
* Lidt rapport og diskussioner om implementering af forskellige ting, bl.a. logikken bag filfordeling imellem flere servere

# 27/10/2026 Tirsdag
* Opsætning af JWT authentication med Microsoft Identity
* Konfigureret Microsoft Identity password politik

# 28/10/2026 Onsdag
* Tilføjelse af login, refresh, register, getme og logout API funktionalitet
* Lave password politik konfigurerbart

# 29/10/2026 Torsdag
* Tilføjelse af CORS politik med en konfigurerbart liste af IP'er/domæner
* Flyt refresh token til at bruge secure cookies

# 30/10/2026 Fredag
* Tilføjelse af API funktionalitet til at lave, slette, opdatere og hente organisationer

# 02/11/2026 Mandag
* Tilføjelse af en "MutationEnvelope" klasse der kan bruges til at indkapsulere data hentet fra services og repositories, sammen med en status, som API'et kan bruge til at styre hvilken HTTP respons den skal give
* Tilføjelse af enkryption service der bruger AES-GCM med en symmetrisk nøgle, til at enkryptere sensitive dataer gemt i databasen

# 03/11/2026 Tirsdag
* Tilføjelse af RSA modul der laver public/private keypairs til SFTP
* Tilføjelse af API funktionalitet til at tilføje SFTP forbindelser, og hente en kode der bruges til at tilføje SFTP forbindelser

# 04/11/2026 Onsdag
* Tilføjelse af API funktionalitet til at acceptere og nægte SFTP forbindelser, og hente godkendte SFTP forbindelser

# 05/11/2026 Torsdag
* Mindre kode oprydning.
* Ændre alle endpoints der tilgår SFTP forbindelser til at kræve ID'et på den organisation den er tilknyttet til

# 06/11/2026 Fredag
* Forbedring af flow med SFTP forbindelser og mindre kode oprydning

# 09/11/2026 Mandag
* Tilføjelse af SMTP konfiguration og email service
* Funktionalitet til at sende email-verifikation links
* Funktionalitet til at bruge email-verifikation links så en bruger kan verificere deres email
* Funktionalitet til at bede om et nyt link til at verificere email

# 10/11/2026 Tirsdag
* Opdater emails sendt til brugeren er styled og matcher vores Fileodon brand
* Funktionalitet til at sende password reset emails
* Funktionalitet til at bruge password reset links så en bruger kan nulstille deres password

# 11/11/2026 Onsdag
* Opdater email service til at bruge en background-worker den kan sende emails i baggrunden, så API'et ikke venter på den
* Flyt fra at bruge SwaggerGen til at bruge OpenAI
* Tilføjelse af validering på alle controller DTO'er

# 12/11/2026 Torsdag
* Funktionalitet til at tjekke igennem API'et, om en fil eksistere, på en SFTP server.
* Funktionalitet til at uploade filer til en SFTP server igennem API'et, med en queue worker der kører i baggrunden og rapportere progress

# 13/11/2026 Fredag
* Funktionalitet til at få en liste af filer på en SFTP server, igennem API'et.

# 14/11/2026 Lørdag
* Funktionalitet til at flytte og omdøbe filer igennem API'et, på en SFTP server.
* Funktionalitet til at downloade som et stream fra en SFTP server, igennem API'et.
* Ændre respons DTO'er til at følge et standard struktur der altid inkludere status og fejlbeskeder, hvis noget gik galt

# 15/11/2026 Søndag
* Funktionalitet til at lave mapper på en SFTP server, igennem API'et
* Funktionalitet til at slette filer og mapper på en SFTP server, igennem API'et
* Tilføjelse af email verification der tjekker og kræver at en email er verificeret, før at brugeren kan oprette noget.

# 16/11/2026 Mandag
* Tilføjelse af asynkrone SFTP uploads der kører i baggrunden i en queue, og distribuerers blandt de valgte SFTP servere.
* Funktionalitet til at hente progress på en upload via job ID

# 17/11/2026 Tirsdag
* Tilføjelse af assymetrisk ED256 nøgle der bliver brugt til at lave JWT tokens til PAM authentication
* Tilføjelse af endpoint til at hente public key til den assymetrisk ED256 nøgle

# 18/11/2026 Onsdag
* Audit logging af SFTP actions
* Global Exception handler