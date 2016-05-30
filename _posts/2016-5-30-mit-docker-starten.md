# Client

## Status des Systems

[azureuser@clientdocker ~]$ sudo subscription-manager list

+-------------------------------------------+
    Status der installierten Produkte
+-------------------------------------------+
Produktname:   Red Hat Enterprise Linux Server
Produkt-ID:    69
Version:       7.2
Architektur:   x86_64
Status:        Unbekannt
Statusdetails: 
Startet:       
Endet:         

Produktname:   Red Hat Enterprise Linux Server - Extended Update Support
Produkt-ID:    70
Version:       7.2
Architektur:   x86_64
Status:        Unbekannt
Statusdetails: 
Startet:       
Endet:         

[azureuser@clientdocker ~]$ 

## Docker installieren

[azureuser@clientdocker ~]$ sudo yum -y install docker device-mapper device-mapper-event-libs
Geladene Plugins: langpacks, product-id, rhui-lb, search-disabled-repos
rhui-PA                                                                                                                                           | 2.9 kB  00:00:00     
rhui-rhel-7-server-rhui-debug-rpms                                                                                                                | 2.9 kB  00:00:00     
rhui-rhel-7-server-rhui-extras-debug-rpms                                                                                                         | 2.9 kB  00:00:00     
rhui-rhel-7-server-rhui-extras-rpms                                                                                                               | 2.9 kB  00:00:00     
rhui-rhel-7-server-rhui-extras-source-rpms                                                                                                        | 3.8 kB  00:00:00     
rhui-rhel-7-server-rhui-optional-debug-rpms                                                                                                       | 2.9 kB  00:00:00     
rhui-rhel-7-server-rhui-optional-rpms                                                                                                             | 3.5 kB  00:00:00     
rhui-rhel-7-server-rhui-optional-source-rpms                                                                                                      | 3.8 kB  00:00:00     
rhui-rhel-7-server-rhui-rh-common-debug-rpms                                                                                                      | 3.8 kB  00:00:00     
rhui-rhel-7-server-rhui-rh-common-rpms                                                                                                            | 3.8 kB  00:00:00     
rhui-rhel-7-server-rhui-rh-common-source-rpms                                                                                                     | 3.8 kB  00:00:00     
rhui-rhel-7-server-rhui-rpms                                                                                                                      | 3.7 kB  00:00:00     
rhui-rhel-7-server-rhui-source-rpms                                                                                                               | 3.8 kB  00:00:00     
rhui-rhel-7-server-rhui-supplementary-debug-rpms                                                                                                  | 2.5 kB  00:00:00     
rhui-rhel-7-server-rhui-supplementary-rpms                                                                                                        | 3.7 kB  00:00:00     
rhui-rhel-7-server-rhui-supplementary-source-rpms                                                                                                 | 3.8 kB  00:00:00     
rhui-rhel-server-rhui-rhscl-7-debug-rpms                                                                                                          | 3.1 kB  00:00:00     
rhui-rhel-server-rhui-rhscl-7-rpms                                                                                                                | 3.1 kB  00:00:00     
rhui-rhel-server-rhui-rhscl-7-source-rpms                                                                                                         | 3.8 kB  00:00:00     
(1/35): rhui-rhel-7-server-rhui-extras-debug-rpms/x86_64/primary_db                                                                               | 8.2 kB  00:00:00     
(2/35): rhui-PA/primary_db                                                                                                                        | 1.8 kB  00:00:00     
(3/35): rhui-rhel-7-server-rhui-extras-source-rpms/x86_64/primary_db                                                                              |  31 kB  00:00:00     
(4/35): rhui-rhel-7-server-rhui-extras-source-rpms/x86_64/group                                                                                   |  104 B  00:00:00     
(5/35): rhui-rhel-7-server-rhui-debug-rpms/7Server/x86_64/primary_db                                                                              | 1.2 MB  00:00:00     
(6/35): rhui-rhel-7-server-rhui-extras-rpms/x86_64/primary_db                                                                                     |  97 kB  00:00:00     
(7/35): rhui-rhel-7-server-rhui-optional-source-rpms/7Server/x86_64/group                                                                         |  104 B  00:00:00     
(8/35): rhui-rhel-7-server-rhui-optional-rpms/7Server/x86_64/primary_db                                                                           | 3.2 MB  00:00:00     
(9/35): rhui-rhel-7-server-rhui-extras-source-rpms/x86_64/updateinfo                                                                              |  51 kB  00:00:00     
(10/35): rhui-rhel-7-server-rhui-optional-debug-rpms/7Server/x86_64/primary_db                                                                    | 930 kB  00:00:00     
(11/35): rhui-rhel-7-server-rhui-optional-source-rpms/7Server/x86_64/primary_db                                                                   | 800 kB  00:00:00     
(12/35): rhui-rhel-7-server-rhui-rh-common-debug-rpms/7Server/x86_64/group                                                                        |  104 B  00:00:00     
(13/35): rhui-rhel-7-server-rhui-rh-common-debug-rpms/7Server/x86_64/primary_db                                                                   |  11 kB  00:00:00     
(14/35): rhui-rhel-7-server-rhui-optional-source-rpms/7Server/x86_64/updateinfo                                                                   | 158 kB  00:00:00     
(15/35): rhui-rhel-7-server-rhui-rh-common-rpms/7Server/x86_64/updateinfo                                                                         |  27 kB  00:00:00     
(16/35): rhui-rhel-7-server-rhui-rh-common-rpms/7Server/x86_64/primary_db                                                                         |  97 kB  00:00:00     
(17/35): rhui-rhel-7-server-rhui-rh-common-source-rpms/7Server/x86_64/group                                                                       |  104 B  00:00:00     
(18/35): rhui-rhel-7-server-rhui-rh-common-source-rpms/7Server/x86_64/primary_db                                                                  |  31 kB  00:00:00     
(19/35): rhui-rhel-7-server-rhui-rh-common-debug-rpms/7Server/x86_64/updateinfo                                                                   | 9.8 kB  00:00:00     
(20/35): rhui-rhel-7-server-rhui-rh-common-rpms/7Server/x86_64/group                                                                              |  104 B  00:00:00     
(21/35): rhui-rhel-7-server-rhui-rh-common-source-rpms/7Server/x86_64/updateinfo                                                                  |  21 kB  00:00:00     
(22/35): rhui-rhel-7-server-rhui-source-rpms/7Server/x86_64/updateinfo                                                                            | 925 kB  00:00:00     
(23/35): rhui-rhel-7-server-rhui-source-rpms/7Server/x86_64/group                                                                                 |  104 B  00:00:00     
(24/35): rhui-rhel-7-server-rhui-supplementary-debug-rpms/7Server/x86_64/primary_db                                                               | 1.2 kB  00:00:00     
(25/35): rhui-rhel-7-server-rhui-supplementary-rpms/7Server/x86_64/primary_db                                                                     | 142 kB  00:00:00     
(26/35): rhui-rhel-7-server-rhui-rpms/7Server/x86_64/primary_db                                                                                   |  21 MB  00:00:00     
(27/35): rhui-rhel-7-server-rhui-supplementary-source-rpms/7Server/x86_64/group                                                                   |  104 B  00:00:00     
(28/35): rhui-rhel-7-server-rhui-supplementary-source-rpms/7Server/x86_64/updateinfo                                                              |  16 kB  00:00:00     
(29/35): rhui-rhel-7-server-rhui-source-rpms/7Server/x86_64/primary_db                                                                            | 1.3 MB  00:00:00     
(30/35): rhui-rhel-server-rhui-rhscl-7-debug-rpms/7Server/x86_64/primary_db                                                                       | 102 kB  00:00:00     
(31/35): rhui-rhel-server-rhui-rhscl-7-source-rpms/7Server/x86_64/group                                                                           |  104 B  00:00:00     
(32/35): rhui-rhel-7-server-rhui-supplementary-source-rpms/7Server/x86_64/primary_db                                                              | 4.6 kB  00:00:00     
(33/35): rhui-rhel-server-rhui-rhscl-7-source-rpms/7Server/x86_64/primary_db                                                                      | 702 kB  00:00:00     
(34/35): rhui-rhel-server-rhui-rhscl-7-source-rpms/7Server/x86_64/updateinfo                                                                      | 200 kB  00:00:00     
(35/35): rhui-rhel-server-rhui-rhscl-7-rpms/7Server/x86_64/primary_db                                                                             | 1.8 MB  00:00:00     
(1/12): rhui-rhel-7-server-rhui-extras-rpms/x86_64/updateinfo                                                                                     |  57 kB  00:00:00     
(2/12): rhui-rhel-7-server-rhui-extras-debug-rpms/x86_64/updateinfo                                                                               | 8.6 kB  00:00:00     
(3/12): rhui-rhel-7-server-rhui-rpms/7Server/x86_64/group_gz                                                                                      | 134 kB  00:00:00     
(4/12): rhui-rhel-7-server-rhui-optional-rpms/7Server/x86_64/group_gz                                                                             | 6.2 kB  00:00:00     
(5/12): rhui-rhel-7-server-rhui-debug-rpms/7Server/x86_64/updateinfo                                                                              | 816 kB  00:00:00     
(6/12): rhui-rhel-7-server-rhui-optional-rpms/7Server/x86_64/updateinfo                                                                           | 885 kB  00:00:00     
(7/12): rhui-rhel-7-server-rhui-optional-debug-rpms/7Server/x86_64/updateinfo                                                                     | 634 kB  00:00:00     
(8/12): rhui-rhel-7-server-rhui-supplementary-rpms/7Server/x86_64/group_gz                                                                        | 8.9 kB  00:00:00     
(9/12): rhui-rhel-7-server-rhui-supplementary-rpms/7Server/x86_64/updateinfo                                                                      |  27 kB  00:00:00     
(10/12): rhui-rhel-server-rhui-rhscl-7-debug-rpms/7Server/x86_64/updateinfo                                                                       |  96 kB  00:00:00     
(11/12): rhui-rhel-7-server-rhui-rpms/7Server/x86_64/updateinfo                                                                                   | 1.2 MB  00:00:00     
(12/12): rhui-rhel-server-rhui-rhscl-7-rpms/7Server/x86_64/updateinfo                                                                             | 397 kB  00:00:00     
Abhängigkeiten werden aufgelöst
--> Transaktionsprüfung wird ausgeführt
---> Paket device-mapper.x86_64 7:1.02.107-5.el7_2.1 markiert, um aktualisiert zu werden
--> Abhängigkeit device-mapper = 7:1.02.107-5.el7_2.1 wird für Paket 7:device-mapper-libs-1.02.107-5.el7_2.1.x86_64 verarbeitet
--> Abhängigkeit device-mapper = 7:1.02.107-5.el7_2.1 wird für Paket 7:device-mapper-event-1.02.107-5.el7_2.1.x86_64 verarbeitet
---> Paket device-mapper.x86_64 7:1.02.107-5.el7_2.2 markiert, um eine Aktualisierung zu werden
---> Paket device-mapper-event-libs.x86_64 7:1.02.107-5.el7_2.1 markiert, um aktualisiert zu werden
---> Paket device-mapper-event-libs.x86_64 7:1.02.107-5.el7_2.2 markiert, um eine Aktualisierung zu werden
---> Paket docker.x86_64 0:1.9.1-40.el7 markiert, um installiert zu werden
--> Abhängigkeit docker-forward-journald = 1.9.1-40.el7 wird für Paket docker-1.9.1-40.el7.x86_64 verarbeitet
--> Abhängigkeit docker-common = 1.9.1-40.el7 wird für Paket docker-1.9.1-40.el7.x86_64 verarbeitet
--> Abhängigkeit docker-selinux >= 1.9.1-40.el7 wird für Paket docker-1.9.1-40.el7.x86_64 verarbeitet
--> Transaktionsprüfung wird ausgeführt
---> Paket device-mapper-event.x86_64 7:1.02.107-5.el7_2.1 markiert, um aktualisiert zu werden
--> Abhängigkeit device-mapper-event = 7:1.02.107-5.el7_2.1 wird für Paket 7:lvm2-libs-2.02.130-5.el7_2.1.x86_64 verarbeitet
---> Paket device-mapper-event.x86_64 7:1.02.107-5.el7_2.2 markiert, um eine Aktualisierung zu werden
---> Paket device-mapper-libs.x86_64 7:1.02.107-5.el7_2.1 markiert, um aktualisiert zu werden
---> Paket device-mapper-libs.x86_64 7:1.02.107-5.el7_2.2 markiert, um eine Aktualisierung zu werden
---> Paket docker-common.x86_64 0:1.9.1-40.el7 markiert, um installiert zu werden
---> Paket docker-forward-journald.x86_64 0:1.9.1-40.el7 markiert, um installiert zu werden
---> Paket docker-selinux.x86_64 0:1.9.1-40.el7 markiert, um installiert zu werden
--> Abhängigkeit policycoreutils-python wird für Paket docker-selinux-1.9.1-40.el7.x86_64 verarbeitet
--> Transaktionsprüfung wird ausgeführt
---> Paket lvm2-libs.x86_64 7:2.02.130-5.el7_2.1 markiert, um aktualisiert zu werden
--> Abhängigkeit lvm2-libs = 7:2.02.130-5.el7_2.1 wird für Paket 7:lvm2-2.02.130-5.el7_2.1.x86_64 verarbeitet
---> Paket lvm2-libs.x86_64 7:2.02.130-5.el7_2.2 markiert, um eine Aktualisierung zu werden
---> Paket policycoreutils-python.x86_64 0:2.2.5-20.el7 markiert, um installiert zu werden
--> Abhängigkeit libsemanage-python >= 2.1.10-1 wird für Paket policycoreutils-python-2.2.5-20.el7.x86_64 verarbeitet
--> Abhängigkeit audit-libs-python >= 2.1.3-4 wird für Paket policycoreutils-python-2.2.5-20.el7.x86_64 verarbeitet
--> Abhängigkeit python-IPy wird für Paket policycoreutils-python-2.2.5-20.el7.x86_64 verarbeitet
--> Abhängigkeit libqpol.so.1(VERS_1.4)(64bit) wird für Paket policycoreutils-python-2.2.5-20.el7.x86_64 verarbeitet
--> Abhängigkeit libqpol.so.1(VERS_1.2)(64bit) wird für Paket policycoreutils-python-2.2.5-20.el7.x86_64 verarbeitet
--> Abhängigkeit libapol.so.4(VERS_4.0)(64bit) wird für Paket policycoreutils-python-2.2.5-20.el7.x86_64 verarbeitet
--> Abhängigkeit checkpolicy wird für Paket policycoreutils-python-2.2.5-20.el7.x86_64 verarbeitet
--> Abhängigkeit libqpol.so.1()(64bit) wird für Paket policycoreutils-python-2.2.5-20.el7.x86_64 verarbeitet
--> Abhängigkeit libapol.so.4()(64bit) wird für Paket policycoreutils-python-2.2.5-20.el7.x86_64 verarbeitet
--> Transaktionsprüfung wird ausgeführt
---> Paket audit-libs-python.x86_64 0:2.4.1-5.el7 markiert, um installiert zu werden
---> Paket checkpolicy.x86_64 0:2.1.12-6.el7 markiert, um installiert zu werden
---> Paket libsemanage-python.x86_64 0:2.1.10-18.el7 markiert, um installiert zu werden
---> Paket lvm2.x86_64 7:2.02.130-5.el7_2.1 markiert, um aktualisiert zu werden
---> Paket lvm2.x86_64 7:2.02.130-5.el7_2.2 markiert, um eine Aktualisierung zu werden
---> Paket python-IPy.noarch 0:0.75-6.el7 markiert, um installiert zu werden
---> Paket setools-libs.x86_64 0:3.3.7-46.el7 markiert, um installiert zu werden
--> Abhängigkeitsauflösung beendet

