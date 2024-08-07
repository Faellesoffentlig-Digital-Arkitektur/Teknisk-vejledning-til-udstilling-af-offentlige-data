# Teknisk vejledning til udstilling af offentlige data



## Baggrund om at udstille offentlige data

Offentlige data bør som udgangspunkt stilles til rådighed for andre, som kan bruge dem. Det kan dog være svært på forhånd at sige, hvad et givet datasæt kan bruges til. Derfor satses der på at få udstillet så mange data som muligt med så lille en indsats som muligt og lade mere omfattende indsatser følge konkret efterspørgsel. Dette ligger også i tråd med Lov om videreanvendelse af den offentlige sektors informationer (PSI-loven) som på baggrund af et EU-direktiv foreskriver, at offentlige data så vidt muligt skal stilles til rådighed for videreanvendelse på konkret anmodning.

Med offentlige data menes der i denne sammenhæng alle informationer, som anvendes til intern sagsbehandling i den offentlige sektor, og som lagres elektronisk af en offentlig institution eller myndighed.

### Hvad får myndigheden ud af at udstille sine data?

Der er konkrete fordele for de myndigheder, der udstiller deres data. For det første kan der opstå nye tjenester, som bidrager til at løse myndighedernes opgaver uden ekstra arbejde for myndigheden. Et eksempel kunne være, at oplysninger om ledige pladser på de videregående uddannelser anvendes af private til at udvikle tjenester, som gør det let for de, der ikke kom ind på drømmestudiet, at finde en anden uddannelse.

En generel rutine med løbende udstilling af data kan spare ressourcer ved manuelle udtræk, om end der også er en risiko for, at udstilling af data kunne give merarbejde i form af flere henvendelser med spørgsmål. Dialog om data kan vendes til en fordel ved, at data bliver forbedret. For eksempel kan man ved at sammenholde CVRs lister over restauranter med de smileys, der er uddelt af Fødevarestyrelsen, afklare, om nogle restauranter har skiftet navn, adresse, ejer og så videre. Det er endda muligt at give borgere og virksomheder mulighed for at angive rettelser til oplysninger, som de mener er forkerte eller mangelfulde.

Når mange myndigheder udstiller deres data, vil de ofte kunne genbruge hinandens oplysninger frem for at indsamle på ny. Det giver effektiviseringer, som frigiver ressourcer til andre opgaver.

### Hvilke data bør myndighederne udstille?

Som udgangspunkt opfordres offentlige institutioner til at udstille alle data, som ikke er fortrolige eller følsomme.

Det kan være kompliceret at vurdere, om et givet datasæt kan offentliggøres, og derfor er den generelle anbefaling at starte med de data, som man er sikker på ikke giver problemer, og derefter overveje at gå videre med dem, hvor der kan være behov for særlige hensyn. Der kan være mange forskellige grunde til, at data ikke umiddelbart kan frigives, for eksempel:

* Ophavsret - en del myndigheder anvender data, som ejes af andre, for eksempel billederne i Kunstindeks, som fotografen har ophavsretten til. I sådanne tilfælde skal det afklares om, og på hvilke vilkår, data kan frigives.
* Personhenførbarhed – hvis der er tale om oplysninger om enkeltstående fysiske eller juridiske personer, kan der være udfordringer og sikkerhedshensyn i forbindelse med at udstille oplysningerne.
* Fortrolighed – relativt få oplysninger må betragtes som fortrolige af hensyn til rigets sikkerhed, igangværende efterforskninger, forretningshemmeligheder eller andre væsentlige hensyn.
* Økonomi – hvis det vil være meget dyrt at ændre de systemer, hvor data ligger, så de udstiller data, kan det være nødvendigt at vente med at udstille selve datasættene. Det vil dog i disse tilfælde være hensigtsmæssigt at offentliggøre en beskrivelse af datasættet, så eksempelvis andre myndigheder kan se at og hvor data findes.

## Hvilket format skal jeg bruge?

Nogle udstillingsformater gør det lettere at genbruge data end andre formater. For eksempel kan webservices med standardiserede JSON-formater meget let tilgås af maskiner og integreres i andre tjenester, mens fx PDF-formater er mindre egnede til automatiske behandlinger.

