# Brute force mot de passe   

___

Les étapes :     
**ifconfig** pour avoir le masque sous réseau et en déduire l'IP du réseau   
Scan du réseau pour voir l'ensemble des ports ouverts et des machines connectées avec **nmap IP du réseau**    
Obtenir des infos sur la cible (son adresse IP, ses ports ouverts, les statuts des ports et les services qu'ils utilisent, son adresse mac, son OS)   
avec **nmap -O IP de la machine connectée** et **nmap --script default IP de la machine connectée au réseau**          
Scan des vulnérabilités avec **nmpap -v --script vuln IP de la machine connectée**  
____

![image](https://github.com/techerbeatrice/brute_force_mot_de_passe/assets/138071140/2fd3b248-1870-4147-9fc5-da17a689d2b6)

![image](https://github.com/techerbeatrice/brute_force_mot_de_passe/assets/138071140/03415c7f-de60-4abb-812c-adda0fd781fb)

https://gist.githubusercontent.com/techerbeatrice/8204e406ba94922aba76167b08c2c38e/raw/fad76d1f4dc16377b9ecd98f9f6f52c13e6a4443/gistfile1.txt


![image](https://github.com/techerbeatrice/brute_force_mot_de_passe/assets/138071140/419dbeba-f18e-4c21-9d4c-df2f7cbbadfb)
