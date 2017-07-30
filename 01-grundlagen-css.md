# CSS – Cooler Look für die Seite
## Was ist CSS?
CSS bedeutet Cascading Style Sheet und damit kannst du deine Webseite, die du mit Hilfe der SushiCard HTML erstellt hast noch etwas schöner gestalten. CSS sind sozusagen Formatvorlagen für deine Seite, die du für jede Seite individuell anlegen kannst. Dadurch sieht jede Seite anders aus.

Du findest bestimmt auch, dass die Webseite, wie sie jetzt aussieht nicht besonders cool und interessant wirkt. Es wäre bestimmt super, wenn man die Farben ändern könnte oder  die Schriftgrößen. Dir fallen bestimmt noch ganz viele andere Dinge ein, die du auf der Seite verändern möchtest.

Aber fangen wir erst mal damit an, wie man CSS in deine HTML-Seite einbindet, damit die Webseite die Angaben überhaupt übernehmen kann.

## Wie kommt das CSS in meine HTML-Datei?
In deiner HTML-Datei gibt es verschiedene Tags. Das ist z.B. die Überschrift, die als `<h1></h1>` gekennzeichnet sind. Diese  Angaben in den spitzen Klammern nennt man Tag. Jedes Tag lässt sich mit CSS ansprechen und somit verändern.

### Mit dem Attribut „style“
Direkt im HTML-Tag kann man mit dem Attribut **style** eine CSS-Angabe eingeben, welche die Überschrift rot erscheinen lässt. Ein Attribut ist eine Art Eigenschaft, die man den HTML-Tags mitgeben kann um die Webseite zu verändern.

Versuche doch selbst einmal die Überschrift in deiner Webseite rot zu färben. Mit folgenden Code wurde die `<h1></h1>`-Überschrift rot eingefärbt.

```html
<h1 style=“color: red“>Meine Überschrift</h1>
// red heißt rot auf Englisch
```

Nun schau dir die Webseite im Browser an. Vergiss nicht zu speichern. Wenn du alles richtig gemacht hast, dann ist die Überschrift jetzt rot.

### Eingebettete Stylesheets
Eine weitere Möglichkeit die CSS-Angaben mit dem HTML zu verbinden, ist die Angabe im Head-Bereich der Webseite. Der Head-Bereich ist alles zwischen den beiden head-Tags `<head></head>`. Hier kann man folgenden Code eintippen:

```html
<head>
  <style type=“text/css“>
    h1 {
     color: red;
    }
  </style>
...  
</head>
```

Lösche jetzt die Anweisung style=“color:red“ weiter unten im `<h1></h1>`-Tag, es sollte dann so aussehen.

```html
<h1 style=“color: red“>Meine Überschrift</h1>
```

Speichere die Datei ab und schau dir die Webseite im Browser an. Wenn du alles richtig gemacht hast, dann ist die Überschrift immer noch rot.

### Externe Stylesheets
Diese beiden Möglichkeiten CSS-Anweisungen in eine HTML-Seite einzubinden sind nur für sehr kurze CSS-Anweisungen geeignet. Viel professioneller und auch nicht schwieriger sind externe Stylesheet-Dateien. Hier werden alle CSS-Anweisungen in eine Datei geschrieben. Das ist erstens übersichtlicher und zweitens lassen sich so gleiche CSS-Anweisungen für mehrere Webseiten verwenden, ohne dass man die Anweisungen in jede HTML-Seite eintippen muss.

Natürlich versuchen wir das nun auch bei deiner Webseite wie die Profis zu machen.

Dazu legst du im Editor eine neue Datei an und speicherst diese unter **styles.css** im gleichen Verzeichnis wie deine HTML-Datei.

TODO: (Screenshot Datei anlegen)

In dieser Datei tippst du nun folgende Anweisung ein:

```css
h1 {
  color: red;
}
```

Abspeichern nicht vergessen.

Dann müssen wir die CSS-Datei noch in die HTML-Datei einfügen. Dazu tippst du folgende Zeile in deine HTML-Datei:

```html
<head>
  <link rel=“stylesheet“ type=“text/css“ href=“styles.css“ />
  <style type=“text/css“>
    h1 {
     color: red;
    }
  </style>
...  
</head>
```

Jetzt kannst du die CSS-Anweisungen, die wir vorhin eingetippt haben wieder löschen, denn die steht ja jetzt in der css-Datei. Im `<head></head>`-Tag steht dann noch folgendes:

```html
<head>
  <link rel=“stylesheet“ type=“text/css“ href=“styles.css“ />
...  
</head>
```

Speichern nicht vergessen! Wenn du alles richtig gemacht hast und du dir die Seite im Browser ansiehst, sollte die Überschrift immer noch rot sein.

## Verschiedene styles
Es gibt natürlich viele verschiedene Eigenschaften, die ein Text haben kann. Wir können z.B. auch die Textgröße ändern. Du hast z.B. das Tag `<p>` für Absätze in deiner HTML-Datei. Wir wollen die Schrift in diesen Absätzen etwas größer machen.

