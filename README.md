# awsfirstec2

###############################
macchina6 

## Machine PUBLIC IP 18.134.158.156

`ssh-keygen -R 18.134.158.156`

`ssh -i mygpt.pem ubuntu@18.134.158.156`

#scp -i mygpt.pem -r your_local_folder ubuntu@13.42.65.228:/path/to/destination

##############################################################

##ssh config vscode
```
Host macchina6
    HostName 18.134.158.156
    User ubuntu
    IdentityFile "C:\Users\Frenz2\My Drive\Lesson\IFOA\IFTS-FSTACK\Less06\mygpt.pem"

```
##############################################################
### Installare Apache WebServer

`sudo apt-get install apache2 -y`

### Avvia il server web:
`sudo systemctl start apache2`

`mkdir -p /home/ubuntu/web`
`sudo nano /etc/apache2/sites-available/mysite.conf`

```
<VirtualHost *:80>
    ServerAdmin webmaster@localhost
    DocumentRoot /home/ubuntu/web
    
    <Directory /home/ubuntu/web>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>

```
#### Abilita il nuovo sito e disabilita il default
`sudo a2ensite mysite.conf`
`sudo a2dissite 000-default.conf`

#### Cambiare i permessi
`chmod 755 /home/ubuntu`

#### Restart server web
`sudo systemctl restart apache2`
