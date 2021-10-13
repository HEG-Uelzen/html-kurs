---
layout: ../layouts/MarkdownLayout.astro
title: Die unterschiedlichen Elemente
description: Überblick über die unterschiedlichen HTML-Elemente

next: /03-mediale-inhalte
previous: /01-einfuehrung
---

Im [vorherigen Kapitel](/01-einfuehrung) haben sie bereites ein erstes inhaltsbeschreibendes HTML-Element kennengelernt: das `h1`-Element für Überschriften. HTML enthält eine Vielzahl an solchen Elementen, um unterschiedliche Inhalte wie Text, Bilder, Videos und vieles mehr strukturiert darstellen zu können. Eine Auswahl der wichtigsten Elemente wird im Folgenden vorgestellt.

## 📝 Text

### Absätze & Zeilenumbrüche

Um in HTML einen zusammenhängenden Textblock darzustellen, kann man das `<p>` (_paragraph_) Element verwenden. Möchte man an bestimmten Stellen für einen festen Zeilenumbruch sorgen, kann man dafür das alleinstehende(!) `<br/>`-Element (_break_) nutzen.

<details>
    <summary><strong>Beispiel:</strong></summary>
    <p>
        Der folgende Code zeigt die Anwendung der beiden erläuterten Elemente:
        <button class="copy-to-clipboard-button" type="button" data-copy-state="copy">
	<span>Copy</span>
</button>
        <pre><code class="language-html">
        &lt;!DOCTYPE html>
        &lt;html lang="de">
        &lt;head>
            &lt;meta charset="UTF-8" />
            &lt;meta http-equiv="X-UA-Compatible" content="IE=edge" />
            &lt;meta name="viewport" content="width=device-width, initial-scale=1.0" />
            &lt;title>Meine tolle Website&lt;/title>
        &lt;/head>
        &lt;body>
            &lt;p>
            Dies ist ein toller Absatz mit ganz viel Text drin. 
            Vielleicht ergibt er mehr Sinn, wenn sie ihn nochmal lesen.
            &lt;/p>
            &lt;p>
            Dies ist ein anderer cooler Absatz mit ganz viel Text drin. &lt;br />
            Das hier wird aufgrund des Zeilenumruchelementes in einer neuen Zeile angezeigt
            &lt;/p>
        &lt;/body>
        &lt;/html>
            </code></pre>
    </p>
    <img src="/images/02-die-unterschiedlichen-elemente/absaetze.png" alt="Screenshot des Beispiels für Absätze & Zeilenumbrüche" class="shadow" width="785" height="188" loading="lazy" />
</details>

### Überschriften

In HTML unterscheidet man zwischen mehreren Größenabstufungen: Es gibt Überschriften der 1., 2., 3., 4., 5. und 6. Ordnung. Das sogenannte `heading`-Element der ersten Überschrift wird als `<h1>HIER STEHT DIE ÜBERSCHRIFT</h1>` definiert. Die anderen Elemente unterscheiden sich in der Definition nur dahingehend, dass sie die Zahl ihrer Ordnung verweden:

<details>
    <summary><strong>Beispiel:</strong></summary>
    <p>
        Der folgende Code zeigt die Nutzung von Überschriften:
        <pre><code class="language-html">
        &lt;!DOCTYPE html>
        &lt;html lang="de">
        &lt;head>
            &lt;meta charset="UTF-8" />
            &lt;meta http-equiv="X-UA-Compatible" content="IE=edge" />
            &lt;meta name="viewport" content="width=device-width, initial-scale=1.0" />
            &lt;title>Meine tolle Website&lt;/title>
        &lt;/head>
        &lt;body>
            &lt;h1>Überschrift 1. Ordnung&lt;/h1>
            &lt;h2>Überschrift 2. Ordnung&lt;/h2>
            &lt;h3>Überschrift 3. Ordnung&lt;/h3>
            &lt;h4>Überschrift 4. Ordnung&lt;/h4>
            &lt;h5>Überschrift 5. Ordnung&lt;/h5>
            &lt;h6>Überschrift 6. Ordnung&lt;/h6>
        &lt;/body>
        &lt;/html>
            </code></pre>
    </p>
    <img src="/images/02-die-unterschiedlichen-elemente/heading.png" alt="Screenshot des Beispiels für Überschriften" class="shadow" width="720" height="288" loading="lazy" />
</details>