Dazu brauchen wir die CSS-Anweisung **font-size**.

Gib folgende Anweisung in deine CSS-Datei ein:

```css
p {
  font-size: 16px;
}
```

Der Wert **16px** ist die Größenangabe für die Schrift und px ist dabei die Maßeinheit. Speicher deine CSS-Datei ab und schau dir die HTML-Datei im Browser an.

### Weitere Textformate
Wie wäre es mit einer anderen Schriftstärke. Diese können wir mit **font-weight** festlegen.
Ergänze folgendes in deiner CSS-Datei:

```css
p {
  font-size: 16px;
  font-weight: bold;
}
```

Abspeichern und im Browser die Webseite anschauen. Nun müssten alle Absätze fett erscheinen. Hier eine kleine Liste von möglichen Textformaten:

* font-weigth: Schriftstärke ändern (siehe oben)
  Mögliche Werte: lighter, light, normal, bold, bolder
* font-family: Schriftart ändern
  Mögliche Werte: alle Schriften, die auf dem Computer installiert sind
```css
p{
font-family: Verdana, arial;
}
```
* font-style: Schriftstil ändern
  mögliche Werte: italic, oblique, normal
```css
p {
font-style: italic;
}
```
* text-decoration: einen Text dekorieren, z.B unterstreichen
    mögliche Werte: underline, overline, line-through, none
```css
p {
text-decoration: underline;
}
```

Damit lässt sich schon einiges gestalten. Probier es einfach mal aus und tippe verschiedene Textformate in deine CSS-Datei ein. Schau dir die Ergebnisse im Browser an.

## Klassen bilden
Mit den Tags und den CSS-Angaben kannst du in deiner Webseite schon ziemlich viel verändern und formatieren.
Aber wenn du eine CSS-Anweisung z.B für den Absatz p einfügst, dann hast du sicherlich bemerkt, dass dann alle Absätze p diese Formatierungen übernehmen. Aber wie kann man nur einen speziellen Absatz z.B. fett gestalten oder mit einer anderen Farbe einfärben?

Dafür brauchen wir Klassen. Mit Klasse ist keine Schulklasse gemeint, sondern mit einer CSS-Klasse kannst du eine Formatierung, die du einmal erstellt hast für mehrere Tags verwenden, indem du in diesem Tag diese Klasse angibst. Der englische Begriff dafür ist **class**.

Ein Klassennamen wird gebildet, indem man sich einen passenden Namen für die Klasse ausdenkt und diesen mit einem Punkt davor in der CSS-Datei angibt. In der HTML-Datei müssen wir dann die Klasse im jeweiligen Tag einfügen.

In deiner HTML-Datei färben wir so nun die Schrift in einem Absatz grün. Folgendes musst du dazu ergänzen:

```html
<p class=“gruen“>
 Hier steht dein Text, der grün werden soll.

 Es kann auch eine Leerzeile drin sein.
</p>
```

In der CSS-Datei brauchen wir nun die entsprechende Klassen-Definition:

```css
.gruen {
 color: green;
}
```

Schau dir das Ergebnis im Browser an. Natürlich speichern nicht vergessen.
TODO: (Screenshot Browser)

Mit den Klassen hast du also die Möglichkeit in jedem gewünschten Tag die Schrift oder Farbe oder beides zu verändern. Du musst nur die Klasse in dem Tag angeben.

## Noch mehr CSS-Angaben
Es gibt natürlich noch ganz viele CSS-Eigenschaften, die man in seiner Webseite verwenden kann. Z.B. möchtest du vielleicht die Abstände zwischen zwei Absätzen ändern oder den Text einrücken.

Dafür gibt es folgende CSS-Anweisungen:
* margin: Außenabstände
* padding: Innenabstände

Man kann den Abstand rundherum mit dem gleichen Wert ändern oder jede Seite extra (also oben, rechts, unten, links):
* margin-top, margin-right, margin-bottom, margin-left
* padding-top, padding-right, padding-bottom, padding-left

Ergänze folgende Anweisung in deiner CSS-Datei:

```css
.gruen {
color: green;
padding-left: 20px;
margin-top: 50px;
}
```

Abspeichern und dann schau dir das Ergebnis im Browser an.

Wenn alles richtig ist, dann ist der Absatz mit grüner Schrift links weiter eingerückt und hat oben einen größeren Abstand.
In deiner Webseite befinden sich noch andere Tags, wie z.B. die Liste `<ul>`. Diese lässt sich auch einrücken, damit deutlich wird, dass es sich um eine Liste handelt.

Ergänze folgende CSS-Angabe in deiner CSS-Datei:

```css
ul {
padding-left: 30px;
}
```

Wenn du abspeicherst und die HTML-Seite im Browser ansiehst, kannst du sehen, dass die Liste nun links weiter eingerückt ist.
Mit diesem Grundwissen kannst du nun schon einiges schöner gestalten in deiner Webseite.

Probier es einfach aus. Bei Fragen kannst du dich jederzeit an die Mentoren wenden.
Wie wäre es mit einer eigenen kleinen Webseite?
Viel Spaß dabei!
