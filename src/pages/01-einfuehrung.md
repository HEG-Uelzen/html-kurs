---
layout: ../layouts/MarkdownLayout.astro
title: Einführung
description: Einführung in das Thema 'Webentwicklung mit HTML'

next: /02-die-unterschiedlichen-elemente
previous: /01-einfuehrung
---

HTML (Abkürzung **H**yper**t**ext **M**arkup **L**anguage) ist der Sprach&shy;syntax für die Struktur&shy;ierung von Web&shy;seiten: Schon seit der Er&shy;findung des WWW (World Wide Web) durch Tim-Berners Lee ist HTML für die visuelle Anzeige von Web&shy;seiten verantwort&shy;lich, inzwischen liegt die Ausszeichnungs&shy;sprache seit 2014 in der 5. Version (HTML5) vor.

## 🚀 Die erste Webseite

Der Start mit HTML ist relativ simpel. Erstellen sie einfach in einen Text&shy;editor ihrer Wahl (für den Einstieg ist [Atom](https://atom.io/) empfehlens&shy;wert) eine Datei mit folgendem Inhalt:

```html
<!DOCTYPE html>
<html lang="de">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Meine tolle Website</title>
  </head>
  <body>
    <h1>Hallo Welt!</h1>
  </body>
</html>
```

Speichern sie diese Datei nun unter einem beliebigen Namen (aber mit der Endung `.html`) ab. Suchen sie die Datei nun über ihren Datei&shy;explorer, und öffnen sie diese mit einem Doppel&shy;klick in ihrem Browser:

<figure>
<img src="/images/01-einfuehrung/hallo-welt.png" alt="Die erste Webseite" class="shadow" />
<figcaption>1.1 Die erste Webseite im Browser (Google Chrome auf macOS 11)</figcaption>
</figure>

### 🦴 Das Skelett einer Webseite

Eine HTML-Webseitebesteht aus verschiedenen (teils ineinander verschachtelten) Elementen. Ein Element wird wird mit folgend&shy;er Syntax definiert:

```html
<ELEMENTBEZEICHNUNG>
  Hier kommt der vom Element deklarierte Inhalt hin (bei einigen Elementen aber
  nicht)
</ELEMENTBEZEICHNUNG>
```

Bei erneuter Betrachtung der HTML-Datei erkennt man einzelne Elemente aus der Browser wieder:

- Der Text des `<title>`-Elements im `<head>`-Bereich taucht in der Navigationsleiste des Browsers auf
- Der Text des `h1`-Elements aus dem `<body>`-Bereich ist als Überschrift auf unserer Webseite erkennbar

Anhand dieser Beispiele kann man gut die Grundstruktur einer Webseite erklären:
Diese wird zunächst von einem `<html>`-Element (mit HTML-versionsspezifischen Prefix) umschlossen, welches auch die Sprache des angebotenen Inhaltes enthält (`de` ➡️ Deutsch):

```html
<!DOCTYPE html>
<html lang="de">
  <!--Die Webseite wird genau hier programmiert!-->
</html>
```

#### 🧍 Kopf & Körper

Der Inhalt des `<html>`-Elements lässt sich in zwei Bereiche aufteilen: das `<head>`-Element und das `<body>`-Element. Dabei wird das `<head>`-Element für die Definierung von Metadaten der Webseite genutzt (Wie dem Tableistentitel [`<title>`-Element]), während das `<body>`-Element die Anzeige des eigentlichen Inhalts der Webseite übernimmt (in unserem Fall die Über&shy;schrift [`h1`-Element]):

```html
<!DOCTYPE html>
<html lang="de">
  <head>
    <!--Kopfelement der Webseite-->
  </head>
  <body>
    <!--Korpus der Webseite-->
  </body>
</html>
```

<article>
  <header><strong>Aufgabe 1:</strong></header>
  <p>
    Änderen sie die bereits entwickelte Webseite so ab, dass diese als Ausgabesprache Englisch verwendet. Veränderen sie sowohl den Inhalt als auch die Metadaten.
  </p>
</article>
