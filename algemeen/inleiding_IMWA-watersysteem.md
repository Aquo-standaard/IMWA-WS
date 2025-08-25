# Het informatiemodel Water (IMWA)

De basis van de Aquo-standaard (Aquo) wordt gevormd door het informatiemodel Water (IMWA). IMWA biedt de basis voor de informatiestructuur die binnen de gegevensuitwisseling wordt gebruikt. Dit betekend dat binnen IMWA de relevante objecten, onderlinge relaties tussen objecten en eigenschappen over objecten die worden gebruikt binnen het waterbeheer beschrijft.

IMWA is een omvangrijk model en is daarom voor de overzichtelijkheid onderverdeeld in een aantal onderdelen die ieder een taak van de waterbeheerder representeren. Dit zijn: watersysteem, waterketen en waterveiligheid.

Naast de drie taken van de waterbeheerder, zijn er binnen IMWA nog een aantal andere onderdelen gemodelleerd die gebruikt worden ter ondersteuning van de drie genoemde taken. Dit zijn: IMWA Kunsterken, OMS Waterprofiel (in ontwikkeling) voor metingen & observaties, IMWA Monitoring (in Ontwikkeling) voor monitoringsgegevens, IMWA Normen (in Ontwikkeling) en IMWA Maatregelen (in ontwikkeling).

Ieder van deze genoemde onderdelen heeft een connectie met IMWA Basis. IMWA Basis is de fundering voor IMWA waar alles samenkomt.

In de onderstaande afbeelding is een (voorlopige) weergave te zien van IMWA en de samenhang tussen de verschillende onderdelen binnen IMWA. **Let op!** Dit is nog niet de definitieve versie van IMWA en is onderheven aan veranderingen die tot stand komen door de verdere doorontwikkeling van IMWA.

![De context van IMWA](./algemeen/Bedrijfsobjecten%20model.jpg)
*Totaalplaat van IMWA in samenhang*

