# Bookstack

_Kurzvortrag im Linux-Workshop Köln am 7. Juli 2026 im Themenabend
Wissensmanagement_

[Bookstack](https://www.bookstackapp.com/) (MIT Lizenz) ist eine einfache
Wiki-Software für die strukturierte Organisation von Informationen.
Als webbasierte Software zum selber hosten eignet sie sich für die
gemeinsame Dokumentenbearbeitung von Arbeitsgruppen und kleinen bis
mittlere Unternehmen.

Bookstack ist in PHP implementiert und benötigt neben einem PHP-fähigen
Webserver eine relationale Datenbank, wobei derzeit MariaDB und MySQL
unterstützt werden.

Dokumente sind in Regalen, Büchern, Kapitel und Seiten organisiert.
Über ein Rechte-/Rollenkonzept können verschiedenen Benutzern unterschiedliche
Rechte an Büchern gegeben werden.
Das System ist streng WYSIWYG-orientiert, optional kann auch in Markdown
editiert werden.

Bookstack kann in eine zentrale Benutzerverwaltung eingebunden werden, z.B.
mit LDAP. Über eine REST API können Dokumente auch von automatischen Prozessen
erzeugt und hochgeladen werden.

