# PHP

---

## **Einführung**

PHP (Hypertext Preprocessor) ist eine serverseitige Skriptsprache, die hauptsächlich zur Webentwicklung verwendet wird. Sie ermöglicht das Erstellen dynamischer Webseiten und Anwendungen.

### Was ist php?

[https://youtu.be/a7_WFUlFS94?si=2__KQMwdJgzF87j0](https://youtu.be/a7_WFUlFS94?si=2__KQMwdJgzF87j0)

---

## **Grundlagen**

### **PHP-Tags**

PHP-Code wird innerhalb von `<?php` und `?>` Tags geschrieben.

```php
<?php
  // PHP-Code hier
?>
```

### **Kommentare**

- **Einzeilige Kommentare**
    
    ```php
    // Dies ist ein Kommentar
    # Dies ist auch ein Kommentar
    ```
    
- **Mehrzeilige Kommentare**
    
    ```php
    /*
      Dies ist ein mehrzeiliger Kommentar
    */
    ```
    

### **Variablen**

Variablen beginnen immer mit einem Dollarzeichen `$`.

```php
<?php
  $name = "Max";
  $alter = 30;
?>
```

### **Datentypen**

- **String**: Zeichenketten
    
    ```php
    $text = "Hallo Welt";
    ```
    
- **Integer**: Ganze Zahlen
    
    ```php
    $zahl = 42;
    ```
    
- **Float**: Gleitkommazahlen
    
    ```php
    $preis = 19.99;
    ```
    
- **Boolean**: Wahrheitswerte (`true` oder `false`)
    
    ```php
    $istWahr = true;
    ```
    
- **Array**: Sammlung von Werten
    
    ```php
    $farben = array("Rot", "Grün", "Blau");
    ```
    
- **Null**: Null-Wert
    
    ```php
    $wert = null;
    ```
    

---

## **Operatoren**

### **Arithmetische Operatoren**

- **Addition**: `$a + $b`
- **Subtraktion**: `$a - $b`
- **Multiplikation**: `$a * $b`
- **Division**: `$a / $b`
- **Modulus**: `$a % $b`
- **Exponentiation**: `$a ** $b`

### **Zuweisungsoperatoren**

- **Einfach**: `$a = $b`
- **Kombiniert**: `+=`, `=`, `=`, `/=`, `%=`, `*=`
    
    ```php
    $a += 5; // entspricht $a = $a + 5;
    ```
    

### **Vergleichsoperatoren**

- **Gleich**: `$a == $b`
- **Identisch (Gleich und gleicher Typ)**: `$a === $b`
- **Ungleich**: `$a != $b` oder `$a <> $b`
- **Nicht identisch**: `$a !== $b`
- **Größer als**: `$a > $b`
- **Kleiner als**: `$a < $b`
- **Größer oder gleich**: `$a >= $b`
- **Kleiner oder gleich**: `$a <= $b`

### **Logische Operatoren**

- **Und**: `$a && $b` oder `$a and $b`
- **Oder**: `$a || $b` oder `$a or $b`
- **Nicht**: `!$a`
- **XOR**: `$a xor $b`

---

## **Steuerstrukturen**

### **if...else**

```php
<?php
  if ($a > $b) {
    // Code, wenn $a größer als $b ist
  } elseif ($a == $b) {
    // Code, wenn $a gleich $b ist
  } else {
    // Code, wenn $a kleiner als $b ist
  }
?>
```

### **switch**

```php
<?php
  switch ($farbe) {
    case "rot":
      // Code für rot
      break;
    case "grün":
      // Code für grün
      break;
    default:
      // Code, wenn keine Bedingung zutrifft
  }
?>
```

### **Schleifen**

- **while**
    
    ```php
    <?php
      while ($i <= 10) {
        // Code
        $i++;
      }
    ?>
    ```
    
- **do...while**
    
    ```php
    <?php
      do {
        // Code
        $i++;
      } while ($i <= 10);
    ?>
    ```
    
- **for**
    
    ```php
    <?php
      for ($i = 0; $i <= 10; $i++) {
        // Code
      }
    ?>
    ```
    
- **foreach** (Für Arrays)
    
    ```php
    <?php
      foreach ($array as $wert) {
        // Code
      }
    ?>
    ```
    
    Mit Schlüssel:
    
    ```php
    <?php
      foreach ($array as $schlüssel => $wert) {
        // Code
      }
    ?>
    ```
    

---

## **Funktionen**

### **Funktionsdeklaration**

```php
<?php
  function name($parameter1, $parameter2) {
    // Code
    return $ergebnis;
  }
?>
```

### **Funktionsaufruf**

```php
<?php
  $resultat = name($wert1, $wert2);
?>
```

### **Optionale Parameter und Standardwerte**

```php
<?php
  function begrüßen($name = "Gast") {
    echo "Hallo, $name!";
  }
?>
```

---

## **Arrays**

### **Array erstellen**

- **Indiziertes Array**
    
    ```php
    <?php
      $früchte = array("Apfel", "Banane", "Orange");
      // Oder seit PHP 5.4
      $früchte = ["Apfel", "Banane", "Orange"];
    ?>
    ```
    
- **Assoziatives Array**
    
    ```php
    <?php
      $alter = array("Peter" => 35, "Ben" => 37, "Joe" => 43);
      // Oder seit PHP 5.4
      $alter = ["Peter" => 35, "Ben" => 37, "Joe" => 43];
    ?>
    ```
    

### **Zugriff auf Array-Elemente**

```php
<?php
  echo $früchte[0]; // Gibt "Apfel" aus
  echo $alter["Peter"]; // Gibt 35 aus
?>
```

### **Array-Funktionen**

- **count()**: Zählt die Elemente eines Arrays
    
    ```php
    $anzahl = count($früchte);
    ```
    
- **array_push()**: Fügt ein oder mehrere Elemente am Ende hinzu
    
    ```php
    array_push($früchte, "Traube");
    ```
    
- **array_pop()**: Entfernt das letzte Element
    
    ```php
    $letztesElement = array_pop($früchte);
    ```
    
- **array_shift()**: Entfernt das erste Element
    
    ```php
    $erstesElement = array_shift($früchte);
    ```
    
- **array_unshift()**: Fügt ein oder mehrere Elemente am Anfang hinzu
    
    ```php
    array_unshift($früchte, "Erdbeere");
    ```
    
- **sort()**: Sortiert ein Array aufsteigend
    
    ```php
    sort($früchte);
    ```
    
- **rsort()**: Sortiert ein Array absteigend
    
    ```php
    rsort($früchte);
    ```
    
- **asort()**: Sortiert ein assoziatives Array nach Werten aufsteigend
    
    ```php
    asort($alter);
    ```
    
- **ksort()**: Sortiert ein assoziatives Array nach Schlüsseln aufsteigend
    
    ```php
    ksort($alter);
    ```
    

---

## **Strings**

### **String-Verkettung**

```php
<?php
  $text1 = "Hallo";
  $text2 = "Welt";
  $text = $text1 . " " . $text2; // Gibt "Hallo Welt"
?>
```

### **String-Funktionen**

- **strlen()**: Länge eines Strings
    
    ```php
    $länge = strlen($text);
    ```
    
- **strpos()**: Position eines Substrings
    
    ```php
    $position = strpos($text, "Welt");
    ```
    
- **str_replace()**: Ersetzen von Text
    
    ```php
    $neuerText = str_replace("Welt", "PHP", $text);
    ```
    
- **substr()**: Teilstring extrahieren
    
    ```php
    $teil = substr($text, 6); // Ab Position 6 bis Ende
    ```
    
- **strtolower()** und **strtoupper()**: Umwandlung in Klein- bzw. Großbuchstaben
    
    ```php
    $klein = strtolower($text);
    $groß = strtoupper($text);
    ```
    

---

## **Superglobale Variablen**

- **$_GET**: Daten aus URL-Parametern
    
    ```php
    $wert = $_GET['parameter'];
    ```
    
- **$_POST**: Daten aus Formularen
    
    ```php
    $wert = $_POST['feldname'];
    ```
    
- **$_SERVER**: Server- und Ausführungsinformationen
    
    ```php
    $skriptName = $_SERVER['PHP_SELF'];
    $serverName = $_SERVER['SERVER_NAME'];
    ```
    
- **$_SESSION**: Session-Variablen
- **$_COOKIE**: Cookies
- **$_FILES**: Hochgeladene Dateien
- **$_REQUEST**: Enthält sowohl $_GET als auch $_POST und $_COOKIE

---

## **Formularverarbeitung**

### **HTML-Formular**

```html
<form method="post" action="verarbeitung.php">
  Name: <input type="text" name="name">
  <input type="submit" value="Absenden">
</form>
```

### **Verarbeitung in PHP**

```php
<?php
  if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $name = $_POST['name'];
    echo "Hallo, " . htmlspecialchars($name);
  }
?>
```

---

## **Sessions**

### **Session starten**

```php
<?php
  session_start();
?>
```

### **Session-Variablen setzen**

```php
<?php
  $_SESSION['username'] = "Max";
?>
```

### **Session-Variablen abrufen**

```php
<?php
  echo $_SESSION['username'];
?>
```

### **Session beenden**

```php
<?php
  session_start();
  session_unset();
  session_destroy();
?>
```

---

## **Cookies**

### **Cookie setzen**

```php
<?php
  setcookie("benutzer", "Max", time() + (86400 * 30), "/"); // Gültig für 30 Tage
?>
```

### **Cookie abrufen**

```php
<?php
  if(isset($_COOKIE["benutzer"])) {
    echo "Benutzer: " . $_COOKIE["benutzer"];
  } else {
    echo "Kein Benutzer-Cookie gesetzt";
  }
?>
```

---

## **Dateioperationen**

### **Datei öffnen**

```php
<?php
  $datei = fopen("datei.txt", "r");
?>
```

### **Datei lesen**

```php
<?php
  $inhalt = fread($datei, filesize("datei.txt"));
?>
```

### **Datei schreiben**

```php
<?php
  $datei = fopen("neuedatei.txt", "w");
  fwrite($datei, "Dieser Text wird in die Datei geschrieben.");
?>
```

### **Datei schließen**

```php
<?php
  fclose($datei);
?>
```

### **Datei in ein Array lesen**

```php
<?php
  $zeilen = file("datei.txt");
  foreach($zeilen as $zeile) {
    echo $zeile . "<br>";
  }
?>
```

---

## **Include und Require**

- **include**: Bindet eine Datei ein; bei Fehler wird eine Warnung ausgegeben, das Skript läuft weiter.
    
    ```php
    <?php
      include 'header.php';
    ?>
    ```
    
- **require**: Bindet eine Datei ein; bei Fehler wird ein Fatal Error erzeugt, das Skript wird abgebrochen.
    
    ```php
    <?php
      require 'config.php';
    ?>
    ```
    
- **include_once** und **require_once**: Wie oben, aber stellt sicher, dass die Datei nur einmal eingebunden wird.

---

## **OOP in PHP**

### **Klassen und Objekte**

```php
<?php
  class Person {
    // Eigenschaften
    public $name;
    public $alter;

    // Konstruktor
    function __construct($name, $alter) {
      $this->name = $name;
      $this->alter = $alter;
    }

    // Methoden
    public function vorstellen() {
      echo "Hallo, ich bin " . $this->name . " und bin " . $this->alter . " Jahre alt.";
    }
  }

  // Objekt erstellen
  $person = new Person("Max", 30);
  $person->vorstellen();
?>
```

### **Sichtbarkeitsmodifizierer**

- **public**: Von überall zugänglich
- **protected**: Nur innerhalb der Klasse und von abgeleiteten Klassen
- **private**: Nur innerhalb der Klasse

### **Vererbung**

```php
<?php
  class Mitarbeiter extends Person {
    public $position;

    function __construct($name, $alter, $position) {
      parent::__construct($name, $alter);
      $this->position = $position;
    }

    public function vorstellen() {
      parent::vorstellen();
      echo " Ich arbeite als " . $this->position . ".";
    }
  }

  $mitarbeiter = new Mitarbeiter("Lisa", 28, "Entwicklerin");
  $mitarbeiter->vorstellen();
?>
```

### **Abstrakte Klassen**

```php
<?php
  abstract class Form {
    abstract protected function berechneFläche();
  }

  class Rechteck extends Form {
    private $breite;
    private $höhe;

    public function __construct($breite, $höhe) {
      $this->breite = $breite;
      $this->höhe = $höhe;
    }

    public function berechneFläche() {
      return $this->breite * $this->höhe;
    }
  }
?>
```

### **Interfaces**

```php
<?php
  interface Bezahlbar {
    public function bezahlen($betrag);
  }

  class Kunde implements Bezahlbar {
    public function bezahlen($betrag) {
      echo "Bezahlt: " . $betrag . " Euro";
    }
  }
?>
```

---

## **Datenbankverbindung mit MySQLi**

### **Verbindung herstellen**

```php
<?php
  $servername = "localhost";
  $benutzername = "benutzer";
  $passwort = "passwort";
  $datenbank = "meine_datenbank";

  // Verbindung erstellen
  $conn = new mysqli($servername, $benutzername, $passwort, $datenbank);

  // Verbindung prüfen
  if ($conn->connect_error) {
    die("Verbindung fehlgeschlagen: " . $conn->connect_error);
  }
?>
```

### **Daten abrufen**

```php
<?php
  $sql = "SELECT id, vorname, nachname FROM benutzer";
  $ergebnis = $conn->query($sql);

  if ($ergebnis->num_rows > 0) {
    while($row = $ergebnis->fetch_assoc()) {
      echo "ID: " . $row["id"]. " - Name: " . $row["vorname"]. " " . $row["nachname"]. "<br>";
    }
  } else {
    echo "Keine Ergebnisse";
  }
?>
```

### **Daten einfügen**

```php
<?php
  $sql = "INSERT INTO benutzer (vorname, nachname, email) VALUES ('Max', 'Mustermann', 'max@example.com')";

  if ($conn->query($sql) === TRUE) {
    echo "Neuer Datensatz erfolgreich erstellt";
  } else {
    echo "Fehler: " . $sql . "<br>" . $conn->error;
  }
?>
```

### **Verbindung schließen**

```php
<?php
  $conn->close();
?>
```

---

## **Fehlerbehandlung**

### **try...catch**

```php
<?php
  try {
    // Code, der einen Fehler verursachen könnte
    if (!file_exists("datei.txt")) {
      throw new Exception("Datei nicht gefunden.");
    }
  } catch (Exception $e) {
    echo 'Fehler: ' . $e->getMessage();
  }
?>
```

---

## **Nützliche Funktionen**

- **echo**: Ausgabe von Strings
    
    ```php
    <?php
      echo "Hallo Welt!";
    ?>
    ```
    
- **print_r()**: Druckt lesbare Informationen über eine Variable (nützlich für Arrays und Objekte)
    
    ```php
    <?php
      print_r($array);
    ?>
    ```
    
- **var_dump()**: Gibt Typ und Wert einer Variable aus
    
    ```php
    <?php
      var_dump($variable);
    ?>
    ```
    
- **empty()**: Prüft, ob eine Variable leer ist
    
    ```php
    <?php
      if (empty($variable)) {
        // Variable ist leer
      }
    ?>
    ```
    
- **isset()**: Prüft, ob eine Variable gesetzt ist
    
    ```php
    <?php
      if (isset($variable)) {
        // Variable ist gesetzt
      }
    ?>
    ```
    
- **include_path**: Gibt den Include-Pfad zurück
    
    ```php
    <?php
      echo get_include_path();
    ?>
    ```
    

---

## **Reguläre Ausdrücke**

- **preg_match()**: Prüft, ob ein String einem Muster entspricht
    
    ```php
    <?php
      if (preg_match("/^([a-zA-Z' ]+)$/", $name)) {
        echo "Gültiger Name";
      } else {
        echo "Ungültiger Name";
      }
    ?>
    ```
    
- **preg_replace()**: Sucht und ersetzt nach einem Muster
    
    ```php
    <?php
      $neuerText = preg_replace("/Hund/", "Katze", $text);
    ?>
    ```
    

---

## **JSON-Verarbeitung**

### **JSON in PHP-Array dekodieren**

```php
<?php
  $jsonString = '{"name":"Max","alter":30}';
  $daten = json_decode($jsonString, true); // true für assoziatives Array
  echo $daten['name']; // Gibt "Max" aus
?>
```

### **PHP-Array in JSON kodieren**

```php
<?php
  $daten = array("name" => "Max", "alter" => 30);
  $jsonString = json_encode($daten);
  echo $jsonString; // Gibt '{"name":"Max","alter":30}' aus
?>
```

---

## **Datei-Uploads**

### **HTML-Formular**

```html
<form action="upload.php" method="post" enctype="multipart/form-data">
  Wähle eine Datei zum Hochladen:
  <input type="file" name="datei" id="datei">
  <input type="submit" value="Upload" name="submit">
</form>
```

### **Verarbeitung in PHP**

```php
<?php
  if ($_SERVER['REQUEST_METHOD'] == 'POST') {
    $zielVerzeichnis = "uploads/";
    $zielDatei = $zielVerzeichnis . basename($_FILES["datei"]["name"]);
    $uploadOk = 1;
    $dateiTyp = strtolower(pathinfo($zielDatei, PATHINFO_EXTENSION));

    // Überprüfen, ob die Datei existiert
    if (file_exists($zielDatei)) {
      echo "Die Datei existiert bereits.";
      $uploadOk = 0;
    }

    // Datei hochladen
    if ($uploadOk == 1) {
      if (move_uploaded_file($_FILES["datei"]["tmp_name"], $zielDatei)) {
        echo "Die Datei ". basename( $_FILES["datei"]["name"]). " wurde hochgeladen.";
      } else {
        echo "Fehler beim Hochladen der Datei.";
      }
    }
  }
?>
```

---

## **Mail versenden**

*Hinweis: Der Mailversand kann serverseitige Konfiguration erfordern.*

```php
<?php
  $empfänger = "email@example.com";
  $betreff = "Testmail";
  $nachricht = "Dies ist eine Testmail.";
  $headers = "From: absender@example.com";

  if (mail($empfänger, $betreff, $nachricht, $headers)) {
    echo "Mail erfolgreich gesendet.";
  } else {
    echo "Fehler beim Senden der Mail.";
  }
?>
```