Cloud Computing
===============

_Manuskript und Linkliste zu meinem Vortrag beim [Software Freedom Day
2012](http://sfd.koelnerlinuxtreffen.de/SFD2012/2012index.html) in
Köln._

Definition und Merkmale
-----------------------

Definition von [Cloud Computing auf Wikipedia](http://de.wikipedia.org/wiki/Cloud-Computing):

-   Definierte Services, SLA, Verantwortung
-   Selbstzuweisung von Leistungen
-   Automatisierbarkeit (CLI / API)
-   (automatische) Skalierbarkeit
-   Zuverlässigkeit, Fehlertoleranz
-   Qualitätssicherung und Optimierung durch den Dienstanbieter
-   Flexibles Kostenmodell, pay-as-you-go

Typologie
---------

### Unterscheidung nach Abstraktionsschicht der Anbieter-Kunde Schnittstelle.

**Infrastructure as a Service (IaaS)**

Anbieter

 - Stellt virtualisierte Serverinfrastruktur bereit
 - CPU, Storage, Network, OS
 - Serviceparameter, Abrechnung

**Platform as a Service (PaaS)**

Anbieter

 - Stellt Laufzeitumgebung für Software bereit
 - Flexible CPU- und Speicherkapazität
 - Dynamisch Anpassbar

**Software as a Service (SaaS)**

Anbieter

 - Stellt benutzungsfertige Software im Netzwerk bereit
 - Kümmert sich eigenständig um Performance, Datensicherung, Zugriffsschutz, etc.

### Unterscheidung nach Lokalität / Dedizierung

**Private Cloud**

 - Aufbau einer Cloud-Infrastruktur auf dedizierter Hardware (für genau einen Kunden oder Inhouse)
 - Nutzung von Cloud Merkmalen (Skalierung, Automatisierung, …)

**Public Cloud**

 - Bereitstellung von Hardware für mehrere/viele Kunden
 - Optimierung der Auslastung, dadurch preiswerte Angebote

**Hybrid Cloud**

 - Nutzung von Private Cloud Diensten im Normalbetrieb
 - Ausweichen auf Public Cloud Angebote bei kurzfristig höherem Ressourcenbedarf

Public Cloud Angebote (Auswahl)
-------------------------------

-   Amazon Elastic Compute Cloud (EC2), Simple Storage Service (S3)
-   Box.com
-   Dropbox
-   Google AppEngine, ComputeEngine, Drive
-   Microsoft Azure, HP Cloud, IBM Cloud, mySAP
-   Ubuntu One

<!-- -->

-   Bindung an den Anbieter?
-   Sicherheit, Datenschutz?

Open Source Cloud Software und Stacks
-------------------------------------

In alphabetischer Reihenfolge.

### IaaS

[AbiCloud](http://freecode.com/projects/abicloud) IaaS Private Cloud
Platform.  
Unterstützt VirtualBox, VMware, KVM und Xen.  
Webbasiert, geschrieben in Java, unter LGPL

[Apache CloudStack](http://www.cloudstack.org/) IaaS Cloud Orchestration
Platform, ursprünglich von Citrix.  
Geschrieben in Java. Bedienung per Web Interface, CLI und REST API.  
Unterstützt VMware, Oracle VM, KVM, XenServer und Xen Cloud Platform.

[Archipel](http://archipelproject.org/)  
Virtuelle Maschinen verwalten und überwachen.  
Geschrieben in JavaScript, Kommunikation über XMPP Server

[Eucalyptus](http://www.eucalyptus.com/)  
IaaS Stack: Compute - Network - Storage - Identity.  
Unterstützt Xen, KVM (VMware in kommerzieller Version); Bucket und Block
based Storage Abstraction.  
Kompatibel zur Amazon Web Services (AWS) API

[Ganeti](http://code.google.com/p/ganeti/)  
Cluster Virtual Server Management Software für Xen, KVM und LXC

[Nimbus](http://www.nimbusproject.org/) - Nimbus is cloud computing for
science.  
Integrationsplattform für Hybride Clouds, unterstützt Amazon EC2, S3,
OpenStack

[OpenNebula](http://opennebula.org/)  
Verwaltung von großen IaaS Umgebungen (Virtualisierung), unterstützt
KVM, Xen, VMware

[OpenQRM](http://www.openqrm.com/)  
Open Source Data Center Automation.  
Unterstützt u.a. VMware, Xen, KVM und Linux-VServer;
Nagios-Konfigurationsgenerierung; Storage Management; HA Features,
Migration, fertiges Images für Debian, Ubuntu, OpenSUSE, CentOS etc.
verfügbar

[OpenStack](http://www.openstack.org/)  
Eine lose Softwaresammlung bestehend aus Tools für Compute (Nova)
ObjectStorage (Swift) und ImageService (Glance).  
Insgesamt eine recht komplexe Umgebung.

[OVirt](http://www.ovirt.org/)  
Server virtualization management system, including HA, live migration,
storage management, system scheduler

### PaaS

[Apache Mesos](http://mesos.apache.org/)  
Plattform zum Bau effizienter verteilter Systeme, skalierbar über 10.000
und mehr Knoten; API in C++, Java und Python.

[AppScale](http://www.appscale.com/)  
API-komptibel mit der Google App Engine, unerstützt Go, Java und Python.

[Cloud Foundry](http://www.cloudfoundry.com/)  
PaaS Plattform zum Entwickeln, Testen, Ausrollen und Skalieren von
Anwendungen.

[DEIS](http://deis.io/)  
PaaS Private Cloud basierend auf Docker und CoreOS.

[Docker.io](https://www.docker.io/)  
Anwendungen in LXC Containern verpacken, ausrollen und betreiben.

[OpenShift](https://openshift.redhat.com/app/) von RedHat  
Platform as a Service, programmierbar in Perl, Python, Java, Ruby oder
PHP.

[ShipBuilder](http://shipbuilder.io/)  
PaaS Plattform, basierend auf Git, Go, LXC und HAProxy.

### SaaS

[Etherpad](http://code.google.com/p/etherpad/)  
Web based realtime collaborative document editor

[OwnCloud](http://owncloud.org/)  
Datencloud: WebDAV, Kalender/Kontakt-Sync, Bookmarks, Editieren direkt
im Web

sowie zahlreiche webbasierte Applikationen wie Groupware, Wikis, CMS,
Foren, BBS, etc.
