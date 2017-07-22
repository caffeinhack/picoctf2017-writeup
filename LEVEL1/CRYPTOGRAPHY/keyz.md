# keyz

## Question
  > While webshells are nice, it'd be nice to be able to login directly. 
  To do so, please add your own public key to ~/.ssh/authorized_keys, using the webshell.
  Make sure to copy it correctly! The key is in the ssh banner, displayed when you login 
  remotely with ssh, to shell2017.picoctf.com
  
## Solution
### 1. Generate a SSH key
  Enter below command.
   ```shell:
   cd ~/.ssh
   ssh-keygen -t rsa -C shell2017.picoctf.com
  ```
  
### 2. Connect ssh into the server
  ```shell:
   cat id_rsa.pub > authorized_keys
  ```
  This command allows us to add the public key to be appended to the end of the authorized_keys file.
  Next go to ssh into server.
  ```shell:
   ssh shell2017.picoctf.com
  ```
### 3. Get the flag
  If you can do it,we get the flag.
  
