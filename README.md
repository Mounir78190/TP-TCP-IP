# TP : TCP/IP

### Table des Matières
1. Introduction
2. Liste-des-manipulations-réalisées
3. Problèmes-rencontrés-et-solutions
4. Analyse-théorique
5. Conclusion
6. Ressources
7. QCM

## 1. Introduction :

Cette évaluation se concentre sur la compréhension pratique des protocoles TCP/IP et UDP dans le cadre des réseaux modernes. Les principaux objectifs sont de démontrer la configuration,
le dépannage et l'analyse des protocoles de communication, y compris des protocoles complémentaires comme DHCP et ARP. Ce README sert de référence pour reproduire les exercices et résoudre les problèmes rencontrés.

## 2. Liste des manipulations réalisées :

###
1. Création de trois routeurs sur cisco :

* Adressage IP interface 0/0 :
  AD : Ipv4 : 192.168.1.1 mask 255.255.255.0
  ![image Ip-AD.](https://imgur.com/howwJE7.png)

  TECH : Ipv4 : 192.168.2.1 mask 255.255.255.0
   ![image Ip-TECH.](https://imgur.com/079TEXS.png)

  COMM : Ipv4 : 192.168.3.1 mask 255.255.255.0
  ![image Ip-COMM.](https://imgur.com/BDoixxy.png)

* Adressage IP interface 0/1 :
    AD : Ipv4 : 10.0.0.1 mask 255.255.255.0
  ![image Ip-AD.](https://imgur.com/Ddp01iO.png)

  TECH : Ipv4 : 10.0.0.2 mask 255.255.255.0
   ![image Ip-TECH.](https://imgur.com/aRuP0c3.png)

  COMM : Ipv4 : 10.0.0.3 mask 255.255.255.0
  ![image Ip-COMM.](https://imgur.com/sZl2oUi.png)


2. Relier les routeurs par un switch.
  
3. Création de trois serveurs pour les sous-réseaux administratif, commercial et technique :

* Adressage IP des trois serveur :
AD-SRV : Ipv4 : 192.168.1.10 mask : 255.255.255.0 passerelle : 192.168.1.1 dns : 8.8.8.8 :
  ![image Ip-AD-SRV.](https://imgur.com/Ots3yrw.png)

TECH-SRV : Ipv4 : 192.168.2.10 mask : 255.255.255.0 passerelle : 192.168.2.1 dns : 8.8.8.8 :
  ![image Ip-TECH-SRV.](https://imgur.com/pmkclIC.png)

COMM-SRV : Ipv4 : 192.168.3.10 mask : 255.255.255.0 passerelle : 192.168.3.1 dns : 8.8.8.8 :
  ![image Ip-COMM-SRV.](https://imgur.com/1jYf489.png)

4. Création de trois pc client pour chaque sous-réseau avec leur adressage :

    ![image Architecture.](https://imgur.com/aH3JqG4.png)

* Adressage IP des trois pc :
AD-CLI : Ipv4 : 192.168.1.100 mask : 255.255.255.0 passerelle : 192.168.1.1 dns : 8.8.8.8 :
  ![image Ip-AD-SRV.](https://imgur.com/Cl42WYe.png)

TECH-CLI : Ipv4 : 192.168.2.100 mask : 255.255.255.0 passerelle : 192.168.2.1 dns : 8.8.8.8 :
  ![image Ip-TECH-SRV.](https://imgur.com/ix6xobA.png)

COMM-CLI : Ipv4 : 192.168.3.100 mask : 255.255.255.0 passerelle : 192.168.3.1 dns : 8.8.8.8 :
  ![image Ip-COMM-SRV.](https://imgur.com/SWqWWGg.png)

5. Analyse des Performances Réseau avec le simulateur de cisco :

![Analyse des Preformances.](https://imgur.com/TZNaNsL.png)

6. Etude compartive : TCP vs UDP dans un environnement simulé :

* Simulation d'envoi de paquets avec TCP :
  Analyse des performances après avoir filtré les paquets TCP et avoir selectionné l'adresse du serveur.
![Analyse des Preformances TCP.](https://imgur.com/nrZV1dv.png)
![Analyse des Preformances TCP.](https://imgur.com/rNUl3yj.png)

* Simulation d'envoi de paquets avec UDP :
  Analyse des performances après avoir configuré un trafic generator :
  ![Config trafic.](https://imgur.com/G7JSHMS.png)
  ![Analyse des performences UDP](https://imgur.com/TAoRptv.png) 

   
## 3. Problèmes Rencontrés et Solutions

### Problème 1: Conflit d'Adresse IP
* Description : Erreur de conflit d'adresse IP lors de la configuration de l'IP statique.
* Solution : Vérification du réseau pour d'autres appareils utilisant la même adresse IP et reconfiguration à une adresse disponible.
  
### Problème 2: Pas de Wireshark pour la Capture de Paquets
* Description : Impossibilité d'utiliser Wireshark sur Cisco.
* Solution : Vérification du réseau avec le simulateur de Cisco, ce qui permet d'avoir un visuel sur les comportements des paquets.

## 4. Analyse Théorique

Le protocole TCP/IP est fondamental pour les réseaux modernes, permettant l'interopérabilité entre différents systèmes. 
TCP offre une transmission fiable, ordonnée et avec contrôle d'erreurs, adaptée aux applications où la précision est critique, 
comme la navigation web et les emails. En revanche, UDP fournit une transmission plus rapide et sans connexion, 
idéale pour les applications en temps réel comme le streaming vidéo et les jeux en ligne.

## 5. Conclusion

Cette évaluation pratique a renforcé notre compréhension des protocoles TCP/IP et UDP, y compris leurs configurations et techniques de dépannage. 
L'expérience pratique, combinée aux connaissances théoriques, a considérablement amélioré notre compréhension de la connectivité et de la performance réseau.

## 6. Ressources

Documentation de Cisco : 
* https://www.netacad.com/resources/lab-downloads?courseLang=en-US
  
Suite de Protocoles TCP/IP :
* https://tools.ietf.org/html/rfc791, https://tools.ietf.org/html/rfc793

## 7. QCM

Quelle est la principale différence entre TCP et UDP ?
  * A. TCP garantit la fiabilité, UDP est plus rapide. 

Quelle couche du modèle TCP/IP gère le routage des paquets ?
  * C. Internet 

Quel protocole est utilisé pour résoudre une adresse IP en adresse MAC ?
  * C. ARP 

Quelle est la taille d'une adresse IPv6 ?
  * C. 128 bits 

Quel outil permet d’analyser les performances d’un réseau en capturant les paquets ?
  * B. Wireshark 
