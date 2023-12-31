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
Dans notre cas, j'ai attribué l'IP 192.168.2.254 /24 à l'interface lan   

on peut administer pfsense via **http://192.168.2.254** qui est l'interface graphique de gestion de pfsense      

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/21d22605-469f-44b1-a206-38fe35fbd641)

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/07ecaa95-b59a-49f5-860a-d29360cdf9cb)

____

Créer deux machines virtuelles : une pour le poste d'administration et une pour le client test.   
Les deux machines virtuelles sont connectées à l'interface LAN de pfSense.   

____
 VM poste d'administration pfsense, login par défaut  **admin / pfsense** :    
 
![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/292f1022-e715-4470-9dec-1793bc39949a)

___

Attribuer une ip statique à la VM cliente et vérifier qu'elle a accès à internet    

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/fc4deab7-5150-4907-964a-17dc4f059844)

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/c268b6f3-514e-4c79-b6c7-b20b96d498e4)

____

Mettre en place une règle de filtrage réseau sur pfsense pour interdire à la machine cliente de sortir du réseau interne   

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/4a318a5e-95b0-4836-8947-996bcdf62fc6)

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/6a657649-909e-4645-9de1-6c067537b9d5)

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/212963bc-e907-4969-9fc8-c84c2e6df83c)

____

Vérification que la VM cliente ne puisse plus accéder à internet   

![image](https://github.com/techerbeatrice/installation_pfsense/assets/138071140/fa70a4ec-a91c-4281-9282-1176d2486bb8)


