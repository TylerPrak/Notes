# SSH
*https://www.ssh.com/ssh/keygen*

## SETUP ssh-keygen for VPS/Public Key Authentication

1. ``ssh-keygen -t rsa -b 4096 -f testkey``
   * Creates public and a private key called testkey.pub/testkeyC

2. ``cd ~/.ssh/ && ls``
   * cd and view .ssh files
3. Copy testkey.pub to clipboard
4. ssh into vps
5. ``cd ~/.ssh/ && vim testkey``
6. Paste into testkey

7. ``cat testkey >> ~/.ssh/authorized_keys``
   * Appends text from testkey file into authorized_keys
8. SSH without typing password works, try ``root@your.server.ip``

## SETUP ssh-keygen for Github
``ssh-keygen -t rsa -b 4096 -c "your@email"``



EXTRAS
-

``ssh`` & flags 

* -t dsa | ecdsa | ed25519 | rsa | rsa1
  choose algorithm to use	

* -b  
  choose key bit size 

* -f file_name 

  choose name of file to store key