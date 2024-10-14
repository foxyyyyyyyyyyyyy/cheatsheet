# HTML

---

## **Einführung**

HTML (HyperText Markup Language) ist die Standard-Auszeichnungssprache zum Erstellen von Webseiten. Sie definiert die Struktur und den Inhalt einer Webseite mithilfe von Tags und Attributen.

### Was ist HTML?

[https://youtu.be/ok-plXXHlWw?si=Kp0-l9J05cASWbdB](https://youtu.be/ok-plXXHlWw?si=Kp0-l9J05cASWbdB)

---

## **Grundstruktur einer HTML-Seite**

```html
<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Titel der Seite</title>
</head>
<body>
  <!-- Inhalt der Seite -->
</body>
</html>
```

- `<!DOCTYPE html>`: Deklariert den Dokumenttyp als HTML5.
- `<html>`: Wurzelelement des HTML-Dokuments.
- `<head>`: Enthält Metadaten, Titel und Verweise auf Skripte und Stylesheets.
- `<body>`: Enthält den sichtbaren Inhalt der Webseite.

---

## **Grundlegende Tags**

### **Textformatierung**

- **Überschriften**
    
    ```html
    <h1>Überschrift 1</h1>
    <h2>Überschrift 2</h2>
    <h3>Überschrift 3</h3>
    <h4>Überschrift 4</h4>
    <h5>Überschrift 5</h5>
    <h6>Überschrift 6</h6>
    ```
    
- **Absätze**
    
    ```html
    <p>Dies ist ein Absatz.</p>
    ```
    
- **Zeilenumbruch**
    
    ```html
    Zeile 1<br>
    Zeile 2
    ```
    
- **Horizontaler Strich**
    
    ```html
    <hr>
    ```
    

### **Textstil**

- **Fettgedruckt**
    
    ```html
    <strong>Wichtiger Text</strong>
    <!-- Oder -->
    <b>Fettgedruckter Text</b>
    ```
    
- **Kursiv**
    
    ```html
    <em>Betonter Text</em>
    <!-- Oder -->
    <i>Kursiver Text</i>
    ```
    
- **Unterstrichen**
    
    ```html
    <u>Unterstrichener Text</u>
    ```
    
- **Durchgestrichen**
    
    ```html
    <s>Durchgestrichener Text</s>
    <!-- Oder -->
    <del>Gelöschter Text</del>
    ```
    
- **Hervorgehoben**
    
    ```html
    <mark>Hervorgehobener Text</mark>
    ```
    

### **Listen**

- **Ungeordnete Liste**
    
    ```html
    <ul>
      <li>Element 1</li>
      <li>Element 2</li>
      <li>Element 3</li>
    </ul>
    ```
    
- **Geordnete Liste**
    
    ```html
    <ol>
      <li>Erstes Element</li>
      <li>Zweites Element</li>
      <li>Drittes Element</li>
    </ol>
    ```
    
- **Verschachtelte Listen**
    
    ```html
    <ul>
      <li>Element 1
        <ul>
          <li>Unterelement 1a</li>
          <li>Unterelement 1b</li>
        </ul>
      </li>
      <li>Element 2</li>
    </ul>
    ```
    

### **Links und Anker**

- **Hyperlink**
    
    ```html
    <a href="<https://www.example.com>">Besuche Example.com</a>
    ```
    
- **E-Mail-Link**
    
    ```html
    <a href="mailto:beispiel@example.com">Schreibe eine E-Mail</a>
    ```
    
- **Ankerlink (Sprungmarke)**
    
    ```html
    <!-- Ziel -->
    <h2 id="abschnitt1">Abschnitt 1</h2>
    
    <!-- Link zum Ziel -->
    <a href="#abschnitt1">Gehe zu Abschnitt 1</a>
    ```
    

### **Bilder**

- **Bild einbinden**
    
    ```html
    <img src="bild.jpg" alt="Beschreibung des Bildes">
    ```
    
    - `src`: Pfad zur Bilddatei.
    - `alt`: Alternativer Text, falls das Bild nicht geladen werden kann.
- **Bildgröße festlegen**
    
    ```html
    <img src="bild.jpg" alt="Beschreibung" width="200" height="100">
    ```
    

### **Tabellen**

```html
<table>
  <caption>Tabellenüberschrift</caption>
  <thead>
    <tr>
      <th>Spalte 1</th>
      <th>Spalte 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Wert 1</td>
      <td>Wert 2</td>
    </tr>
    <tr>
      <td>Wert 3</td>
      <td>Wert 4</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="2">Tabellenfuß</td>
    </tr>
  </tfoot>
</table>
```

- `<table>`: Definiert eine Tabelle.
- `<thead>`, `<tbody>`, `<tfoot>`: Strukturieren den Tabellenkopf, -körper und -fuß.
- `<tr>`: Tabellenzeile.
- `<th>`: Tabellenkopfzelle (fett und zentriert).
- `<td>`: Tabellendatenzelle.
- `colspan` und `rowspan`: Bestimmen die Anzahl der Spalten oder Zeilen, die eine Zelle überspannt.

### **Formulare**

```html
<form action="verarbeitung.php" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name">

  <label for="email">E-Mail:</label>
  <input type="email" id="email" name="email">

  <input type="submit" value="Absenden">
</form>
```

- `action`: Ziel-URL, an die die Formulardaten gesendet werden.
- `method`: HTTP-Methode (`get` oder `post`).

### **Formularelemente**

- **Textfeld**
    
    ```html
    <input type="text" name="benutzername">
    ```
    
- **Passwortfeld**
    
    ```html
    <input type="password" name="passwort">
    ```
    
- **E-Mail-Feld**
    
    ```html
    <input type="email" name="email">
    ```
    
- **Nummerfeld**
    
    ```html
    <input type="number" name="anzahl" min="1" max="10">
    ```
    
- **Checkbox**
    
    ```html
    <input type="checkbox" name="option" value="1"> Option 1
    ```
    
- **Radiobutton**
    
    ```html
    <input type="radio" name="geschlecht" value="männlich"> Männlich
    <input type="radio" name="geschlecht" value="weiblich"> Weiblich
    ```
    
- **Dropdown-Menü**
    
    ```html
    <select name="farbe">
      <option value="rot">Rot</option>
      <option value="grün">Grün</option>
      <option value="blau">Blau</option>
    </select>
    ```
    
- **Mehrzeiliges Textfeld**
    
    ```html
    <textarea name="nachricht" rows="5" cols="30"></textarea>
    ```
    
- **Submit-Button**
    
    ```html
    <input type="submit" value="Absenden">
    ```
    
- **Reset-Button**
    
    ```html
    <input type="reset" value="Zurücksetzen">
    ```
    

### **Semantische Elemente (HTML5)**

- **Artikel**
    
    ```html
    <article>
      <!-- Eigenständiger Inhalt -->
    </article>
    ```
    
- **Abschnitt**
    
    ```html
    <section>
      <!-- Thematisch zusammenhängender Inhalt -->
    </section>
    ```
    
- **Header**
    
    ```html
    <header>
      <!-- Kopfbereich einer Seite oder eines Abschnitts -->
    </header>
    ```
    
- **Footer**
    
    ```html
    <footer>
      <!-- Fußbereich einer Seite oder eines Abschnitts -->
    </footer>
    ```
    
- **Navigation**
    
    ```html
    <nav>
      <!-- Navigationslinks -->
    </nav>
    ```
    
- **Aside**
    
    ```html
    <aside>
      <!-- Nebeninhalt oder Randnotizen -->
    </aside>
    ```
    
- **Main**
    
    ```html
    <main>
      <!-- Hauptinhalt der Seite -->
    </main>
    ```
    

### **Medien**

- **Audio einbinden**
    
    ```html
    <audio controls>
      <source src="musik.mp3" type="audio/mpeg">
      Ihr Browser unterstützt das Audio-Element nicht.
    </audio>
    ```
    
- **Video einbinden**
    
    ```html
    <video width="320" height="240" controls>
      <source src="video.mp4" type="video/mp4">
      Ihr Browser unterstützt das Video-Element nicht.
    </video>
    ```
    
- **YouTube-Video einbetten**
    
    ```html
    <iframe width="560" height="315" src="<https://www.youtube.com/embed/VIDEO_ID>" frameborder="0" allowfullscreen></iframe>
    ```
    

### **Meta-Tags**

- **Zeichensatz festlegen**
    
    ```html
    <meta charset="UTF-8">
    ```
    
- **Viewport für mobile Geräte**
    
    ```html
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    ```
    
- **Seitentitel**
    
    ```html
    <title>Titel der Seite</title>
    ```
    
- **Beschreibung für Suchmaschinen**
    
    ```html
    <meta name="description" content="Beschreibung der Webseite">
    ```
    
- **Schlüsselwörter**
    
    ```html
    <meta name="keywords" content="HTML, CSS, JavaScript">
    ```
    

### **Favicon hinzufügen**

```html
<link rel="icon" href="favicon.ico" type="image/x-icon">
```

---

## **Attribute**

- **Globale Attribute** (können in jedem Element verwendet werden)
    - `class`: CSS-Klassenname
        
        ```html
        <div class="container"></div>
        ```
        
    - `id`: Eindeutige Identifikation
        
        ```html
        <h1 id="haupttitel">Titel</h1>
        ```
        
    - `style`: Inline-CSS-Stile
        
        ```html
        <p style="color: red;">Roter Text</p>
        ```
        
    - `title`: Tooltip-Text beim Überfahren mit der Maus
        
        ```html
        <abbr title="HyperText Markup Language">HTML</abbr>
        ```
        
    - `lang`: Sprachangabe
        
        ```html
        <p lang="de">Dies ist ein deutscher Text.</p>
        ```
        
    - `data-*`: Benutzerdefinierte Datenattribute
        
        ```html
        <div data-role="admin"></div>
        ```
        
- **Spezifische Attribute**
    - **Hyperlink (`<a>`)**
        - `href`: Zieladresse
        - `target`: Festlegt, wo das verlinkte Dokument geöffnet wird (`_blank`, `_self`, `_parent`, `_top`)
            
            ```html
            <a href="<https://www.example.com>" target="_blank">Externer Link</a>
            ```
            
    - **Bild (`<img>`)**
        - `src`: Bildquelle
        - `alt`: Alternativtext
        - `width` und `height`: Größe des Bildes
    - **Formularelemente**
        - `name`: Name des Feldes (wichtig für die Formularverarbeitung)
        - `value`: Voreingestellter Wert
        - `placeholder`: Platzhaltertext
        - `required`: Pflichtfeld
            
            ```html
            <input type="text" name="benutzername" placeholder="Benutzername" required>
            ```
            
        - `disabled`: Deaktiviert das Element
        - `readonly`: Nur lesbar

---

## **Dokumentstruktur und Kommentare**

### **Kommentare**

```html
<!-- Dies ist ein Kommentar und wird nicht im Browser angezeigt -->
```

### **Dokumentabschnitte**

- **Kopfbereich**
    
    ```html
    <head>
      <!-- Metadaten, Titel, Verweise auf CSS und JS -->
    </head>
    ```
    
- **Körperbereich**
    
    ```html
    <body>
      <!-- Sichtbarer Inhalt der Webseite -->
    </body>
    ```
    

---

## **Verlinkung von CSS und JavaScript**

### **Externes Stylesheet einbinden**

```html
<link rel="stylesheet" href="styles.css">
```

### **Internes Stylesheet**

```html
<style>
  body {
    background-color: #f0f0f0;
  }
</style>
```

### **Inline-Stil**

```html
<p style="color: blue;">Blauer Text</p>
```

### **Externes JavaScript einbinden**

```html
<script src="script.js"></script>
```

### **Inline-JavaScript**

```html
<script>
  alert('Hallo Welt!');
</script>
```

---

## **Spezielle Zeichen und Symbole**

- **HTML-Entities**
    - `&amp;` für `&`
    - `&lt;` für `<`
    - `&gt;` für `>`
    - `&quot;` für `"`
    - `&apos;` für `'`
    - `&copy;` für ©
    - `&reg;` für ®
    - `&euro;` für €
    - `&nbsp;` für ein geschütztes Leerzeichen
    
    Beispiel:
    
    ```html
    <p>&copy; 2024 Mein Unternehmen</p>
    ```
    

---

## **Barrierefreiheit**

- **Alt-Text für Bilder**
    
    ```html
    <img src="bild.jpg" alt="Beschreibung des Bildes">
    ```
    
- **Label für Formularelemente**
    
    ```html
    <label for="email">E-Mail:</label>
    <input type="email" id="email" name="email">
    ```
    
- **Tabulatorreihenfolge festlegen**
    
    ```html
    <a href="#" tabindex="1">Erster Link</a>
    <a href="#" tabindex="2">Zweiter Link</a>
    ```
    
- **Aria-Attribute**
    
    ```html
    <div role="navigation" aria-label="Hauptnavigation">
      <!-- Navigationslinks -->
    </div>
    ```
    

---

## **Canvas und SVG**

### **Canvas (Zeichenfläche)**

```html
<canvas id="meinCanvas" width="200" height="100"></canvas>
```

JavaScript zum Zeichnen:

```jsx
var canvas = document.getElementById('meinCanvas');
var context = canvas.getContext('2d');
context.fillStyle = '#FF0000';
context.fillRect(0, 0, 200, 100);
```

### **SVG (Scalable Vector Graphics)**

```html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow" />
</svg>
```

---

## **Responsive Webdesign**

### **Viewport-Meta-Tag**

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### **Media Queries**

In CSS:

```css
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

---

## **Dokumentenkonformität und Validierung**

- **Doctype-Deklaration**
    
    ```html
    <!DOCTYPE html>
    ```
    
- **Validierung**
    
    Verwenden Sie den W3C-Validator, um Ihr HTML zu überprüfen: [https://validator.w3.org/](https://validator.w3.org/)
    

---

## **Best Practices**

- **Saubere und ordentliche Struktur**
    - Einrückungen verwenden.
    - Konsistente Namensgebung für Klassen und IDs.
- **Semantisches HTML**
    - Verwenden Sie die richtigen Tags für den entsprechenden Inhalt (z. B. `<header>`, `<nav>`, `<main>`, `<footer>`).
- **Barrierefreiheit berücksichtigen**
    - Alt-Texte für Bilder.
    - Labels für Formularelemente.
    - Überschriftenhierarchie einhalten.
- **Externe Ressourcen minimieren**
    - Kombinieren und minimieren Sie CSS- und JS-Dateien.
    - Verwenden Sie Caching, wo möglich.
- **Performance optimieren**
    - Bilder komprimieren.
    - Lazy Loading für Bilder implementieren.
    - GZIP-Komprimierung auf dem Server aktivieren.

---

## **Meta-Tags für SEO**

- **Titel und Beschreibung**
    
    ```html
    <title>Meine Webseite</title>
    <meta name="description" content="Beschreibung meiner Webseite">
    ```
    
- **Robots-Meta-Tag**
    
    ```html
    <meta name="robots" content="index, follow">
    ```
    
- **Canonical-Link**
    
    ```html
    <link rel="canonical" href="<https://www.example.com/aktueller-pfad>">
    ```
    
- **Open Graph Tags (für Social Media)**
    
    ```html
    <meta property="og:title" content="Titel der Seite">
    <meta property="og:description" content="Beschreibung der Seite">
    <meta property="og:image" content="<https://www.example.com/bild.jpg>">
    <meta property="og:url" content="<https://www.example.com/>">
    ```
    

---

## **Favicons und Web App Manifest**

### **Favicon**

```html
<link rel="icon" href="favicon.ico" type="image/x-icon">
```

### **Web App Manifest (für Progressive Web Apps)**

- **manifest.json**
    
    ```json
    {
      "name": "Meine App",
      "short_name": "App",
      "start_url": "/",
      "display": "standalone",
      "icons": [
        {
          "src": "icon/lowres.webp",
          "sizes": "64x64",
          "type": "image/webp"
        },
        {
          "src": "icon/hd_hi",
          "sizes": "128x128"
        }
      ]
    }
    ```
    
- **Einbindung in HTML**
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```
    

---

## **Spezielle Elemente und Attribute**

- **Details und Zusammenfassung**
    
    ```html
    <details>
      <summary>Mehr erfahren</summary>
      <p>Zusätzliche Informationen.</p>
    </details>
    ```
    
- **Progress (Fortschrittsanzeige)**
    
    ```html
    <progress value="70" max="100">70%</progress>
    ```
    
- **Meter (Messwert)**
    
    ```html
    <meter min="0" max="100" value="75">75%</meter>
    ```
    
- **Bildkarten**
    
    ```html
    <figure>
      <img src="bild.jpg" alt="Beschreibung">
      <figcaption>Bildunterschrift</figcaption>
    </figure>
    ```
    

---

## **iframes**

- **Einbettung externer Inhalte**
    
    ```html
    <iframe src="<https://www.example.com>" width="600" height="400" frameborder="0"></iframe>
    ```
    
- **Attribute**
    - `src`: URL des eingebetteten Inhalts.
    - `width` und `height`: Größe des iframes.
    - `frameborder`: Rahmen um das iframe (0 oder 1).
    - `allowfullscreen`: Erlaubt Vollbildmodus.

---

## **Eingebettete Inhalte**

- **Objekt**
    
    ```html
    <object data="animation.swf" type="application/x-shockwave-flash" width="400" height="300">
      <param name="movie" value="animation.swf">
      <!-- Fallback-Inhalt -->
      Ihr Browser unterstützt keine eingebetteten Objekte.
    </object>
    ```
    
- **Embed**
    
    ```html
    <embed src="animation.swf" width="400" height="300">
    ```
    

---

## **Veraltete Tags (Nicht mehr verwenden)**

- `<font>`: Verwenden Sie stattdessen CSS.
- `<center>`: Verwenden Sie `text-align: center;` in CSS.
- `<big>`, `<small>`: Verwenden Sie CSS-Schriftgrößen.
- `<strike>`: Verwenden Sie `<s>` oder CSS `text-decoration: line-through;`.