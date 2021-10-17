---
layout: ../layouts/MarkdownLayout.astro
title: Mediale Inhalte
description: Überblick über die unterschiedlichen HTML-Elemente, mit denen man mediale Inhalte in eine Webseite einbetten kann

next: /04-css
previous: /02-die-unterschiedlichen-elemente
---

Im [vorherigen Kapitel](/02-die-unterschiedlichen-elemente) haben sie bereits die grundlegenden HTML-Elemente zum Beschreiben von Inhalt (primär Text) kennengelernt. Nun widmen wir uns dem Einbinden von medialen Inhalten in eine HTML-Webseite.

## 🖼️ Bilder

Bilder können mit dem `<img />` Element (_image_) in eine Webseite eingebunden werden. Dabei sollten dem Element mindestens die beiden folgende Parameter mitgegeben werden:

- `src` - Dieser Parameter gibt die Adresse (entweder aus dem Internet oder Dateienverzeichnis) des Bildes an
- `alt` - Dieser Parameter legt den Alternativtext fest den Nutzerinnen und Nutzer angezeigt bekommen, wenn das Bild (noch) nicht geladen wurde

Damit sieht ein einfaches Bildelement wie folgt aus:

```html
<img src="https://picsum.photos/300/200" alt="Ein zufälliges Bild" />
```

Außerdem kann man die Performance seiner Bilder verbessern, wenn man folgende Parameter zusätzlich mit angibt:

- `width` und `height` - Diese beiden Parameter geben die Länge und Breite des Bildes an. Somit weiß der Browser, wieviel visuellen Platz das Bild nach dem Ladeprozess einnimmt und hält diesen frei.
- `loading="lazy"` - Dieser Parameter sorgt für ein sogenanntes _Lazyloading_ des Bildes. Damit wird das Bild von den meisten Webbrowsern erst geladen, wenn der User zu dem Bereich der Seite gescrollt hst, auf dem sich das Bild befindet (dies verbessert die Performance, da Bilder so erst geladen werden, wenn sie wirklich gebraucht werden)

Damit sieht das erweiterte Bildelement wie folgt aus:

```html
<img
  src="https://picsum.photos/300/200"
  alt="Ein zufälliges Bild"
  width="300"
  height="200"
  loading="lazy"
/>
```

<small>Die Bilder der gezeigten HTML-Elemente stammen von <a href="https://picsum.photos/" target="_blank" rel="noopener">Lorem Picsum</a>, einem Dienst, von dem man kostenlos zufällige Bilder anzeigen lassen kann</small>

<article>
  <header><strong>Übung:</strong></header>
  <p>
    Probiere das Bildelement selbst aus, versuche auch die Adresse des Bildes abzuändern, sodass ein selbst ausgewähltes Bild angezeigt wird (Frei verwendbare Bilder sind beispielsweise auf <a href="https://unsplash.com" target="_blank" rel="noopener">Unsplash</a> verfügbar)
  </p>
</article>

### Bilder mit Bildunterschrift

Für Bilder mit Bildunterschriften gibt es das `<figure></figure>` Element. Dieses enthält das Bild (wie gewohnt mit dem `<img></img>` Tag repräsentiert) sowie das sogenannte `<figcaption></figcaption>` Element, in dem die Bildunterschrift steht:

```html
<figure>
  <img
    src="https://picsum.photos/300/200"
    alt="Ein zufälliges Bild"
    width="300"
    height="200"
    loading="lazy"
  />
  <figcaption>
    Zu sehen ist ein zufälliges Bild mit der Größe 300x200
  </figcaption>
</figure>
```

<div style="width: 100%;">
  <figure>
  <img src="/images/03-mediale-inhalte/figcaption.png" alt="Screenshot des Beispiels für das Figcaption-Element" class="shadow" width="480" height="256" loading="lazy" />
  <figcaption>3.1 Ein Beispiel für das <code>figcaption</code> Element</figcaption>
  </figure>
</div>

## 🎵 Audiodateien

Um Audiodateien in die Webseite einzubinden, kann man das `<audio></audio>` Element. Dieses enthält ferner folgende Inhalte:

- den Parameter `controls`, damit Elemente zum Starten/Stoppen der Audiodatei angezeigt werden
- ein `<source></source>` Element, welches den Pfad/die Adresse zu der Audiodatei sowie deren Kodierung (Format) enthält
- Einen Text, der angzeigt wird, falls der Browser das Element nicht darstellen kann.

```html
<audio controls>
  <source src="./audio/sound.mp3" type="audio/mpeg" />
  The browser isn't supporting this audio element.
</audio>
```

<small>Dieses Audioelement zeigt eine mp3-Datei namens `sound.mp3` an, die sich in einem Ordner namens `audio` befindet, der neben der entsprechenden HTML-Datei plaziert ist.</small>

## 🎞️ Videos

Die Vorgehensweise um Videos in HTML anzuzeigen, ist ähnlich der von Audiodateien: Auch hier werden `controls` und `<source></source>` Element angegeben. Außerdem sollte das `<video></video>` Element einen `width` Parameter enthalten (wie das [Bildelement](#️-bilder)):

```html
<video controls width="480">
  <source src="./video/video.mp4" type="video/mp4" />
  The browser isn't supporting this video element.
</video>
```

<small>Dieses Videoelement zeigt eine mp4-Datei namens `video.mp4` an, die sich in einem Ordner namens `video` befindet, der neben der entsprechenden HTML-Datei plaziert ist.</small>

## Das `iframe`-Element

Das `<iframe></iframe>` Element ist ein besonderes Element: Es kann genutzt werden, um (beliebige) Inhalte anderer Websites einzubinden: So bietet beispielsweise YouTube die Einbindung von Videos der Plattform mithilfe des `iframe` Elements an. Aber auch andere Dienste (speziell die, die mediale Inhalte offerieren), bieten die Einbindung mit iframes an (wie z.B. [Giphy](https://giphy.com/)).
