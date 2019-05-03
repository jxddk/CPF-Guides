# CSS

(inden du begynder på CSS, skal du nok lære at bruge HTML)

## Værktøje

Ligesom med HTML, CSS kan bare skrives med en rent almindlig teksteditor, men
 der findes jo mange andre muligheder; de samme programmer der er gode til at 
 skrive HTML, plejer også at være gode til CSS.

## Kom i Gang

### Sådan Tilføjer Man CSS til HTML

Man kan brug CSS til at tilføje stil til en webside. CSS kan føjes til en 
webside på tre måder (som er listet herunder). Det er en dårlig idè at brug 
flere end en måde på en projekt!

#### CSS i \<head> Elementet

Man kan rigtig nemt skrive noget CSS i en HTML side, med den følgende mønster:

```html
<html>
    <head>
        <title>CSS Eksemple</title>
        <!-- Man skriver CSS i <style> elementet -->
        <style>
            // det her er CSS!
            #mainText
            {
                color: #00FF00;
            }
        </style>
    </head>
    <body>
        <p id="mainText">Hej</p>    
    </body>
</html>
```

#### Linked CSS

At skrive CSS i \<head>\<style> er en fint måde at gøre det på,
men nogen gange vil man kunne brug et andet fil til sin CSS, og så læse det
 fra HTML siden. Det gøre det letter at holde styre på CSS, versus HTML.
 
Så skriver man bare den samme code man havde i \<style> elementet, og gemmer 
det som en `.css` fil, f.eks. `stylesheet.css`. Så skal man bare føje en 
`<link>` element til sin HTML side, med `href` attributen der siger hvor din 
CSS fil hedder:

```html
<head>
    <link href="stylesheet.css" rel="stylesheet">
</head>
```

`rel` attributen skal bare sige "stylesheet", sådan at HTML siden hvordan `
.css` filen skal fortålkes.

#### Inline CSS

I stedet for at holde CSS helt separat fra resten af siden, man kan godt bare
 skrive CSS som en attribute af en element.
 
`<p style="color: #00FF00;" id="mainText">Hej</p>`

Det er hurtig og enkelt, men når man skriver en masse HTML, kan det godt bliv
 hurtig forvirrende. Men der er ikke noget galt med at brug inline CSS, når 
 det giver bedste mening til projeket.

Ud af disse tre muligheder, anbefaler jeg at man bruger CSS i \<head> 
elementet som begynder, så man kan bedre henvise til sin HTML.

### CSS Struktur

Inden du begynder på at bruge CSS, skal du lige forstå strukturen af en CSS 
fil. Kigge lige på eksemplen:

```css
#mainText
{
    color: #00FF00;
    bg-color: #FF00FF;
}
```

På den første linje, fortæller man hvilken HTML elementer skal påvirkes af 
denne CSS. `#` betyder at vi vil kun udvælge elementer med en `id` attribute 
der svarer til hvad vi har skrevet (f.eks. `<p id="mainText">`). Derefter, 
åbner vi brackets (`{ ... }`), og putter nogle CSS egenskaber derind. Vi vil 
føje `color` og `bg-color` (background-color) egenskaber til vores udvælgt 
element. Hver egenskab er på en linje med den sammen syntaks. Linjen starter 
med ejenskabs navn, og så en `:`, og så en værdi til egenskab (f.eks, hvad 
for en farve det skal være), og så slutter med en `;`.

Denne eksemple påvirker kun elementer med en rigtig `id`, og pga. at en `id` 
burde være unik, denne CSS påvirker kun en element. Derfor, bruger man 
`class` attributten til at udvælge flere elementer af en slags.

```html
<p class="text">Hej</p>
<p class="not_text">Nej</p>
<p class="text">Bye</p>
```

For at udvælge kun "Hej" og "Bye", kunne man skrive:

```css
.text
{
    // css here
}
```

Forskellen er, at man skriver `.text`, i stedet for `#text`, for at udvælge 
elementer med den rigtig `class`, i stedet for den rigtig `id`. Hvis man vil 
udvælge alle elementer af en slags (f.eks. alle `<p>` elementer), bruger man 
ingen specialtegn:

