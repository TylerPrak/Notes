# SSH 

###### Resources

- *https://www.ssh.com/ssh/keygen*

- ``man ssh`` 

## Setup Passwordless Login for your Server(Public Key Authentication) in 7 Easy Steps

1. ``ssh-keygen -t rsa -b 4096 -f testkey``

   * Entering this command will generate two files -  a public/private key named testkey.pub and testkey

     Once the command is entered, the program will ask you a few questions. Press enter unless you want to encrypt your key with a passphrase. After both keys are generated, we need to copy the contents of the public key file.

     Flags Explained: The ``-t`` flag chooses what algorithm to use(In this case ``rsa``) The ``-b`` flag decides bit size of the key. The ``-f`` flag takes in a parameter that chooses the name of the key files. See 1st link in [resources](#Resources) for more detail.

2. ``cd ~/.ssh/ && ls``

   * Next is changing the current directory to where ssh keys are usually stored and listing the files in that directory. Here you should see the file we just created called **testkey.pub**.

3. Copy the contents of testkey.pub to clipboard

4. Connect to your server(``ssh``)

5. ``cd ~/.ssh/ && vim testfile``

   * Like earlier in step 2), we change the current directory to where the ssh keys are stored except this time we are creating a file. 

6. Paste what we copied in step 3) into the file, then save it. 

7. ``cat testfile >> ~/.ssh/authorized_keys``

   * After saving the file, entering this command will append the contents of **testfile** into authorized_keys.

**SSHing into your server should now work without entering the password congratulations~**

## SETUP ssh-keygen for Github
``ssh-keygen -t rsa -b 4096 -c "your@email"