Det kan være svært at vurdere, om det vil give værdi at bruge ressourcer på at videreudvikle data før udstilling i specifikke formater. Det, der oftest giver værdi, er at få gjort opmærksom på, at data findes og at få stillet dem til rådighed. Derfor bør man udstille i de formater, man allerede har dem i.

Der er mulighed for at udstille i yderligere formater hen ad vejen, hvis det viser sig, at der er efterspørgsel efter bestemte data i bestemte formater. PSI-loven giver mulighed for, at de, der er interesserede i at genbruge data, kan betale marginalomkostningerne ved udvikling af snitflader.

## Hvordan bruger jeg et givet format?

Når myndigheden skal udstille nye data – altså data som ikke har været udstillet før – bør man vælge det format, der giver den bedste balance mellem omkostninger og egnethed til formålet. For hvert format er der nogle ting, som du bør være opmærksom på, og dette afsnit sigter på at berøre dem. Dette afsnit handler kun om, hvordan snitfladerne bedst tilrettelægges, så maskiner kan tilgå dem direkte. Råd og vejledning om, hvordan netsteder og webløsninger bør udformes, kan du finde på arkitektur.digst.dk.

### Webservices

For data som ændres ofte, og hvor hvert enkelt udtræk er begrænset i størrelse, er det meget relevant at udstille data via webservices.

Der er flere forskellige måder at lave en webservice, men nogle af de mest brugte er SOAP og REST. Generelt kan SOAP mere end REST, men REST services er meget nemme at udvikle og anvende, så det er en meget brugt standard.

### Database

Ligesom webservices giver direkte databaseadgang mulighed for at tilgå data dynamisk. Databaser har den fordel, at de kan give brugerne mulighed for selv at sammensætte netop det udtræk, de er interesserede i.

Der er dog nogle sikkerhedsmæssige bekymringer ved at tillade eksterne databaseudtræk, og en databaseadgang er kun nyttig, hvis strukturen i databasen og betydningen af de enkelte tabeller og felter er veldokumenteret.

Ofte kan der relativt enkelt og billigt oprettes webservices, som udstiller data fra en database, hvilket kan være en let måde at afhjælpe sikkerhedsbekymringerne.

### JSON

JSON er et meget udbredt format til udveksling af data, fordi det giver gode muligheder for at bevare strukturen i data og formatet er relativt kompakt og dermed egnet til overførsel af større mængder strukturerede data.

### XML

XML er et andet udbredt format til udveksling af data, fordi det giver gode muligheder for at bevare strukturen i data og den måde filerne opbygges på lader udviklerne skrive dele af dokumentationen ind sammen med data, uden at det forstyrrer læsningen af dem.

### RDF

Et relativt nyt format kaldet RDF gør det muligt at udstille data i en form, så maskiner delvist kan forstå og fortolke data. RDF giver særdeles gode muligheder for automatisk viderebehandling af data, men da formatet er meget frit – på linje med XML – er der behov for profileringer.

### Regneark

Mange myndigheder har oplysninger liggende i regneark, for eksempel Microsoft Excel. Disse data kan ofte anvendes umiddelbart med de rette beskrivelser af, hvad de forskellige kolonner betyder.

Dog vil der i en del tilfælde være makroer og formler i regnearkene, som kan være noget mere besværlige at have med at gøre. Det er derfor tilrådeligt at dokumentere sådanne beregninger ved siden af regnearket, da det generelt er mere tilgængeligt for brugerne at læse.

### Kommaseparerede filer

CSV-filer kan være et nyttigt format, da det er kompakt og dermed velegnet til at overføre store sæt af data med samme struktur.

Dog er formatet så begrænset, at data ofte er ubrugelige uden dokumentation, idet det kan være svært at gennemskue, hvilken betydning de forskellige kolonner har. Det er derfor særligt vigtigt for kommaseparerede formater, at dokumentationen af de enkelte felter er præcis.

Desuden er det afgørende, at strukturen i filen overholdes, idet en enkelt udeladelse af et felt kan forrykke læsningen af alle resterende data i filen uden reel mulighed for at rette op på det, da det ikke vil kunne afgøres, hvordan de resterende data skal fortolkes.

