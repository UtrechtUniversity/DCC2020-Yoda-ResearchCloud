# Werkpakket Basis
[(terug naar index)](index.md)

## Ambitie
Als **onderzoeker** 
wil ik een **vindbare en toegankelijke workspace**
zodat ik mijn **analyse en data management op een 
veilige en schaalbare manier** kan doen

## Uitvoering en resultaten
Bij dit werkpakket hebben we SURF Research Cloud (SRC) verkend en daarbij onderzocht welke 
ondersteuning en voorzieningen onderzoekers en hun ondersteuners nodig hebben 
bij gebruik van deze oplossing.  Dit hebben we uitgevoerd door functies van de dienst
uit te proberen, en aan de hand van deze gegevens een team te formeren voor het ondersteunen
van pilots.   
Gerelateerd materiaal:
- [whoarewe](https://utrechtuniversity.github.io/researchcloud-items/whoiswho.html) beschrijft het
pilot team dat gebruik van de dienst ondersteunt. Onderscheid wordt gemaakt tussen functioneel beheer
gerelateerde activiteiten enerzijds en consultancy/ontwikkeling activiteiten anderzins.

Vervolgens heeft dit team de pilot gebruikers begeleid bij on-boarding en gebruik.
Daarbij is gedurende het proces feedback verzameld over gebruiksgemak, wensen, en knelpunten.
Deze feedback is gebruikt om instructie materiaal mee samen te stellen. Ook heeft dit geleid
tot een aantal verbeter suggesties voor de dienst (ingediend bij SURF Servicedesk dan wel besproken
met het SURF SRC Team).     
Gerelateerd materiaal:
- [primer for users](https://utrechtuniversity.github.io/researchcloud-items/primer-for-users.html)
bevat instructies voor nieuwe gebruikers.
- [SRC workshop](https://utrechtuniversity.github.io/researchcloud-items/primer/workshop-src.html)
geeft het ondersteuning team suggesties voor het met 1:1 workshops begeleiden van on-boarding 
van nieuwe gebruikers.

Voor een nuttig gebruik van SRC door de pilot users heeft het team
de SRC catalogus uitgebreid met eigen items en hiervoor configuratie-scripts ontwikkeld.   
Gerelateerd materiaal:
- [Matlab workbench](https://utrechtuniversity.github.io/researchcloud-items/playbooks/matlab.html)
is een catalogus item (plugin) waarmee onderzoekers tijdrovende analyses en
simulaties gemakkelijk en snel op krachtige workspaces kunnen uitvoeren.
- [Python workbench](https://utrechtuniversity.github.io/researchcloud-items/playbooks/python-workbench.html)
is een plugin die het voor Research Engineers gemakkelijk maakt Python
applicaties te ontwikkelen en beschikbaar te stellen. De workbench biedt de mogelijkheid
voor het seleteren van een specifieke Python interpreter versie en afhankelijkheden tussen 
Python modules kunnen met package manager Poetry beheerd worden.  
- [iRODS icommands](https://utrechtuniversity.github.io/researchcloud-items/playbooks/icommands.html)
is een plugin die de commandline tools van iRODS installeert in een workspace.
Daarmee kunnen datamanagers en onderzoekers de Yoda datamanagement
omgeving benaderen vanuit SRC. 
- [iSelect](https://utrechtuniversity.github.io/researchcloud-items/roles/irods_iselect.html)
is een binnen het project gerealiseerde op Python gebaseerde applicatie en plugin-rol, 
die de verbinding met een Yoda datamanagement server configureert met de voor die server 
benodigde eigenschappen.
SRC gebruikers kunnen hun favoriete Yoda (of iRODS) omgeving uit een lijst selecteren.        
Gerelateerd materiaal:
- [catalog items](https://utrechtuniversity.github.io/researchcloud-items/) git repository met
scripts voor deployment van SRC plug-ins, waaronder de hierboven uitgelichte voorbeelden.

Vanwege het pay-per-use karakter van de dienst hebben we ook onderzocht hoe kosten verrekening zou
kunnen gaan plaatsvinden. Uitgangspunt vormt de accounting rapportage vanuit SURF zoals die
medio 2021 is ingeregeld.  De accounting concepten van SURF zijn geprojecteerd op verrekening
en doorbelasting behoeften vanuit de instelling. Met een Proof-Of-Concept is vastgesteld dat
de accounting rapportage geautomatiseerd zou kunnen worden verwerkt om doorbelasting mee te sturen.   
Gerelateerd materiaal:
- [accounting](w1/w1-accounting.pdf) bevat een uiteenzetting van accounting concepten, 
aanbevelingen voor gebruik van deze concepten, en de source en resulatten van de Proof-Of-Concept.


# Bevindingen en aanbevelingen
Onderzoekers zijn enthousiast over SURF Research Cloud. De on-boarding van nieuwe gebruikers
vergt nog wel veel handmatige en tijdrovende activiteiten.

**Aanbeveling 1:** Versnel het wallet uitgifte proces door ondersteuners via de portal
wallets te laten aanmaken voor onderzoekers (SURF, UU).

Het universiteitsbreed inzetten van SURF Research Cloud vraagt om structurele ondersteuning
in de vorm van functioneel beheer en het bieden (en onderhouden) van een aantrekkelijke
portfolio aan catalogus items.

**Aanbeveling 2:** Start een project om de huidige UU-pilot van SURF Research Cloud 
te bestendigen in een structurele UU dienst (UU). 
Werk daarbij samen met SURF en andere instellingen om een gemeenschappelijke portfolio
te ontwikkelen en te onderhouden (UU, SURF, andere instellingen).
 
NB: Aanbeveling 2 heeft inmiddels opvolging gekregen: 1) Er ligt een projectplan ter goedkeuring
bij UU management voor implementatie van de dienst in 2022. 2) In 2022 starten UU, TU/e, 
WUR, en HU met een vervolg DCC project dat zich ten doel stelt een developer community,
richtlijnen en portfolio items te ontwikkelen voor SURF Research Cloud. 

