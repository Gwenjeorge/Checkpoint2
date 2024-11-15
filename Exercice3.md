## EXERCICE 3 

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

