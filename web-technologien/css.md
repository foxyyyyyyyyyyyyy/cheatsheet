# CSS

---

## **Einführung**

CSS (Cascading Style Sheets) ist eine Stylesheet-Sprache, die verwendet wird, um das Layout, die Farben, Schriftarten und andere Designaspekte von HTML-Dokumenten zu gestalten. Es trennt das visuelle Design vom Inhalt und ermöglicht so eine flexible und wieder verwendbare Gestaltung von Webseiten.

### Was ist CSS?

[https://youtu.be/OEV8gMkCHXQ?si=hUkGBkmr3V8dDJHc](https://youtu.be/OEV8gMkCHXQ?si=hUkGBkmr3V8dDJHc)

---

## **Grundsyntax**

### **Selektoren**

Selektoren werden verwendet, um HTML-Elemente auszuwählen, die gestylt werden sollen.

- **Elementselektor**
    
    ```css
    p {
      /* Stilregeln für alle <p>-Elemente */
    }
    
    ```
    
- **Klassenselektor**
    
    ```css
    .classname {
      /* Stilregeln für Elemente mit class="classname" */
    }
    
    ```
    
- **ID-Selektor**
    
    ```css
    #idname {
      /* Stilregeln für das Element mit id="idname" */
    }
    
    ```
    
- **Gruppenselektor**
    
    ```css
    h1, h2, h3 {
      /* Stilregeln für h1, h2 und h3 Elemente */
    }
    
    ```
    
- **Universalselektor**
    
    ```css
    * {
      /* Stilregeln für alle Elemente */
    }
    
    ```
    
- **Attributselektor**
    
    ```css
    input[type="text"] {
      /* Stilregeln für alle <input>-Elemente mit type="text" */
    }
    
    ```
    
- **Nachkomme**
    
    ```css
    ul li {
      /* Stilregeln für alle <li> innerhalb von <ul> */
    }
    
    ```
    
- **Kind**
    
    ```css
    ul > li {
      /* Stilregeln für direkte Kinder <li> von <ul> */
    }
    
    ```
    
- **Geschwister**
    - **Adjazentes Geschwister**
        
        ```css
        h2 + p {
          /* Stilregeln für <p>, das direkt nach einem <h2> kommt */
        }
        
        ```
        
    - **Allgemeines Geschwister**
        
        ```css
        h2 ~ p {
          /* Stilregeln für alle <p>, die nach einem <h2> kommen */
        }
        
        ```
        

### **Kombination von Selektoren**

```css
div.classname#idname > p {
  /* Stilregeln für <p> innerhalb eines <div> mit class="classname" und id="idname" */
}

```

### **Pseudo-Klassen**

- **Interaktion**
    
    ```css
    a:hover {
      /* Stilregeln, wenn die Maus über einem Link schwebt */
    }
    
    input:focus {
      /* Stilregeln, wenn ein Input-Feld den Fokus hat */
    }
    
    ```
    
- **Struktur**
    
    ```css
    li:first-child {
      /* Stilregeln für das erste <li> innerhalb seines Elternteils */
    }
    
    li:last-child {
      /* Stilregeln für das letzte <li> innerhalb seines Elternteils */
    }
    
    tr:nth-child(even) {
      /* Stilregeln für gerade Zeilen einer Tabelle */
    }
    
    tr:nth-child(odd) {
      /* Stilregeln für ungerade Zeilen einer Tabelle */
    }
    
    ```
    

### **Pseudo-Elemente**

- **Erste Zeile oder erster Buchstabe**
    
    ```css
    p::first-line {
      /* Stilregeln für die erste Zeile eines Absatzes */
    }
    
    p::first-letter {
      /* Stilregeln für den ersten Buchstaben eines Absatzes */
    }
    
    ```
    
- **Inhalte einfügen**
    
    ```css
    p::before {
      content: "Hinweis: ";
      /* Fügt vor jedem Absatz "Hinweis: " ein */
    }
    
    p::after {
      content: " - Ende";
      /* Fügt nach jedem Absatz " - Ende" ein */
    }
    
    ```
    

---

## **Box-Modell**

Das Box-Modell beschreibt, wie der Browser die Größe eines Elements berechnet.

- **Inhalt (content)**: Der eigentliche Inhalt, z. B. Text oder Bilder.
- **Innenabstand (padding)**: Abstand zwischen Inhalt und Rahmen.
- **Rahmen (border)**: Umrandung des Elements.
- **Außenabstand (margin)**: Abstand zwischen dem Element und seinen Nachbarn.

### **Eigenschaften des Box-Modells**

- **Breite und Höhe**
    
    ```css
    width: 200px;
    height: 100px;
    
    ```
    
- **Padding**
    
    ```css
    padding: 10px; /* Alle Seiten */
    padding-top: 10px;
    padding-right: 15px;
    padding-bottom: 10px;
    padding-left: 15px;
    
    ```
    
- **Margin**
    
    ```css
    margin: 20px; /* Alle Seiten */
    margin-top: 20px;
    margin-right: 25px;
    margin-bottom: 20px;
    margin-left: 25px;
    
    ```
    
- **Border**
    
    ```css
    border: 1px solid black; /* Stil für alle Seiten */
    border-top: 2px dashed red;
    border-right: 3px dotted green;
    border-bottom: 4px double blue;
    border-left: 5px groove orange;
    
    ```
    
- **Box Sizing**
    
    ```css
    box-sizing: content-box; /* Standard, Größe beinhaltet nicht padding und border */
    box-sizing: border-box; /* Größe beinhaltet padding und border */
    
    ```
    

---

## **Hintergründe und Farben**

### **Farbangaben**

- **Schlüsselwörter**
    
    ```css
    color: red;
    background-color: blue;
    
    ```
    
- **Hexadezimale Werte**
    
    ```css
    color: #ff0000;
    background-color: #0000ff;
    
    ```
    
- **RGB**
    
    ```css
    color: rgb(255, 0, 0);
    background-color: rgb(0, 0, 255);
    
    ```
    
- **RGBA (mit Transparenz)**
    
    ```css
    color: rgba(255, 0, 0, 0.5); /* 50% transparent */
    
    ```
    
- **HSL**
    
    ```css
    color: hsl(120, 100%, 50%); /* Grünton */
    
    ```
    
- **HSLA**
    
    ```css
    color: hsla(120, 100%, 50%, 0.3); /* Grünton mit 30% Deckkraft */
    
    ```
    

### **Hintergrundeigenschaften**

- **Hintergrundfarbe**
    
    ```css
    background-color: #f0f0f0;
    
    ```
    
- **Hintergrundbild**
    
    ```css
    background-image: url('bild.jpg');
    
    ```
    
- **Wiederholung**
    
    ```css
    background-repeat: repeat; /* Standard */
    background-repeat: no-repeat;
    background-repeat: repeat-x;
    background-repeat: repeat-y;
    
    ```
    
- **Position**
    
    ```css
    background-position: center center;
    background-position: top right;
    background-position: 50% 50%;
    
    ```
    
- **Größe**
    
    ```css
    background-size: cover;
    background-size: contain;
    background-size: 100px 200px;
    
    ```
    
- **Anhang**
    
    ```css
    background-attachment: scroll; /* Standard */
    background-attachment: fixed;
    
    ```
    
- **Mehrere Hintergründe**
    
    ```css
    background-image: url('bild1.jpg'), url('bild2.png');
    background-position: left top, right bottom;
    background-repeat: no-repeat, repeat;
    
    ```
    

---

## **Text und Schriftarten**

### **Textfarbe**

```css
color: #333333;

```

### **Textausrichtung**

```css
text-align: left;
text-align: center;
text-align: right;
text-align: justify;

```

### **Textdekoration**

```css
text-decoration: none;
text-decoration: underline;
text-decoration: line-through;
text-decoration: overline;
text-decoration: underline overline;

```

### **Texttransformierung**

```css
text-transform: uppercase; /* Großbuchstaben */
text-transform: lowercase; /* Kleinbuchstaben */
text-transform: capitalize; /* Erstbuchstaben groß */

```

### **Textschatten**

```css
text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);

```

### **Zeilenhöhe**

```css
line-height: 1.5; /* Relativ zur Schriftgröße */
line-height: 20px; /* Absolute Höhe */

```

### **Schriftfamilie**

```css
font-family: 'Arial', sans-serif;

```

### **Schriftgröße**

```css
font-size: 16px;
font-size: 1em;
font-size: 100%;

```

### **Schriftstil**

```css
font-style: normal;
font-style: italic;
font-style: oblique;

```

### **Schriftgewicht**

```css
font-weight: normal;
font-weight: bold;
font-weight: 700;

```

### **Schriftvariante**

```css
font-variant: normal;
font-variant: small-caps;

```

### **Import von Webfonts**

```css
@import url('<https://fonts.googleapis.com/css?family=Roboto&display=swap>');

body {
  font-family: 'Roboto', sans-serif;
}

```

---

## **Listen und Tabellen**

### **Listeneigenschaften**

- **Aufzählungszeichen**
    
    ```css
    list-style-type: disc; /* Standard für ungeordnete Listen */
    list-style-type: circle;
    list-style-type: square;
    list-style-type: decimal; /* Standard für geordnete Listen */
    list-style-type: lower-alpha;
    list-style-type: upper-roman;
    
    ```
    
- **Bild als Aufzählungszeichen**
    
    ```css
    list-style-image: url('symbol.png');
    
    ```
    
- **Position**
    
    ```css
    list-style-position: inside;
    list-style-position: outside; /* Standard */
    
    ```
    
- **Kurzschreibweise**
    
    ```css
    list-style: square inside url('symbol.png');
    
    ```
    

### **Tabelleneigenschaften**

- **Rahmen**
    
    ```css
    table, th, td {
      border: 1px solid black;
    }
    
    ```
    
- **Rahmenkollaps**
    
    ```css
    table {
      border-collapse: collapse;
      /* oder */
      border-collapse: separate;
      border-spacing: 5px;
    }
    
    ```
    
- **Zellabstand und -innenabstand**
    
    ```css
    td {
      padding: 10px;
      /* cellspacing ist in HTML veraltet, verwenden Sie stattdessen border-spacing */
    }
    
    ```
    
- **Textausrichtung**
    
    ```css
    th {
      text-align: left;
    }
    
    td {
      text-align: center;
      vertical-align: top;
    }
    
    ```
    

---

## **Positionierung**

### **Positionsarten**

- **Static (Standard)**
    
    ```css
    position: static;
    
    ```
    
- **Relative**
    
    ```css
    position: relative;
    top: 10px; /* Verschiebt das Element um 10px nach unten relativ zu seiner normalen Position */
    left: 5px;
    
    ```
    
- **Absolute**
    
    ```css
    position: absolute;
    top: 50px; /* Position relativ zum nächsten positionierten Vorfahren */
    left: 100px;
    
    ```
    
- **Fixed**
    
    ```css
    position: fixed;
    bottom: 0;
    right: 0;
    
    ```
    
- **Sticky**
    
    ```css
    position: sticky;
    top: 0;
    
    ```
    

### **Z-Index**

```css
z-index: 1; /* Stapelreihenfolge, höhere Werte liegen oben */

```

### **Overflow**

```css
overflow: visible; /* Standard */
overflow: hidden;
overflow: scroll;
overflow: auto;

```

### **Float und Clear**

- **Float**
    
    ```css
    float: left;
    float: right;
    
    ```
    
- **Clear**
    
    ```css
    clear: left;
    clear: right;
    clear: both;
    
    ```
    

---

## **Flexbox**

Flexbox ist ein Layout-Modul, das das Ausrichten und Verteilen von Elementen in einem Container vereinfacht.

### **Container-Eigenschaften**

- **Display**
    
    ```css
    display: flex;
    /* oder */
    display: inline-flex;
    
    ```
    
- **Flex-Richtung**
    
    ```css
    flex-direction: row; /* Standard */
    flex-direction: row-reverse;
    flex-direction: column;
    flex-direction: column-reverse;
    
    ```
    
- **Flex-Wrap**
    
    ```css
    flex-wrap: nowrap; /* Standard */
    flex-wrap: wrap;
    flex-wrap: wrap-reverse;
    
    ```
    
- **Flex-Flow (Kurzschreibweise für flex-direction und flex-wrap)**
    
    ```css
    flex-flow: row wrap;
    
    ```
    
- **Justify-Content (Ausrichtung entlang der Hauptachse)**
    
    ```css
    justify-content: flex-start; /* Standard */
    justify-content: flex-end;
    justify-content: center;
    justify-content: space-between;
    justify-content: space-around;
    justify-content: space-evenly;
    
    ```
    
- **Align-Items (Ausrichtung entlang der Querachse)**
    
    ```css
    align-items: stretch; /* Standard */
    align-items: flex-start;
    align-items: flex-end;
    align-items: center;
    align-items: baseline;
    
    ```
    
- **Align-Content (Ausrichtung von mehrzeiligen Inhalten)**
    
    ```css
    align-content: stretch; /* Standard */
    align-content: flex-start;
    align-content: flex-end;
    align-content: center;
    align-content: space-between;
    align-content: space-around;
    align-content: space-evenly;
    
    ```
    

### **Elementeigenschaften**

- **Order**
    
    ```css
    order: 0; /* Standardwert */
    
    ```
    
- **Flex Grow**
    
    ```css
    flex-grow: 1; /* Wie viel das Element wachsen kann */
    
    ```
    
- **Flex Shrink**
    
    ```css
    flex-shrink: 1; /* Wie viel das Element schrumpfen kann */
    
    ```
    
- **Flex Basis**
    
    ```css
    flex-basis: auto; /* Startgröße des Elements */
    
    ```
    
- **Flex (Kurzschreibweise für flex-grow, flex-shrink und flex-basis)**
    
    ```css
    flex: 1 1 auto;
    
    ```
    
- **Align Self**
    
    ```css
    align-self: auto; /* Standard */
    align-self: flex-start;
    align-self: flex-end;
    align-self: center;
    align-self: baseline;
    align-self: stretch;
    
    ```
    

---

## **Grid Layout**

Das CSS Grid Layout ermöglicht die Erstellung komplexer zweidimensionaler Layouts.

### **Container-Eigenschaften**

- **Display**
    
    ```css
    display: grid;
    /* oder */
    display: inline-grid;
    
    ```
    
- **Grid-Template-Columns und Grid-Template-Rows**
    
    ```css
    grid-template-columns: 200px 1fr 2fr;
    grid-template-rows: 100px auto;
    
    ```
    
- **Grid-Template-Areas**
    
    ```css
    grid-template-areas:
      "header header"
      "sidebar main"
      "footer footer";
    
    ```
    
- **Grid-Gap (Abstand zwischen den Zellen)**
    
    ```css
    grid-gap: 10px;
    grid-row-gap: 15px;
    grid-column-gap: 20px;
    
    ```
    
- **Justify-Items (Ausrichtung der Zellen auf der Inline-Achse)**
    
    ```css
    justify-items: start; /* Standard */
    justify-items: end;
    justify-items: center;
    justify-items: stretch;
    
    ```
    
- **Align-Items (Ausrichtung der Zellen auf der Block-Achse)**
    
    ```css
    align-items: start;
    align-items: end;
    align-items: center;
    align-items: stretch; /* Standard */
    
    ```
    

### **Elementeigenschaften**

- **Grid-Column und Grid-Row**
    
    ```css
    grid-column: 1 / 3; /* Startet in Spalte 1 und endet vor Spalte 3 */
    grid-row: 2 / 4;
    
    ```
    
- **Grid-Area**
    
    ```css
    grid-area: header;
    
    ```
    
- **Justify-Self und Align-Self**
    
    ```css
    justify-self: center;
    align-self: end;
    
    ```
    

---

## **Übergänge und Animationen**

### **Übergänge**

- **Transition**
    
    ```css
    transition-property: all; /* Oder spezifische Eigenschaften */
    transition-duration: 0.5s;
    transition-timing-function: ease; /* linear, ease-in, ease-out, ease-in-out */
    transition-delay: 0s;
    
    /* Kurzschreibweise */
    transition: property duration timing-function delay;
    transition: all 0.5s ease-in-out 0s;
    
    ```
    
- **Beispiel**
    
    ```css
    .button {
      background-color: blue;
      transition: background-color 0.3s;
    }
    
    .button:hover {
      background-color: red;
    }
    
    ```
    

### **Animationen**

- **@keyframes**
    
    ```css
    @keyframes animationName {
      from {
        /* Anfangszustand */
      }
      to {
        /* Endzustand */
      }
    
      /* Oder in Prozent */
      0% { /* Anfang */ }
      50% { /* Mitte */ }
      100% { /* Ende */ }
    }
    
    ```
    
- **Animation-Eigenschaften**
    
    ```css
    animation-name: animationName;
    animation-duration: 2s;
    animation-timing-function: linear;
    animation-delay: 0s;
    animation-iteration-count: infinite; /* oder eine Zahl */
    animation-direction: normal; /* reverse, alternate, alternate-reverse */
    animation-fill-mode: none; /* forwards, backwards, both */
    animation-play-state: running; /* paused */
    
    /* Kurzschreibweise */
    animation: name duration timing-function delay iteration-count direction fill-mode play-state;
    
    ```
    
- **Beispiel**
    
    ```css
    .rotierendesElement {
      animation: rotation 5s infinite linear;
    }
    
    @keyframes rotation {
      from {
        transform: rotate(0deg);
      }
      to {
        transform: rotate(360deg);
      }
    }
    
    ```
    

---

## **Transformationen**

### **2D-Transformationen**

- **translate**
    
    ```css
    transform: translate(50px, 100px);
    
    ```
    
- **rotate**
    
    ```css
    transform: rotate(45deg);
    
    ```
    
- **scale**
    
    ```css
    transform: scale(2); /* Verdoppelt die Größe */
    transform: scale(1.5, 0.5); /* Skaliert unterschiedlich auf X- und Y-Achse */
    
    ```
    
- **skew**
    
    ```css
    transform: skew(30deg, 20deg);
    
    ```
    
- **Mehrere Transformationen**
    
    ```css
    transform: translate(50px, 100px) rotate(45deg) scale(1.5);
    
    ```
    

### **3D-Transformationen**

- **rotateX, rotateY, rotateZ**
    
    ```css
    transform: rotateX(45deg);
    transform: rotateY(30deg);
    transform: rotateZ(60deg);
    
    ```
    
- **perspective**
    
    ```css
    transform: perspective(500px) rotateY(45deg);
    
    ```
    
- **transform-style**
    
    ```css
    transform-style: preserve-3d;
    
    ```
    

---

## **Responsive Design**

### **Media Queries**

```css
@media (max-width: 600px) {
  /* Stilregeln für Bildschirme kleiner als 600px */
}

@media (min-width: 601px) and (max-width: 1200px) {
  /* Stilregeln für Bildschirme zwischen 601px und 1200px */
}

@media (orientation: landscape) {
  /* Stilregeln für Querformat */
}

```

### **Viewport-Meta-Tag (im HTML)**

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">

```

---

## **SASS/SCSS (Präprozessor)**

SASS (Syntactically Awesome Style Sheets) erweitert CSS um Funktionen wie Variablen, Verschachtelung und Mixins.

### **Variablen**

```scss
$primary-color: #333;
$padding: 10px;

.button {
  background-color: $primary-color;
  padding: $padding;
}

```

### **Verschachtelung**

```scss
.navbar {
  ul {
    list-style: none;
    li {
      display: inline-block;
      a {
        text-decoration: none;
      }
    }
  }
}

```

### **Mixins**

```scss
@mixin border-radius($radius) {
  border-radius: $radius;
  -moz-border-radius: $radius;
  -webkit-border-radius: $radius;
}

.box {
  @include border-radius(10px);
}

```

### **Funktionen**

```scss
$base-font-size: 16px;

h1 {
  font-size: $base-font-size * 2;
}

.container {
  width: percentage(600px / 960px); /* Gibt 62.5% */
}

```