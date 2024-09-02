<!--

author: Gregor Große-Bölting
email:  ggb@informatik.uni-kiel.de
version: 0.1
language: en
narrator: UK English Female

-->

# LiaScript Workflow-Workshop

![Workflow - Symboldbild](img/alvaro-reyes-qWwpHwip31M-unsplash.jpg "Foto von <a href="https://unsplash.com/de/@alvarordesign?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Alvaro Reyes</a> auf <a href="https://unsplash.com/de/fotos/person-die-an-bord-an-blauem-und-weissem-papier-arbeitet-qWwpHwip31M?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Unsplash</a>")

## Grundlagen: Markdown

> Markdown is intended to be as easy-to-read and easy-to-write as is feasible.
> 
> Readability, however, is emphasized above all else. A Markdown-formatted document should be publishable as-is, as plain text, without looking like it’s been marked up with tags or formatting instructions. While Markdown’s syntax has been influenced by several existing text-to-HTML filters — including Setext, atx, Textile, reStructuredText, Grutatext, and EtText — the single biggest source of inspiration for Markdown’s syntax is the format of plain text email.
> 
> To this end, Markdown’s syntax is comprised entirely of punctuation characters, which punctuation characters have been carefully chosen so as to look like what they mean. E.g., asterisks around a word actually look like \*emphasis\*. Markdown lists look like, well, lists. Even blockquotes look like quoted passages of text, assuming you’ve ever used email.
>
> -- https://daringfireball.net/projects/markdown/syntax

### "Standard" Markdown

Der [ursprüngliche Markdown-Standard](https://daringfireball.net/projects/markdown/syntax) umfasst nur wenige Elemente: Überschriften, Aufzählungen, Zitate, Code (Blocks), horizontale Linien, Links, Fett- und Kursivschreibweise, Bilder, sowie die Möglichkeit Syntax-Elemente zu *escapen* (mit einem \\). 

Verschiedene *Anbieter* haben diesen ursprünglichen Standard um eigene Elemente erweitert. Mit am bekanntesten ist vermutlich die [Github-Variante](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) von Markdown. 

### LiaScript-Markdown

LiaScript stellt weitere Markdown-Syntax zur Verfügung, die insbesondere auf die Verwendung im Bereich der Erstellung von OER ausgelegt ist, d.h. bspw. Elemente für Quizze, Multimedia, etc.

Diese *neue* Syntax wird häufig nicht von anderen Markdown-Interpretern unterstüzt und entsprechend falsch, anders oder gar nicht dargestellt.

### Tabellen

Tabellen sind im ursprünglichen Markdown-Standard nicht vorgesehen und notorisch anstrengend in Markdown zu erstellen. Es gibt aber hilfreiche Tools, die bei der Erstellung unterstützen, bspw. https://www.tablesgenerator.com/markdown_tables

Auch weitere Aufgaben lassen sich so automatisieren; häufig ist eine Lösung nur eine Google-Suche weit entfernt...

## Editieren: VS Code (oder Atom)

Für das (insbesondere lokale) Editieren von Markdown-Dateien ist ein *Plain Text*-Editor notwendig, wie bspw. [Visual Studio Code (VS Code)](https://code.visualstudio.com/), das als Open Source-Software entwickelt wird und kostenlos installierbar ist.

Für VS Code gibt es zwei Extensions, die die Arbeit mit LiaScript deutlich vereinfachen:

* [LiaScript Preview](https://marketplace.visualstudio.com/items?itemName=LiaScript.liascript-preview) bietet eine Vorschau der Markdown-Dokumente als LiaScript-Kurse. Die Vorschau kann gestartet werden, in dem man in VS Code *Strg* + *Umschalt* + *p* drückt und anschließend *LiaScript Preview ...* eintippt. 
* [LiaScript Snippets](https://marketplace.visualstudio.com/items?itemName=LiaScript.liascript-snippets) stellt verschiedene Markdown-Snippets zur Verfügung und ermöglicht bspw. auch die schnelle Generierung von Tabellen. Nach der Installation der Extension ist eine weitere Konfiguration notwendig, s. Link.

Extensions können in VS Code selbst gesucht und installiert werden:

1. Extensions-Tab auswählen:

![Extensions Tab](img/vs_code_extensions1.png)

2. Extensions suchen und installieren klicken.

![Extensions Tab, jetzt ausgewählt](img/vs_code_extensions2.png)

## Zusammenarbeiten

Hier wird's interessant... 

### CAU Cloud

![Boromir weiß Bescheid!](img/8smnql.jpg)

Niemals (niemals, nie) sollten LiaScript-Markdown Dateien über den Cloud-Editor der CAU Cloud geöffnet werden: Der Editor fügt schon durch das bloße Öffnen unerwünschte Sonderzeichen ein, die die Dokumente (insbesondere Tabellen und Quizze) zerstören. 

Die CAU Cloud bzw. OwnCloud stellt einen Desktop-Client zur Verfügung, der die Dateien und Verzeichnisse auf den lokalen Rechner synchronisiert. Dadurch ist eine gute Zusammenarbeit möglich. Nähere Informationen dazu gibt es hier: https://www.rz.uni-kiel.de/de/angebote/storage/cau-cloud

### git und Github

Noch eine bessere Möglichkeit der Zusammenarbeit bieten git und Github. 

VS Code bietet von Hause aus die Möglichkeit eigene Projekte mit git zu verwalten. Dafür ist die vorherige Installation eines [git Clients](https://git-scm.com/downloads) nötig. 

Für Details ist die VS Code-Hilfe zu dem Thema zu empfehlen: https://code.visualstudio.com/docs/sourcecontrol/overview Daraus ist auch das folgende Video...

<iframe width="560" height="315" src="https://www.youtube.com/embed/i_23KUAEtUM?si=pidcuGkhajN4JEsu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Publizieren

Wie kann ich meinen schönen Kurs nun anderen zur Verfügung stellen, bspw. Studierenden? Diese Frage ist derzeit leider noch nicht so einfach zu beantworten.

### LiaScript Webservice

Das ist die einfachste Variante: Sofern das LiaScript-Markdown bei Github liegt, kann man den Dokumentenlink kopieren und auf der LiaScript-Startseite einfügen:

![Startseite von LiaScript](img/liascript-service.png)

Im Ergebnis erhält man ein *Rendering* des eigenen Kurses, dass dann bspw. mit Studierenden geteilt werden kann.

### CAU Webservice

Es gibt probeweise einen [LiaScript Webservice vom RZ](https://vm077.test.rz.uni-kiel.de/), der nur aus dem Uni-Netz erreichbar ist. Der Service läuft nicht  sehr stabil und wird nicht regelmäßig gewartet.

Es ist möglicherweise nicht klug ihn zu verwenden.


### Statische Website(n)

Mit dem [LiaScript-Exporter](https://github.com/LiaScript/LiaScript-Exporter) ist eine Umwandlung des eigenen LiaScript-Kurses in diverse Ausgabeformate möglich. Die Steuerung erfolgt über die Kommandozeile und erfordert die vorherige Installation von [NodeJS](https://nodejs.org/en/download/).

Der Exporter eröffnet die Möglichkeit eine statische Website zu generieren, die dann über *ganz normalen* Webspace ausgeliefert werden kann. 

## Die Zukunft: LiveEditor

https://liascript.github.io/LiveEditor/
