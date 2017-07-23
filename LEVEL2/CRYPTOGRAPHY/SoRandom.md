# SoRandom

## Question
  > We found sorandom.py running at shell2017.picoctf.com:19789.
    It seems to be outputting the flag but randomizing all the characters first.
    Is there anyway to get back the original flag?
    Update (text only) 16:16 EST 1 Apr Running python 2 (same version as on the server)

## Solution
### 1. Connect
  ```shell:
   nc shell2017.picoctf.com  19789
  ```
  Connecting to the provided service gives us a string.
  ```shell:
   Unguessably Randomized Flag: BNZQ:2m8807395d9os2156v70qu84sy1w2i6e
  ```
### 2. Write a decrypting program
  Looking in the 'sorandom.py', we see encrypting algorithm.
  We notice that the random generator has already been preseeded.
  It is easy to write decrypting program.
  ```shell:
  #!/usr/bin/python -u
  import random,string

  flag = "BNZQ:4pg33e44sdu4wu8198y15q685vpx8041"
  encflag = ""
  random.seed("random")
  for c in flag:
    if c.islower():
      #rotate number around alphabet a random amount
      encflag += chr((ord(c)-ord('a')-random.randrange(0,26))%26 + ord('a'))
    elif c.isupper():
      encflag += chr((ord(c)-ord('A')-random.randrange(0,26))%26 + ord('A'))
    elif c.isdigit():
      encflag += chr((ord(c)-ord('0')-random.randrange(0,10))%10 + ord('0'))
    else:
      encflag += c
  print "Unguessably Randomized Flag: "+encflag
  ```

### 3. Get the flag
  Decrypt the flag, we get the flag.