Abhängigkeiten aufgelöst

=========================================================================================================================================================================
 Package                                    Arch                     Version                                 Paketquelle                                           Größe
=========================================================================================================================================================================
Installieren:
 docker                                     x86_64                   1.9.1-40.el7                            rhui-rhel-7-server-rhui-extras-rpms                   7.8 M
Aktualisieren:
 device-mapper                              x86_64                   7:1.02.107-5.el7_2.2                    rhui-rhel-7-server-rhui-rpms                          252 k
 device-mapper-event-libs                   x86_64                   7:1.02.107-5.el7_2.2                    rhui-rhel-7-server-rhui-rpms                          169 k
Als Abhängigkeiten installiert:
 audit-libs-python                          x86_64                   2.4.1-5.el7                             rhui-rhel-7-server-rhui-rpms                           69 k
 checkpolicy                                x86_64                   2.1.12-6.el7                            rhui-rhel-7-server-rhui-rpms                          247 k
 docker-common                              x86_64                   1.9.1-40.el7                            rhui-rhel-7-server-rhui-extras-rpms                    55 k
 docker-forward-journald                    x86_64                   1.9.1-40.el7                            rhui-rhel-7-server-rhui-extras-rpms                   827 k
 docker-selinux                             x86_64                   1.9.1-40.el7                            rhui-rhel-7-server-rhui-extras-rpms                    73 k
 libsemanage-python                         x86_64                   2.1.10-18.el7                           rhui-rhel-7-server-rhui-rpms                           94 k
 policycoreutils-python                     x86_64                   2.2.5-20.el7                            rhui-rhel-7-server-rhui-rpms                          435 k
 python-IPy                                 noarch                   0.75-6.el7                              rhui-rhel-7-server-rhui-rpms                           32 k
 setools-libs                               x86_64                   3.3.7-46.el7                            rhui-rhel-7-server-rhui-rpms                          485 k
