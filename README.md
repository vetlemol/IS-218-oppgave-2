## Endringer i oppgave 2
README-filen i Github-repositoriet har blitt oppdatert med mer informasjon, inkludert lenke til datasettene som har blitt brukt og en oversikt over benyttede teknologier. Til forskjell fra forrige innlevering har oppgaven blitt skrevet inn i et dokument. I tillegg er det lagt ved en kort gif i mappeinnleveringen som viser applikasjonen i bruk. For å få bedre flyt har formatet blitt endret slik at teksten får en tydeligere struktur. 

## Oppgave 2: Geografiske IT-utvikling
### 1.0 Introduksjon
I denne oppgaven er det utviklet en kartløsning som gir brukeren mulighet til å utforske forekomster av truede og fremmede arter i et avgrenset geografisk område. Ved å kombinere åpne datasett med verktøy for geografisk visualisering, presenteres informasjon som kan gi økt innsikt i hvilke arter som er registrert i nærområdet, og hvilken grad av trussel de representerer for norsk natur. Løsningen legger til rette for at brukeren selv kan undersøke artstyper og utbredelse basert på eget geografisk utvalg.

### 1.1 Problemstilling
Hensikten med problemstillingen er å kartlegge både naturverdier og naturtrusler i nærområdet, og øke bevisstheten om hvordan truede og truende arter påvirker biomangfoldet lokalt.

Er det stor sannsynlighet for å se truede arter i studentenes nærområde? Hvilke arter er kritisk og sterkt truet? Hvilke arter kan anses som truende for norsk natur og biomangfold?  Hvilke arter er mest truende for naturen i studentenes nærområder?

### 2.0 Løsning
Gruppen har hentet datasettet “Rødlistearter” fra Geonorge, og har valgt ut kritisk truet og sterkt truet arter. Videre er det brukt “Artskart fremmede arter” for å hente ut fremmede arter som kan være truende for norsk natur. Supabase fungerer som databasen som lagrer artsinformasjonen, mens kartvisningen er implementert med Leaflet sammen med utvidelsene markercluster for gruppering av markører og draw for å tegne områder. 
Kartet initialiseres med Kristiansand som senterpunkt og setter opp fire ulike markercluster-grupper for forskjellige kategorier av arter basert på fare for utryddelse eller fare for norsk natur. Når brukeren tegner et rektangel på kartet, henter systemet data fra Supabase med serversidefiltrering som begrenser dataene til funn fra 2010 eller senere innenfor det spesifikke geografiske området og kun henter relevant data fra radene.
Kartet (se Utklipp 1) antyder at Kristiansand sentrum er et område der truede arter potensielt kan observeres. Arter blir representert i klynger, der man får oversikt over både truede og truende arter i området. Gruppen tar forbehold om at dataene i datasettene kan være utdatert, og at avvik eller feil kan forekomme.

![](Bilde1.png)

Utklipp 1: Kart over Kristiansand med et markert område der arter visualiseres som klynger. 


På kartet vises kritisk truede arter som røde punkter, mens de sterkt truede artene vises som blå prikker, se Utklipp 2. Videre er de høyt truede artene representert av grå prikker og de svært høyt truende artene vises som sorte prikker, se Utklipp 3. Mer informasjon om de ulike artene vises ved å klikke på punktet, hvor det oppgis funnår, artens navn, samt antall registrerte funn. 

![](Bilde2.png)

Utklipp 2: Eksempel på informasjon som kommer opp ved å trykke på et valgt punkt. De blå punktene viser sterkt truede arter.

![](Bilde3.png)
Utklipp 3: Eksempel på informasjon som kommer opp ved å trykke på et valgt punkt. De grå punktene viser høyt truende arter.

I Kristiansand sentrum finnes det både arter som utgjør en trussel mot norsk natur og arter som regnes som truede. Antall punkter i figurene indikerer et begrenset biomangfold i studentenes nærområde. Utklipp 2 viser at studentene har mulighet til å observere truede arter, som bulmeurt, i sitt nærområde. Dataene fra Utklipp 3 viser at studentene også kan komme i kontakt med truende arter som platanlønn. Det er viktig å merke seg at tallene er basert på eldre data og kan ha endret seg siden innsamlingen.
Hele løsningen er satt sammen med standard webteknologier som HTML, CSS, JavaScript, og fokuserer på effektiv datahåndtering og brukervennlig visualisering, slik at brukere enkelt kan utforske artsmangfoldet i selvvalgte geografiske områder. Systemet ligger i et åpent repository i Github https://github.com/vetlemol/IS-218-oppgave-2

## 3.0 Konklusjon
Kartløsningen viser hvordan geografiske informasjonssystemer kan brukes til å kartlegge truede og fremmede arter i et avgrenset område. Løsningen kan gi økt bevissthet rundt artsmangfoldet i Norge, selv om dataene kan være noe utdaterte.


![](Video.gif)

Figur 4 viser hvordan systemet brukes


## 4.0 Referanseliste
Artsdatabanken (u.å.) Fremmedartlista. Geonorge. https://kartkatalog.geonorge.no/metadata/fremmedartlista/53f55741-c9b3-419b-bb86-15bd2a2413e1 
Artsdatabanken (u.å.) Rødlistearter. Geonorge. https://kartkatalog.geonorge.no/metadata/roedlistearter/00b0ab63-de0b-4f12-ac40-655de5163b8d 
