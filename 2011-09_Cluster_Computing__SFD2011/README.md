# Cluster Computing mit freier Software

_Manuskript und Linksammlung zu meinem Vortrag “Cluster Computing” am
[Software Freedom Day
2011](http://sfd.koelnerlinuxtreffen.de/SFD2011/2011index.html) in
Köln._

## Definition “Cluster”

“Cluster (Informatik), eine Menge von Objekten mit ähnlichen
Eigenschaften [...]  
Computercluster, einen Verbund von Computern zur Steigerung der
Rechenleistung oder Ausfallsicherheit”

(Quelle: [Wikipedia](http://de.wikipedia.org/wiki/Cluster))

## Cluster-Typologie

- **Workstation Cluster** bei denen sich Benutzer an allen Rechnern
  des Clusterverbundes anmelden können und stets ihre gewohnte
  Arbeitsumgebung vorfinden.
- **High Performance Cluster (HPC)** bei denen viele Rechner verbunden
  werden, um die Leistung (Rechenleistung,
  Durchsatz, Speicherkapazität) zu erhöhen.
- **High Availability (HA) Cluster** bei denen Rechner redundant
  parallel betrieben werden, um die Verfügbarkeit und
  Ausfallsicherheit zu erhöhen.
- **Inverse Virtualization**, bei der mehrere physische Rechner
  genutzt werden, um nach außen einen logischen Dienst zu erbringen;
  im Gegensatz zur Virtualisierung, wo auf einer Hardware mehrere
  logische Dienste betrieben werden.

## Workstation-Cluster

Ziele:

- Einheitliche Arbeitsumgebung unabhängig vom Arbeitsplatz
- Geringer Administrationsaufwand durch Homogenität der Maschinen

Mechanismen:

- Zentrale Benutzerverwaltung
- Zentrale Benutzerverzeichnisse
- Zentrale Softwareverteilung
- Zentrales Konfigurationsmanagement
- Automatische Installation

### Zentrale Benutzerverwaltung

- [Network Information
  Service (NIS)](http://de.wikipedia.org/wiki/Network_Information_Service)
  (ehemals Yellow Pages, YP), Nachfolger
  [NIS+](http://en.wikipedia.org/wiki/NIS%2B)
- [Name Service
  Switch (NSS)](http://de.wikipedia.org/wiki/Name_Service_Switch) zur
  Benutzerverwaltung - Verwaltung von Benutzern, Gruppen und
  Shadow-Informationen in externer Datenquelle
- [Pluggable Authentication
  Module (PAM)](http://de.wikipedia.org/wiki/Pluggable_Authentication_Modules) -
  Authentifikation, Passwortänderung und Password Policy über externe
  Dienste
- [NSS-LDAP](http://www.padl.com/OSS/nss_ldap.html) /
  [PAM-LDAP](http://www.padl.com/OSS/pam_ldap.html) -
  Benutzerinformationen in LDAP Verzeichnisdienst
- [NSS-MySQL](http://libnss-mysql.sourceforge.net/) -
  Benutzerinformation in MySQL Datenbank
- [NSS-PgSQL](http://freshmeat.net/projects/nsspgsql/) -
  Benutzerinformation in PostgreSQL Datenbank

### Zentrale Homeverzeichnisse

Netzwerk-Filesysteme:

- [Network File
  System (NFS)](http://de.wikipedia.org/wiki/Network_File_System)
- [SMB/CIFS (Microsoft)](http://de.wikipedia.org/wiki/Server_Message_Block) -
  freie Serversoftware [Samba](http://www.samba.org/)
- [AFP (Apple)](http://de.wikipedia.org/wiki/Apple_Filing_Protocol) -
  freie Serversoftware [Netatalk](http://netatalk.sourceforge.net/)

Cluster-Filesysteme:

- [Oracle Cluster File
  System (OCFS2)](https://de.wikipedia.org/wiki/OCFS2)
- [Global File System (GFS) von
  RedHat](http://de.wikipedia.org/wiki/Global_File_System)
- [General Parallel File System (GPFS) von
  IBM](https://www.ibm.com/docs/en/gpfs/4.1.0.4?topic=guide-introducing-general-parallel-file-system)
- [Ceph](http://ceph.newdream.net/)
- [GlusterFS](http://www.gluster.org/)
- [AndrewFS](http://en.wikipedia.org/wiki/Andrew_File_System)
- [Lustre](http://wiki.lustre.org/index.php/Main_Page)
- [FhGFS](http://www.fhgfs.com/) - Fraunhofer File System

### Automatisierte Installation, Softwareverteilung und Konfigurationsmanagement

- [Anaconda / Kickstart von
  RedHat](http://fedoraproject.org/wiki/Anaconda)
- [JumpStart von SUN/Oracle](https://en.wikipedia.org/wiki/JumpStart_(software))
- [YaST / AutoYaST (SUSE)](http://de.wikipedia.org/wiki/YaST)
- [m23](http://m23.sourceforge.net/) - Installation, Inventar,
  Paketverwaltung
- [BCFG2](hhttp://bcfg2.org/) - Paketverwaltung,
  Reverse Engineering auf Basis von Python/Cheetah Template
- [FAI](http://fai-project.org/) - Fully Automated Installation; der
  Hauptentwickler arbeitet am Rechenzentrum der Uni Köln
- [cfengine](http://cfengine.com/) - Regelbasierte
  Konfigurationsverwaltung
- [etckeeper (Debian)](https://etckeeper.branchable.com/) -
  Versionskontrolle für /etc Verzeichnis
- [Chef](https://www.chef.io/products/chef-infra) -
  Konfigurationsmanagement Library auf Basis von Ruby und CouchDB
- [Ansible](http://www.ansible.com/) - Konfigurationsmanagement und IT
  Automation für Linux Clients, stellt geringe Anforderungen an
  die Systemumgebung.
- [GOsa²](https://github.com/gosa-project) - zentrales PC
  Management, Fokus auf Arbeitsplatzrechner in der öffentlichen
  Verwaltung, nutzt LDAP für das Repository und FAI für die
  Erstinstallation
- [Clacks](http://www.clacks-project.org/) - designierter Nachfolger
  von GOsa²
- [REX](http://rexify.org/) - zentrales Konfigurationsmanagement mit
  SSH und Perl
- [OPSI](http://www.opsi.org/) - Installation, Softwareverteilung,
  Inventur und Lizenzmanagement für Windows-und seit Version 4.0.5
  auch für Linux-Desktops; basierend auf Linux Servern
- [Spacewalk](http://spacewalk.redhat.com/) - Inventarisierung,
  Paketmanagement und Konfigurationsmanagement, hauptsächlich für
  RedHat/Fedora, eingeschränkt auch Debian und SuSE. Kommerzielle
  Version als
  [Satellite](http://www.redhat.com/products/enterprise-linux/rhn-satellite/) verfügbar.
- [Uranos](https://sourceforge.net/projects/uranos/) -
  Automatische Installation und Patchmanagement für viele verschiedene
  Betriebssysteme mit deren nativen Methoden (z.B. SuSE AutoYaST,
  Debian preseed, RedHat Kickstart).
- [WPKG](http://wpkg.org/) - Softwareverteilung für Windows Desktops

## High Performance Cluster (HPC)

Ziel:

- Skalierung der Leistung (CPU, Speicher, Durchsatz) durch Kopplung
  mehrerer Computer

Mechanismen:

- **Parallele Programmierung** mit speziellen Programmiersprachen oder
  Erweiterungen verbreiteter Sprachen; meist C/C++ oder Fortran
- **Parallelisierungsbibliotheken** mit Funktionen für die
  Parallelisierung, Kommunikation und Synchronisation
- **Automatische Parallelisierung** durch Verteilung der Prozesse auf
  Rechnerknoten, meist als Kernel-Erweiterung für Linux

### Programmiersprachen für Parallelprogrammierung

- [OpenMP](http://openmp.org/) – Multi-platform shared memory, eine
  Erweiterung der Sprachen C/C++ und Fortran für die Parallele
  Programmierung
- [Sieve C++ Parallel Programming
  System](http://en.wikipedia.org/wiki/Sieve_C%2B%2B_Parallel_Programming_System) -
  (mittlerweile kommerzielle) Erweiterung für C++
- [Split-C](http://now.cs.berkeley.edu/split-c.html) -
  Erweiterung der Sprache C, freier Download, Lizenz unklar
- [Unified Parallel
  C](http://en.wikipedia.org/wiki/Unified_Parallel_C) - Ein Nachfolger
  von Split-C, Verbreitung im akademischen Umfeld
- [OpenACC](http://www.openacc-standard.org/) - Compilererweiterung
  für C, C++ und Fortran, Anlehnung an OpenMP, Fokus auf
  Spezialprozessoren wie GPUs.
- [Go](http://golang.org/) ist eine junge Programmierspache mit
  eingebauter Unterstützung für nebenläufige/parallele Programmierung
  nach dem Vorbild von [Hoare’s Communicating Sequential
  Processes](http://en.wikipedia.org/wiki/Communicating_sequential_processes)
  ([Themenseite zu Go](https://github.com/hweidner/golang-de/wiki)).
- [Erlang](http://de.wikipedia.org/wiki/Erlang_%28Programmiersprache%29)
  ist eine funktionale Sprache mit Unterstützung für
  nebenläufige Prozesse.

### Bibliotheken für Parallelprogramierung

- [Message Passing Interface (MPI
  / MPI-2)](http://de.wikipedia.org/wiki/Message_Passing_Interface) -
  Standard und Bibliothek für Nachrichtenaustausch bei parallelen
  Berechnungen
- [Intel Thread Building Blocks](http://threadingbuildingblocks.org/)
- [Thrust](https://nvidia.github.io/cccl/thrust/) - Bibliothek für parallele
  Algorithmen und Datenstrukturen für C++ als Erweiterung
  der STL (Standard Template Library).
- [Golem](http://code.google.com/p/golem/) (Go Launch on
  Every Machine) ist ein System zum Rechnen wissenschaftlicher
  Probleme und Datenanalysen auf mehreren Rechnern; geschrieben in Go.

### Kernelerweiterungen / Cluster Stacks

- [OpenSSI](https://en.wikipedia.org/wiki/OpenSSI) - Single System Image Cluster
  Environment für Linux
- [Beowulf Cluster](http://www.beowulf.org/) - eine Sammlung von
  Standards zum Bau von Clustern
- [MOSIX](http://www.mosix.org/) / freie Implementierung
  [openMOSIX](http://en.wikipedia.org/wiki/OpenMosix) (eingestellt) /
  Nachfolger [LinuxPMI](http://linuxpmi.org/)

### HPC-Distributionen

- [PelicanHPC](https://sourceforge.net/projects/pelicanhpc/) - eine
  Cluster-Distribution auf USB-Stick
- [ClusterKnoppix](http://en.wikipedia.org/wiki/ClusterKnoppix)
  (Projektseite momentan nicht erreichbar, Projekt wurde
  vermutlich eingestellt)

## High Availability (HA) Cluster

Ziele:

- Erhöhung der Verfügbarkeit von Diensten
- Verringerung/Vermeidung von Downtimes

Mechanismen:

- Redundanz
- Trennung von Physik und Logik
- Ausfallerkennung und automatisches Failover

### Standards

- [Open Cluster Framework (OCF)](https://en.wikipedia.org/wiki/Open_Cluster_Framework)
- [Application Interface
  Specification (AIS)](https://en.wikipedia.org/wiki/Application_Interface_Specification)
  des [Service Availability Forum (SAF)](https://en.wikipedia.org/wiki/Service_Availability_Forum)

### HA-Clusterstacks

- [Heartbeat](http://www.linux-ha.org/wiki/Heartbeat) - früher ein
  vollständiger Clusterstack, mittlerweile nur noch Low Level
  Knoten-Kommunikation als Unterbau für Pacemaker
- [Pacemaker](http://www.linux-ha.org/wiki/Pacemaker) - Cluster
  High-Level Ressourcenverwaltung, benötigt
  Kommunikationsschicht (z.B. Heartbeat-3, OpenAIS oder Corosync)
- OpenAIS - freie Implementierung von AIS (nicht mehr auffindbar,
  wurde vermutlich eingestellt und durch Corosync ersetzt)
- [Corosync](http://www.corosync.org/) - eine auf das nötigste
  reduzierte Variante von OpenAIS, ausreichend als Unterbau für
  Pacemaker

## Inverse Virtualization Cluster

Ziele:

- Skalierbare und flexible Netzdienste
- Erhöhung der Verfügbarkeit und Performance von Diensten

Mechanismen:

- Flexible und skalierbare Abbildung von Diensten auf gleichartige,
  unabhängig arbeitende Server
- Lastverteilung (Round Robin, Least Connection)
- Health Check und automatischer Ausschluss bei Ausfall

### Netzwerkdienste

- [IP Virtual System (IPVS)](http://www.linuxvirtualserver.org/) im
  Linux-Kernel / ipvsadm zur Steuerung.
- [Ldirector daemon](http://horms.net/projects/ldirectord/) -
  Konfiguration von Load Balancern auf Basis von IPVS, Health Checks
  und Failover.
- [Keepalived](http://www.keepalived.org/) - ein anderes Frontend für
  IPVS mit eingebautem Cluster-Failover und VRRP zum Abgleich
  von Verbindungen.
- [HAproxy](http://haproxy.1wt.eu/) - Eigenständiger Load Balancer im
  Userspace für TCP und HTTP.
- [Balance GPL](http://www.inlab.de/balance.html) - einfacher TCP Load
  Balancer für Linux und Solaris.

### Load Balancer für Web-Anwendungen

- [Squid](http://www.squid-cache.org/) - eigentlich ein WWW-Proxy, der
  aber auch als Reverse Proxy und Load Balancer eingesetzt
  werden kann.
- [Varnish Cache](https://www.varnish-cache.org/) - Open Source
  Caching Proxy und Load Balancer
- [Apache Web Server](http://httpd.apache.org/) mit Modul
  [mod\_proxy\_balancer](http://httpd.apache.org/docs/2.2/mod/mod_proxy_balancer.html)
- [Pound](http://www.apsis.ch/pound) - Reverse Proxy, Load Balancer
  und HTTPS Terminator für Web-Dienste
- oft in Kombination mit anderen Aufgaben eingesetzt, z.B. Caching,
  Zugriffskontrolle, Protokollierung, GeoIP