Aktualisiert für Abhängigkeiten:
 device-mapper-event                        x86_64                   7:1.02.107-5.el7_2.2                    rhui-rhel-7-server-rhui-rpms                          167 k
 device-mapper-libs                         x86_64                   7:1.02.107-5.el7_2.2                    rhui-rhel-7-server-rhui-rpms                          305 k
 lvm2                                       x86_64                   7:2.02.130-5.el7_2.2                    rhui-rhel-7-server-rhui-rpms                          1.0 M
 lvm2-libs                                  x86_64                   7:2.02.130-5.el7_2.2                    rhui-rhel-7-server-rhui-rpms                          872 k

Transaktionsübersicht
=========================================================================================================================================================================
Installieren   1 Paket  (+9 Abhängige Pakete)
Aktualisieren  2 Pakete (+4 Abhängige Pakete)

Gesamte Downloadgröße: 13 M
Downloading packages:
Delta RPMs disabled because /usr/bin/applydeltarpm not installed.
(1/16): audit-libs-python-2.4.1-5.el7.x86_64.rpm                                                                                                  |  69 kB  00:00:00     
(2/16): checkpolicy-2.1.12-6.el7.x86_64.rpm                                                                                                       | 247 kB  00:00:00     
(3/16): device-mapper-event-1.02.107-5.el7_2.2.x86_64.rpm                                                                                         | 167 kB  00:00:00     
(4/16): device-mapper-1.02.107-5.el7_2.2.x86_64.rpm                                                                                               | 252 kB  00:00:00     
(5/16): device-mapper-event-libs-1.02.107-5.el7_2.2.x86_64.rpm                                                                                    | 169 kB  00:00:00     
(6/16): device-mapper-libs-1.02.107-5.el7_2.2.x86_64.rpm                                                                                          | 305 kB  00:00:00     
(7/16): docker-forward-journald-1.9.1-40.el7.x86_64.rpm                                                                                           | 827 kB  00:00:00     
(8/16): docker-common-1.9.1-40.el7.x86_64.rpm                                                                                                     |  55 kB  00:00:00     
(9/16): docker-1.9.1-40.el7.x86_64.rpm                                                                                                            | 7.8 MB  00:00:00     
(10/16): docker-selinux-1.9.1-40.el7.x86_64.rpm                                                                                                   |  73 kB  00:00:00     
(11/16): lvm2-libs-2.02.130-5.el7_2.2.x86_64.rpm                                                                                                  | 872 kB  00:00:00     
(12/16): libsemanage-python-2.1.10-18.el7.x86_64.rpm                                                                                              |  94 kB  00:00:00     
(13/16): policycoreutils-python-2.2.5-20.el7.x86_64.rpm                                                                                           | 435 kB  00:00:00     
(14/16): python-IPy-0.75-6.el7.noarch.rpm                                                                                                         |  32 kB  00:00:00     
(15/16): lvm2-2.02.130-5.el7_2.2.x86_64.rpm                                                                                                       | 1.0 MB  00:00:00     
(16/16): setools-libs-3.3.7-46.el7.x86_64.rpm                                                                                                     | 485 kB  00:00:00     
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Gesamt                                                                                                                                   7.8 MB/s |  13 MB  00:00:01     
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
Warnung: RPMDB wurde außerhalb von yum verändert.
  Aktualisieren    : 7:device-mapper-1.02.107-5.el7_2.2.x86_64                                                                                                      1/22 
  Aktualisieren    : 7:device-mapper-libs-1.02.107-5.el7_2.2.x86_64                                                                                                 2/22 
  Aktualisieren    : 7:device-mapper-event-libs-1.02.107-5.el7_2.2.x86_64                                                                                           3/22 
  Aktualisieren    : 7:device-mapper-event-1.02.107-5.el7_2.2.x86_64                                                                                                4/22 
  Aktualisieren    : 7:lvm2-libs-2.02.130-5.el7_2.2.x86_64                                                                                                          5/22 
  Aktualisieren    : 7:lvm2-2.02.130-5.el7_2.2.x86_64                                                                                                               6/22 
  Installieren     : checkpolicy-2.1.12-6.el7.x86_64                                                                                                                7/22 
  Installieren     : docker-common-1.9.1-40.el7.x86_64                                                                                                              8/22 
  Installieren     : audit-libs-python-2.4.1-5.el7.x86_64                                                                                                           9/22 
  Installieren     : docker-forward-journald-1.9.1-40.el7.x86_64                                                                                                   10/22 
  Installieren     : setools-libs-3.3.7-46.el7.x86_64                                                                                                              11/22 
  Installieren     : python-IPy-0.75-6.el7.noarch                                                                                                                  12/22 
  Installieren     : libsemanage-python-2.1.10-18.el7.x86_64                                                                                                       13/22 
  Installieren     : policycoreutils-python-2.2.5-20.el7.x86_64                                                                                                    14/22 
  Installieren     : docker-selinux-1.9.1-40.el7.x86_64                                                                                                            15/22 
  Installieren     : docker-1.9.1-40.el7.x86_64                                                                                                                    16/22 
  Aufräumen        : 7:lvm2-2.02.130-5.el7_2.1.x86_64                                                                                                              17/22 
  Aufräumen        : 7:lvm2-libs-2.02.130-5.el7_2.1.x86_64                                                                                                         18/22 
  Aufräumen        : 7:device-mapper-event-1.02.107-5.el7_2.1.x86_64                                                                                               19/22 
  Aufräumen        : 7:device-mapper-event-libs-1.02.107-5.el7_2.1.x86_64                                                                                          20/22 
  Aufräumen        : 7:device-mapper-1.02.107-5.el7_2.1.x86_64                                                                                                     21/22 
  Aufräumen        : 7:device-mapper-libs-1.02.107-5.el7_2.1.x86_64                                                                                                22/22 