### Tekstdokument

Klassiske dokumenter i formater som Word, ODF, OOXML eller PDF kan være tilstrækkelige til udstilling af visse former for data – for eksempel relativt stabile adresselister eller tilsvarende. Det kan være billigt at udstille i, da det ofte er det format, data er født i.

Formatet giver ikke støtte til at holde strukturen stringent, hvilket ofte medfører, at det er svært at indlæse data maskinelt. Sørg derfor for at bruge skabeloner som basis for dokumenter, der skal udstille data til genbrug, så det kræver mindst muligt at hive informationen ud af dokumenterne.

Det kan også støtte videreanvendelse af data at bruge typografiopmærkning så meget som muligt, så det bliver lettere for en maskine at skelne overskrifter (helst typeangivne) fra indhold og så videre.

Generelt anbefales det ikke at udstille i tekstbehandlingsformat, hvis data forefindes i et andet format.

### Scannet billede

Scannet billede er i de fleste sammenhænge det mindst velegnede dataformat for data. TIFF og JPG-2000 kan dog opmærkes med dokumentation af, hvad der er på billedet – helt op til at opmærke et billede af et dokument med hele tekstindholdet af dokumentet. Det kan være relevant at udstille data som billeder, hvis data ikke er født elektronisk – et oplagt eksempel er gamle kirkebøger og andre arkivalier.

### Proprietære formater

En del fagsystemer med videre har egne dataformater, som de kan lagre eller eksportere data i.

Det kan i visse tilfælde være tilstrækkeligt at udstille data i et sådant format – især hvis det forventes, at videreanvendelse vil ske i et tilsvarende system som det, de kommer fra. Det bør altid oplyses, hvor man kan finde mere information om sådanne proprietære formater, eksempelvis ved at oplyse et link til leverandørens hjemmeside.

Generelt anbefales det dog at udstille data i ikke-proprietære formater, hvor det kan lade sig gøre.

### HTML

Mange data ligger i dag tilgængelige i HTML-format på forskellige netsteder. Dette kan sagtens være tilstrækkeligt, hvis de pågældende oplysninger er meget stabile og begrænsede i omfang.

I en del tilfælde er det dog relevant at have data i en form, som er lettere at downloade og bearbejde, men da det er let og billigt at henvise til en side på et netsted, kan det være et godt udgangspunkt i udstilling af data.

Typisk vil det være mest hensigtsmæssigt at anvende tabeller i HTML-dokumenterne til at holde data, og her er det vigtigt, at de forskellige datafelter, der udstilles, får angivet id’er, som gør det let at finde og bearbejde data.

## Hvordan skal det dokumenteres?

Overordnet er rådet om dokumentation at gøre det så godt som muligt. Dokumentationen (metadata) er ofte vigtigere end formatet, da det er relativt enkelt at konvertere veldokumenterede data mellem formater, men sværere at anvende uforståelige data selv i de bedste formater.

Betydningen af data bør dokumenteres. Fx ved kobling til en datamodel med semantiske definitioner gerne i henhold til FDA-modelreglerne, men – er data simple kan en PDF med beskrivelse ofte være nok.

Desuden bør det samlede datasæt dokumenteres. Her er det altid væsentligt at sikre, at dokumentationen har det rette indhold for at gøre det muligt og let at finde og genbruge data. Beskriv gerne som minimum:

* Navn på datasættet
* En tekstbaseret beskrivelse af datasættets formål og indhold. Det er ofte meget værdifuld viden for at gøre det lettere at vurdere, om et datasæt er relevant til en given anvendelse.

Derudover vil det blandt andet være en fordel, hvis dokumentationen også indeholder en beskrivelse af:

* Hvilket format data er udstillet i
* Hvor data kan findes. Angiv gerne en URL, IP-adresse, eller hvad der nu måtte være relevant. For data, som endnu ikke udstilles, kan det give mening at offentliggøre en beskrivelse af datasættet på fx myndighedens egen hjemmeside med angivelse af et telefonnummer eller en email-adresse, man kan kontakte for at bede om at få udstillet data.
* Hvordan datasættet er opbygget – herunder specifik dokumentation af, hvilke felter der betyder hvad.
* Hvilke vilkår gælder for tilgang og anvendelse. Hvis der kræves betaling, godkendelse, hensyn til fortrolighed eller andet, er det vigtigt at angive dette.
* Kvalitet af data – hvor korrekte mener du selv, dine data er, hvor kommer de fra, og hvor tit opdateres de?
* Kontaktoplysninger, så brugerne kan give feedback på datakvaliteten, formatet eller andet.

