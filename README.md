# Installation du firewall PfSense
___

Après avoir téléchargé l'image iso du site officiel  

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/3b778182-9eff-4a20-90f1-decc221a016b)

_____

Création de la VM PfSense   

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/1e6d9f10-f224-4fd0-a831-42dc7fe25787)

________

Configuration des 2 interfaces dans la partie réseau   
Une interface constitue l'accès à l'extérieur via **un pont**, appelé **WAN** du point de vue de pfSense   
L'autre sert de connexion avec **réseau interne** que pfSense appelle **LAN**    

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/f1b9f30c-2424-488d-857a-71a3356da60f)

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/0ab05f92-6db2-44eb-8441-513b6fead3ee)

_____

A cette étape d'installation, appuyer sur la barre d'espace pour valider le disque sélectionné   

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/fca55ae5-c4a2-49e3-974c-9c896aec15b5)

____

Au redémarrage, affichage des 2 interfaces wan et lan  
PfSense a attribué l'interface wan à em0 et a récupéré une adresse IP,   
il a attribué également l'interface lan à em1 et a récupéré une adresse IP   

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/faef0ca0-e500-4b08-aca1-b14fe9a00f8c)

____

Modifier l'adresse IP l'interface lan pour pouvoir administrer pfsense à partir d'une vm qui sera dans le réseau interne   
Dans notre cas, j'ai attribué l'IP 192.168.2.1 /24 à l'interface lan   

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/705013b4-2fd4-48fd-9ed0-5a2c0549251e)

_____

on peut administer pfsense via https://192.168.2.1 qui est l'interface graphique de gestion de pfsense   

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/0190869a-b3fc-43d4-bf3b-06efc2857fbc)