rhui-rhel-7-server-rhui-rpms/7Server/x86_64/productid                                                                                             | 1.7 kB  00:00:00     
rhui-rhel-7-server-rhui-supplementary-rpms/7Server/x86_64/productid                                                                               | 1.7 kB  00:00:00     
rhui-rhel-server-rhui-rhscl-7-debug-rpms/7Server/x86_64/productid                                                                                 | 1.7 kB  00:00:00     
rhui-rhel-server-rhui-rhscl-7-rpms/7Server/x86_64/productid                                                                                       | 1.7 kB  00:00:00     
  Überprüfung läuft: docker-selinux-1.9.1-40.el7.x86_64                                                                                                             1/22 
  Überprüfung läuft: 7:device-mapper-libs-1.02.107-5.el7_2.2.x86_64                                                                                                 2/22 
  Überprüfung läuft: libsemanage-python-2.1.10-18.el7.x86_64                                                                                                        3/22 
  Überprüfung läuft: docker-1.9.1-40.el7.x86_64                                                                                                                     4/22 
  Überprüfung läuft: python-IPy-0.75-6.el7.noarch                                                                                                                   5/22 
  Überprüfung läuft: 7:lvm2-2.02.130-5.el7_2.2.x86_64                                                                                                               6/22 
  Überprüfung läuft: 7:device-mapper-1.02.107-5.el7_2.2.x86_64                                                                                                      7/22 
  Überprüfung läuft: setools-libs-3.3.7-46.el7.x86_64                                                                                                               8/22 
  Überprüfung läuft: docker-forward-journald-1.9.1-40.el7.x86_64                                                                                                    9/22 
  Überprüfung läuft: 7:device-mapper-event-libs-1.02.107-5.el7_2.2.x86_64                                                                                          10/22 
  Überprüfung läuft: audit-libs-python-2.4.1-5.el7.x86_64                                                                                                          11/22 
  Überprüfung läuft: docker-common-1.9.1-40.el7.x86_64                                                                                                             12/22 
  Überprüfung läuft: checkpolicy-2.1.12-6.el7.x86_64                                                                                                               13/22 
  Überprüfung läuft: 7:device-mapper-event-1.02.107-5.el7_2.2.x86_64                                                                                               14/22 
  Überprüfung läuft: 7:lvm2-libs-2.02.130-5.el7_2.2.x86_64                                                                                                         15/22 
  Überprüfung läuft: policycoreutils-python-2.2.5-20.el7.x86_64                                                                                                    16/22 
  Überprüfung läuft: 7:device-mapper-event-libs-1.02.107-5.el7_2.1.x86_64                                                                                          17/22 
  Überprüfung läuft: 7:device-mapper-event-1.02.107-5.el7_2.1.x86_64                                                                                               18/22 
  Überprüfung läuft: 7:device-mapper-libs-1.02.107-5.el7_2.1.x86_64                                                                                                19/22 
  Überprüfung läuft: 7:lvm2-libs-2.02.130-5.el7_2.1.x86_64                                                                                                         20/22 
  Überprüfung läuft: 7:device-mapper-1.02.107-5.el7_2.1.x86_64                                                                                                     21/22 
  Überprüfung läuft: 7:lvm2-2.02.130-5.el7_2.1.x86_64                                                                                                              22/22 

