# Management Tools für Wireguard VPNs

_Vortrag beim Freien Software Abend Köln/Düsseldorf am 24. Februar 2021._

[Wireguard](https://www.wireguard.com/) ist ein relativ junges VPN-Produkt
und seit Linux 5.6 im Linux-Kernel.
Es basiert auf modernen kryptographischen Algorithmen und Protokollen, ist
einfach zu konfigurieren und sehr performant.
Neben Linux werden auch viele andere Betriebssysteme unterstützt.

Nach einem kurzen Blick auf die VPN Grundlagen beleuchtet der Vortrag
die kryptographischen und netzwerktechnischen Grundlagen und erörtert
die Designentscheidungen von Wireguard. Es werden Beispiele für
Konfigurationen und die Kommandos rund um Wireguard gezeigt. Ein
Blick auf die Management-Lösungen
[Wireguard-UI](https://github.com/ngoduykhanh/wireguard-ui) und
[Tailscale](https://tailscale.com/) schließt den Vortrag ab.

## Ergänzende Informationen

**Beispiel für eine Wireguard-Konfiguration mit Debian ifupdown**

basierend auf einem Kommentar im Chat von BigBlueButton während des Vortrags.

```
auto wg0
iface wg0 inet static
  address   192.168.200.8/24

  pre-up    ip link add wg0 type wireguard
  pre-up    wg setconf wg0 /etc/wireguard/wg0.conf
  post-up   ip route add 192.168.200.1/32 dev wg0

  post-down ip link del wg0
```

**Artikel: [Wie viele Codezeilen hat Wireguard](https://blog.hweidner.de/post/2021/wireguard-lines-of-code/)**

Als Argument für Wireguard wird häufig der kleine Codeumfang und die damit
verbundene geringere Anfälligkeit für Softwarefehler gegenüber älteren
VPN Lösungen genannt.
Der Artikel geht der Frage nach, welchen Codeumfang Wireguard genau hat.

