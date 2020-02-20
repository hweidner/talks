# Betrieb eines E-Mail-Servers unter Linux

_Vortrag beim Linux-Workshop Köln am 7. Mai 2019._

E-Mail ist einer der ältesten Dienste im Internet. Das Thema hat sich jedoch im Laufe der letzten 25 Jahren stark verändert. Wegen des hohen Aufkommens an unerwünschter Werbemail (SPAM) greifen die Betreiber großer E-Mail-Server zu immer aufwändigeren Mechanismen, um SPAM von erwünschter E-Mail zu trennen.

Der Vortrag behandelt die wichtigsten Aspekte beim Betrieb eines eigenen E-Mail-Servers unter Linux. Im ersten Teil werden die wesentlichen Komponenten (MTA, MUA, MDA) und Protokolle (SMTP, POP, IMAP) vorgestellt, konkrete Implementierungen in Freier Software benannt und ihr Zusammenspiel erläutert. Der Teil endet mit einer Übersicht über obligatorische und optionale Maßnahmen beim Betrieb eines Servers.

Im zweiten Teil beschreibe ich mein eigenes, aus historischen Gründen gewachsenes Setup. Kern dessen ist ein E-Mail-Server auf einem bei einem Provider gemieteten Server mit dem Betriebssystem Debian GNU/Linux 9 und der Software Postfix, Dovecot, procmail und dem Client mutt. Daneben kommen Thunderbird und K-9 Mail zum Einsatz. Zusätzlich nutze ich Accounts bei einem öffentlichen E-Mail Provider zwecks Datensicherung und Erhöhung der Verfügbarkeit.

Den Abschluss bildet ein Ausblick auf Alternativen zum Betrieb eines eigenen E-Mail-Servers.
