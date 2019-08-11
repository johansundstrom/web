# Webbutveckling

* Metod
* Designprinciper
* HTML och CSS
* Javascript
* Typografi för webb
* Bild för webb
* Layout för webb
* Webbeditorer
* Navigation

## Metod

* HISU

## Designprinciper

* Kognition/perception
* Gestaltlagar
* Visuell struktur
* Typografi
* Bilder
* SNL

## Visual Studio Code - 1

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
* Selector - property: value
* Div/span, ID/Class

## Navigation

* Länkprinciper

## Javascript

* Javascript engine
* Developer tools - JS console
* ```<script>``` tag
* window.alert("Hej");
* DOM
* document.getElementById("test").innerHTML = "Hej";
* Events - onclick(), onmouseover(), onload(), onchange()...
* Functions
* Variabler, scope

## CSS Framework - 1

* Bootstrap
* Versioner - 4.3
* Principen

## Syntactically Awesome Style Sheets - Sass

* Skapa Projmapp
* Install Node/NPM
* Kontrollera - node -v, npm -v
* npm init
* Öppna package.json
* npm install -g node-sass
* package.json - "sass": "node-sass --watch scss/ output css/"
* npm run sass
* Redigera style.scss
  
```sass
$bg: "123456";
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

* se.svg

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

## CSS Framework - 2

* Bilder
* Responsiv bildstorlek
  
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
* Därefter med Extention - Bootstrap 4 (Ashok Koyi)
