# Computercraft Lua Programmierung

[Tutorials - ComputerCraft Wiki](https://www.computercraft.info/wiki/Tutorials)
![mindmap.jpg](https://res.craft.do/user/full/159935f9-5e4d-0afb-2c79-97ce3d2d9945/doc/63d4fe2e-a399-49c6-9889-0d6d3b3f8cff/2c86a1e3-d9e3-42fb-9394-3d23a05b00f6)

## Hello World

   Um "Hello World!" in Computercraft auszugeben, verwende einfach den Befehl `print("Hello World!")`.

## Variablen

   Variablen in Computercraft können mit dem Zuweisungsoperator `=` erstellt werden.

   Zum Beispiel: `local name = "Alex"`.

## If, Then, Else

   Die Verwendung von Bedingungen in Computercraft erfolgt mit `if`, `then` und optional `else`. Beispiel:

```lua
if energyLevel > 50 then
  print("Energy level is high")
else
  print("Energy level is low")
end
```

## function

   Funktionen in Computercraft werden mit dem Schlüsselwort `function` definiert. Beispiel:

```lua
function greetPlayer(name)
  print("Hello, " .. name)
end
```

## Schleifen

Schleifen wie `for` und `while` können in Computercraft verwendet werden, um wiederholte Aktionen auszuführen.

### **for**

   Die for-Schleife in Computercraft ermöglicht es, eine Anweisungssequenz eine bestimmte Anzahl von Malen zu wiederholen. Die allgemeine Syntax für die for-Schleife ist:

```lua
for i = 1, 5 do
  print(i)
end
```

   In diesem Beispiel wird die Anweisung `print(i)` fünfmal ausgeführt, wobei `i` von 1 bis 5 inkrementiert wird. Die for-Schleife kann auch über Elemente einer Tabelle iterieren:

```lua
local fruits = {"apple", "banana", "orange"}
for key, value in pairs(fruits) do
  print(value)
end
```

   Hier wird die for-Schleife verwendet, um jedes Element der Tabelle `fruits` zu durchlaufen und den Wert auszugeben.

### **while**

   Die while-Schleife in Computercraft führt eine Anweisungssequenz aus, solange eine Bedingung wahr ist.

   Die allgemeine Syntax für die while-Schleife ist:

```lua
local count = 1
while count <= 5 do
  print(count)
  count = count + 1
end
```

   In diesem Beispiel wird die Anweisung `print(count)` ausgeführt, solange `count` kleiner oder gleich 5 ist. Die while-Schleife wird solange wiederholt, bis die Bedingung nicht mehr erfüllt ist.

## Table

   Tabellen in Computercraft sind äußerst vielseitig und ermöglichen die Speicherung und Organisation von Daten in einer Liste. Hier sind einige grundlegende Konzepte und Anwendungen von Tabellen in Computercraft:

### Tabellen erstellen

   Tabellen können in Computercraft mit geschweiften Klammern `{}` erstellt werden. Zum Beispiel:

```lua
local fruits = {"apple", "banana", "orange"}
```

   In diesem Beispiel wird die Tabelle `fruits` erstellt und mit den Elementen "apple", "banana" und "orange" initialisiert.

### Auf Elemente in einer Tabelle zugreifen

   Der Zugriff auf Elemente in einer Tabelle erfolgt über den Index des Elements. In Lua (der Sprache von Computercraft) beginnt der Index bei 1. Zum Beispiel:

```lua
print(fruits[2]) -- Gibt "banana" aus
```

### Tabellen durchlaufen

   Tabellen können mithilfe von Schleifen wie der for-Schleife durchlaufen werden, um auf ihre Elemente zuzugreifen. Zum Beispiel:

```lua
for key, value in pairs(fruits) do
  print(value)
end
```

   Die `pairs`-Funktion ermöglicht es, über die Elemente der Tabelle zu iterieren und sowohl den Index als auch den Wert jedes Elements abzurufen.

### Tabellen als assoziative Arrays

   Tabellen in Lua können auch als assoziative Arrays verwendet werden, was bedeutet, dass sie nicht nur numerische Indizes haben müssen. Zum Beispiel:

```lua
local person = {name="John", age=30, city="New York"}
print(person["age"]) -- Gibt 30 aus
```

   In diesem Beispiel wird die Tabelle `person` als assoziatives Array verwendet, wobei die Schlüssel "name", "age" und "city" verwendet werden, um auf die entsprechenden Werte zuzugreifen.

   Tabellen sind ein leistungsstarkes Konzept in Computercraft und ermöglichen die effiziente Verwaltung von Daten in Form von Listen, assoziativen Arrays und vielem mehr.

## Klassen

   In Computercraft können Klassen mithilfe von Tabellen und Metatables simuliert werden, um objektorientierte Programmierung zu unterstützen.

   In Computercraft gibt es keine direkte Unterstützung für Klassen im herkömmlichen Sinne wie in objektorientierten Sprachen. Allerdings können Klassenähnliche Strukturen mithilfe von Tabellen und Metatables simuliert werden, um objektorientierte Konzepte zu unterstützen. Hier ist eine Anleitung, wie man Klassenähnliche Strukturen in Computercraft erstellen kann:

### Klassenähnliche Strukturen mit Tabellen und Metatables

In Lua, der Sprache von Computercraft, können Klassenähnliche Strukturen mithilfe von Tabellen und Metatables erstellt werden. Eine Metatable ist eine Tabelle, die das Verhalten von anderen Tabellen ändern kann, ähnlich wie Klassen in objektorientierten Sprachen.

#### Schritt 1: Definieren der Klasse

Erstelle eine Tabelle, die die Eigenschaften und Methoden der "Klasse" enthält. Zum Beispiel:

```lua
local Animal = {
  name = "",
  sound = "",
  makeSound = function(self)
    print(self.sound)
  end
}
```

#### Schritt 2: Erstellen von Instanzen

Erstelle Instanzen der "Klasse", indem du neue Tabellen erstellst und die Metatable der "Klasse" zuweist. Zum Beispiel:

```lua
local cat = {name = "Whiskers", sound = "Meow"}
setmetatable(cat, {__index = Animal})
```

#### Schritt 3: Verwendung von Instanzen

Verwende die erstellten Instanzen, um auf ihre Eigenschaften und Methoden zuzugreifen. Zum Beispiel:

```lua
print(cat.name) -- Gibt "Whiskers" aus
cat:makeSound() -- Gibt "Meow" aus
```

Durch die Verwendung von Metatables und Tabellen können Klassenähnliche Strukturen in Computercraft simuliert werden, um objektorientierte Konzepte wie Vererbung und Methodenaufrufe zu unterstützen. Obwohl dies nicht die herkömmliche Klassenimplementierung ist, ermöglicht es dennoch die Organisation von Daten und Verhalten in einer strukturierten und wieder verwendbaren Weise.

?descriptionFromFileType=function+toLocaleUpperCase()+{+[native+code]+}+File&mimeType=application/octet-stream&fileName=Computercraft+Lua+Programmierung.md&fileType=undefined&fileExtension=md
