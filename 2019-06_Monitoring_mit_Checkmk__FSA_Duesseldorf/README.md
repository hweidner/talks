# Monitoring mit Checkmk

_Vortrag am Freien Software Abend am 26. Juni 2019 in Düsseldorf._

Checkmk (alte Schreibweise: Check_MK) ist ein Monitoring-System für IT-Netzwerke. Es wurde ursprünglich als Erweiterung für Nagios entwickelt, um dessen wichtigsten beiden Schwächen zu beseitigen: die geringe Performance und das mühsame Eintragen der zu überwachenden Informationen jedes Hosts in die Konfiguration. Mittlerweile ist Checkmk ein eigenständiges Monitoring-System, das jedoch im Kern immer noch auf Nagios aufbaut. Die Raw Edition von Checkmk ist freie Software unter der GNU GPL Version 2.

Im ersten Teil werden Aufbau, Arbeitsweise und Möglichkeiten von Checkmk vorgestellt. Im zweiten Teil zeige ich das bestehende Monitoring meiner privaten IT-Infrastruktur mit Checkmk.

Im dritten Teil wird live eine Checkmk Instanz eingerichtet und einige Hosts in das Monitoring aufgenommen. Dabei werden in der Inventarisieriung die zu überwachenden Eigenschaften der Hosts bestimmt und mit der Überwachung begonnen. Es wird gezeigt, wie ein eigener, anwendungsbezogener Check als Shellskript geschrieben und in den Checkmk Agent eingebunden wird.

## Links

* [Das offizielle Checkmk Handbuch](https://checkmk.de/cms.html)
* [Schreiben von Local Checks](https://checkmk.de/cms_localchecks.html)
* [Checkmk Alarmierungen über Telegram verschicken](https://www.karl-deutsch.at/check_mk_notifications_telegram.html)
* [Checkmk Agent als App für Android](https://play.google.com/store/apps/details?id=mrm.marco.probeomd&hl=de)
* [Der Unterschied zwischen Raw Edition (GPLv2) und Enterprise Edition](https://checkmk.de/editions.html)

