# Oversigt: Programmering en Webside fra Bunden

**OBS**: Du behøver ikke overhovedet læse alting. Den vigtigste information 
fra hver sektion kommer til sidste i sektionen. Du kan bare følge 
overskrifterner og læse den sidste stykke af hver sektion, og så går det fint.

***

Projektets formål er at bygge din egne webside 100% selv. Hvis du har lyst 
til at bygge noget rigtig compleks, det kunne være at du kommer til at bygge 
en multiplayer spil. Ellers, hvis du er mere til HTML og CSS, du kan bygge en
 rigtig smuk webside.
 
Du kommer til at bruge fire programmeringsprog til denne projekt: HTML, CSS, 
Javascript, og Python (med Flask). Jeg har skrevet nogle korte guides til at 
hjælpe dig på vej; disse guides inkludere en cheat sheet og nogle små opgaver.

## Hvordan Fungere en Webside?

Det bliver meget lettere at forstå hvad man laver, hvis man fortså lidt om 
systemet man arbejder på. Her giver jeg en kort beskrivelse for hvad en 
webside er, og hvad der sker når man besøger en.

Vi starter med en computer, some vi kalder for Server. Serveren er bare en 
almindlig Windows 7 computer, som kan køre Microsoft Word og Steam. Det kan 
også køre Google Chrome. På Servers desktop ligger der en HTML fil, der 
hedder index.html. Det ser sådan ud:

```html
<html>
    <body>
        Hello World    
    </body>
</html>
```

Hvis man åbner filen i Chrome, ser man en hvid webside men sort tekst, der 
siger "Hello World". Chrome læser filens indhold, og bruger den til at vise 
en webside.

Server har også adgang til en netværk af andre computere (det er selvfølig 
Internetet). Alle computere på nettet har en **unik** IP addresse, sådan så 
at vi kan genkende hindanden. IP addresser kan erstattes med en domain name 
(f.eks. 8.8.8.8 -> google.com), men det glemmer vi for nu. Når en computer 
har et andets addresse, det kan sende information over nettet. Man skal have 
er router, til at håndtere hvordan indkommende og udkommende information skal
 håndteres.
 
Servers addresse er 123.45.6.7, og andre computere kan sende information til 
denne addresse. Når routeren modtager denne information, kan Server give 
denne information til noget software, og så sende noget tilbage. Det kan, for
 eksemple, være den HTML fil. Det er også muligt, at Server bare tager denne 
 information, og gemmer det til en database. Teoretisk set, kunne denne 
 software lave hvad som helst; man kunne få det til at slukke computeren, 
 eller starte en spil på Steam, når en anden computer besøger en webside.
 
Softwaren som Server bruger til at håndtere information fra nettet er sin 
server software (selvfølig), og det kan være alt muligt. I denne guide vi 
bruger Python med Flask som vores server software.

Så siger vi at der er en anden computer, der hedder User. User er også en 
Windows maskine med Google Chrome. User åbner chrome, og taster ind 
``http://123.45.6.7/index.html`` Chrome forstår at det skal sende en HTTP 
(HyperText Transfer Protocol) besked til Servers IP addresse, og at det skal 
bede om en webside er hedder index.html. Denne beskede bliver sendt igennem
nettet til Server, hvis software  fortålker beskeden. Softwaren forstår at
 det skal sende sin index.html fil til User, så det svarer med filens indhold.
 Chrome på Users computer modtager filen, og bygger websiden fra HTML koden.
 
Det er selvfølig ikke den meste teknisk forklaring, men du kan forhåbenlig 
bedre forstår hvad der sker når du besøger en webside.

Her er en oversigt, der forklar hvordan din webside kommer til at fungere:

```
Bruger sender en besked:
Brugers computer -> Webbrowser -> Din IP -> Router -> Din computer -> Flask
Flask fortålker beskeden, og svarer med nogle HTML kode:
Flask -> Din computer -> Brugers IP -> Router -> Brugers Webbrowser
Og så ser brugeren en webside.
```

## Programmeringsprog: HTML, CSS, Javascript, og Python

Til at lave en webside, skal du bruge fire sprog. Hvert sprog har en special 
grammatik og funktion.

* HTML: Det bruger man til at bygger formen af en webside. Med HTML, 
fortæller man hvad for nogle ting der skal være på websiden, f.eks., tekst, 
billeder, knapper, osv. Hvis en webside var et hus, så er HTML alle murer og 
møbler. HTML er ikke en "rigtig" programmeringsprog, pga. at det har ingen 
funktionalitet. Man kan ikke få det til at gøre noget, udover at fortælle 
hvad websidens indhold skal være.

* CSS: Det bruger man til at give stil til din webside. CSS fortæller hvor 
stor ting skal være, hvad for en farve de skal have, og hvor de skal være på 
siden. Man kan også brug den nyeste udgave af CSS til at lave animationer. I 
den hus analogi, CSS er det der fortæller at murerne er hvide, sofaen er blå,
 og at sengetøjet dækker hele sengen. CSS er heller ikke en rigtig 
 programmeringsprog, fordi det bare beskriver ting.

