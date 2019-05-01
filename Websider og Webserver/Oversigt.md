#Oversigt: Programmering en Webside fra Bunden

Projektets formål er at bygge din egne webside 100% selv. Hvis du har lyst 
til at bygge noget rigtig compleks, det kunne være at du kommer til at bygge 
en multiplayer spil. Ellers, hvis du er mere til HTML og CSS, du kan bygge en
 rigtig smuk webside.
 
Du kommer til at bruge fire programmeringsprog til denne projekt: HTML, CSS, 
Javascript, og Python (med Flask). Jeg har skrevet nogle korte guides til at 
hjælpe dig på vej; disse guides inkludere en cheat sheet og nogle små opgaver
. Jeg anbafaler er du læser første denne side, og så start med at lære HTML. 

##Hvordan Fungere en Webside?

*(Du behøver ikke læse denne sektion, men du kommer til at forstå din webside 
rigtig meget bedre hvis du gøre)*

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
Windows maskine med Google Chrome. User åbner chrome, og taster ind:

`
http://123.45.6.7/index.html
`

Chrome forstå det som en

##