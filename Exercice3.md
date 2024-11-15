## EXERCICE 3 

## PARTIE 1 - ROUTAGE 

##### QUESTION 1  
C'est un switch, il permet de connecter les différentes PC à la passerelle sur le routeur via 
un lien unique.  

##### QUESTION 2  

C'est un routeur, il permet de router le trafic du réseau 10.10.0.0/16 vers d'autres réseaux extérieurs. 
Par exemple le réseau 10.12.2.0/24 qui lui est directement connecté.

##### QUESTION 3  

f0/0 est l'interface du routeur sur le réseau 10.10.0.0/16  
g1/0 est l'interface du routeur sur le réseau 10.12.2.0/24  

##### QUESTION 4  
C'est le CIDR, les 16bits du masque réseau, qui définit la partie réseau de l'adresse IP de PC2, en l'état : "10.11"

##### QUESTION 5  

C'est l'adresse de l'interface du routeur, qui, si il est correctement configuré, doit être sa passerelle.  

##### QUESTION 6  

PC1 : 10.10.4.1/16  
Réseau : 10.10.0.0/16  
Host min : 10.10.0.1  
Host max : 10.10.255.254  
Broadcast :10.10.255.255  

PC2 :10.11.80.2/16  
Réseau : 10.11.0.0/16  
Host min : 10.11.0.1  
Host max : 10.11.255.254  
Broadcast : 10.11.255.255  

PC5 :10.10.4.7/15  
Réseau : 10.10.0.0/15  
Host min : 10.10.0.0  
Host max : 10.11.255.254  
Broadcast : 10.11.255.255   

##### QUESTION 7  

Les PC1, PC3, PC4 vont tous pouvoir communiquer car appartiennent au même réseau 10.10.0.0/16.  
En revanche le PC2 et le PC5, appartenant respectivement aux réseaux 10.11.0.0/16 et 10.10.0.0/15, ne peuvent communiquer avec les autres sans un dispositif de routage (que le switch n'apporte pas dans le cas présent)  

##### QUESTION 8  

Seul les PC1, PC3 et PC4 pourront utiliser la passerelle du routeur dans le même réseau et pourront donc traverser le routeur.  

##### QUESTION 9  
Aucune incidence  

##### QUESTION 10  
Installer un serveur DHCP (sur le routeur par exemple ou sur un des postes).  
Modifier les configurations de chaque ordinateur pour les passer en dynamique.  

## PARTIE 2 - WIRESHARK  

#### FICHIER 1  

##### QUESTION 11  

Il s'agit de 00:50:79:66:68:00 qui est PC1.  

##### QUESTION 12  

Oui elle a réussi. Il s'agit d'un ping entre PC1 et PC2

##### QUESTION 13  

PC1 
MAC : 00:50:79:66:68:00  
IP :  10.10.4.1  

PC2  
MAC : 00:50:79:66:68:03  
IP : 10.10.4.2  

##### QUESTION 14  

Protocole ARP. Son rôle est de résoudre des des IP à des adresses MACS 

##### QUESTION 15

Le routeur B n'a pas de rôle.
Le switch A diffuse la requête ARP sur tous le réseau, puis redirige la réponse de PC4 vers PC1

#### FICHIER 2

##### QUESTION 16  

10.10.80.3. Il s'agit de PC3

##### QUESTION 17  

Il s'agit d'une requête ping. Il attends une réponse qui permet de vérifier si l'hôte interrogé est joignable.  

##### QUESTION 18  

Non la communication n'a pas réussi. Bien qu'étant physiquement le même réseau, la cible est dans un autre réseau logique.

##### QUESTION 19  

C'est une réponse de la passerelle du routeur dans le réseau local. La ping a tenté par défaut de sortir par cette passerelle 
pour chercher un potentiel 10.11.80.2 mais le routeur ne connaissant pas la route vers cette IP lui a répondu que la destination n'était pas atteignable.

##### QUESTION 20

Le rôle du switch  est de transmettre les paquets dans un même réseau ce qui n'est pas le cas. Donc il n'a eu aucun rôle
Le rôle du routeur est de transmettre des les paquets entre différents réseau. Il a donc tenté de le faire mais ne connaissait pas de chemin vers le réseau 
10.11.0.0.16.

#### FICHIER 3

##### QUESTION 21

10.10.4.2 : PC4
172.16.5.253 : Interface du deuxième routeur R2

##### QUESTION 22  

CA:01:DA:D2:00:1C  : MAC de l'interface du router r1 dans le réseau 10.12.2.0/24
CA:03:9E:EF:00:38  : MAC de l'interface du router r2 dans le réseau 10.12.2.0/24

##### QUESTION 23

L'enregistrement est faites sur le routeur R1





Modifier les configurations de chaque ordinateur pour les passer en dynamique.  

