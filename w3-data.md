# Werkpakket Data
[(terug naar index)](index.md)

## Ambitie
Als **onderzoeker** 
wil ik **gemakkelijk data kunnen uitwisselen** tussen Yoda en 
SURF Research Cloud
zodat ik van mijn analyses in workspaces **de data goed kan beheren**. 

Als **data manager**
wil ik **gevoelige data kunnen uitwisselen** tussen Yoda en
SURF Research Cloud
zodat **gevoelige data veilig in analyses gebruikt** kunnen worden. 

## Uitvoering en resultaten
In dit werkpakket maken we een aantal realisaties voor het benaderen
van in Yoda vastgelegde data binnen de context van een 
SURF Research Cloud (SRC) workspace. 
Daarnaast onderzoeken we hoe gevoelige data op een veilige wijze
beschikbaar kan worden gemaakt in een SRC workspace.

Voor het benaderen van Yoda data vanuit een SRC workspace zijn verschillende
realisaties gewenst omdat er conflicterende behoeften
bestaan voor de interactie tussen gebruiker en systeem. 
Er zijn onderzoekers die graag een grafische desktop omgeving gebruiken
en andere onderzoekers die opdrachten liever via de commandline *shell* verstrekken.
De voor SRC gerealiseerde integraties zijn: 
desktop applicatie voor synchronisatie, netwerk disk, commandline.   
Gerelateerd materiaal:
- [Grafische irsync](https://github.com/UtrechtUniversity/researchcloud-items/blob/main/docs/roles/irods_guisync.md)
bevat een binnen het project ontwikkelde, op Python en Gtk3 gebaseerde, desktop applicatie. 
De gebruiker kiest uit een lijst een Yoda folder en een SRC folder, daarna wordt de data
gesynchroniseerd in de gewenste richting. 
- [Ontwerp robuuste data transfer](https://github.com/UtrechtUniversity/energize) 
bevat een ontwerp voor een uitbreiding van de grafische irsync om onder meer transfer van grote 
databestanden (> 1 TB) herstartbaar te maken. 
- [Testrapport netwerk disk](w3/w3-test-mounted-disk-public.pdf) beschrijft een praktijk test van 
een mogelijkheid om Yoda als gekoppelde netwerk disk te benaderen (WebDAV protocol). Deze methode 
maakt gebruik van een bestaande SRC voorziening voor koppelen ResearchDrive en van de binnen
het project ontwikkelde Data Access password feature in Yoda. 
Data op een netwerk disk is voor workspace applicaties te benaderen alsof het een lokaal 
filesysteem betreft en vormt daardoor een gebruikers-vriendelijke oplossing. De toepasing van
deze oplossing vereist nog dat SURF een kwetsbaarheid in de SRC ResearchDrive koppeling oplost.  
- [Commandline iCommands set](https://utrechtuniversity.github.io/researchcloud-items/playbooks/icommands.html)
bevat een voorziening om data transfer met Linux shell commando's te kunnen uitvoeren. De 
gerealiseerde scripts installeren de iRODS icommands toolset in een 
SRC workspace (zie ook werkpakket 1). 

Een veelvoorkomende use-case in onderzoek betreft het verwerken van tijdelijk beschikbaar gestelde 
privacy- of anderszins gevoelige data.  
Instellingen en onderzoekers wensen hiervoor voldoende maatregelen te kunnen treffen om de 
vertrouwelijkheid van de data te beschermen.  Een onderdeel van deze maatregelen vormt het 
gecontroleerd transport van data van en naar de verwerkingslokatie.    
We onderzoeken hoe deze 'sluis' functie kan worden geimplementeerd. We onderkennen drie varianten
waarbij de implementatie van de sluisfunctie in een separate omgeving in SRC onze voorkeur heeft.   
Gerelateerd materiaal:
- [sluisfunctie ontwerp](w3/w3-sluisfunctie-ontwerp.pdf) bevat een analyse op hoofdlijnen van 
de vereisten voor een sluisfunctie, architecturele opties voor implementatie met voor- en nadelen
van de verschillende opties.


# Bevindingen en aanbevelingen
Voor de verwerking van gevoelige data is de huidige functionaliteit van SURF Research Cloud 
onvoldoende geschikt. De beoogde sluisfunctie zal alleen effect hebben als de workspace
voldoende geisoleerd is van het internet.

**Aanbeveling 1:** Implementatie van een workspace configuratie geschikt voor gevoelige data (SURF).
Na oplevering kan de ontworpen sluisfunctie geimplementeerd kan worden (UU). 

De gerealiseerde gebruiksvriendelijke interface voor het uitwisselen van data met Yoda/iRODS 
is nog niet geschikt voor grotere bestanden (Terrabytes) waar eisen worden gesteld aan
herstartbaarheid van het data transfer proces.

**Aanbeveling 2:** Aandacht vragen bij iRODS consortium voor de realisatie van betere client-side 
tools (UU, SURF en andere iRODS Consortium leden).
