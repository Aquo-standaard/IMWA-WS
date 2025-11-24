# Modelelementen

Modelelementen zijn de bouwstenen van een informatiemodel. Ze bepalen de structuur en werking van het model. Elk element heeft een specifieke functie binnen het informatiemodel en daarmee ook in het beheer van data.  

Elk informatiemodel heeft een aantal vaste elementen. Door deze elementen goed te begrijpen, wordt het model en de catalogus makkelijker te lezen.

## Objecttypen

Een object is een modelelement dat wordt gebruikt om de objecten waarover wordt gesproken in een specifiek werkveld te modelleren (voor de watersector bijvoorbeeld een oever, een waterbodem, een observatie, een norm etc.). Deze objecttype hebben bijna altijd eigenschappen die wij attributen noemen. D Deze objecttypen hebben altijd relaties met elkaar. Deze relaties zorgen er voor de alle objecten in het model in samenhang worden gebracht en een betekenisvolle eenheid vormen. In het model zijn dit de verschillende blokken die zijn aangeduid als *Objecttype*.

## Attribuut

Een attribuut is een eigenschap of kenmerk van een object. Deze eigenschappen weergeven de informatie die een waterbeheerder wil uitwisselen over een bepaald object (bijvoorbeeld de breedte van een kunstwerk, het type wandconstructie). In het model worden deze eigenschappen weergeven in de objecttype met de aanduiding *Attribuutsoort*.

## Datatypen

Een datatype is altijd verbonden aan een attribuut. Het datatype bepaald in wat voor vorm/in wat voor waarde een attribuut uitgewisseld kan worden. Enkele datatypen die voorkomen in IMWA zijn:

- `integer` (geheel getal)
- `characterstring` (tekst)
- `date` (datum)
- `year` (jaar)
- `GM_Object` (geometrie)
- `measure` (waarde & eenheid)
- `type....` (Aquo-domeintabel)

Er wordt een verschil gemaakt tussen *primitieve datatypen* complexe datatypen. Primitieve datatypen zijn eenvoudige datatypen die bestaan uit één element zoals een integer bestaat uit enkel één getal. Complexe datatypen bestaan uit twee of meer elementen bijvoorbeeld, een measure bestaat uit een getal en een eenheid. In het model worden deze datatypen weergeven bij de attributen met de aanduiding *Datatype*.

Naast deze datatypen kunnen attributen gekoppeld zijn aan een Aquo-domeintabel. Bij een attribuut moet dan een waarde uit de aangegeven Aquo-domeintabel worden aangegeven bijvoorbeeld, attribuut typeSluis verwijst naar de domeintabel SluisType waaruit de waarde keersluis kan worden gekozen.

## Gegevensgroepen
Soms worden meerdere attributen gegroepeerd in een *gegevensgroep*. De attributen in zo’n groep horen inhoudelijk bij elkaar en worden als een geheel behandeld bijvoorbeeld, de gegevensgroep *afmetingen*, waarin de attributen *lengte*, *breedte* en *hoogte* zitten. Gegevensgroepen kunnen bij meerdere objecttypen tegelijk  worden gebruikt.

## Relaties

Objecttypen worden met elkaar gekoppeld door middel van relaties. Binnen het informatiemodel kunnen verschillende typen relaties worden gebruikt. Ieder van deze relaties heeft een andere rol binnen het informatiemodel en loopt altijd van het ene naar het andere objecttype. Deze relatie heeft altijd een richting. In de meeste gevallen loopt deze van een *bron* naar een *doel*. De belangrijkste relaties die voorkomen binnen IMWA zijn als volgt:

- **Generalisatie**  
Een generalisatie geeft aan dat een object een specialisatie is van een ander object. Deze relatie is te is te lezen als *'is-een'*. In het model wordt deze relatie weergeven met de aanduiding *Generalisatie*. Als een object een generalisatie relatie heeft met een ander object dan is er ook sprake van overerving van de attributen. Overerving betekent dat het onderliggende object de attributen erft het bovenliggende object bijvoorbeeld, een sluis is-een kunstwerk en erft dus ook alle attributen van kunstwerk.

- **Associatie**  
Een associatie beschrijft een relatie tussen twee objecten. Deze relatie geeft aan dat de objecten een verbindingen hebben met elkaar die niet hiërarchisch is zoals bij een generalisatie. Deze relatie heeft altijd een naam die de aard van de relatie tussen de twee objecten beschrijft bijvoorbeeld, een oppervlaktewaterlichaam heeft-een oever, of een observatie wordt-uitgevoerd-door een observator. In het model wordt deze relatie weergeven met de aanduiding *Relatiesoort*.gevensdefinitie.
