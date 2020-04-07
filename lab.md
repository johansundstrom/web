# LAB

## Javascript

### Inspectverktyget i Webbläsaren

1. Browser developers tools
2. identifiera navigation - element/console/ etc...
3. Identifiera "element selector" och "toggle device"
4. i Console...
5. skriv ```document``` och undersök
6. skriv ```domument.head``` och undersök
7. skriv ```document.title``` och undersök
8. skriv ```document.URL``` och undersök
9. skriv ```a = "johan```
9. skriv ```a```
9. skriv ```typeof(a)```
9. skriv ```a = 123```
9. skriv ```typeof(a)```
9. skriv ```a = true```
9. skriv ```typeof(a)```
5. skapa ett nytt HTML-dokument och lägg till en div#myDiv i body
6. skriv ```var a = document.getElementById('myDiv')```
7. skriv ```a``` och undersök resultatet
5. Besvara, vad är a för typ av variabel nu?
8. skriv ```a.innerHTML('Johan')```
5. Vad hände på webbsidan?
7. skriv ```a``` och undersök resultatet
5. skriv ```a.hidden = true```
5. Vad hände på webbsidan?
5. skriv ```a.hidden = false```
5. skriv ```a.insertAdjacentHTML('afterend', '<span>Sundström</span>')
5. Vad hände på webbsidan?

insertAdjacentHTML har 4 parametrar...
* ```beforebegin``` före vald element (som är a i detta fall)
* ```afterbegin``` innanför valt element, innan eventuella child's
* ```beforeend``` innanför valt element, efter eventuella child's
* ```afterend``` efter vald element

5. Skriv ```a.style.color = 'red'````
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
    <script>
        var a = document.getElementById('myDiv');
        a.innerHTML = 'Johan';
    </script>
</head>
<body>
    <div id="myDiv"></div>
</body>
</html>
```

* Visa i webbläsare, studera resultatet. Intressant?
-Inte intressant, då koden inte exekverar

### Javascript events

| Event | Description |
|---|---|
|onchange |	An HTML element has been changed |
|onclick |	The user clicks an HTML element |
|onmouseover |	The user moves the mouse over an HTML element |
|onmouseout |	The user moves the mouse away from an HTML element |
|onkeydown |	The user pushes a keyboard key |
|onload |	The browser has finished loading the page |

* Eventet ``onload``` kan starta scriptet
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

* ```setInterval``` har som indata en funktion utan namn (anonym funktion) och ett millisekundvärde
* Den anonyma funktionen anropas varje 1000mS (varje sekund)
* ```setInterval``` anropas ända tills ```clearInterval()``` anropas eller fönstret stängs
* Det anonyma funktionsuttrycket anropar funktionen myTimer
* myTimer skriver ut ett landsspecifikt uttryck av lokal tid