Installiert:
  docker.x86_64 0:1.9.1-40.el7                                                                                                                                           

Abhängigkeit installiert:
  audit-libs-python.x86_64 0:2.4.1-5.el7                      checkpolicy.x86_64 0:2.1.12-6.el7                  docker-common.x86_64 0:1.9.1-40.el7                    
  docker-forward-journald.x86_64 0:1.9.1-40.el7               docker-selinux.x86_64 0:1.9.1-40.el7               libsemanage-python.x86_64 0:2.1.10-18.el7              
  policycoreutils-python.x86_64 0:2.2.5-20.el7                python-IPy.noarch 0:0.75-6.el7                     setools-libs.x86_64 0:3.3.7-46.el7                     

Aktualisiert:
  device-mapper.x86_64 7:1.02.107-5.el7_2.2                                     device-mapper-event-libs.x86_64 7:1.02.107-5.el7_2.2                                    

Abhängigkeit aktualisiert:
  device-mapper-event.x86_64 7:1.02.107-5.el7_2.2 device-mapper-libs.x86_64 7:1.02.107-5.el7_2.2 lvm2.x86_64 7:2.02.130-5.el7_2.2 lvm2-libs.x86_64 7:2.02.130-5.el7_2.2

Komplett!
[azureuser@clientdocker ~]$ 


