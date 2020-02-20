# Parallelprogrammierung in Go

_Vortrag auf der OpenRheinRuhr 2016_

Go ist eine relativ junge Programmiersprache, deren Entwicklung maßgeblich von Google getragen wird. Um die Möglichkeiten aktueller Mehrkernprozessoren auszuschöpfen, ist die Unterstützung nebenläufiger und paralleler Programmierung Bestandteil der Sprache. Go orientiert sich dabei am Modell der Communicating Sequential Processes (CSP), das von Tony Hoare bereits 1978 vorgestellt wurde.

Nach einer kurzen Einführung in nebenläufige und parallele Programmierung wird gezeigt, wie CSP in Go umgesetzt ist. Über Goroutinen kann Programmcode nebenläufig ausgeführt werden. Die Go-Runtime verteilt die Goroutinen auf Threads des Betriebssystems, so dass die Möglichkeiten mehrerer CPU-Kerne ausgeschöpft werden können. Über Channels können Goroutinen Daten austauschen und den Programmablauf synchronisieren.

Daneben ermöglicht es Go, dass parallele Programmteile auf gemeinsamen Speicher zugreifen. Hierbei kann es zu Wettlaufsituationen (Race Conditions) kommen. Daher müssen die Zugriffe synchronisiert werden. Dazu bietet die Go-Standardbibliothek verschiedene Mechanismen an. Im Memory Modell ist spezifiziert, welche Garantien die Sprache in Bezug auf parallele Zugriffe auf gemeinsamen Speicher bietet.
