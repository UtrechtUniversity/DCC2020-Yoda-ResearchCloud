# Werkpakket Identiteiten
[(terug naar index)](index.md)

## Ambitie
Als **onderzoeker** 
wil ik **vanuit SURF Research Cloud gemakkelijk authenticeren bij Yoda**
zodat ik **mijn Yoda data kan benaderen**.

## Uitvoering en resultaten

- hoe kan een gebruiker meerdere diensten gebruiken met dezelfde identiteit?
  -> gedelegeerde autorisatie is de oplossing
  -> Data access password  + POC
[identiteiten ontwerp](w2/w2-Integreren_Yoda_en_SURF_Research_Cloud_identiteiten.pdf)
[Data Access Password Yoda](https://utrechtuniversity.github.io/yoda/design/overview/authentication.html)

[Data Acccess testrapport](w3/w3-test-mounted-disk-public.pdf)

- hoe kan een dienst als Yoda gebruikt worden in collaboraties gedefinieerd door SRAM?
  -> SRAM heeft meer implicaties dan gedacht
  -> LDAP niet de oplossing voor alles
  -> user provisioning via SRAM?
[autoprovisioning](w2/w2-Autoprovisioning_Yoda_SRAM.pdf)





## Bevindingen en aanbevelingen

Een gedelegeerde autorisatie methode 
kan gebruikt worden om diensten zoals Yoda te ontsluiten binnen een workspace
van SURF Research Cloud. 

**Aanbeveling 1:** Uitwerken van een visie op gedelegeerde autorisatie 
(door SURF en UU: SURF SRAM, SURF ResearchCloud, Yoda, iRODS).

**Aanbeveling 2:** iRODS en Yoda in het algemeen geschikt maken voor gebruik 
van OIDC tokens (iRODS, SURF, UU). 

Het koppelen van bestaande diensten aan SRAM is niet triviaal.
Naast uitbesteding van authenticatie aan SRAM dient de dienst namelijk
iedere SRAM-CO (collaboratie) afzonderlijk te kunnen verwerken (multi-tenant).

**Aanbeveling 3:** Besluit nemen over ondersteunen (externe) SRAM-CO's in Yoda (door UU).
Daarbij ook afwegen of groepsbeheer volledig wordt uitbesteed aan SRAM danwel 
voor een hybride oplossing wordt gekozen.

