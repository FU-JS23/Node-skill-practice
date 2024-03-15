# Grundläggande övningar Node.js

## Async code

### Polka lover
Gör en funktion vid namn ```letsDance(danceStyle)```som bygger på ett ```Promise```. 
Funktionen ska ta ett argument ```danceStyle```. Om dansen som erbjuds är *polka* ska dansen godkännas med frasen *Yes, polka is my thing!*. Om Dansstilen som erbjuds är något annat så ska dansförfrågan rejectas med en *syrlig diss*. Funktionen ska ta *2s* på sig att svara.

```
letsDance('waltz')
.then(resp => console.log(response)) // ...
.catch(diss => console.log(diss)) // Not even if a pandemic roamed the earth
```

Använd ```setTimeout``` för att fördröja funktionerna.
Testa med fördel både ```.then()``` och ```async/await```.


### Webbprojektet
**Du ska göra ett webbprojekt.**
Gör en promise kedja för detta projekts moment i följande ordning med följande tider:

1. Researcha målgruppen - 4s
2. Skissa upp en design på papper  - 2s
3. Gör skissen till pixel perfect mockup I Figma / XD 	- 3s
4. Koda - 3s
5. Stackoverflow:a fel  - 1s
6. Testa produkten - 2s 
7. Fira lyckat projekt - 1s

Använd ```setTimeout``` för att fördröja funktionerna.
Testa med fördel både ```.then()``` och ```async/await```.


### Modulize it!
Dela upp momenten i *uppgift 2* i varsin modul som du importerar ( require ) i ```index.js```.


### Chuck Norris module
Gör en modul som  med hjälp av ```NPM modulen node-fetch``` hämtar ett random Chuck Norris påstående från url:
```https://api.chucknorris.io```
Hantera eventuella fel som kan uppstå med en egen *errorHandling-module* som skriver felet i en logg-fil med namn 
```errors.txt.```


## Core Modules

### Datorrapporten ( OS, FS )

Samla in systeminformation om din dator ( os-modulen )
- vilken modell ( PC, Mac, Linux )
- villet OS ( Windows, OSX, Linux)
- hur mycket RAM
- Vilken CPU och hur många kärnor
- Fler spec som du finner intressant

Samla all information i textfilen **sytemrapport.txt**.


### Intervjun (RL, FS)
Liten kort intervju med 3-5 frågor med Readline. 
Spara svaren i en textfil med namn **intervjupersonensförnamn.txt**


### Chuck Norris Chunker (RL, FS)
Läs in filen ```chucknorris.txt```.
Dela upp den så att varje påstående får en egen txt-fil.


### Chuck Norris Rater (RL, FS)
Gör ett readline-program som går igenom varje påstående i **chucknorris.txt** och ställer frågan:

```
Hur roligt är detta påstående på en skala 1-10?
```

Spara samtliga svar i samma txt-fil i följande struktur:

```
1. Joke: <joke>
Funny: 1
—
2. Joke: ...
```


### API Spara skämt (HTTP, FS)
Du ska bygga ett API där man kan spara och hämta skämt.

Ditt API ska ha följande funktionalitet:

|endpoint|metod|desc
|---|---|---|
|**/jokes**|GET| Returnerar en array med samtliga skämt.
|**/jokes**|POST| Skicka in jokes i följande format ```{ joke : <String> }```.
|**/random**|GET| Returnerar ett slumpat skämt från dina sparade.

Det räcker med att du sparar dina skämt i en array i Node, men vill du göra det mer avancerat; spara dem i en txt-fil.


### Rövarspråket Webbapp (HTTP, HTML, CSS, FETCH)
Du ska göra en webbapp som kan konvertera vanlig text till [rövarspråket](https://sv.wikipedia.org/wiki/Rövarspråket).
Din app består av två delar; En *frontend* och en *backend* ( API ).

#### Frontend
Din frontend ska bestå av en snyggt formaterad ```index.html``` som kan göra ```GET``` och ```POST``` requests med hjälp av fetch API:et. Ditt gränssnitt ska ha minst ha en *textarea* och en *button*. Det är viktigt att din .html-fil innehåller alla resurser, både HTML, CSS och JS.


Förslag på GUI hittar du [här](https://www.figma.com/file/vjly6mDgb7EjrvKE3dZQ5o/R%C3%B6varspr%C3%A5ket-UI?node-id=1%3A2).

#### Backend
Gör ett API med följande *endpoints* och *metoder*.

|endpoint|metod|desc
|---|---|---|
|**/**|GET| Servar ```public/index.html```
|**/text** | POST | Tar emot en sträng och konverterar den till *rövarspråket* och returnerar.

Försök att jobba med *moduler* och *asynkrona funktioner* på node-sidan.
