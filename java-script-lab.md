# LAB

## Javascript

### Inspectverktyget i Webbläsaren

1. Browser developers tools
2. Identifiera navigation - element/console/ etc...
3. Identifiera "element selector" och "toggle device"
4. I Console...
5. Skriv ```document``` och undersök
6. Skriv ```domument.head``` och undersök
7. Skriv ```document.title``` och undersök
8. Skriv ```document.URL``` och undersök
9. Skriv ```a = "johan```
9. Skriv ```a```
9. Skriv ```typeof(a)```
9. Skriv ```a = 123```
9. Skriv ```typeof(a)```
9. Skriv ```a = true```
9. Skriv ```typeof(a)```
5. Skapa ett nytt HTML-dokument och lägg till en div#myDiv i body
6. Skriv ```var a = document.getElementById('myDiv')```
7. Skriv ```a``` och undersök resultatet
5. Besvara, vad är a för typ av variabel nu?
8. Skriv ```a.innerHTML('Johan')```
5. Vad hände på webbsidan?
7. Skriv ```a``` och undersök resultatet
5. Skriv ```a.hidden = true```
5. Vad hände på webbsidan?
5. Skriv ```a.hidden = false```
5. Skriv ```a.insertAdjacentHTML('afterend', '<span>Sundström</span>')```
5. Vad hände på webbsidan?

insertAdjacentHTML har 4 parametrar...
* ```beforebegin``` före vald element (som är a i detta fall)
* ```afterbegin``` innanför valt element, innan eventuella child's
* ```beforeend``` innanför valt element, efter eventuella child's
* ```afterend``` efter vald element

5. Skriv ```a.style.color = 'red'```
5. Vad hände på webbsidan?

Med Javascript når vi allt, inklusive CSS, i ett HTML-dokument genom DOM. 

### Javascript med kod

Skriv följande kod
```javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id="myDiv"></div>
    
    <script>
        var a = document.getElementById('myDiv');
        a.innerHTML = 'Johan';
    </script>    
</body>
</html>
```

* Visa i webbläsare, studera resultatet. Intressant?
-Inte intressant, då koden inte exekverar

### Javascript events

| Event | Beskrivning |
|---|---|
|onchange |	HTML-element har ändrats |
|onclick |	Användaren klickar på ett HTML-element |
|onmouseover |	Användaren flyttar in muspekaren på ett  HTML element |
|onmouseout |	Användaren flyttar ut muspekaren från ett  HTML element |
|onkeydown |	Användaren klickar på en tangent |
|onload |	Webbläsaren har laddat hela HTML-dokumentet |

* Eventet ```onload``` kan starta scriptet
* ```onload``` etableras på body-elementet
* ```onload``` anropar en funktion med namnet ```minFunktion```
* Dess argument (indata) är tomt, men parenteser måste finnas

```javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        function minFunktion(){
            var obj = document.getElementById('myDiv');
            obj.innerHTML = 'Johan';
            obj.style.color = 'red';
        }
    </script>
</head>
<body onload="minFunktion()">
    <div id="myDiv"></div>
</body>
</html>
```

* Funktionen ```minFunktion``` har funktionsuttryck inom { ... }
* Funktionen ```minFunktion``` skapar objektet ```obj``` och tilldelas HTML-elementet ```id='myDiv'```
* Observera radslutstecknet ```;```

### Enkel klocka

```javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        function minFunktion(){
            var myVar = setInterval(function() {
                myTimer();
            }, 1000);

            function myTimer() {
                var myTime = new Date();
                myDiv = document.getElementById("myDiv");
                myDiv.innerHTML = myTime.toLocaleTimeString();
            }
        }
    </script>
</head>
<body onload="minFunktion()">
    <div id="myDiv"></div>
</body>
</html>
```

* ```setInterval``` (ett tidsevent) har som indata en funktion utan namn (anonym funktion) och ett millisekundvärde
* Den anonyma funktionen anropas varje 1000mS (varje sekund)
* ```setInterval``` anropas ända tills ```clearInterval()``` anropas eller fönstret stängs
* Det anonyma funktionsuttrycket anropar funktionen ```myTimer```
* ```myTimer``` skriver ut ett landsspecifikt uttryck av lokal tid
