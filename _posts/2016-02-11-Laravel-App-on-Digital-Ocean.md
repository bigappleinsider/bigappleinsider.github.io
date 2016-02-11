---
layout: post
title: Laravel App on Digital Ocean
---
Get your $10 credit @DigitalOcean - that's 2 month of server time - 512 MB/ 1 CPU/ 20 GB SSD/ 1000 GB Transfer https://www.digitalocean.com/?refcode=40a47f269a5b

1. **Copy Keys**
`ssh-copy-id user@123.45.56.78`
or 
`cat ~/.ssh/id_rsa.pub | ssh user@123.45.56.78 "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys"`
https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2

2. Error logs: /var/log/apache/error.log

3. **Installing composer**
`curl -sS https://getcomposer.org/installer | php
mv composer.phar /usr/local/bin/composer`
https://getcomposer.org/doc/00-intro.md

4. **Installing curl**
`sudo apt-get update
sudo apt-get install php5-curl`

5. **Add swap memory**

 * First try to run composer this way: 

`php -d memory_limit=-1 /usr/local/bin/composer update`
If it works, just add memory_limit=-1 to your php.ini and you should be good.

 * If it doesn't and your box is a Homestead or Ubuntu, check if you have swap memory in your server:

`free -h`

And you should see something like:
Swap: 2.0G 93M 1.9G

If you don't, you better add some to your box:

    sudo dd if=/dev/zero of=/swapfile bs=1024 count=2048k
    sudo mkswap /swapfile
    sudo swapon -a
    echo "/swapfile none swap sw 0 0" | sudo tee -a /etc/fstab
    echo 10 | sudo tee /proc/sys/vm/swappiness
    echo vm.swappiness = 10 | sudo tee -a /etc/sysctl.conf
    chown root:root /swapfile
    sudo chmod 0600 /swapfile
https://laracasts.com/discuss/channels/forge/laravel-5-deploy

**Enable rewrite module**

`sudo a2enmod rewrite
sudo service apache 2 restart`