Zie voor verdere toelichting van de samenhang tussen de verschillende domeinen in de IMWA bij IMWA Basis: [Catalogus IMWA Basis](https://aquo-standaard.github.io/IMWA-basis/#cat)

## IMWA Watersysteem

Er kan op verschillende manieren (perspectieven) naar een watersysteem gekeken worden. Hoe naar het watersysteem gekeken wordt, is afhankelijk van het werkveld of interesse van een persoon. Het perspectief op het watersysteem bepaald welke informatie gewenst is. En tussen verschillende perspectieven zit vaak een nuancering in informatiebehoefte. In IMWA Watersysteem zijn daarom 4 perspectieven verwerkt:

- Geografie - de ligging en karakterisering van objecten
- Beleid - het beleid dat wordt toegepast(zoals Kaderrichtlijn Water, peilbeheer)
- Juridisch - de wet- en regelgeving die geldig is (zoals Omgevingswet)
- Hydrologie - de verbondenheid van oppervlaktewater in een netwerk

Sommige objecten komen alleen in één perspectief voor en sommige objecten bestaan in meerdere perspectieven en zijn dan met elkaar verbonden.

Toelichting aan de hand van het object oppervlaktewaterlichaam dat in alle perspectieven voorkomt:

- 'geografie': waar ligt het oppervlaktewater en hoe heet het?
- 'beleid': welke doelen moeten er gehaald worden voor dit oppervlaktewater en vanuit welk beleid?
- 'hydrologie': hoe is het oppervlaktewater verbonden met andere wateren?
- 'juridisch': welke wetgeving is er van toepassing in het oppervlaktewater?

### Modelleerbeslissingen

Er zijn vaak meerdere opties om informatie te structureren in een informatiemodel. Hieronder een overzicht van de modelleerbeslissingen zoals we die voor IMWA Watersysteem hebben genomen.

1. **Voor het overzicht is IMWA Watersysteem opgesplitst in de perspectieven:** Geografie, Beleid (KRW/peilbeheer), Juridisch (Omgevingswet) en Hydrologie (netwerk). Ieder perspectief bevat zijn eigen objecten (met eigenschappen), maar heeft wel relaties naar objecten uit de andere perspectieven. Ieder perspectief heeft zijn eigen diagrammen.

2. **De ruimtelijke relaties tussen objecten in IMWA Watersysteem** zijn niet verder uitgewerkt in het conceptuele model. Dit zijn relaties die aangeven hoe objecten ten opzichte van elkaar in de ruimte liggen. Dit is niet nodig/gewenst omdat het model bedoeld is als algemene beschrijving en niet specifiek is voor een bepaald uitwisseldoel. Voor elk uitwisseldoel zullen de benodigde relaties, in overleg met de waterbeheerders, worden bepaald. Ze worden uitgewerkt in de logische informatiemodellen, die hiervoor uit het conceptuele model worden afgeleid.

3. **Voor zowel oppervlaktewaterlichaam als grondwaterlichaam** zijn 2 objecten gemodelleerd. Binnen het perspectief Kaderrichtlijn Water zijn KRWOppervlatewaterlichaam en KRWGrondwaterlichaam gemodelleerd specifiek voor de Kaderrichtlijn Water. Binnen het perspectief juridisch zijn Oppervlaktewaterlichaam en Grondwaterlichaam gemodelleerd specifiek voor de Omgevingswet. Er is hiervoor gekozen omdat ze een andere context en eigenschappen hebben die niet verenigbaar zijn binnen de gegevensuitwisseling.

4. **Er is geen object AfvoergebiedAanvoergebied** binnen het perspectief beleid gemodelleerd. Dit is besloten n.a.v. de consultatie en in samenspraak met DAMO In plaats daarvan is er gekozen om een object Afwateringsgebied te modelleren. Afwateringsgebied kijkt hoe water afwatert in het gebied zelf. Het gaat niet over de aanvoer en afvoer van water tussen verschillende gebieden.

5. **Onder afwateringsgebied zijn verschillende specialisaties gemodelleerd.** Dit zijn: peilgebied, peilafwijkinggebied, bemalingsgebied, boezem, polder, stroomgebied en afwateringseenheid. Dit zijn allemaal gebieden met een andere grondslag waar beleid op wordt uitgeoefend. Peilgebied en peilafwijkinggebied hebben ook nog een 'ligt in' relatie met peilbesluitgebied. Peilgebied en peilafwijkinggebied hebben een juridische grondslag. Bemalingsgebied, polder, boezem, stroomgebied en afwateringseenheid hebben een geografische grondslag. Waarbij stroomgebied en afwateringseeheid weer een hydrologisch grondslag hebben. Doordat deze specialisaties verschillende grondslagen kunnen hebben, waarin beleid wordt uitgeoefend, heeft het moederobject afwateringsgebiedsgebied, twee moederobjecten uit de NEN3610:2022, namelijk juridische ruimte en geografische ruimte.

6. **De objecten OppervlaktewaterKnooppunt, OppervlaktewaterSegment en OppervlaktewaterKruising** (perspectief Hydrologie) zijn directe specialisaties van de objecten met dezelfde naam in INSPIRE. De NEN3610:2022 (het bovenliggende model van Aquo) schrijft namelijk voor dat INSPIRE gevolgd dient te worden bij het modelleren van netwerken.

7. **In het juridisch perspectief hebben we het object Waterstaatkundig gebied toegevoegd.** Dit is een juridisch gebied waarop wetten zoals de Omgevingswet van toepassing zijn. Onder waterstaatkundige gebied hebben wij twee specialisaties gemodelleerd namelijk, waterstaatwerk en waterstaatkundige zone. Waterstaatswerk en waterstaatkundige zone zijn daarmee ook juridische ruimtes. Waterstaatswerk heeft ook weer drie specialisaties conform de definitie van waterstaatswerk in de Omgevingswet: oppervlaktewaterlichaam, bergingsgebied en waterkering. In dit juridische gebied waterstaatswerk liggen daadwerkelijke fysieke objecten, zoals gemaal, dijk, sluis, bergingsgebied, waterbodem, oppervlaktewater etc. waar wetgeving op van toepassing is. Deze fysieke objecten zijn op andere plaatsten in IMWA gemodelleerd, zoals IMWA Kunstwerken en in het perspectief Geografie binnen IMWA Watersysteem. De verschillende waterstaatkundige gebieden hebben een ruimtelijke relatie met elkaar, waarmee deze geaggregeerd kunnen worden. In het conceptueel model zijn deze ruimtelijke relaties niet specifiek gemaakt. Deze relaties moeten concreet gemaakt worden binnen de logische informatiemodellen voor een specifiek informatie uitwisseldoel.

8. **De objecten Kunstwerk en Waterkering hebben, in het perspectief Juridisch, een andere kleur.** Dit is omdat deze objecten uit respectievelijk IMWA Kunstwerken en IMWA Waterveiligheid komen. Kunstwerk en Waterkering hebben via het Juridische perspectief van IMWA Watersysteem een relatie met de waterstaatswerk.

9. **In het juridisch perspectief is een koppeling gelegd** tussen het Waterstaatkundig gebied en de objecten gebiedsaanwijzing water en watersysteem en beperkingsgebied uit het conceptueel informatiemodel Omgevingswet. Zo is er een verbinding tussen IMWA en dit model.

10. **In het peilbeheerperspectief is een vergelijkbare koppeling gelegd** tussen Peilgebied en gebiedsaanwijzing water en watersysteem uit het conceptueel model van de Omgevingswet. Dezelfde koppeling is ook gemaakt met Peilafwijkinggebied. Hierdoor sluiten IMWA en het conceptueel model Omgevingswet goed op elkaar aan.

11. **Vanuit het perspectief van de Kaderrichtlijn Water** spelen er veel meer objecten een rol dan de objecten die nu zijn gemodelleerd binnen dit perspectief. Denk hierbij aan impact, kwaliteitselement, belasting, uitzonderingsbepalingen, maatregelen etc. Deze objecten zijn nu niet binnen het perspectief voor de Kaderrichtlijn Water gemodelleerd, maar worden in andere onderdelen van IMWA ondergebracht. Waar deze precies zullen worden ondergebracht moet nog worden bepaald

12. **Duin en hoge grond zijn toegevoegd** aan het diagram geografie als specialisaties van bodem.

### Openstaande acties

Naar aanleiding van de feedback op IMWA Watersysteem zijn er een aantal acties die in de toekomst ondernomen moeten worden. Deze acties moeten of met de waterbeheerders worden besproken of intern worden uitgewerkt.

Heb je een idee over of een antwoord op één van deze gebruikersvragen, of wil je uitgenodigd worden om mee te praten? Stuur dan een bericht met je feedback of aanmelding naar servicedesk@ihw.nl.

1. **Onderzoeken hoe wij de juiste context en gebruik kunnen aangeven** bij de verschillende domeintabellen en domeinwaarden.

2. **Er moet een begrip worden opgesteld voor 'operationeel peil'** en worden gerelateerd aan de andere type peilen die voorkomen binnen de Aquo-standaard.

3. **De domeintabel ProfielverdedigingConstructieType moet worden gecontroleerd op volledigheid.** Dit moet worden gedaan samen met de waterbeheerders. Hier ligt de inhoudelijke kennis.

4. **De domeintabel SubstraatType moet worden gecontroleerd op volledigheid.** Dit moet worden gedaan samen met de waterbeheerders. Hier ligt de inhoudelijke kennis.

5. **Met de waterbeheerders moet worden afgestemd** welke materialen relevant zijn voor profielverdediging constructies. De domeintabel waarin deze voorkomen kan ook worden gebruikt voor kunstwerken.

6. **Er moet samen met de waterbeheerder worden bepaald** voor wel uitwisseldoel welke relatie gebruikt mag worden voor tussen de verschillende afwateringsgebieden. Dit kan alleen als er een concreet uitwisseldoel bekend is.

7. **De mogelijkheid onderzoeken om de gegevensgroep literatuurverwijzing verplaatsen** van het perspectief beleid Kaderrichtlijn Water naar IMWA Basis, zodat deze gegevensgroep breder gebruikt kan worden.

8. **De domeinlijst WaterstaatkundigeZoneType voorleggen** aan de waterbeheerders voor om de compleetheid te controleren.

9. **De domeintabel OeverType moet samen met de waterbeheerders worden nagelopen** op volledigheid.

10. **De domeintabel OppervlaktewaterType moet samen met de waterbeheerders worden nagelopen** op volledigheid.

11. **Net zoals bij IMWA Kunstwerken zijn de definities** voor de domeinwaarden voor de domeinwaarden nog niet opgesteld. Deze zullen wij op een later moment opstellen samen met de waterbeheerders.

12. **Mogelijkheid modelleren om boven- en ondergrens uit te kunnen wisselen** voor flexibele streefpeilen binnen IMWA Normen.

13. **Mogelijkheid met Linked-data onderzoeken** om direct te linken naar lijsten bij de bron zoals bevaarbaarheidsklasse uit de BRT.

14. **Domeintabel StreefpeilType moet samen met de waterbeheerders worden samengesteld.**