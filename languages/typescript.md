# Typescript

## **Einführung**

TypeScript ist eine typisierte Obermenge von JavaScript, die zu reinem JavaScript kompiliert wird. Es fügt statische Typisierung und erweiterte Features hinzu, die die Entwicklung großer Anwendungen erleichtern.

### Was ist Typescript?

[https://youtu.be/zQnBQ4tB3ZA?si=0zYYL-FalwZa-7_t](https://youtu.be/zQnBQ4tB3ZA?si=0zYYL-FalwZa-7_t)

---

## **Grundlegende Typen**

### **Primitive Typen**

- **boolean**
    
    ```tsx
    let isDone: boolean = false;
    ```
    
- **number**
    
    ```tsx
     decimal: number = 6;
    let hex: number = 0xf00d;
    let binary: number = 0b1010;
    let octal: number = 0o744;
    ```
    
- **string**
    
    ```tsx
    let color: string = "blau";
    let sentence: string = `Die Farbe ist ${color}`;
    ```
    
- **array**
    
    ```tsx
    let list: number[] = [1, 2, 3];
    // Oder generische Array-Typen
    let list: Array<number> = [1, 2, 3];
    ```
    
- **tuple**
    
    ```tsx
    let x: [string, number];
    x = ["Hallo", 10];
    ```
    
- **enum**
    
    ```tsx
    enum Farbe {
      Rot,
      Grün,
      Blau,
    }
    let c: Farbe = Farbe.Grün;
    ```
    
- **any**
    
    ```tsx
    let ungewiss: any = 4;
    ungewiss = "vielleicht ein String";
    ungewiss = false;
    ```
    
- **void**
    
    ```tsx
    function warnUser(): void {
      console.log("Achtung!");
    }
    ```
    
- **null und undefined**
    
    ```tsx
    let u: undefined = undefined;
    let n: null = null;
    ```
    
- **never**
    
    ```tsx
    function error(message: string): never {
      throw new Error(message);
    }
    ```
    

---

## **Typanmerkungen**

### **Variablen**

```tsx
let zahl: number = 5;
```

### **Funktionen**

```tsx
function addieren(a: number, b: number): number {
  return a + b;
}
```

### **Optionale Parameter und Standardwerte**

```tsx
function baueName(vorname: string, nachname?: string): string {
  if (nachname) {
    return vorname + " " + nachname;
  } else {
    return vorname;
  }
}

function baueNameMitStandard(vorname: string, nachname = "Mustermann"): string {
  return vorname + " " + nachname;
}
```

### **Rest-Parameter**

```tsx
function buildName(vorname: string, ...restNamen: string[]) {
  return vorname + " " + restNamen.join(" ");
}
```

---

## **Interfaces**

### **Einfaches Interface**

```tsx
interface Person {
  vorname: string;
  nachname: string;
}

function begrüßen(person: Person) {
  console.log("Hallo, " + person.vorname + " " + person.nachname);
}

let user = { vorname: "Max", nachname: "Mustermann" };
begrüßen(user);
```

### **Optionale Eigenschaften**

```tsx
interface Rechteck {
  breite: number;
  länge?: number;
}
```

### **Readonly Eigenschaften**

```tsx
interface Punkt {
  readonly x: number;
  readonly y: number;
}

let p1: Punkt = { x: 10, y: 20 };
// p1.x = 5; // Fehler: x ist schreibgeschützt
```

### **Funktionstypen**

```tsx
interface Suchfunktion {
  (quelle: string, substr: string): boolean;
}

let meineSuche: Suchfunktion;
meineSuche = function (q, s) {
  return q.search(s) > -1;
};
```

---

## **Klassen**

### **Grundlegende Klassen**

```tsx
class Tier {
  name: string;

  constructor(name: string) {
    this.name = name;
  }

  bewegen(meter: number) {
    console.log(`${this.name} bewegt sich ${meter}m weit.`);
  }
}

let tier = new Tier("Elefant");
tier.bewegen(10);
```

### **Vererbung**

```tsx
class Hund extends Tier {
  bellen() {
    console.log("Wuff! Wuff!");
  }
}

let hund = new Hund("Bello");
hund.bellen();
hund.bewegen(5);
```

### **Modifizierer**

- **public**: Überall zugänglich.
- **private**: Nur innerhalb der Klasse zugänglich.
- **protected**: In der Klasse und in abgeleiteten Klassen zugänglich.

```tsx
class Person {
  protected name: string;
  constructor(name: string) {
    this.name = name;
  }
}

class Mitarbeiter extends Person {
  private abteilung: string;

  constructor(name: string, abteilung: string) {
    super(name);
    this.abteilung = abteilung;
  }

  getElevatorPitch() {
    return `Hallo, mein Name ist ${this.name} und ich arbeite in der ${this.abteilung}.`;
  }
}
```

---

## **Generics**

### **Einfaches Generic**

```tsx
function identität<T>(arg: T): T {
  return arg;
}

let ausgabe = identität<string>("Hallo Welt");
```

### **Generische Klassen**

```tsx
class GenerischeZahl<T> {
  nullWert: T;
  addieren: (x: T, y: T) => T;
}

let meineNummer = new GenerischeZahl<number>();
meineNummer.nullWert = 0;
meineNummer.addieren = function (x, y) {
  return x + y;
};
```

### **Generische Einschränkungen**

```tsx
interface Länge {
  länge: number;
}

function loggingIdentität<T extends Länge>(arg: T): T {
  console.log(arg.länge);
  return arg;
}
```

---

## **Enums**

### **Numerische Enums**

```tsx
enum Richtung {
  Oben = 1,
  Unten,
  Links,
  Rechts,
}
```

### **String Enums**

```tsx
enum Antwort {
  Nein = "NEIN",
  Ja = "JA",

```

---

## **Type Aliases**

```tsx
type Name = string;
type NameResolver = () => string;
type NameOrResolver = Name | NameResolver;

function getName(n: NameOrResolver): Name {
  if (typeof n === "string") {
    return n;
  } else {
    return n();
  }

```

---

## **Union und Intersection Types**

### **Union Types**

```tsx
function printId(id: number | string) {
  console.log("Ihre ID ist: " + id);
}
```

### **Type Guards**

```tsx
function isNumber(x: any): x is number {
  return typeof x === "number";
}
```

### **Intersection Types**

```tsx
interface Person {
  name: string;
}

interface Mitarbeiter {
  firma: string;
}

type Angestellter = Person & Mitarbeiter;

let angestellter: Angestellter = { name: "Max", firma: "ABC GmbH" };
```

---

## **Namespaces und Module**

### **Namespaces**

```tsx
namespace Validatoren {
  export interface StringValidator {
    isAcceptable(s: string): boolean;
  }

  export class LettersOnlyValidator implements StringValidator {
    isAcceptable(s: string) {
      return /^[A-Za-z]+$/.test(s);
    }
  }
}

let validator = new Validatoren.LettersOnlyValidator();
```

### **Module (ES6-Importe und -Exporte)**

- **Exportieren**
    
    ```tsx
    export class Tier {
      // ...
    }
    ```
    
- **Importieren**
    
    ```tsx
    import { Tier } from "./tier";
    ```
    

---

## **Dekoratoren**

*Hinweis: Dekoratoren sind ein experimentelles Feature und erfordern die Aktivierung in der tsconfig.json.*

### **Klassendekorator**

```tsx
function versiegeln(constructor: Function) {
  Object.seal(constructor);
  Object.seal(constructor.prototype);
}

@versiegeln
class Greeter {
  greeting: string;
  constructor(message: string) {
    this.greeting = message;
  }
}
```

### **Methodendekorator**

```tsx
function enumerable(value: boolean) {
  return function (
    target: any,
    propertyKey: string,
    descriptor: PropertyDescriptor
  ) {
    descriptor.enumerable = value;
  };
}

class Beispiel {
  @enumerable(false)
  method() {
    // ...
  }
}
```

---

## **Asynchrone Programmierung**

TypeScript unterstützt die gleichen asynchronen Muster wie JavaScript, einschließlich Promises und async/await.

### **Async/Await**

```tsx
async function beispielAsync(): Promise<void> {
  const wert = await getPromiseWert();
  console.log(wert);
}
```

---

## **Fehlerbehandlung**

### **try...catch mit Typen**

```tsx
try {
  // Möglicherweise fehlerhafter Code
} catch (e) {
  console.error((e as Error).message);
}
```

---

## **Type Assertions**

### **"as"-Syntax**

```tsx
let someValue: any = "Dies ist ein String";
let strLength: number = (someValue as string).length;
```

### **Angle-Bracket-Syntax**

```tsx
let someValue: any = "Dies ist ein String";
let strLength: number = (<string>someValue).length;
```

---

## **Nützliche Befehle**

- **TypeScript Compiler (tsc)**
    
    Kompiliert TypeScript-Dateien zu JavaScript.
    
    ```bash
    tsc app.ts
    ```
    
- **tsconfig.json**
    
    Konfigurationsdatei für den Compiler. Erstellen Sie eine mit:
    
    ```bash
    tsc --init
    ```