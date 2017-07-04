# looooong

## Question
  > I heard you have some "delusions of grandeur" about your typing speed. How fast can you go at shell2017.picoctf.com:59858?
  
## Solution
  First you can't type in time, so you should solve with programming.

### 1. Programming Program
  Programming program save answer strings to file.
  Make file in your PC and edit like here.
  
  ```python
  # input target char and string length
  length = input()
  length = int(length)
  char = input()
  result = ''
  
  # make file which have answer string
  f = open('hoge.txt', 'w')
  for count in range(0, length):
    result += char
  
  f.write(result)
  ```
  
### 2. Connect Target With Netcat
  Connect your web terminal and type like here.
  ```shell
  nc shell2017.picoctf.com 59858
  ```
  you may be told a question.
  
### 3. Run program and get answer
  Type like here to run your program.
  ```shell
  python3 $filename
  ```
  For example,
  ```shell
  python3 spam.py
  ```
  Then, type character of the question, enter and characters length.  
  
  After running program, open `hoge.txt` with your editor and copy all characters.  
  
### 4. Get Flag
  Paste to web terminal with `ctrl + shift + V` and type specified character.  
  You can get the flag !  
  
  
