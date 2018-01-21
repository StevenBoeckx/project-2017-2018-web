# Raspberry-pi installatie om te gebruiken als server
Deze 'tutorial' gaat er vanuit dat je raspberry pi boot met een OS.

## Apache
#### Installatie
Installeren van alle packages voor apache server
```sh
sudo apt-get install apache2 php libapache2-mod-php
```
#### Instellingen
+ De juiste folders instellen waar de website staat in de *.conf file (etc/apache2/)
+ Alle routes redirecten naar index.php
## Mysql
#### Installatie
Eerst zorgen dat alles up-to-date is
```sh
sudo apt-get update && sudo apt-get upgrade
```
Installeren van de mysql server
```sh
sudo apt-get install mysql-server --fix-missing
```
Installeren van de mysql client voor de database intestestellen
```sh
sudo apt-get install mysql-client
```
#### Instellingen
+ bind address in *my.cnf* in comment zetten
+ users toevoegen met minimale autiriteit
+ nieuwe database toevoegen

## Lets-encrypt
Gekopieerd uit markdown van **Ruben Charlier**
Installeren

    sudo apt-get install python-certbot-apache
    
Certificaat aanvragen

    sudo certbot certonly --standalone --preferred-challenges http -d example.com

Config files in apache automatisch aanpassen

    sudo certbot --apache
    
Waar staan mijn certificaten?
```
    1) sudo ls /etc/letsencrypt/live/slimmeparking.hopto.org    //hier vindt je de certificaten terug
    2) nakijken van certificaat met die commando: 
    3) sudo nano /etc/apache2/sites-available/default-ssl.conf
    4) SSLEngine on
	   SSLCertificateFile    /etc/letsencrypt/live/yourdomain.com/cert.pem
	   SSLCertificateKeyFile /etc/letsencrypt/live/yourdomain.com/privkey.pem
	   SSLCertificateChainFile /etc/letsencrypt/live/yourdomain.com/fullchain.pem
```
