# Unix Terminal Cheat Sheet

Hvis du bruger Unix terminalen, du har nok lært at der er rigtig meget man 
skal huske. Disse kommandoer bliver meste brugbart, når du bruger terminalen:

## Navigation og Filer

* `cd ___` - Skift til mappe `___`. Hvis du ikke specificere en mappe, 
skifter du til din user hjemme.

* `ls` - Udskriv alle filer i mappen

* `mkdir ___` - Lav mappe der hedder `___`

* `rm ___` - Fjern fil der hedder `___`

* `rm -r ___` - Fjern mappe der hedder `___`

## Filredigering

* `cat > ___` - Lav en fil der hedder `___`, og begynd at skrive i den. 
Ctrl+C for at lukke filen.

* `nano ___` - Sammen som `cat`, men lidt mere advanceret. Ctrl+Z for at 
lukke filen.

## System

* `ifconfig` - Se netværk detaljer

* `killall ___` - Stop alle processer der hedder `___`

* `sudo ___` - Lav kommando `___` som administrator (du bliver bedt om din 
kodeord)