<article>
  <header><strong>Aufgabe 2:</strong></header>
  <p>
    Programmieren sie eine Webseite, die genau so wie der folgende Screenshot aussieht:
  </p>
  <img src="/images/aufgaben/aufgabe2.png" alt="Screenshot für Aufgabe 2" class="shadow" width="763" height="399" loading="lazy" />
</article>

### Sonstige Textformatierung

Text kann fett dargestellt werden, in dem er in einen `<b></b>` Tag eingbettet wird. Für kursiven Text sorgt der `<i></i>` Tag. Beide Elemente können kombiniert.

Mit den Elementen `<big></big>` und `<small></small>`kann Text größer oder kleiner dargestellt werden.

Mit dem `<sub></sub>` Element kann Text niedriggestellt werden. Mit dem `<sup></sup>` Element wird Text hochgestellt.

<article>
  <header><strong>Aufgabe 3:</strong></header>
  <p>
    Programmieren sie eine Webseite, die genau so wie der folgende Screenshot aussieht:
  </p>
  <img src="/images/aufgaben/aufgabe3.png" alt="Screenshot für Aufgabe 3" class="shadow" width="765" height="402" loading="lazy" />
</article>

## 🔗 Links

Das `<a></a>` Element (Anchor Element) wird zur Verlinkungen auf andere Seiten genutzt. Enthält immer den `href` Parameter, der die Adresse zu der verlinkten Seite enthält:

```html
<a href="https://google.de">Dieser Link führt auf google.de</a>
```

## 📑 Listen

### ⏺ Stichpunkte

Für Listen mit Stichpunkte wird in HTML das `<ul></ul>` Element verwendet (aus dem Englischen für _unordered list_). Jedes `<li></li>` Element (Listenelement) in dieser Liste wird mit einem Stichpunkt versehen.

### 🔢 Nummerierte Listen

Für Listen mit Stichpunkte wird in HTML das `<ol></ol>` Element verwendet (aus dem Englischen für _ordered list_). Jedes `<li></li>` Element (Listenelement) in dieser Liste wird mit einer durchgehenden Nummerierung versehen.

### 🧭 Navigation

In HTML gibt es außerdem das `<nav></nav>` Element, welches für Navigationen verwendet wird. In dieses wird oft eine _unordered list_ mit den Navigationselementen gepackt.

<details>
    <summary><strong>Beispiel:</strong></summary>
    <p>
        Der folgende Code zeigt die Nutzung von Listen:
        <pre><code class="language-html">
        &lt;!DOCTYPE html>
        &lt;html lang="de">
        &lt;head>
            &lt;meta charset="UTF-8" />
            &lt;meta http-equiv="X-UA-Compatible" content="IE=edge" />
            &lt;meta name="viewport" content="width=device-width, initial-scale=1.0" />
            &lt;title>Meine tolle Website&lt;/title>
        &lt;/head>
        &lt;body>
            &lt;ul>
              &lt;li>Stichpunkt&lt;/li>
              &lt;li>Noch ein Stichpunkt&lt;/li>
            &lt;/ul>
            &lt;ol>
              &lt;li>Erster Aufzählungspunkt&lt;/li>
              &lt;li>Ein weiterer Punkt&lt;/li>
            &lt;/ol>
        &lt;/body>
        &lt;/html>
            </code></pre>
    </p>
    <img src="/images/02-die-unterschiedlichen-elemente/listen.png" alt="Screenshot des Beispiels für Listen" class="shadow" width="720" height="128" loading="lazy" />
</details>

<article>
  <header><strong>Aufgabe 4:</strong></header>
  <p>
    Programmieren sie eine Webseite, die genau so wie der folgende Screenshot aussieht (Aussehen der Liste kann abweichen):
  </p>
  <img src="/images/aufgaben/aufgabe4.png" alt="Screenshot für Aufgabe 4" class="shadow" width="769" height="410" loading="lazy" />
</article>

## 📦 Container Elemente

Es gibt in HTML außerdem noch sogenannte Containerelemente, die lediglich den Zweck erfüllen, mehrere HTML-Elemente zusammenzufassen, was bei der Strukturierung sowie dem noch später erklärten visuellen Design einer Webseite unglaublich hilfreich sein kann. Hier wird oft das `<div></div>` Element verwendet, welches bei bloßer Benutzung keinen besonderen Effekt erzeugt, dennoch später oft dabei hilft, Websitecode in verständliche Abschnitte zu unterteilen.
