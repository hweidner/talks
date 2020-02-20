# Spectre und Meltdown

_Vortrag beim [Linux-Workshop Köln](http://www.uni-koeln.de/themen/linux/)
am 9. Januar 2018._

Meltdown und Spectre sind die Namen zweier Angriffsvarianten auf
Hardware-Schwachstellen in diversen Mikroprozessoren.

Mit Hilfe
von Seitenkanalangriffen kann bei Prozessoren, die *speculative
execution* unterstützen, der Inhalt von Speicherbereichen
rekonstruiert werden. Die Spectre-Angriffe benötigen dazu geeigneten
Programmcode im Adressraum des Opfers, z.B. im Kernel. Bei Meltdown
wird zusätzlich eine weitere Schwachstelle in Prozessoren von Intel
und ARM ausgenutzt, so dass der Angriff über die Grenzen des Adressraum
hinweg funktioniert.

Die Angriffe wurden im Sommer 2017 von verschiedenen Forscherteams
untersucht, u.a. im Google Project Zero und an der TU Graz. Im Januar
2018 wurden die Schwachstellen öffentlich.

Die meisten Linux-Distributionen haben mittlerweile ein Security Update
für den Kernel herausgegeben, das die KAISER/KPTI Patches beinhaltet.
Diese bewirken eine vollständige Trennung von User- und Kernel-Adressraum
durch und stellen somit ein Workaround gegen den Meltdown Angriff dar.
Allerdings beinträchtigen die Patches die Performance, bei I/O-lastigen
Workloads wurden bis zu 50% Performanceverlust gemessen.

Google hat gegen eine Variante des Spectre Angriffs die Retpoline Patches
entwickelt. Diese sind noch nicht in die Distributionen eingeflossen. Auch
hier wurden teilweise Peformanceverluste gemessen.

## Links

 * [Veröffentlichung des Google Project Zero](https://googleprojectzero.blogspot.de/2018/01/reading-privileged-memory-with-side.html)
 * [Übersichtsseite zu Meltdown und Spectre](https://meltdownattack.com/),
   mit Verweisen auf Forschungspapers und Herstellerreaktionen.
 * [Artikel im Register](https://www.theregister.co.uk/2018/01/02/intel_cpu_design_flaw/)
   vom 2. Januar und
   [weitere Analysen](https://www.theregister.co.uk/2018/01/04/intel_amd_arm_cpu_vulnerability/).
 * [Deutschsprachige Erläuterung](https://www.computerbase.de/2018-01/intel-cpu-pti-sicherheitsluecke/)
 * [Spectre Demo-Exploit](https://gist.github.com/ErikAugust/724d4a969fb2c6ae1bbd7b2a9e3d4bb6),
   zeigt die grundsätzliche Funktionsweise und Wirksamkeit des Spectre-Angrifffs.
 * [Liste von Advisories und Herstellerreaktionen](https://www.bleepingcomputer.com/news/security/list-of-meltdown-and-spectre-vulnerability-advisories-patches-and-updates/)
 * [Erläuterungen zu den KAISER/KPTI Patches im Linux Kernel](https://lwn.net/Articles/738975/)
 * [Benchmarks der KPTI Patches](https://www.phoronix.com/scan.php?page=article&item=linux-415-x86pti)
   zeigen den Performanceverlust nach den Patches gegen Meltdown
 * [Benchmarks der Retpoline-Patches](https://www.phoronix.com/scan.php?page=article&item=linux-retpoline-benchmarks)
   gegen den Spectre-Angriff

