# SSH
*https://www.ssh.com/ssh/keygen*

## SETUP ssh-keygen for VPS

1. ``ssh-keygen -t rsa -b 4096 -f testkey``

* Creates public and a private key called testkey.pub/testkeyC

2. ``cd ~/.ssh/ && ls``

* cd and view .ssh files

3. copy testkey.pub to clipboard
4. ssh into vps
5. cd ~/.ssh/ && vim testkey
6. paste into testkey

7. ``cat testkey >> ~/.ssh/authorized_keys``
   * Appends text from testkey file into authorized_keys
8. SSH without typing password works root@ip

## SETUP ssh-keygen for Github
``ssh-keygen -t rsa -b 4096 -c "your@email"``

EXTRAS
-

ssh
* t dsa | ecdsa | ed25519 | rsa | rsa1
choose algorithm to use	
* b  
choose key bit size
* f choose name of file to store key
file_name