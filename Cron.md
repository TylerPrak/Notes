# **Cron**

###### Resources

- ``man cron``

Native linux utility that allows commands to be run at a certain schedule 

| Crontab |                                            |
| ------- | ------------------------------------------ |
|         | -l cats cron job file                      |
|         | -e edit cron job file                      |
|         | -u user_name -e edit file for another user |
|         | https://crontab.guru/                      |
|         | format generator                           |
|         | e.g                                        |
|         | 0 0 1 3,6,9,12 * certbot renew             |
|         | Renew every 90 days on the 1st day         |