# De Aquo-standaard

De Aquo-standaard (Aquo) is de Nederlandse standaard voor het uitwisselen van gegevens binnen de watersector.  
Informatie is een belangrijke motor voor het functioneren van de watersector. Steeds meer en verschillende overheidslagen en instanties werken samen en wisselen informatie uit. Daarom is het belangrijk dat we allemaal dezelfde betekenis geven aan de gegevens en woorden die we gebruiken. En dat we gemeenschappelijke afspraken maken over hoe we gegevens beschrijven en de manier waarop we ze uitwisselen.

Dankzij de Aquo-standaard is het mogelijk om op een uniforme en efficiënte manier gegevens uit te wisselen tussen partijen die betrokken zijn bij waterbeheer. Bovendien maakt toepassing van de standaard het mogelijk om informatie zo te ordenen en te beheren dat de actualiteit, juistheid en consistentie van die informatie wordt geborgd.  
De Aquo-standaard draagt daarmee bij aan de kwaliteit van het waterbeheer. Het eenvoudig en eenduidig delen van informatie levert voordeel op in tijd en geld.

Aquo is voor overheidsorganisaties een verplichte open standaard, die is ontwikkeld en wordt beheerd door het Informatiehuis Water. Het Informatiehuis Water is een samenwerkingsprogramma van Rijkswaterstaat, de waterschappen en de provincies.  
Het Informatiehuis Water ontzorgt waterbeheerders en beleidsmakers bij het uitwisselen van waterinformatie.

## Het Informatiemodel Water (IMWA)

De basis van de Aquo-standaard (Aquo) wordt gevormd door het informatiemodel Water (IMWA). IMWA biedt de basis voor de informatiestructuur die binnen de gegevensuitwisseling wordt gebruikt. Dit betekent dat binnen IMWA de relevante objecten, onderlinge relaties tussen objecten en eigenschappen over objecten die worden gebruikt binnen het waterbeheer beschrijft.

IMWA is een omvangrijk informatiemodel en is daarom voor de overzichtelijkheid onderverdeeld in een aantal onderdelen domeimen die ieder een taak van de waterbeheerder representeren of daar een belangrijke rol in spelen. Dit zijn: watersysteem, waterveieligheid, waterketen (nog niet beschikbaar).

Naast de drie taken van de waterbeheerder, zijn er binnen IMWA nog een aantal andere onderdelen gemodelleerd die gebruikt worden ter ondersteuning van de drie genoemde taken. Dit zijn: IMWA Kunsterken, OMM-W (in ontwikkeling) voor metingen, observaties, monitoring, toetsen & beoordelen, IMWA Normen (in Ontwikkeling) en IMWA Maatregelen (in ontwikkeling).

Ieder van deze genoemde onderdelen heeft een connectie met IMWA Basis. IMWA Basis is de fundering voor IMWA waar alles samenkomt.

In de onderstaande afbeelding is een (voorlopige) weergave te zien van IMWA en de samenhang tussen de verschillende onderdelen binnen IMWA. Let op! Dit is nog niet de definitieve versie van IMWA en is onderheven aan veranderingen die tot stand komen door de verdere doorontwikkeling van IMWA.

![De context van IMWA](./algemeen/Bedrijfsobjecten%20model.jpg)
*Totaalplaat van IMWA in samenhang*

Zie voor verdere toelichting van de samenhang tussen de verschillende domeinen in de IMWA bij IMWA Basis: [Catalogus IMWA Basis](https://aquo-standaard.github.io/IMWA-basis/#cat)

## MIM-conform

De Aquo-informatiemodellen zijn opgezet volgens het **MIM - Metamodel Informatie Modellering** ([geostandaarden.nl](https://docs.geostandaarden.nl/mim/mim/)). MIM biedt een gemeenschappelijk vertrekpunt voor het maken van informatiemodellen. De afspraken reiken over de grenzen van bestuurslagen heen en zijn toepasbaar in uiteenlopende domeinen. Het volgen van MIM zorgt er ook voor dat er een gelaagdheid is aangebracht in de informatiemodellen

- **Conceptueel model**: Hierin zijn alle toepassingen aangegeven waarvoor op dit moment Aquo-informatiemodellen beschikbaar zijn.
- **Logisch model**: Dit is een selectie uit het semantische model, die specifiek is voor een bepaald werkveld of uitwisseldoel.
- **Fysiek model**: Hiermee kunnen programmeurs aan de slag ten behoeve van een geautomatiseerde (computer naar computer) gegevensuitwisseling.

Zie voor verdere toelichting:  
[Metamodel Informatie Modellering](https://docs.geostandaarden.nl/mim/mim/)

De Aquo-informatiemodellen zijn gemodelleerd met behulp van **UML (Unified Modeling Language)** in **Enterprise Architect**.
