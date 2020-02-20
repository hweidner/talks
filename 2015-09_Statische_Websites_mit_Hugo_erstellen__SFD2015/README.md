# Statische Websites mit Hugo erstellen

_Vortrag auf dem Software Freedom Day 2015 in Köln._

Viele Webseiten werden heute mit Content Management Systemen (CMS)
verwaltet. Sie erlauben eine Trennung von Logik, Inhalt und Layout und
setzen diese Bestandteile beim Abruf der Seite dynamisch zusammen. CMS
sind häufig in Skriptsprachen wie PHP geschrieben und generieren die
fertige Webseite meist beim Abruf, indem sie den Inhalt aus einer
Datenbank mit dem Layout-Template zusammen führen. Das ermöglicht eine
flexible Steuerung, hat jedoch seinen Preis bei der Performance und
Sicherheit der Website.

[Hugo](http://gohugo.io/) ist ein Generator für statische Websites. Er
ermöglicht es, die fertigen Seiten nicht erst zur Laufzeit, sondern zum
Publikationszeitpunkt zu erzeugen. Der Webserver muss nur noch fertige
Dateien ausliefern, was der Performance, Skalierbarkeit und Sicherheit
zugutekommt. Hugo wurde in der Programmiersprache Go geschrieben und
wird unter der Simple Public License (SimPL) veröffentlicht.

Hugo basiert auf diversen bewährten Technologien. Die Inhalte werden in
der Auszeichnungssprache
[Markdown](http://daringfireball.net/projects/markdown/) geschrieben; wo
deren Möglichkeiten nicht ausreichen, kann auch direkt HTML eingefügt
werden. Für Templates und der Zugriff auf variable Elemente wird die
Syntax der Go-Bibliothek
[html/template](http://golang.org/pkg/html/template/) verwendet.
Kontrollinformationen und die Konfigurationsdatei können wahlweise in
[YaML](http://yaml.org/), [TOML](https://github.com/toml-lang/toml) oder
[JSON](http://json.org/) geschrieben werden. Durch die Implementierung
in Go gilt Hugo als besonders schnell. Der Autor [Steve
Francia](http://spf13.com/) gibt die Geschwindigkeit der
Seitengenerierung auf aktuellen PCs mit etwa 1ms pro Seite an. Damit
lassen auch Sites mit mehreren Tausend Dokumenten in Sekunden
generieren.

Der Vortrag stellt die Software Hugo vor, erläutert die
Basistechnologien und zeigt Beispiele für die Erstellung einer einfachen
Site.