* Javascript: Det bruger man til alle funktionalitet på en webside. Hvis man 
klikker på en knappe, og så kommer der en alert op, det er Javascript der 
gøre det. Hvis websiden er konstant opdateret med nye overskrifter fra DR, 
det er Javascript. Javascript er den programmeringsprog som er en del af 
websiden. Hvis HTML fortæller at der er en oven i huset, og CSS fortæller at 
den er sort, Javascript er electriciteten der gøre den varm. 

* Python: Det er en programmeringsprog der køre på en computer, ikke på en 
webside. I denne projekt, bruger vi det til at håndtere vores webside. Python
 kan bruge alle mulige "libraries" til at gøre flere ting. Libraries er andre
 mennesker's kode, som du kan bruge til at hurtige løse svare problemer. Vi 
 kommer til at udvikle vores server software med en Python library der hedder
 Flask.
 
En kort oversigt:

* HTML: Hvad der er på websiden

* CSS: Hvordan det ser ud

* Javascript: Hvad det gøre (på websiden)

* Python: Hvad det gøre (på computeren)

* Flask: En library til Python der hjælper *meget* med at lave en web server.

## Kom i Gang: HTML

Man bruger HTML til at sige hvad websidens indhold skal være.

Klik over til HTML.md, og prøv lære det lidt at kende.

Inden du fortsætter, skal du kunne:

* Lave en HTML side med en image, link, og button.

## Quick start: Flask

Nu vil du nok kunne få den webside op på nettet, uden at skulle ved alting om
Python. Første, skal du
[download Python 3](https://www.python.org/downloads/).

Hvis noget ikke fungere, skal du bare spørge en pirat kaptajn, eller bruge 
Google!

## Kom i Gang: CSS

## Kom i Gang: Javascript

## Kom i Gang: Python

## Kom i Gang: Flask

## Tillæg: Løser Problemer med Google

Halvdelen af at være programmør er at kunne bruge Google til at finde ud af 
ting (det er ikke et joke, det er *mindst* 50% af den tid jeg bruger på 
projekter). At finde løsninger til dine problemer er en færdighed du kommer 
til at blive rigtig god til, så får du nogle tips til det her.

Man kan næsten altid finde dokumentation for libraries eller software på 
nettet. For eksemple, hvis du vil vide lige præcis hvordan Flask håndtere en 
"response" fra nettet, kan du finde udviklerners beskrivelse på deres 
[documentation side](http://flask.pocoo.org/docs/1.0/api/#response-objects).
Det er brugbart at kunne forstå tungt dokumentation. Man kan som regel finde 
den rigtig dokumentation ved at søge, f.eks., ``python 3.7 string join 
documentation``.

Hvis du har ingen anelse for hvad man overhoved skal lave, er det nok bedste 
at søge efter hvad man vil lave i forbindelse med programmeringsproget. F.eks.,
``python 3 how to join two strings``. Du kommer til at finde de bedste 
resultater på
[StackOverflow](https://stackoverflow.com/),
som er den meste populær forumer til programmeringshjælp.

Hvis du får en error når du prøver at køre din kode, skal du nok bare søge 
efter error teksten i forbindelse med programmeringsproget og functionen.
For eksemple, man kunne få den følgende error:

```python
>>> ''.join([1, 2, 3])
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: sequence item 0: expected str instance, int found
```

Så er en god Google søgelse måske ``python join TypeError: expected str 
instance, int found``. Og så finder man
[en god resultat](https://stackoverflow.com/questions/10880813/typeerror-sequence-item-0-expected-string-int-found).

Du skal øve dig it at finde løsninger til dine problemer! Det bliver din 
meste vigtig færdighed som programmør.

## Tillæg: Hosting til Din Projekt

Efter du har fået din projekt til at køre på en lokale netværk, vil du nok 
kunne få den op på nettet. Du kan gøre det fra din egen computer, men så skal
 det være tændt for at andre kan besøg din webside. Derfor, finder man en 
 "hosting service" til at køre din server for dig. 

## Tillæg: Projekt Ideèr

Nok den sværeste del af at lave en projekt, er at få en idè til hvad du skal 
overhovedet lave! Jeg vil give dig en liste, som måske sparker lidt 
inspiration til dig.

Du kunne, for eksemple, lave din egne udgave af en nuværende webside:

* En social netværk: Facebook, Instagram, osv.

* En chat program: Discord

Nok den meste populær og udfordrende idè er at lave en spil

* En idle-spil (f.eks. Cookie Clicker, Universal Paperclips)

* En multiplayer quiz (f.eks. Kahoot, Jeopardy)

* En grafisk multiplayer spil (udfordrende!) (f.eks Agar.io, Fortnite, 
Runescape)

(Jeg vil tilføje til denne liste, når jeg eller dig kommer i tænke om noget 
flere gode!)

Være **IKKE** bange for at eksperimenter!