## Start Docker Dämon

[azureuser@clientdocker ~]$ sudo systemctl start docker.service
[azureuser@clientdocker ~]$ sudo systemctl enable docker.service
Created symlink from /etc/systemd/system/multi-user.target.wants/docker.service to /usr/lib/systemd/system/docker.service.
[azureuser@clientdocker ~]$ systemctl status docker.service
● docker.service - Docker Application Container Engine
   Loaded: loaded (/usr/lib/systemd/system/docker.service; enabled; vendor preset: disabled)
   Active: active (running) since Mo 2016-05-30 09:51:51 UTC; 31s ago
     Docs: http://docs.docker.com
 Main PID: 3061 (sh)
   CGroup: /system.slice/docker.service
           ├─3061 /bin/sh -c /usr/bin/docker-current daemon $OPTIONS            $DOCKER_STORAGE_OPTIONS            $DOCKER_NETWORK_OPTIONS            $ADD_REGISTRY   ...
           ├─3062 /usr/bin/docker-current daemon --selinux-enabled --add-registry registry.access.redhat.com
           └─3063 /usr/bin/forward-journald -tag docker
[azureuser@clientdocker ~]$ 

## Docker-Image ziehen

[azureuser@clientdocker ~]$ sudo docker pull registry.access.redhat.com/rhel7/rhel
Using default tag: latest
c453594215e4: Download complete 
Status: Downloaded newer image for registry.access.redhat.com/rhel7/rhel:latest
registry.access.redhat.com/rhel7/rhel: this image was pulled from a legacy registry.  Important: This registry version will not be supported in future versions of docker.

[azureuser@clientdocker ~]$ 

## Listen der Docker Images 

[azureuser@clientdocker workspace]$ sudo docker images
REPOSITORY                              TAG                 IMAGE ID            CREATED             VIRTUAL SIZE
registry.access.redhat.com/rhel7/rhel   latest              c453594215e4        3 weeks ago         203.4 MB
[azureuser@clientdocker workspace]$ 

## System muss subscr. werden, damit auch docker yum klappt

[azureuser@clientdocker workspace]$ sudo subscription-manager register --username=XXXXXX
Registriere bei: subscription.rhn.redhat.com:443/subscription
Passwort: 
Das System wurde mit folgender ID registriert: cbce03a4-da5d-4308-8a86-918a52a80b7b 
[azureuser@clientdocker workspace]$ sudo subscription-manager repos --list
Diesem System stehen keine Repositorys durch Subskriptionen zur Verfügung.
[azureuser@clientdocker workspace]$ sudo subscription-manager repos --enable=rhel-7-server-extras-rpms
Fehler: rhel-7-server-extras-rpms ist kine gültige Repository-ID. Verwenden Sie die --list Option, um gültige Repositorys anzuzeigen.
[azureuser@clientdocker workspace]$ sudo subscription-manager list --available | miore
-bash: miore: Kommando nicht gefunden.
^C
User interrupted process.
[azureuser@clientdocker workspace]$ sudo subscription-manager list --available | more
+-------------------------------------------+
    Verfügbare Subskriptionen