```html
p
{
    // css here
}
```

Man kan skrive kommentar i CSS med `//`.

### Elementære Egenskaber

Der findes helt vildt mange CSS egenskaber, men du bvehøver ikke kende dem 
alle. Jeg beskriver lige de meste brugbare, og så kan du godt kom i gang.

* `color` - Hvad for en farve teksten skal have (f.eks `color: blue` eller 
`color: #FF00FF`)

* `bg-color` eller `background-color` - Hvad for en farve bagrundet af 
elementet skal have (f.eks `bg-color: blue` eller `background-color: #FF00FF`)

* `font-size` - Tekststørrelse (f.eks `font-size: 25px`)

* `width` og `height` - Hvor bred og høj en element skal være (f
.eks `width: 50px` betyder at elementet skal være 50 pixels bred)

* `min-width`, `max-width`, `min-height`, `max-width` - Minimum eller 
maksimum størrelse af en element (f.eks. `max-width: 100px`)

* `padding`, `padding-top`, `padding-bottom`, `padding-left`, `padding-right` -
 Hvor meget ekstra plads elementet skal få indenfor elementet selv (f.eks. 
 `padding-left: 20px`)

* `margin`, `margin-top`, `margin-bottom`, `margin-left`, `margin-right` -
 Hvor meget ekstra plads elementet skal få *udenfor* elementet selv. Du skal 
 nok leje med `padding` og `margin` for at forstå forskel.

