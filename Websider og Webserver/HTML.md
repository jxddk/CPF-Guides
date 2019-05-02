# HTML

## Værktøje

Du hehøver ikke noget specialt software til at skrive HTML; du kan bare brug 
Notepad/Noteblok til at skrive en tekst fil, og gem den som webside.html. Du 
kan åbne siden med Google Chrome, og så se resultatet.

Man kan også bruge software, der fortæller når man har skrevet noget forkert, 
og hjælper med at skrive hurtig. Jeg kan godt lige 
[Sublime Text 3](https://www.sublimetext.com/3),
men
[Notepad++](https://notepad-plus-plus.org/)
eller
[Atom](https://atom.io/)
er også rigtige gode.

## Kom i Gang

### En Enkelt Prøveside

Første, skal du kunne bare lave en enkelt fil. Åbner din teksteditor 
(Notepad/Noteblok, hvis ikke du bruger noget specialt), og skrive den følgende:

```html
<html>
    <body>
        <p>Hello World</p>
    </body>
</html>
```

Gem filen som `page.html`, og så åbne det i in browser (du kan nok bare dragge 
den over til browservinduet). Hvis du bare ser `Hello World`, det er 
en succes (hvis du ser koden selv, så er noget gået galt).

### Grammatik

En HTML fil består af elementer. Dette er en element:

```html
<element id="theElement">I'm an element!</element>
```

En element er defineret af sine "tags", og det har en der åbner elementet, og
en der lukker den. Den åbner med `<element>` tagget, og lukker med 
`</element>` tagget. Elementer er beskrivet af "attributes", som er indenfor 
den første tag. Her, `element` har en attribute der hedder `id`, og har værdien
`theElement`. En element kan indhold andre elementer mellem sine tags, eller 
det kan bare indhold rent tekst.

Kig tilbage til `page.html`, som du lige har lavet. Du kan godt se, at den 
består af en `html` element, der indholder en `body` element, der indholder 
en `p` (paragraf) element, der indholder tekst. Ingen af elementerne har 
attributes.

### Struktur

```html
<html>
    <head>
        <title>A Page</title>
    </head>
    <body>
        <p id="mainText">Some text</p>
    </body>
</html>
```

Du skal starte din HTML side med en `html` element, der indholder resten af 
siden. Man kan tilføj en `head` element, der indholder information om siden, 
f.eks. titlen.  `body` elementet, der kommer efter headen, indholder 
elementerne som du kommer til at kunne se på siden.

Selvdom der er ikke nødvendig at formatet ser så organizeret ud, det er meget
 letter at læse og derfor lave om end, f.eks:
 
```
<html><head><title>A Page</title></head><body><p id="mainText">Some text</p></body></html>
```

### Elementære Elements

Her er nogle elementer, du kommer til at bruge tit (og, hvordan du bruger dem).

#### \<p> - Paragraf

En paragaf, skal bare indholde tekst

```html
<p>This is just some text.</p>
```

#### \<h1> - Heading

En heading (overskrift), som udtrykkes som stor tekst. Der findes også h2, 
h3, osv., som er bare mindre udgaver af den samme.

```html
<h1>HeadingText</h1>
```

#### \<hr> - Horisontal Line

Bare en horisontal line på siden. Det behøver ikke have en lukkende tag.

```html
<hr>
```

#### \<br> - Break

Ligesom `<hr>`, men bare en usynlig ny line i teksten.

```html
<br>
```

#### \<img> - Image

En foto på din side

```html
<img src="https://codingpirates.dk/wp-content/uploads/2016/09/Forside-Logo
.png" height="50" width="50"/>
```

Bemærk at du skal give en filnavn eller URL i `src` attributen. Det kan 
skrives uden en lukkende tag, bare med en `/` til sidst. `height` og `width` 
er ikke nøgvendig, men kan være brugebare.

#### \<a> - Link

En `<a>` link indholder nogle tekst som man kan klikke på som et link.

```html
Besøg <a href="https://codingpirates.dk">Coding Pirates</a> på nettet!
```

Man skal skriv en URL i `href` attributen. En `<a>` element kan også indholde
 f.eks. en billede, som så fungere også som et link.

#### \<title> - Titlen

En `<title>` tag skal være indenfor din `<head>` element. Indholder kommer 
til at være tilten af din webside når man åbner den i browseren.

```html
<head>
    <title>My Page</title>
</head>
```

### Andre Elementer

#### \<!-- Kommentar -->

Hvis du vil skrive nogle kommentar i din HTML kode, som ikke er synligt på 
siden, kan du skrive dine kommentar sådan:

```html
<p>Some text saying some <!-- Hemmelig kommentar fra udvilkeren --> things inside a p tag</p>
```

#### \<ul>, \<ol>, \<li> - Lister

`ul` betyder Unordered List, `<ol>` betyder Ordered List, og `<li>` betyder 
List Item.

```html
<ul>
    <li>Mælk</li>
    <li>Æg</li>
    <li>Brød</li>
</ul>
<ol>
    <li>One</li>
    <li>Two</li>
    <li>Three</li>
</ol>
```

#### \<div> - Divider

En `<div>` element er meste brugbar når man bruger CSS. Det kan gruppe 
elementer sammen:

```html
<div>
    <img src="http://web.site/img.jpg"/>
    <p>That's a picture.</p>
</div>
```

#### \<button> - Button

En `<button>` tag definer en button, der kan køre Javascript når man klikker 
den. Eksemplen herunder er en button der siger "Click Me", og siger "Hej" når
 man klikker den.
 
```html
<button onclick="alert('Hej')">Click Me</button>
```

#### \<input> - Input

#### \<table>, \<tr>, \<td> - Tables

#### \<i>, \<b>, \<u> - Tekst Stil

#### \<video> - Video

#### \<iframe> - Webside Frame

#### \<blink>, \<marquee> - Sjov Tekst

#### Flere Elementer

Du kan finde flere elementer på
[W3Schools](https://www.w3schools.com/tags/)
eller
[Mozilla](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

### Attributes

Elementer kan have alle mulige attributes (egenskaber), som bliver meste 
brugbare når du skal brug CSS og Javascript. `id` definere en **unik** navn 
til elementet, sådan så at man kan specificere elementet med Javascript. 
`class` definere hvilken gruppe elementet høre til, sådan så at CSS kan give 
den sammen stil til hele gruppen. `style` definere nogle CSS, som giver stil 
til elementet.

```html
<p id="mainText" class="textBlock" style="color: red;">This is my text.</p>
```

## Oversigt

En HTML side består af elementer, der er defineret ved en tag. Elementer kan 
have attributes, der beskriver dem. Elementer kan indholde hinanden. 

## Opgaver

Hvis du du øve dig, prøve lave en af de her opgaver. Du må gerne kopier tekst
 fra en eksemple, men prøve at skrive det selv, og ikke bare copy-paste.
 
* En webside, der fortæller om dig.

* To sider, der linker til hindanden.

* En webside med nogle billeder, og en af dem linker til et andet side på 
nettet.

Hvis du mangler inspiration til et større projekt, prøv en af de her:

* Et nyt design til Facebook

* En Wikipedia side om dig

* Få inspiration fra *alle* websider du besøger! Prøv lave en kopi af en af dem

* Søge efter nogle design inspiration, f.eks.
[her](https://www.webdesign-inspiration.com/)

## Cheat Sheet

Denne kan du brug til at hurtig slå op hvad for nogle elementer du kender, og
 hvordan man bruger dem.

### Element Struktur

```html
<p id="mainText">Some text</p>
```

Husk at man åbner en element sådan: `<element>`, og lukker den sådan: 
`</element>`. Nogle elementer kan bare skrives sådan: `<img id="Image"/>`. 
Elementer kan indholde andre elementer indenfor sine åbende og lukkende tags.
 Elementer kan indholde attributes (egenskaber) indenfor sine åbenende tag 
 sådan: `<element attribute="Attribute Value">"`. 

### Side Struktur

```html
<html>
    <head>
        <title>A Page</title>
    </head>
    <body>
        <p id="mainText">Some text</p>
    </body>
</html>
```

### Liste over Elementer

Du kan kigge tilbage til Elementære Elementer og Andre Elementer for at se, 
hvordan de bruges.

### Eksemple Side med Nogle Elementer