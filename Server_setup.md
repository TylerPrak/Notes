# Server setup

1. **``adduser user_name``** 
2. **``usermod -aG sudo user_name``**
3. **``sudo apt-get update -y && apt-get install nginx -y``**

4. ### Firewall - ``ufw``    

   * *applist* - shows available apps
   * *status* - shows firewalled apps
   * *allow* 'app_name'

**e.g** ``sudo ufw allow 'Nginx Full'``

- *Nginx Full* opens, 
  - port 80 (normal, unencrypted web traffic)
  - port 443 (TLS/SSL encrypted traffic)

5. ### Install certificate

   * Certbot **PPA**(Personal Package Archive)
     ``sudo apt-get update
     sudo apt-get install software-properties-common
     sudo add-apt-repository universe
     sudo add-apt-repository ppa:certbot/certbot
     sudo apt-get update``

   * Installs certbot

     ``sudo apt-get install certbot python-certbot-nginx``                  

   * Get/Install certificate w automatic configure

     ``sudo certbot --nginx``

6. ### Certificate Renew

   * Test Auto Renewal by running

     ``sudo certbot renew --dry-run``

   Certbot packages has cron job/systemd timer that renew certificates automatically before expire installed in 
   */etc/crontab/*   */etc/cron./*  *systemctl list-timers*

7. ### Confirm cert works by going to site and seeing a lock next to URL

## EXTRA 

``Crontab`` command & flag options  

* -l cats cron job file

* -e edit cron job file

* -u user_name -e edit file for another user
  [Cronjob format generator](https://crontab.guru/) 
  **e.g** *Renew certificate every 90 days on the 1st day*
  ``0 0 1 3,6,9,12 * certbot renew``

  