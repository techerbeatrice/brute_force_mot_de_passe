# Brute force mot de passe   

___

Les étapes :     
**ifconfig** pour avoir le masque sous réseau et en déduire l'IP du réseau   
Scan du réseau pour voir l'ensemble des ports ouverts et des machines connectées avec **nmap IP du réseau**    
Obtenir des infos sur la cible (son adresse IP, ses ports ouverts, les statuts des ports et les services qu'ils utilisent, son adresse mac, son OS)   
avec **nmap -O IP de la machine connectée** et **nmap --script default IP de la machine connectée au réseau**          
Scan des vulnérabilités avec **nmpap -v --script vuln IP de la machine connectée**  
____

![image](https://github.com/techerbeatrice/brute_force_mot_de_passe/assets/138071140/6cb1fc55-2bb3-454e-ba26-3e3463fa15a6)

![image](https://github.com/techerbeatrice/brute_force_mot_de_passe/assets/138071140/03415c7f-de60-4abb-812c-adda0fd781fb)


