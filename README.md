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

&ensp;
## Préface
Ça fait un bon bout de temps que j’ai configuré mon réseau donc je n’ai pas eu la chance de documenter chaque étape. Alors il manquera certainement des captures écrans ici et là. J'ai aussi refait le câblage de la maison au fur et à mesure dans chaque étape avec des câbles d'ethernet que j'ai acheté chez Bestbuy ainsi une agrafeuse pour câble.

## Étape 1: Activer le « bridge mode » dans la page admin du routeur/modem de FAI (Fournisseur accès internet)
Il faut tout d’abord activer l’option bridge mode du routeur/modem de FAI. Cette option vise à amener la connexion internet à l’intérieur de votre maison et vous laisse aussi la possibilité à utiliser des équipements, notamment un pare-feu ou un routeur, sous votre contrôle.

Dans mon cas, les informations pour se connecter dans la page admin sont écrites en arrière du routeur/modem de FAI et j’ai réussi à activer l’option « bridge mode » . Il est aussi le bon moment à <mark>**changer le mot de passe par défaut du compte admin**</mark> pour augmenter le niveau de sécurité. 

Certains routeurs ou modems nécessitent l’installation d’une application pour faire les changements. Ou dans certains cas, nécessite une commande cmd « ipconfig » pour trouver l’adresse IP de la page admin avec l’information du « Défault Gateway ». Néanmoins, tout est trouvable avec une petite recherche google. 


## Étape 2: Configuration de la boîte Pfsense SG-2100

Malheureusement je n’ai pas de capture d’écran ni de documentation pour la configuration de Pfsense. Par contre, j’ai suivi la vidéo suivante pour me guider dans la configuration :
https://www.youtube.com/watch?v=fsdm5uc_LsU

Malgré que la vidéo date depuis 4 ans, les éléments essentiels sont les mêmes.

Selon la documentation de Pfsense, la configuration par défaut devrait être le plus sécuritaire donc il n'y a aucun problème à l'utilisé une fois que la boîte est configurée.

Cependant, je veux créer des Vlans, donc je navigue....(continue avec des captures d'écran)

## Étape 3:


