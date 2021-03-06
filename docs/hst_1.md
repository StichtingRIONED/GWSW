# Evaluatie Nulmeting

De juiste interpretatie van de nulmeting-resultaten vraagt kennis van het gehele proces. De GWSW Nulmeting dient alleen door daarin getrainde adviseurs uitgevoerd te worden. 
Algemene informatie over de GWSW Nulmeting is te vinden in:
* Het document GWSW Nulmeting Beschrijving (download op [apps.gwsw.nl](https://apps.gwsw.nl) )

## Procedure meting gegevenskwaliteit
* Vul de GWSW Dataset: upload een GWSW.orox export
* Start de nulmeting: toets de dataset aan de gekozen conformiteitsklasse, bijvoorbeeld "MdsPlan" 
* Voer de nulmeting uit en analyseer de resultaten
* Doe eerst een "quick-scan". Als er veel onbekende of te globale typeringen zijn, is de overige kwaliteitsmeting niet betrouwbaar. Breng dan eerst de database voor wat betreft de typering op orde. Daarmee voorkom je dat er twee keer een “zwaar” metingtraject wordt doorlopen. (ervaring met case Tholen)
* Gebruik de GWSW-Geoserver (via het WFS protocol) om de grafische presentatie te vergelijken met die van het Beheersysteem
* Voer de nulmeting opnieuw uit en herleid de foutmeldingen:
	- Oorzaak in native database? (dus beheersysteem nodig bij de analyse) = melden bij beheerder
	- Oorzaak in de exportfunctie Orox ? (opbouw/mapping GWSW.orox bestand onvoldoende)  = melden bij softwareleverancier (altijd via RIONED)
	- Oorzaak in de nulmeting (foute werking) = melden bij RIONED
	- Oorzaak in de ontologie (GWSW algemeen of de CFK, bijvoorbeeld: bepaalde types ontbreken nog) = melden bij RIONED

## Eerdere analyse van de werking
(oktober 2017 - januari 2018)

**Inrichting conformiteitsklassen**
Op de websites de kwaliteit van de conformiteitsklassen (bijvoorbeeld [MdsPlan](https://apps.gwsw.nl/MdsPlan)) controleren:
* Zijn alle soorten vermeld?
	- Zijn ze niet te globaal?
	- Zijn ze niet te gedetailleerd?
* Zijn alle kenmerken vermeld?
	- Zijn ze terecht verplicht? ("exact = 1")
	- Zijn ze terecht optioneel?

**Document GWSW Nulmeting Beschrijving controleren:**
* Is het leesbaar voor buitenstaanders?
* Is het volledig?
	
**De rapportage van de nulmetingen (vooralsnog in platte csv-vorm) controleren:**
* Is het leesbaar voor buitenstaanders?
* Staat er voldoende informatie in om conclusies te kunnen trekken?
* Welke vervolgrapportage (met die conclusies) moet er komen?
