# Aandachtspunten bij upload naar GWSW-Dataset #

Deze analyse is gebaseerd op:
* de verslaggeving van Diet van Wendel (mailing dd najaar 2017) 
* de verslaggeving van Gwendolijn Vugs (notitie dd 20180124, kenmerk N002-1260650GBV-V01-hgm-NL)
* de meldingen van de GWSW Adviseurs (vanaf februari 2018 tot heden)

## Geconstateerd tijdens upload GWSW.orox ## 

Tip: de foutmeldingen en het vermelde regelnummer ("[line nnn]") zijn niet altijd traceerbaar in het .orox-bestand. Parse het bestand met het beheersysteem voor een aanvullende analyse.

Response: "RDF Parse Error: IRI included an unencoded space: '32' [line 13]" (20171031)
<span style="color:blue">_Oorzaak: bug in Obsurv versie 2.0. In IRI bestandsnaam (metagegevens) kan geen spatie voorkomen. (regelnummer van de melding kan dus iets afwijken van die in het .orox bestand)_</span>

Response: "RDF Parse Error: Expected ':', found '\r' [line nnnn]" (20171031)
<span style="color:blue">_Oorzaak: bug in Obsurv versie 2.0. In IRI gwsw-concept ":Buiten gebruik"staan spaties. Concept-IRI moet zijn :LozeLeiding._</span>

Response: "RDF Parse Error: Illegal predicate value: \"xxx\"^^ [line nnn]" (20171031)
<span style="color:blue">_Oorzaak: bug in Kikker. In IRI bim-concept Stelsel staan spaties._</span>

Response: "RDF Parse Error: Unexpected end of file" (20171101)
<span style="color:blue">_Oorzaak: mogelijke bug in Obsurv, laatste regel is geen afgeronde triple._</span>

Response GWSW Server: "fout bij decoding … geen utf-8 ?" (20171101)
<span style="color:blue">_Oorzaak: mogelijke bug in Kikker. GWSW Server is gevoelig voor bestandsformaat, moet UTF-8 zijn (zonder BOM / Signature). Dat geldt ook wanneer er een enkel niet-UTF-8-karakter voorkomt. Dan het bestand expliciet opnieuw opslaan in UTF-8 (lukt nog niet met Notepad++, wel met Visual Studio)._</span>

Upload geslaagd, alleen geen putten en leidingen zichtbaar (20180906, Haarlemmermeer)
<span style="color:blue">_Oorzaak: In de Kikker-export conform GWSW-OroX versie 1.4 waren de prefixes voor GWSW-concepten en Gemeente-objecten juist gedefinieerd, maar omgedraaid toegepast in het GWSW.orox bestand._</span>
