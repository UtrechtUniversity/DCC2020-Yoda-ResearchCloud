# Werkpakket Data
[(terug naar index)](index.md)

## Ambitie
Als **onderzoeker** 
wil ik **gemakkelijk data kunnen uitwisselen** tussen Yoda en 
SURF Research Cloud
zodat ik van mijn analyses in workspaces **de data goed kan beheren**. 


## Uitvoering en resultaten

TODO: hier documentatie toevoegen die informatie, bevindingen en deelresulaten als
link in zich dragen.  poc?

[sluisfunctie ontwerp](w3/w3-sluisfunctie-ontwerp.pdf)

[grafische irsync](https://github.com/UtrechtUniversity/researchcloud-items/blob/main/docs/roles/irods_guisync.md)

[ontwerp robuuste data transfer](https://github.com/UtrechtUniversity/energize)

[testrapport mounted](w3/w3-test-mounted-disk-public.pdf)


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