Som en hjælp til at beskrive data findes her på siden DCAT-AP-DK, som er en specifikation til beskrivelse af datasæt og datakataloger til anvendelse i dansk fællesoffentlig regi. Specifikationen omfatter basisoplysninger om datasæt, som fx titel, beskrivelse, udgiver, udgivelsesdato mv., samt en ensartet struktur for disse oplysninger i et fælles udvekslingsformat, som gør det muligt at dele oplysninger om datasæt på en effektiv måde. Specifikationen resulterer i en såkaldt anvendelsesprofil baseret på internationale og nationale specifikationer. 

## Tjekliste

1. Få et overblik over, hvilke data du har. - Det er nyttigt for dig selv at vide og nødvendigt for at kunne udstille dem
2. Vurdér om der er fortrolighedshensyn. - Hvis der er, så tag sikkerhedshensyn før data udstilles.
3. Dokumentér dine data - Dokumentation er afgørende for brugbarheden. - og det giver tit dig et bedre overblik over dine data
4. Få registreret dine data i Datavejviser, også data du ikke umiddelbart udstiller. - Det giver værdi at oplyse om data, også selvom du ikke udstiller dem lige nu. Det kan være, at data har så meget værdi for nogen, at de vil hjælpe med at få dem udstillet.
5. Udstil data som du har dem. - Kvaliteten af data kan løbende forbedres, hvis nogen får nok nytte af det.

Du kan sende en e-mail til os på [arkitektur@digst.dk](mailto:arkitektur@digst.dk), hvis du er i tvivl om noget, eller du har brug for konkret hjælp med at få udstillet dine data.

Endvidere har standardiseringsorganisationen W3C har udgivet vejledninger på engelsk:

[http://www.w3.org/DesignIssues/GovData](http://www.w3.org/DesignIssues/GovData)

[http://www.w3.org/TR/gov-data/](http://www.w3.org/TR/gov-data/)

[Permanent URL til artiklen: https://arkitektur.digst.dk/node/1095](https://arkitektur.digst.dk/node/1095)

[Tilbage til toppen](#top)

Opdateret 17. august 2023

DokumentinformationIndholdsfortegnelse

* [Baggrund om at udstille offentlige data](#baggrund-om-at-udstille-offentlige-data)
  * [Hvad får myndigheden ud af at udstille sine data?](#hvad-fr-myndigheden-ud-af-at-udstille-sine-data)
  * [Hvilke data bør myndighederne udstille?](#hvilke-data-br-myndighederne-udstille)
* [Hvilket format skal jeg bruge?](#hvilket-format-skal-jeg-bruge)
* [Hvordan bruger jeg et givet format?](#hvordan-bruger-jeg-et-givet-format)
  * [Webservices](#webservices)
  * [Database](#database)
  * [JSON](#json)
  * [XML](#xml)
  * [RDF](#rdf)
  * [Regneark](#regneark)
  * [Kommaseparerede filer](#kommaseparerede-filer)
  * [Tekstdokument](#tekstdokument)
  * [Scannet billede](#scannet-billede)
  * [Proprietære formater](#proprietre-formater)
  * [HTML](#html)
* [Hvordan skal det dokumenteres?](#hvordan-skal-det-dokumenteres)
* [Tjekliste](#tjekliste)

Titel Teknisk vejledning til udstilling af offentlige data

Seneste opdateringsdato

17\. august 2023

Arkitekturperspektiv

Applikation

Dokument beskrivelse

Vejledningen har til formål at gøre det lidt lettere at få et overblik over, hvad der skal til for, at en offentlig myndighed kan udstille sine data til videre brug af andre myndigheder eller private virksomheder.

FDA Status

Færdig

Produktlivscyklus

Færdig

Versionsnummer

1.2
