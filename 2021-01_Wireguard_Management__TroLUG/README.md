# Management Tools für Wireguard VPNs

_Vortrag in der Troisdorfer Linux User Group am 7. Januar 2021._

Wireguard ist ein Standard für schnelle und sichere VPN-Verbindungen
und seit Linux 5.6 im Kernel. Die Konfiguration erfolgt über eine
Konfigurationsdatei und CLI-Tools.

In den letzten zwei Jahren wurden mehrere Projekte für Management-Lösungen
rund um Wireguard gestartet. Drei davon stellt der Vortrag vor:

**Wireguard-UI** ist ein einfaches, webbasiertes Management-Tool für
einen zentralen Wireguard-Server. Es erlaubt einem VPN-Administrator
die Einstellung globaler Parameter, der serverseitigen Konfiguration
und der Anbindung an Clients. Die Client-Konfigurationen werden direkt
am Server erzeugt und als QR-Code angezeigt, so dass sie mit den 
offiziellen Wireguard Apps für Android und iOS direkt eingelesen werden
können.

**Subspace** ist, ähnlich wie Wireguard-UI, eine webbasierte Applikation
zur Verwaltung von Wireguard-Verbindungen an einem Server. Es erlaubt
die Anbindung an eine zentrale Benutzerverwaltung mit SAML, so dass
jeder angemeldete Benutzer seine eigenen Endgeräte im VPN verwalten kann.

**Tailscale** ist eine Infrastruktur zur Verwaltung von Peer-to-Peer
basierten VPN-Verbindungen auf Basis von Wireguard. Derzeit sind nur
die Linux- und Adroid-Clients freie Software, die Freigabe weiterer
Komponenten wurde aber in Aussicht gestellt. Bei Tailscale registrierte
Endgeräte bauen Tunnels auf, so dass sie sich gegenseitig über gesicherte
VPN-Verbindungen erreichen können, unabhängig vom Standort und der
verwendeten Internet-Anbindung.

Im Vortrag werden die Funktionen der jeweiligen Lösungen kurz erläutert
und anhand konkreter Installationen demonstriert.

