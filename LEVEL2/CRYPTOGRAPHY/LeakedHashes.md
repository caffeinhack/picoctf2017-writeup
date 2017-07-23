# LeakedHashes

## Question
  > Someone got hacked! Check out some service's password hashes that were leaked at hashdump.txt!
   Do you think they chose strong passwords? We should check... The service is running at shell2017.picoctf.com:4145!

## Solution
### 1. Click & Connect
  First, click 'hashdump.txt' and get text.
  There are usernames and passwords. Passwords are hashed by MD5.
  Next, click `connect` and connect to terminal.

### 2. Connect to service
  Enter below code.
  ```shell:
  nc shell2017.picoctf.com 4145
  ```
  Choose your favorite username written in 'hashdump.txt' and enter to terminal.
  Next, dehash passwords.We can dehash it easily with webtools.
  It is a link which I used.`http://www.md5portal.com`
  Enter dehashed password to terminal.
  ```shell:
  welcome to shady file server. would you like to access the cat ascii art database? y/n
  ```
  We get this string. It's almost over when I get here.

### 3. Get the flag
  Enter `y` and we can get the flag.
