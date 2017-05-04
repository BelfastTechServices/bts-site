bts
==============

# Setup - multiple domains/ssl sites

```
sudo nano /etc/apache2/sites-available/bts-ssl.conf

sudo a2ensite bts-ssl; sudo service apache2 restart

cd; sudo add-apt-repository ppa:certbot/certbot; sudo apt-get update; sudo apt-get install python-certbot-apache

sudo certbot --apache -d belfasttechservices.co.uk -d www.belfasttechservices.co.uk --agree-tos --renew-by-default --no-redirect
```

# install

## git instructions

```
sudo rm -rf bts-site /var/www/bts-ssl

### https url

git clone https://github.com/chris18890/bts-site.git

### git url

eval $(ssh-agent -s); ssh-add .ssh/github_rsa

git clone git@github.com:chris18890/bts-site.git

sudo cp -r bts-site/bts/ /var/www/bts-ssl
```
