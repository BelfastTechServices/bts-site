bts
==============

# Setup - multiple domains/ssl sites

```
sudo nano /etc/apache2/sites-available/bts-ssl.conf

sudo a2ensite bts-ssl; sudo service apache2 restart

cd; wget https://dl.eff.org/certbot-auto; chmod a+x certbot-auto

sudo ./certbot-auto --apache -d belfasttechservices.co.uk -d www.belfasttechservices.co.uk --agree-tos --renew-by-default --no-redirect
```

# install

## git instructions

```
sudo rm -rf bts-site /var/www/bts-ssl

git clone https://github.com/chris18890/bts-site.git

sudo cp -r bts-site/bts/ /var/www/bts-ssl
```
