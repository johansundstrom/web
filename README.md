# Webbutveckling

![GitHub last commit](https://img.shields.io/github/last-commit/johansundstrom/web?style=plastic)
<img src="https://img.shields.io/badge/Status-In Progress-orange?style=plastic">
<img src="https://img.shields.io/github/issues/johansundstrom/web?style=plastic">

* Metod
* Designprinciper
* HTML och CSS
* Javascript
* Typografi för webb
* Bild för webb
* Layout för webb
* Webbeditorer
* Navigation

## Metod för webbprojekt

HISU

* Research
* Strategi
* Design & dokumentation
* Presentation

## Designprinciper

* Kognition/perception
* Gestaltlagar
* Visuell struktur (hierarki)
* Typografi
* Bilder
* SNL

## Visual Studio Code - 1

* Installera
* Color Theme
* Extensions - Live Server (Microsoft), Lorem ipsum (Daniel Imms)

## HTML/CSS

* Standard, W3C, WD-CR-PR-REC, Version 5.2
* Syfte med HTML
* Några elemement
* Struktur, element, attribut
* Semantisk struktur - header/nav/section/article/aside/footer


## Visual Studio Code - 2

* Command Palette - F1 (CTRL + Shift + P)
* Emmet - <https://docs.emmet.io/cheat-sheet>

## CSS

* Standard, W3C, CSS delas upp i Modules-publiceras som Levels och publiceras som Snapshots
* Syfte med CSS
* Browser default, browser reset
* inline, embed, linked
* Selector - property: value
* Div/span, ID/Class

## Navigation

* Länkprinciper

## Javascript

* Javascript engine
* Högnivå, interpreterande skriptspråk
* ECMA Script (European Computer Manufacturers Association)
* Developer tools - JS console
* HTML ```<script>```-tag
* ```window.alert("Hej");```
* DOM
* ```document.getElementById("test").innerHTML = "Hej";```
* Events - onclick(), onmouseover(), onload(), onchange()...
* Variabler, scope
* Functions

```javascript
function FtoC(celcius){
    var fahrenheit = celcius * 9/5 +32;
    return fahrenheit;
}
var myTemp = FtoC(100);
console.log(myTemp);
```

## CSS Framework - 1

* Bootstrap
* Versioner - 4.3 (aug 2019)
* Principen

## Syntactically Awesome Style Sheets - SASS

1. Skapa Projmapp
2. Install Node/NPM
3. Kontrollera - ```node -v``` och ```npm -v```
4. ```npm init (--yes)```
5. Öppna package.json
6. ```npm install -g node-sass```
7. package.json - "sass": "node-sass --watch scss/ output css/"
8. ```npm run sass```
9. Redigera style.scss

Exempel på SASS-variabler

```css
$base-color: #123456;
$color-dark: rgba($base-color, 0.88);
$myWidth: 800px;
$myNav: $myWidth * 0.25;
```

## SVG

* Scalar Vector Graphics
* Illustrator
  
```html
<svg width="500" height="500">
    <g transform="translate(50, 0)">
    <rect x="0" y="0" width="50" height="50" fill="orange"></rect>
    <rect x="60" y="20" rx="10" ry="10" width="150" height="150" fill="steelblue"></rect> <!-- rundade hörn -->
    <circle cx="50" cy="250" r="50" fill="red"></circle>
    <ellipse cx="200" cy="80" rx="100" ry="50"></ellipse>
    <line x1="400" y1="40" x2="100" y2="200" style="stroke:#ccc;stroke-width:2"></line>
    <polygon points="200, 10 250, 190 160, 210" fill="green"></polygon>
    <g transform="translate(300, 10)">
        <polyline points="0,40 40,40 40,80 80,80 80,120 120,120 120,160" fill="none" stroke="blue"></polyline>
    </g>
    <path d="M0 200 L50 50 L100 150 L150 100 L200 150 Z" fill="none" stroke="red" stroke-width="5" stroke-dasharray="20,10,5,5,5,10"></path>
    <path d="M 50 150 q 150 -300 300 50" stroke="lightblue" stroke-width="5" fill="none"></path>
    <text x="250" y="200" fill="red" transform="rotate(30 20,40)">Min text</text>
    </g>
</svg>
```

* Om man sparar som fil...
```
<svg version="1.1"
     baseProfile="full"
     xmlns="http://www.w3.org/2000/svg"
     ...
```

* svgfil som bild
```<img src="image.svg" alt="image">```

## Glyphicons

* Font Awesome
* Bygger på SVG
* <https://fontawesome.com/start>
  
```html
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.8.1/css/all.css"
      integrity="sha384-50oBUHEmvpQ+1lW4y57PTFmhCaXp0ML5d60M1M7uH2+nqUivzIebhndOJK28anvf" crossorigin="anonymous">
<style>
    .fab { color:#3c5a99; font-size: 50px;}
</style>
...
<i class="fab fa-facebook-square"></i>
```

## Bootstrap Icons (v5.2)

* CDN'a in bootstrap icons i HEAD
* ```<i class="bi bi-facebook"></i>```

## CSS Framework - 2

* Fasta bildstorlekar i dynamiska miljöer
* Bildhantering i Bootstrap
  
```html
<div class="container">
    <img src="images/bredbild.jpg" class="img-fluid" alt="Colorful">
</div>
```

* Addera ram

```html
<div class="container">
    <img src="images/bredbild.jpg" class="img-fluid rounded" alt="Colorful">
</div>
```

* Runda hörn

```html
<div class="container">
    <img src="images/bredbild.jpg" class="img-fluid rounded" alt="Colorful">
</div>
```

```css
.myrounded {
    border-radius: 20px;
}
```

* Skugga

```html
<figure class="figure">
    <img src="images/bredbild.jpg" class="img-fluid shadow-lg p-0 rounded" alt="Colorful">
    <figcaption class="figure-caption text-right">En bild Caption</figcaption>
</figure>
```

* Text overlay

```html
<div class="row">
    <div class="col">
        <img src="images/bredbild.jpg" class="img-fluid shadow-lg p-0 rounded" alt="Colorful">
        <p class="myoverlay">Text över bild</p>
    </div>
</div>
```

```css
.myoverlay {
    z-index: 1;
    font-size: 3em;
    color: blue;
    line-height: 1.1em;
    position: absolute;
    top: 10%;
    left: 10%
}
```

## Layout med Bootstrap

* Först för hand
* Därefter med VS Code Extention - Bootstrap 4 (Ashok Koyi)
* b4-
* b4-navbar-default
* ...


## Layout med CSS Grid

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="grid.css">
</head>
<body>
    <div class="grid-container">
        <div class="grid-item grid-item-1">1</div>
        <div class="grid-item grid-item-2">2</div>
        <div class="grid-item grid-item-3">3</div>
        <div class="grid-item grid-item-4">4</div>
        <div class="grid-item grid-item-5">5</div>
        <div class="grid-item grid-item-6">6</div>
        <div class="grid-item grid-item-7">7</div>
        <div class="grid-item grid-item-8">8</div>
        <div class="grid-item grid-item-9">9</div>
      </div>
</body>
</html>
```

```css
/*
    display: grid;
    display: inline-grid;
    grid-gap: 10px;

*/
.grid-container,  .grid-item {
    padding: 3px;
}

.grid-container {
    display: grid;
    background-color: red;

    grid-gap: 3px;
  }

.grid-item { 
    
    background-color: rgba(255, 255, 255);
}

.grid-item-1 {
    grid-column-start: 1;
    grid-column-end: 2;
    /* grid-column: 1 / 5  -  shorthand for grid-column-start/end */
    grid-row-start: 1;
    grid-row-end: 5;
}

.grid-item-2 {
    grid-column-start: 2;
    grid-column-end: 3;
}

.grid-item-3 {
    grid-column-start: 3;
    grid-column-end: 4;
}
```