I stedet for at bruge pixels (`px`), kan man bruge andre måler. Dem kan du 
læse om [på W3Schools](https://www.w3schools.com/cssref/css_units.asp).

* `position` - Hvordan element skal placeres. Kan være `static` (default, 
elementet kommer bare efter den tidligere element), `relative` (placeres 
anderledes, i forhold til sin `static` placering), `absolute` (placeres i 
forhold til elementet der indholder den), eller `fixed` (elementet er 
placeret på et præcis sted på siden, og er ikke påvirket af scrolling). Du 
kommer til at brug `static` og `absolute` mest. Bruges som f.eks. `position: 
absolute;`.
 
* `left`, `right`, `top`, `bottom` -  Hvor elementen skal ligge, i forhold til
`top`/`bottom` af websiden. F.eks. `top: 50px; left: 25px;`.

* `text-align` - Hvordan teksten skal justeres (`left`, `right`, `center`).
F.eks. `text-align: center;`

* `vertical-align` - Hvordan en element skal være i forhold til sin parent 
element (elementet der indholder den). Det er så svært at brug `vertical-align`,
at det er blivet til en joke (f.eks. denne webside:
[css-vertical-center.com](http://css-vertical-center.com)). Det kan være 
`top`, `middle`, eller `bottom`, f.eks `vertical-align: middle;`.

* `z-index` - Hvordan elementer sidder over hinanden. Forstil dig at 
websiden er en stak af elementer, med nogle som bliver dække af andre. 
Elementer med et lav `z-index` er på bunden af stakken, og elementer med en høj
`z-index` er på toppen. `z-index` er normalt automatisk, men man kan selv 
bestemme det med f.eks. `z-index: 100`.

* `display` - Hvordan elementet skal vises. `block` er default, men det kan 
være `inline` (vises ved siden af ændre elementer, i stedet for under), 
`none` (gemt), eller mange andre. Bruges som f.eks. `display: none;`

[W3Schools](https://www.w3schools.com/cssref/) har en liste over flere 
elementer, hvis du har brug for flere.

### Farver i CSS

CSS sproget kender nogle navner til farver, som kan bruges: `red, blue, 
green, white, black` (det kender faktisk flere end hundred, men mange af dem 
hedder noget weird ligesom `MediumOrchid`). Men i CSS (og de fleste andre 
programmeringsprog), man kan beskrive *alle* farver med numre.

Nummersystem til farver hedder RGB (**r**ød, **g**røn, **b**lå), og det 
kommer an på at alle farver kan beskrives som en blænding af rød, grøn, og 
blå, i forskellige mængter. Hvert nummer er mellem 0 og 255. For eksemple, rent 
gule kan beskrives som en masser rød, en masse grøn, og ingen blå: 255, 255, 0.
Man har 256^3 (16,777,216) mulige farver, så man behøver ikke navnegive dem 
alle. I CSS, denne RGB format er skrevet som en "hex triplet", eller "hex 
code". "Hex" betyder at i stedet for a brug base 10 til sine nummer, man 
bruger base 16 (du behøver ikke fortså det, bare brug det). For eksemple, i 
hex, 255 bliver til "FF". Så i stedet for at skrive "gule" som (255, 255, 0),
 man kan skrive det som #FFFF00.
 
Rent praktisk set, behøver du ikke at kunne huske hvordan man lave farver i 
hex RGB; der findes rigtig mange farver-vælgende værktøj til web design, som 
giver dig farvens navn i #FFFF00 format. Du kan bare Google "hex 
color picker", eller besøg
[en webside med sådan en værktøj](https://www.quackit.com/css/css_color_codes.cfm).

Du kommer nok til at finde ud af, at det er svært at vælge gode farver! 
Derfor anbefaler jeg, at du bruger nogle værktøl til designere, til at vælge 
en god blænding af farver. Jeg kan bedste lige Material Design stil til mine 
projekter, så derfor bruger jeg
[Material-UI Color Guide](https://material-ui.com/style/color/)
eller
[Material Design Color Palette](https://www.materialpalette.com/)
til at finde gode, moderne farver.

### Pseudo-Classes

Husk, hvordan man udvælger elementer:

```html
#mainText
```

Man kan også definere en stil til elementer, som brugeren har aktiveret, 
eller klikker på, osv., med pseudo-classes. For eksemple, det er mulig at 
skifte baggrund på en element, når brugeren bevæger musen over den:

```html
#mainText
{
    bg-color: red:
}
#mainText:hover
{
    bg-color: blue;
}
```

`:hover` er en pseudo-class, som kun er aktiveret når elementets tilstand 
er `hover`. Andre pseudo-classes er `fullscreen` (når websiden er fullscreen)
, `focus` (med f.eks. en `<input>`, når brugeren skriver i den), eller 
`active` (når brugeren klikker på noget).
[Mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes) 
har et liste over flere pseudo-elementer.

### Animationer

Med CSS3 (som fungere på de fleste browsers), kan man animere elementer. 
Denne sektion er TODO, jeg skal skrive lidt mere senere, men animationer er 
også kompliceret; slå op en tutorial, hvis du rigtig vil gå op i det.

### OBS: CSS er Svært!

CSS er faktisk rimlig kompliceret, selvom det ikke virker svært når man 
begynder at brug den. Problemen er tit, at man forstå hvad man vil gøre, men 
ikke kan finde ud af hvordan det kan lad sig gøre. Bare rolig, du er 
overhovedet ikke den eneste i verden med denne problem. Øve dig, og lære 
nogle gode tricks, og det bliver letter med tiden.

## Oversigt

CSS kan føjes til en webside som en del af `<head>` elementet, som et andet 
fil, eller som en attribute af elementer. En CSS fil ser sådan ud:

```css
.textBlock
{
    bg-color: blue;
    color: red;
}
#mainText
{
    color: black;
    text-align: center;
}
```

En CSS block definere hvad for nogle elementer skal udvælges, og så definere 
nogle stilegenskaber til dem.

## Opgaver

* Lave en af HTML opgaver, og gøre det så pænt som muligt

## Cheat Sheet

Kig på Elementære Elementer eller CSS Struktur, hvis du har brug for en 
oversigt over hvad du har lært.

### Selectors

* `#mainText` - Udvælge elementer med `id` attributen `mainText` (f.eks. `<p 
id="mainText">`)

* `.mainText` - Udvælge elementer med `class` attributen `mainText` (f.eks. `<p 
class="mainText">`)

* `mainText` - Udvælge elementer med `mainText` tag (f.eks. 
`<mainText>Hej</mainText>`)