+-------------------------------------------+
schnipp - schnapp
azureuser@clientdocker workspace]$ sudo subscription-manager attach --pool=xxxxxxxxxxxxxxxxxxxxxx
Eine Subskription wurde erfolgreich verknüpft für: Red Hat Enterprise Linux Server, Standard (Physical or Virtual Nodes)
[azureuser@clientdocker workspace]$ BB

## Custom Image erzeugen

index.html:

[azureuser@clientdocker workspace]$ cat index.html 
<html><body><p>
Nginx als Beispiel für ein Custom Image!
</p></body></html>

[azureuser@clientdocker workspace]$ 

Dockerfile:

[azureuser@clientdocker workspace]$ cat Dockerfile 
FROM registry.access.redhat.com/rhel7/rhel
MAINTAINER XXXXXX@XXXXXXXXXXXXXXXX.de

RUN yum -y update
RUN yum -y install httpd

ADD index.html /var/www/html

[azureuser@clientdocker workspace]$ 


build:

[azureuser@clientdocker workspace]$ sudo docker build -t XXXX-image-example .
Sending build context to Docker daemon 3.072 kB
Step 1 : FROM rhel7/rhel
 ---> c453594215e4
Step 2 : MAINTAINER XXXX@XXXXXXXXXXXXXX.de
 ---> Using cache
 ---> ae80e230f4b7
Step 3 : RUN yum -y update
 ---> Using cache
 ---> aba316862d53
Step 4 : RUN yum -y install nginx14
 ---> Running in 74864439675a
Loaded plugins: ovl, product-id, search-disabled-repos, subscription-manager
No package nginx14 available.
Error: Nothing to do
The command '/bin/sh -c yum -y install nginx14' returned a non-zero code: 1
[azureuser@clientdocker workspace]$ vi Dockerfile 
[azureuser@clientdocker workspace]$ sudo docker build -t xxxX-image-example .
Sending build context to Docker daemon 3.072 kB
Step 1 : FROM registry.access.redhat.com/rhel7/rhel
 ---> c453594215e4
Step 2 : MAINTAINER xxxxx@xxxxxxxxxxxxx.de 
 ---> Using cache
 ---> ae80e230f4b7
Step 3 : RUN yum -y update
 ---> Using cache
 ---> aba316862d53
Step 4 : RUN yum -y install httpd
 ---> Running in 21e74c196610
Loaded plugins: ovl, product-id, search-disabled-repos, subscription-manager
Resolving Dependencies
--> Running transaction check
---> Package httpd.x86_64 0:2.4.6-40.el7_2.1 will be installed
--> Processing Dependency: httpd-tools = 2.4.6-40.el7_2.1 for package: httpd-2.4.6-40.el7_2.1.x86_64
--> Processing Dependency: system-logos >= 7.92.1-1 for package: httpd-2.4.6-40.el7_2.1.x86_64
--> Processing Dependency: /etc/mime.types for package: httpd-2.4.6-40.el7_2.1.x86_64
--> Processing Dependency: libaprutil-1.so.0()(64bit) for package: httpd-2.4.6-40.el7_2.1.x86_64
--> Processing Dependency: libapr-1.so.0()(64bit) for package: httpd-2.4.6-40.el7_2.1.x86_64
--> Running transaction check
---> Package apr.x86_64 0:1.4.8-3.el7 will be installed
---> Package apr-util.x86_64 0:1.5.2-6.el7 will be installed
---> Package httpd-tools.x86_64 0:2.4.6-40.el7_2.1 will be installed
---> Package mailcap.noarch 0:2.1.41-2.el7 will be installed
---> Package redhat-logos.noarch 0:70.0.3-4.el7 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

================================================================================
 Package          Arch       Version               Repository              Size
================================================================================
Installing:
 httpd            x86_64     2.4.6-40.el7_2.1      rhel-7-server-rpms     1.2 M
Installing for dependencies:
 apr              x86_64     1.4.8-3.el7           rhel-7-server-rpms     103 k
 apr-util         x86_64     1.5.2-6.el7           rhel-7-server-rpms      92 k
 httpd-tools      x86_64     2.4.6-40.el7_2.1      rhel-7-server-rpms      82 k
 mailcap          noarch     2.1.41-2.el7          rhel-7-server-rpms      31 k
 redhat-logos     noarch     70.0.3-4.el7          rhel-7-server-rpms      13 M

Transaction Summary
================================================================================
Install  1 Package (+5 Dependent packages)

