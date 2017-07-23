# computeRSA

## Question
  > RSA encryption/decryption is based on a formula that anyone can
  find and use, as long as they know the values to plug in.
  Given the encrypted number 150815, d = 1941, and N = 435979,
  what is the decrypted number?

## Solution
### 1.Decrypting number
   You can decrypt number using this equation.
   ```shell:
   decrypted = (encrypted) ^ d mod N
   ```
   Using python, we can decrypt it easily.
   ```shell:
   pow(150815,1941,435979)
   ```
   We get the decrypted number.
