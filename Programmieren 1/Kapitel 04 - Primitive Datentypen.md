#Programmieren #Datentypen

## Java-Bezeichner
Für Variablen, Methoden, Klassen, Schnittstellen werden **Bezeichner** - auch *Identifizierer* genannt - vergeben.

- Folge von Zeichen
- muss mit Unicode-Buchstabe beginnen
- nach dem ersten Buchstaben auch Ziffern
- Groß- und Kleinschreibung wird unterschieden
- Leerzeichen verboten
- Reservierte Schlüsselwörter verboten

### Konventionen für Bezeichner
- Packages: Kleinschreibung mit Punkt (".")
- Klassen, Interfaces: UpperCamelCase
- Methoden: lowerCamelCase
- Variablen: lowerCamelCase
- Konstanten(static, final): UPPER_SNAKE_CASE 

### Anweisungen
>**Definition**
>Eine Anweisung (Statement) ist ein vom Programmierer erstellter Befehel zur Lösung einer Aufgabe

Ein Programm besteht aus einer Folge von Anweisung, welche in bestimmter Reihenfolge ausgeführt werden.

##### Syntax
Einfache Anweisung: **;**
Anweisugnsblock : **{}**

## Datentypen
### Primitive Datentypen
**Zahlen (nummerisch)**
- Ganzzahl-Datentypen
	- byte, short, int, long
- Gleitkommazahl-Datentypen
	- flaot, double

**Zeichen (alphabetisch)**
- Alphanummerischer Zeichen
	- char

**Boolesche (logische, Wahrheitswerte)**
- Repräsentation von Wahrheitswerten
	- true, false

#### Interne Darstellung von Zeichen
**Druckbare Zeichen**
- Groß- und Kleinschreibung, Ziffern, Sonderzeichen

**Steuerzeichen**
- Zeilenvorschub, horizontale Tabulator

##### Zeichen werden als Bitkombination codiert
- Java verwendet den Unicode (ASCII Teilmenge)
- Ein Zeichen sind zwei Bytes

##### Literale
> Im Quelltest verwendete Werte (z.B. Zahlen) werden als Literale bezeichnet

##### Escape-Sequenz
Steuerzeichen oder "richtige"Zeichen können per Escape-Sequenz übertragen werden

Wird durch \ eingeleitet.
**Beispiel:** $\backslash$b -> Tabulator, $\backslash$n line feed


## Variablen
> Definition
> Anweisungen eines Programms arbeiten mit Daten, die unterschiedliche Werte (variable Werte) annehmen können

Für die Variable wird der entsprechende Speicherplatz im Arbeitsspeicher reserviert

Zugriff auf den Speicherplatz über den Variablennamen (Bezeichner)

**Deklarieren**
int a;

**Initialisieren**
a = 12;

### Gültigkeitsbereiche lokaler Variablen
>**Definition**
>Variablen, die innerhalb eines Anweisungsblocks (z.B. Methode) deklariert werden, heißen **lokale Variablen**.

- sind nur innerhalb des deklarierten Blocks gültig
- eine lokale Variable verliert ihre Gültigkeit mit der schließenden Klammer **}**

##### Syntax
``` bash
type identifier [= init_value] {, identifier[= init_value]}
```

**Beispiel:** 
``` Java
int a = 3, int b = 4, c, d = 9;
```


### Typkompatibilität und Typkonversion
##### Typkompatibilität
Einer Variable kann nur ein Wert eines Datentyps zugewiesen werden, den sie selbst besitzt oder den sie aufgrund ihres Wertebereiches umfasst.

**Beispiel:** *int* ist kompatibel zu *double*, aber *double* nicht zu *int*

##### Typkonversion
Bei kompatiblen Typen führt Java automatisch eine implizite Typkonversion durch. Ansonsten kann eine explizite  Typkonversion *(cast)* durchgeführt werden.
	boolean kann nicht umgewandelt werden

``` Java
(type) expression
int number = (int)1.23
```

### Symbolische Konstanten - unveränderliche Variablen
>Definition
>Sobald während der Programmausführung eine Wertzuweisung erfolgt ist, ist diese endgültig *(final)*. Es kann keine zweite Wertzuweisung an eine Konstante erfolgen nachdem sie einen Wert erhalten hat (auch in Zuweisung möglich).

**Beispiel:**
``` Java
final double MWST = 0.19;
final double PI;
PI = 3.141592
```


==**ANHANG**== selber angucken