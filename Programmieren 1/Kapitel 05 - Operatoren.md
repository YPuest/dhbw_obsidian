#Programmieren #Operatoren

## Ausdrücke, Arten von Operatoren

>**Definition**
>Ein Ausdruck ist eine Folge von Operatoren und Operanden welche z.B. die Berechnung eines Wertes festlegt.

Wenn ein Ausdruck ausgewertet wird, liefert er als Ergebnis einen Wert (Resultat).
Mögliche Operanden sind z.B. Variablen und Konstanten.

### Arten von Operatoren
- [[Kapitel 05 - Operatoren#Arithmetische Operatoren|Arithmetische Operatoren]]
- [[Kapitel 05 - Operatoren#Inkrement- und Dekrement-Operatoren|Inkrement- und Dekrement-Operator]]
- [[Kapitel 05 - Operatoren#Vergleichsoperatoren|Vergleichsoperatoren]] 
- [[Kapitel 05 - Operatoren#Logische Operatoren|Logische Operatoren]] 
- [[Kapitel 05 - Operatoren#Bitlogische Operatoren|Bitlogische Operatoren]] 
- [[Kapitel 05 - Operatoren#Zuweisungsoperatoren|Zuweisungsoperatoren]]
- [[Kapitel 05 - Operatoren#Bedingungsoperator|Bedingungsoperator]]

## Kategorisierung von Operatoren
**Nach Anzahl der Operatoren**

| Anzahl der Operanden | Bezeichnung       | Bseispiel |
| -------------------- | ----------------- | --------- |
| 1                    | Unärer Operator   | i++       |
| 2                    | Binärer Operator  | a + b     |
| 3                    | Ternärer Operator | (a\==0) ? "Null" : "Nicht Null"          |

**Nach Priorität**
- hochste Priorität: 1
- niedrigste Priorität: 13

**Nach Assoziativität**
- rechts (von rechts nach links)
- links (links nach rechts)

## Typisierung von Operatoren

| Typ                             | Bezeichnung | Java-Datentypen                   |
| ------------------------------- | ----------- | --------------------------------- |
| Integraler Typ ("ganze Zahlen") | I           | byte, short, int, long, (char)    |
| Nummerischer Typ                | N           | I und float, double               |
| Logischer Typ                   | L           | boolean                           |
| Primitiver Typ                  | P           | N und L                           |
| Referenz                        | R           | Klassen und Arrays (inkl. String) |
| Alle Typen                      | A            |                                   |

## Arten von Operatoren
##### Arithmetische Operatoren

| Operator | Name                      | Priorität | Typisierung | Operanden | Assoziativität |
| -------- | ------------------------- | --------- | ----------- | --------- | -------------- |
| +        | Unäres Plus Vorzeichen    | 1         | N           | 1         | rechts         |
| -        | Unäres Minus Vorz.-Umkehr | 1         | N           | 1         | rechts         |
| +        | Addition                  | 3         | N, N        | 2         | links          |
| -        | Subtraktion               | 3         | N, N        | 2         | links          |
| *        | Multipliktation           | 2         | N, N        | 2         | links          |
| /        | Division                  | 2         | N, N        | 2         | links          |
| %        | Rest (Mudolo)             | 2         | N, N        | 2         | links               |

>Resultattyp: **N** (numerisch)

> Wenn beide Operanden ganzzahlig (d.h. von einem Ganzzahl-Datentyp) sind, ist auch das Resultat ganzzahlig; ansonsten ist das Resultat eine Gleitpunktzahl

**Beispiele:**
- 1 + 3 = 4
- 1 + 3.0 = 4.0
- 5 / 2 = 2
- 5.0 / 2 = 2.5

##### Inkrement- und Dekrement-Operatoren

| Operator | Name      | Priorität | Typisierung | Operanden | Assoziativität |
| -------- | --------- | --------- | ----------- | --------- | -------------- |
| ++       | Inkrement | 1         | N           | 1         | rechts         |
| --       | Dekrement | 1         | N           | 1         | rechts               |

>Resultattyp: **N** (numerisch)

>Der Operator kann vor oder nach dem Operand stehen (Präfixform/Postform)

**Beispiele:**
i++; *->* Wert wird erst nach ausgeführter Operation addiert
++i; *->* Wert wird vor der ausgeführten Operation addiert

**Code:**
``` Java
int i=0;  
int j=0;  
j = ++i;  // i=1, j=1
int k = j++ + ++i; //j=1, i=2
//j=2, i=2
```

##### Vergleichsoperatoren

| Operator | Name          | Priorität | Typisierung | Operanden | Assoziativität |
| -------- | ------------- | --------- | ----------- | --------- | -------------- |
| ==       | Gleichheit    | 6         | A, A        | 2         | links          |
| !=       | Ungleichheit  | 6         | A, A        | 2         | links          |
| <        | Kleiner       | 5         | N, N        | 2         | links          |
| <=       | Kleinergleich | 5         | N, N        | 2         | links          |
| >        | Größer        | 5         | N, N        | 2         | links          |
| >=       | Größergleich  | 5         | N, N        | 2         | links               |

> Resultattyp: **L** (boolean)

##### Logische Operatoren

| Operator | Name             | Priorität | Typisierung | Operanden | Assoziativität |
| -------- | ---------------- | --------- | ----------- | --------- | -------------- |
| !        | Nicht (Negation) | 1         | L           | 1         | rechts         |
| &        | Und              | 7         | L, L        | 2         | links          |
| &&       | Und verkürzt     | 10        | L, L        | 2         | links          |
| \|       | Oder             | 9         | L, L        | 2         | links          |
| \| \|     | Oder verkürzt    | 11        | L, L        | 2         | links          |
| ^        | Exklusives Oder  | 8         | L, L        | 2         | links               |

>Resultattyp: **L** (boolean) 

>**Merke:**
>Bei den verkürtzen Operatoren && und | | wird der 2. Operand nur dann ausgewertet, wenn das Ergebnis der Operation nicht schon nach dem 1. Operanden fest steht. 
> *Wichtig: auswirkungen auf z.B. i++*

##### Bitlogische Operatoren

| Operator | Name             | Priorität | Typisierung | Operanden | Assoziativität |
| -------- | ---------------- | --------- | ----------- | --------- | -------------- |
| ~        | Komplement       | 1         | I           | 1         | rechts         |
| &        | Bitw. Und        | 7         | I, I        | 2         | links          |
| \|       | Bitw. Oder       | 9         | I, I        | 2         | links          |
| ^        | Bitw. Exkl. Oder | 8         | I, I        | 2         | links               |

>Resultattyp: **I** (Integral)

**Beispiel:**
``` Java
byte a = 5;             //00000101
byte n = 66;            //01000010
byte c = (byte)(a|B);   //01000111
```

##### Zuweisungsoperatoren
>In Java ist eine Zuweisung, z.B. i = i + 1, auch ein Ausdruck ('Zuweisungsausdruck').

**Beispiele:**
- (i = 2) + (k = 3)      Wert des Ausdrucks: 5
- i = k = 1                 Entspricht i = (k = 1). Wert des Ausdrucks: 1
- i += 5                     Der Wert von i wird um 5 erhöht. Wert des Ausdrucks: erhöhter i-Wert


##### Bedingungsoperator

| Operator | Name               | Priorität | Typisierung | Operanden | Assoziativität |
| -------- | ------------------ | --------- | ----------- | --------- | -------------- |
| ?:       | Bedingungsoperator | 12        | L, A, A     | 3         | rechts               |

>Resultattyp: A (Alle Typen)

>Der **Bedingungsoperator** ist der einzige dreistellige Operator in Java. Der erste Operand (conditional_expression, ce) erwartet einen logischen Ausdruck, in dessen Abhängigkeit entweder der zweite (falls ce\==*true*) oder dritte Operand (falls ce\==*false*) zurückgeliefert wird.

**Syntax:**
``` Bash
conditional_expression ? expression1 : expression2
```

**Beispiele:**
``` Java
boolean b = true; 
System.out.println(b ? 1 : 2); // Ausgabe: "1"

int a = 3, b = 5, max; 
max = (a > b) ? a : b;
```


### Zusammenfassung: Priorität von Operatoren

| Operator                                           | Priorität | Assoziativität |
| -------------------------------------------------- | --------- | -------------- |
| ++, --, !, ~, (Typ), +, - (unäres Plus und Minus)  | 1         | rechts         |
| \*, /, %                                           | 2         | links          |
| +, -                                               | 3         | links          |
| <<, >>, >>>                                        | 4         |                |
| <, <=, >, >=, instanceoF                           | 5         | links          |
| \==, !=                                            | 6         | links          |
| &                                                  | 7         | links          |
| ^                                                  | 8         | links          |
| \|                                                 | 9         | links          |
| &&                                                 | 10        | links          |
| \|\|                                               | 11        | links          |
| ?:                                                 | 12        | rechts         |
| =, \*=, /=, %=, +=, -=, <<=, >>=, >>>=, &=, ^=,\|= | 13        | rechts               |


## Ausgabe

**Drei Streams**
- Standartausgabe: System.out
- Standartfehlerausgabe: System.err
- Standarteingabe: System.in

### Daten formatiert Ausgeben

>**Syntax:**
>printf

``` Java
System.out.printf( "Hello %s. Missed call from %s.\n", "Ulli", "Tanja" ); 

int i = 123; System.out.printf( "|%d| |%d|\n" , i, -i); // |123| |-123|

System.out.printf( "|%5d| |%5d|\n" , i, -i); // |  123| |  -123| 
System.out.printf( "|%-5d| |%-5d|\n" , i, -i); // |123  | |-123  | 

double d = 1234.5678;

System.out.printf( "|%10f| |%10f|\n" , d, -d); // |1234,567800| |-1234,567800| 
System.out.printf( "|%10.2f| |%10.2f|%n" , d, -d); // |   1234,57| |   -1234,57|
System.out.printf( "|%010.2f| |%010.2f|\n", d, -d); // |0001234,57| |-001234,57|
```


##### Überischt zur Formatierung mit *printf*

| Umwandlungszeichen | Argument-Kategorie | Ergebnis-String                     |
| ------------------ | ------------------ | ----------------------------------- |
| %d                 | Ganzzahl           | Dezimale Ganzzahl mit Vorzeichen    |
| %f                 | Gleitkommazahl     | Gleitkommazahl in Standart-Notation |
| %b                 | boolean            | *false* oder *true*                 |
| %c                 | Zeichen            | Unicode-Zeichen                     |
| %s                 | String             | String                              |
| %\%                |                    | Prozentzeichen                      |
| %n                 |                    | Neue Zeile                          |
| %t, %T             | date/time          | Datums-/Zeitangabe, s.Klasse java.util.Formatter                                    |


## Scanner

>Für den Zweck der Eingabe von primitiven Datentypen und Strings gibt es die Klasse java.util.Scanner.

**Beispiel:**
``` Java
java.util.Scanner scan = new java.util.Scanner(System.in); 
int i = scan.nextInt();
double d = scan.nextDouble();
String word = scan.next(); // nächster Token

System.out.print("Please enter an integer number: "); 
String input = scan.next(); // Einlesen als String 
int i = Integer.parseInt(input); // Konvertierung in in
```

