
### LOAD MODULE
sudo ln -s /etc/apache2/mods-available/cgi.load /etc/apache2/mods-enabled/

### EDIT HOST
sudo nano /etc/apache2/sites-available/000-default.conf

### HOST FILE

```bash
<VirtualHost *:80>

        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/html
        ScriptAlias "/cgi-bin/" "/var/www/html/cgi-bin/"

        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined

</VirtualHost>

```
sudo systemctl status apache2
sudo systemctl restart apache2
