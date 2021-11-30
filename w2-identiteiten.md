# Werkpakket Identiteiten
[(terug naar index)](index.md)

## Ambitie
Als **onderzoeker** 
wil ik **vanuit SURF Research Cloud gemakkelijk authenticeren bij Yoda**
zodat ik **mijn Yoda data kan benaderen**.

## Uitvoering en resultaten
In dit werkpakket hebben we de ambitie belicht vanuit twee perspectieven:   
1) Het perspectief van de gebruiker (hoe kan met dezelfde identiteit  
toegang tot zowel SURF Research Cloud (SRC) als ook Yoda verkregen worden) en    
2) het perspectief van de dienst (hoe kan Yoda de in SRAM gedefinieerde 
collaboraties ondersteunen).

Voor het eerste onderdeel hebben we onderzocht hoe een identiteit momenteel geregistreerd
wordt in SRC, SRAM en Yoda en wat de implicaties daarvan zijn voor praktische koppeling of hergebruik
over diensten heen. Onze conclusie is dat *single-sign-on* authenticatie vanwege een aantal praktische 
belemmeringen nog niet direct realiseerbaar is. De implementatie van een methode voor gedelegeerde
autorisatie is al wel haalbaar. Deze methode hebben we vervolgens uitgewerkt tot een nieuwe
feature *data access password*, die we in Yoda hebben gerealiseerd. Deze feature wordt gepackaged
voor productie met Yoda 1.8.  
Het genereren van access tokens via de OIDC standaard zal vereisen dat iRODS meer complete 
ondersteuning biedt voor authenticatie middels OIDC. Naar verwachting komt dit beschikbaar
per iRODS 4.3.
Uit een praktijk test met SRC en Yoda blijkt dat het data access password gebruikt kan worden
om Yoda data op eenvoudige wijze beschikbaar te maken in een SRC workspace.   
Gerelateerd materiaal:
- [Analyse hergebruik identiteiten](w2/w2-Integreren_Yoda_en_SURF_Research_Cloud_identiteiten.pdf)
bevat de resultaten van het onderzoek naar registratie van identiteiten en de impact daarvan
op hergebruik.
- [Data Access Password Yoda](https://utrechtuniversity.github.io/yoda/design/overview/authentication.html)
beschrijft de gerealiseerde Yoda feature. NB: beschikbaar vanaf Yoda 1.8. 
In de bijbehorende git repository is ook de source code beschikbaar. 
- [Data Acccess testrapport](w3/w3-test-mounted-disk-public.pdf) bevat de resultaten van een praktijk
test waarbij Yoda data beschikbaar wordt binnen SRC met gebruik van het data access password token.


Bij het tweede onderdeel hebben we onderzocht of de Yoda functies *Gebruikersbeheer* en 
*Externe User Service* (deels) via *provisioning* zouden kunnen worden uitbesteed naar SRAM. 
De verwachting was dat hiermee consortia op generieke en uniforme wijze ondersteund 
zouden kunnen worden over diensten heen.
Gedurende het onderzoek hebben we meer inzicht verkregen in de toegevoegde waarde van SRAM en hoe SRAM
zich verhoudt tot SURFConext (en daar ook deels van afhankelijk is).
Dat SRAM niet de organisatie maar de collaboratie centraal stelt, heeft gevolgen voor
het aansluiten van diensten zoals Yoda. Deze gevolgen zijn niet alleen technisch van aard, maar
hebben ook organisatorische en juridische consequenties.   
Uitbesteden van gebruikersbeheer van een dienst zoals Yoda naar SRAM vereist overigens naast 
aanpassingen in authenticatie en user provisioning ook een aanpassing/projectie van autorisaties. 
Per SRAM collaboratie zal een afzonderlijke context nodig zijn (multi-tenant concept).   
Gerelateerd materiaal:
- [autoprovisioning](w2/w2-Autoprovisioning_Yoda_SRAM.pdf) bevat de analyse rond inzet van SRAM voor beheren van gebruikers van Yoda zoals hierboven genoemd.

## Bevindingen en aanbevelingen

Een gedelegeerde autorisatie methode 
kan gebruikt worden om diensten zoals Yoda te ontsluiten binnen een workspace
van SURF Research Cloud. 

**Aanbeveling 1:** Uitwerken van een visie op gedelegeerde autorisatie binnen
de SRAM en/of SURFConext federatie
(door SURF en UU: SURF SRAM, SURF ResearchCloud, Yoda, iRODS).

**Aanbeveling 2:** iRODS en Yoda in het algemeen geschikt maken voor gebruik 
van OIDC tokens (iRODS, SURF, UU). 

Het koppelen van bestaande diensten aan SRAM is niet triviaal.
Naast uitbesteding van authenticatie aan SRAM dient de dienst namelijk
iedere SRAM-CO (collaboratie) afzonderlijk te kunnen verwerken (multi-tenant).

**Aanbeveling 3:** Besluit nemen over ondersteunen (externe) SRAM-CO's in Yoda (door UU).
Daarbij ook afwegen of groepsbeheer volledig wordt uitbesteed aan SRAM danwel 
voor een hybride oplossing wordt gekozen.

