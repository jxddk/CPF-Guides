# Javascript

(inden du begynder på Javascript, skal du nok lære at bruge HTML. Du skal 
også have en *god* forstårelse for bloksprogrammering, f.eks på microbit 
eller Scratch)

## Værktøje

Ligesom HTML eller CSS, du behøver ikke at bruge noget speciale software til 
at skrive Javascript. Man kan godt bare brug Notepad/Noteblok, eller en anden
tekst editor.

Du skal også kunne brug din browsers Dev Tools.

* Chrome: Ctrl+Shift+J
* Firefox: Ctrl+Shift+K

Det hjælper dig at debug din kode, og at skrive Javascript i consolen.

## Kom i Gang

### Sådan Tilføjer man Javascript til en Webside

Ligesom CSS, man kan skrive Javascript direkte ind i en webside, eller linke 
til en anden fil. Hvis man gemmer sin Javascript kode i en anden fil, det kan
linkes til websiden sådan:
```html
<html><head><script src="script.js"></script></head></html>
```
Ellers, kan du bare skrive Javascript i `script` elementet selv:

```html
<html><head><script>
function helloWorld() {
    console.log('Hello World');
}
</script></head></html>
```
Jeg anbefaler at du skriver din Javascript direkte ind i websiden, så det 
bliver letter at holde styre på både din HTML og Javascript.

### Hurtig Introduktion til Javascript

Javascript har meget (næsten alting) til fælles med bloksprogrammering på 
Microbit. Du kan bruge variabler, funktioner, if sætninger, for og while loops,
osv. i din kode. Hvis ikke du har lært disse koncepter, bliver det svært for
 dig at gøre så meget med Javascript.
 
Hvis du ønkser at lære disse koncepter, anbefaler jeg tutorialerne fra
[TutorialsPoint](https://www.tutorialspoint.com/javascript)
eller fra
[Javascript.info](https://javascript.info/first-steps).

Men, du kan godt brug lidt Javascript på din webside uden lære det hele.

Her, demonstrere jeg de meste grundlæggende Javascript sætninger. Være 
opmærksom på at linjer der starter med `//` er en kommentar, og ikke kode.

```javascript
// definere en variable der hedder x, og har en værdi 10
var x = 10;
// definere en variable der hedder z, og er tekst
var z = "Hello ";
// 'var' betyder at vi definere en variable. Linjen skal slutte med ;

// en if-sætning. Det starter med en betingelse (conditional): hvis x er lige med 10
// bemærk, == betyder 'er lige med', = betyder 'får værdien'
if (x == 10) 
{
    // alt hvad der er imellem {} kun køre hvis betingelsen er sandt
    // her, vi ser at variablen z (som vi har definere i forvejen) får en ny værdi
    z = "Goodbye ";
}

// nu, definere vi en funktion der hedder saySomething. den modtager en parameter (lokal variable) der hedder text.
function saySomething(text)
{
    // en for-loop gøre en ting flere gang. det kraver flere sætninger
    for (                   // start for loop
        var i=0;            // vi laver en nu variable der hedder i
        i < text.length;    // loopen forsætter kun hvis i er mindre en længden af text variablen
        i++)                // i++ betyder at vær gang loopen genstarter, i bliver plus i plus en
    {
        // console.log udskriver tekst til Javascript console
        // tekst[i] får bogstaven på en indeks (f.eks., 'Hi'[0] er 'H', og 'Hi'[1] er 'i' )
        console.log( text[i] );
    }
}

// call (aktivere) funktionen; variablen 'tekst' får værdien af variablen 'z'
saySomething(z);
```

Du kan bare copy-paste den kode ind i din Javascript console, og se hvad det 
udskriver.

### Hello World

Vi starter med en simpelt Javascript funktion som siger "Hello World" til 
brugeren. Man laver en funktion i Javascript sådan:

```javascript
function helloWorld() {
    // code goes here
}
```

Så har vi defineret en funktion der hedder `helloWorld`. Det skal vi kunne 
call (eller, aktivere) fra vores webside. Lad os nu tilføje en button element
 til websiden. Denne button skal have en `onclick` attribute, der giver 
 navnet af vores Javascript funktion (og, `()`, for at call funktionen):

````html
<button id="helloButton" onclick="helloWorld()">Click Me</button>
````

Nu, det eneste der mangler er at udfulde vores funktion. Vi bruger Javascripts
`alert` funktion, for give besked til brugeren:

```javascript
function helloWorld() {
    // code goes here
    alert('Hello World');
}
```
 
Til sidst, ser websiden sådan ud:

```html
<html>
    <head>
        <script>
            function helloWorld() {
                // code goes here
                alert('Hello World');
            }
        </script>
    </head>
    <body>
        <button id="helloButton" onclick="helloWorld()">Click Me</button>
    </body>
</html>
```

Så kan man nu klikke på din button, og få en besked.

### Ændre HTML Elementer

En af de ting man bruger Javascript til meste, er at ændre en websides 
indhold. Man kan ændre alle elementer, eller tilføje nye, bare med Javascript
. Først, skal man kunne hensive til en element. I den tidligere eksemple, 
lavet vi en button med `id` "helloButton". Det gøre man med denne funktion:

```javascript
document.getElementById('helloButton')
```

Denne funktion giver en reference (henvisning (?)) til elementet. Nu, kan vi 
brug det til at ændre elementet selv. Lad os nu ændre elementets indhold:

```javascript
document.getElementById('helloButton').innerHTML = "I am a button";
```

Man kan også ændre CSS på elementet:

```javascript
document.getElementById('helloButton').style.color = "red";
document.getElementById('helloButton').style.bgColor = "blue";
document.getElementById('helloButton').style.fontSize = "128px";
```

### Input fra Websiden

Man kan brug HTML `input` elementer til at tag nogle data fra brugeren, og 
gøre noget med det i Javascript. I denne eksemple, laver vi en webside som 
tilføjer to numre. Vi laver to `input` elementer, en button, og et sted at vise
 en resultat:

```html
<input type="number" id="firstNumber" value="5"></input>
<input type="number" id="secondNumber" value="3"></input>
<hr>
<button onclick="doMath()">Add Numbers</button>
<p>Your result is: <span id="resultView">- - -</span></p>

```

Så, kan vi få deres indhold sådan:

```javascript
document.getElementById('firstNumber').value;
```

Og brug det i vores `doMath` funktion:

```javascript
function doMath() {
    num1 = document.getElementById('firstNumber').value;
    num2 = document.getElementById('secondNumber').value;
    
    // num1 and num2 are strings, and need to be ints
    num1 = parseInt(num1);
    num2 = parseInt(num2);
    
    document.getElementById('resultView').innerHTML = num1 + num2;
}
```

## Opgaver

For at øve dig, prøve en af de her opgaver:

* En webside der beder dig om dit navn, og så siger et personligt hej til dig

* En regnemaskine, der kan tilføje, minus, gange, og dividere to numre,

* En tic-tac-toe spil, til to spiller (ekstra udfording: lave en program der 
kan spil imod sig selv)

Hvis du skal have inspiration til er større projekt, prøve en af de her ideèr:

* En idle-spil (ligesom Cookie Clicker, A Dark Room, eller Universal Paperclips)

* En text-adventure spil