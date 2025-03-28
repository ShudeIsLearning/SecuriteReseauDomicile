<h1 align="center">SecuriteReseauDomicile</h1>

## Description
Ce projet est la procédure qui décrire les solutions de sécurité que j’ai dans mon réseau domicile. En même temps, je voudrais aussi prendre cette opportunité à faire le câblage du réseau de la maison pour rendre la connexion plus stable avec nos machines en les branchant avec un câble d’ethernet.

## Équipement
- Combinaison de modem et routeur de fournisseur accès internet
- Pare-feu Pfsense Netgate 2100
- Commutateur de TP-Link TL-SG108E
- Routeur Speedefy AC2100 (En mode Point d'accès, je vais le changer bientôt car il ne répond pas à mon besoin)

## Objectifs
- Fournir une connexion plus stable aux appareils de la maison en les branchant avec un câble d'ethernet
- Segmentation de réseau avec la fonction de VLAN
- Implémentation des règles de pare-feu pour restreint des communications ou des connexions
- Configurer des services de Pfsense pour améliorer la sécurité du réseau (Par exemple: pfBlockerNG)


## Schémas du réseau domicile
<p align="center">
  <img width="1000" height="600" src="https://github.com/ShudeIsLearning/SecuriteReseauDomicile/blob/main/Images/ReseauDomicile.jpg">
</p>

- Implémentation de Pfsense et commutateur géré pour créer des règles et des Vlans afin de renforcer la sécurité du réseau.
-	Vlan 1 : un vlan que j’ai créé pour des machines virtuelles que je dois encore faire des recherches. Il n’est pas utilisé pour le moment.
-	Vlan 2 : Un vlan  pour mon laptop de jeu. Je veux segmenter le trafic réseau des jeux pour la sécurité. 
-	Lan qui a seulement mon ordinateur de bureau auquel j’administre les autres équipements à partir de là.
-	Vlan 4 : Pour le laptop de famille.
-	Vlan 5 : Point d’accès pour répondre au besoin des connexions sans fil, regroupe ainsi les appareils comme téléphone cellulaire et ordi portable.
-	Je voulais aussi connecter une imprimante au réseau pour tout le monde a accès. Par contre, je pense que c’est un peu trop compliqué à gérer la sécurité et les mises à jour d’une imprimante. Alors je la laisse de côté. Ma famille pourrait utiliser l’imprimante avec un câble qui connecte l’ordi vers l’imprimante pour imprimer ce dont ils ont besoin.
-	Je voudrais implémenter plus tard une IDS comme Suricata avec mon Raspi pour avoir une couche de sécurité de plus dans mon réseau.

## Préface

