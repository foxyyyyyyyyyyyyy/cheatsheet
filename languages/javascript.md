# Javascript

### Was ist Javascript?

[https://youtu.be/DHjqpvDnNGE?si=zTfIeLsQnQRKhNMe](https://youtu.be/DHjqpvDnNGE?si=zTfIeLsQnQRKhNMe)

## **Grundlagen**

### **Variablen deklarieren**

- **var**: Funktion- oder globaler Scope.

```jsx
var x = 10;
```

- **let**: Block Scope, neuere Art.

```jsx
let y = 20;
```

- **const**: Block Scope, unveränderliche Variable.

```jsx
const z = 30;
```

### **Datentypen**

- **Primitive Typen**: `String`, `Number`, `Boolean`, `Null`, `Undefined`, `Symbol`, `BigInt`
- **Objekte**: `Object`, `Array`, `Function`, etc.

### **Operatoren**

- **Arithmetische Operatoren**: `+`, ``, ``, `/`, `%`, `*`
- **Zuweisungsoperatoren**: `=`, `+=`, `=`, `=`, `/=`, `%=`
- **Vergleichsoperatoren**:
    - Gleich: `==`, Identisch: `===`
    - Ungleich: `!=`, Nicht identisch: `!==`
    - Größer als: `>`, Kleiner als: `<`
    - Größer gleich: `>=`, Kleiner gleich: `<=`
- **Logische Operatoren**: `&&` (Und), `||` (Oder), `!` (Nicht)

---

## **Steuerstrukturen**

### **if...else**

```jsx
if (Bedingung) {
  // Code, wenn Bedingung wahr ist
} else if (AndereBedingung) {
  // Code, wenn AndereBedingung wahr ist
} else {
  // Code, wenn keine Bedingung wahr ist
}

```

### switch

```jsx
switch (Ausdruck) {
  case Wert1:
    // Code
    break;
  case Wert2:
    // Code
    break;
  default:
    // Code
}

```

### Schleifen

- **for**
    
    ```jsx
    for (let i = 0; i < 5; i++) {
      // Code
    }
    
    ```
    
- **while**
    
    ```jsx
    while (Bedingung) {
      // Code
    }
    ```
    

- **do...while**
    
    ```jsx
    do {
      // Code
    } while (Bedingung);
    ```
    

- **for...of** (Iterieren über iterable Objekte)
    
    ```jsx
    for (let element of array) {
      // Code
    }
    ```
    

- **for...in** (Iterieren über Eigenschaften eines Objekts)
    
    ```jsx
    for (let key in object) {
      // Code
    }
    ```
    

## **Funktionen**

### **Funktionsdeklaration**

```jsx
function name(parameter1, parameter2) {
  // Code
}
```

### **Funktionsausdruck**

```jsx
const name = function(parameter1, parameter2) {
  // Code
};
```

### **Arrow Functions**

```jsx
const name = (parameter1, parameter2) => {
  // Code
};
```

---

## **Arrays**

- **Array erstellen**
    
    ```jsx
    const array = [element1, element2, element3];
    ```
    
- **Zugriff auf Elemente**
    
    ```jsx
    let element = array[index];
    ```
    
- **Methoden**
    - **push()**: Fügt Elemente am Ende hinzu.
        
        ```jsx
        array.push(element);
        ```
        
    - **pop()**: Entfernt letztes Element.
        
        ```jsx
        array.pop();
        ```
        
    - **shift()**: Entfernt erstes Element.
        
        ```jsx
        array.shift();
        ```
        
    - **unshift()**: Fügt Elemente am Anfang hinzu.
        
        ```jsx
        array.unshift(element);
        ```
        
    - **slice()**: Gibt einen Teil des Arrays zurück.
        
        ```jsx
        array.slice(startIndex, endIndex);
        ```
        
    - **splice()**: Fügt Elemente ein oder entfernt sie.
        
        ```jsx
        array.splice(startIndex, deleteCount, item1, item2);
        ```
        
    - **forEach()**: Iteriert über jedes Element.
        
        ```jsx
        array.forEach((element) => {
          // Code
        });
        ```
        

---

## **Objekte**

- **Objekt erstellen**
    
    ```jsx
    const person = {
      name: "Max",
      alter: 30,
    };
    ```
    
- **Zugriff auf Eigenschaften**
    - Punktnotation:
        
        ```jsx
        person.name;
        ```
        
    - Klammernotation:
        
        ```jsx
        person["name"];
        ```
        
- **Methoden hinzufügen**
    
    ```jsx
    person.grüßen = function() {
      console.log("Hallo!");
    };
    ```
    

---

## **DOM-Manipulation**

- **Elemente auswählen**
    - **getElementById()**
        
        ```jsx
        document.getElementById("id");
        ```
        
    - **getElementsByClassName()**
        
        ```jsx
        document.getElementsByClassName("className");
        ```
        
    - **querySelector()**
        
        ```jsx
        document.querySelector("selector");
        ```
        
- **Ereignisse hinzufügen**
    
    ```jsx
    element.addEventListener("click", function() {
      // Code
    });
    ```
    

---

## **Asynchrone Programmierung**

### **setTimeout**

```jsx
javascript
Code kopieren
setTimeout(function() {
  // Code
}, millisekunden);

```

### **setInterval**

```jsx
setInterval(function() {
  // Code
}, millisekunden);
```

### **Promises**

```jsx
const promise = new Promise((resolve, reject) => {
  // Asynchroner Code
});
```

### **async/await**

```jsx
async function name() {
  const result = await promise;
}
```

---

## **Fehlerbehandlung**

### **try...catch**

```jsx
try {
  // Code, der Fehler verursachen könnte
} catch (error) {
  // Fehlerbehandlung
} finally {
  // Optionaler Code, der immer ausgeführt wird
}
```

---

## **Nützliche Funktionen**

- **console.log()**: Ausgabe in der Konsole.
    
    ```jsx
    console.log("Nachricht");
    ```
    
- **parseInt(), parseFloat()**: Konvertierung in Zahlen.
    
    ```jsx
    parseInt("10"); // Gibt 10 zurück
    ```
    
- **isNaN()**: Prüft, ob Wert keine Zahl ist.
    
    ```jsx
    isNaN("Hallo"); // Gibt true zurück
    ```