Total download size: 14 M
Installed size: 18 M
Downloading packages:
--------------------------------------------------------------------------------
Total                                              7.5 MB/s |  14 MB  00:01     
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
  Installing : apr-1.4.8-3.el7.x86_64                                       1/6 
  Installing : apr-util-1.5.2-6.el7.x86_64                                  2/6 
  Installing : httpd-tools-2.4.6-40.el7_2.1.x86_64                          3/6 
  Installing : mailcap-2.1.41-2.el7.noarch                                  4/6 
  Installing : redhat-logos-70.0.3-4.el7.noarch                             5/6 
  Installing : httpd-2.4.6-40.el7_2.1.x86_64                                6/6 
  Verifying  : httpd-2.4.6-40.el7_2.1.x86_64                                1/6 
  Verifying  : redhat-logos-70.0.3-4.el7.noarch                             2/6 
  Verifying  : apr-1.4.8-3.el7.x86_64                                       3/6 
  Verifying  : mailcap-2.1.41-2.el7.noarch                                  4/6 
  Verifying  : apr-util-1.5.2-6.el7.x86_64                                  5/6 
  Verifying  : httpd-tools-2.4.6-40.el7_2.1.x86_64                          6/6 

Installed:
  httpd.x86_64 0:2.4.6-40.el7_2.1                                               

Dependency Installed:
  apr.x86_64 0:1.4.8-3.el7                   apr-util.x86_64 0:1.5.2-6.el7     
  httpd-tools.x86_64 0:2.4.6-40.el7_2.1      mailcap.noarch 0:2.1.41-2.el7     
  redhat-logos.noarch 0:70.0.3-4.el7        

Complete!
 ---> 43492109a3cc
Removing intermediate container 21e74c196610
Step 5 : ADD index.html /var/www/html
 ---> 314c6d2fc438
Removing intermediate container fb5e65c65697
Successfully built 314c6d2fc438
[azureuser@clientdocker workspace]$ 

[azureuser@clientdocker workspace]$ sudo docker images
REPOSITORY                              TAG                 IMAGE ID            CREATED             VIRTUAL SIZE
xxxx-image-example                      latest              314c6d2fc438        2 minutes ago       389.1 MB
registry.access.redhat.com/rhel7/rhel   latest              c453594215e4        3 weeks ago         203.4 MB
[azureuser@clientdocker workspace]$ 

## Testweiser Start auf dem Client

[azureuser@clientdocker workspace]$ sudo docker run -d -t --name=myexample -p 80:80 -i xxxx-image-example:latest /usr/sbin/httpd -DFOREGROUND
b127f9d8c332ff34f78480821a433921f548d850ab6d4372f24503e8984ebc55
Usage of loopback devices is strongly discouraged for production use. Either use `--storage-opt dm.thinpooldev` or use `--storage-opt dm.no_warn_on_loop_devices=true` to suppress this warning.
[azureuser@clientdocker workspace]$ netstat -tupln | grep 80
(Für "-p": geteuid()=1000 konnte keine Information gelesen werden; sie sollten Root sein.)
tcp6       0      0 :::80                   :::*                    LISTEN      -                   
[azureuser@clientdocker workspace]$ curl localhost:80
<html><body><p>
Nginx als Beispiel für ein Custom Image!
</p></body></html>

[azureuser@clientdocker workspace]$ 

## Docker-Image versandfertig machen

[azureuser@clientdocker workspace]$ sudo docker save -o xxxX-image-example.tar xxxx-image-example:latest
[azureuser@clientdocker workspace]$ ls
Dockerfile  index.html  xxxx-image-example.tar
[azureuser@clientdocker workspace]$ ls -al
insgesamt 389048
drwxrwxr-x. 2 azureuser azureuser        69 30. Mai 11:13 .
drwx------. 6 azureuser azureuser      4096 30. Mai 11:04 ..
-rw-rw-r--. 1 azureuser azureuser       153 30. Mai 11:04 Dockerfile
-rw-rw-r--. 1 azureuser azureuser        78 30. Mai 10:42 index.html
-rw-r--r--. 1 root      root      398372864 30. Mai 11:14 xxxx-image-example.tar
[azureuser@clientdocker workspace]$ gzip i
index.html              xxxxx-image-example.tar  
[azureuser@clientdocker workspace]$ gzip i
index.html              xxxX-image-example.tar  
[azureuser@clientdocker workspace]$ gzip i
index.html              xxxX-image-example.tar  
[azureuser@clientdocker workspace]$ gzip i
index.html              xxxx-image-example.tar  
[azureuser@clientdocker workspace]$ gzip xxxx-image-example.tar 
[azureuser@clientdocker workspace]$ 

# Server

## image.tar.gz kopieren

## docker installieren wie vor ...

## Image importieren

[azureuser@serverdocker ~]$ sudo docker load < xxxx-image-example.tar.gz 
[azureuser@serverdocker ~]$ sudo docker images
REPOSITORY           TAG                 IMAGE ID            CREATED             VIRTUAL SIZE
xxxx-image-example   latest              314c6d2fc438        29 minutes ago      389.1 MB
[azureuser@serverdocker ~]$ sudo docker run -d -t --name=myexample -p 80:80 -i xxxX-image-example:latest /usr/sbin/httpd -DFOREGROUND
b3c1def297520f37401a904b18f68e032f6130e311d5d25d9d0fa6fcbed5972e
Usage of loopback devices is strongly discouraged for production use. Either use `--storage-opt dm.thinpooldev` or use `--storage-opt dm.no_warn_on_loop_devices=true` to suppress this warning.
[azureuser@serverdocker ~]$ curl localhost:80
<html><body><p>
Nginx als Beispiel für ein Custom Image!
</p></body></html>

[azureuser@serverdocker ~]$ 




