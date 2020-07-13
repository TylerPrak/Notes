## /tmp 

* Store and access temporary files that is open to any user/app
* Automatically removed based on 
  1. With every reboot(Ubuntu) -- Distributions like Fedora mount a virtual filesystem using  **/tmp**  as a ram disk using the tmpfs filesystem. This means that system reboot = all information lost
  2. Cronjobs -- unless purge script to exclude
* Avoid create large files -- takes up RAM space instead of hard disk space, may cause memory overload
* Fedora distribution(may work on other but untested) -- ``sudo systemctl mask tmp.mount`` disables tmpfs for /tmp to take up hard disk, reboot for effect

