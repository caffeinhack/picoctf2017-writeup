# WorldChat

## Question
  > We think someone is trying to transmit a flag over WorldChat. Unfortunately, there are so many other people talking that we can't really keep track of what is going on! Go see if you can find the messenger at shell2017.picoctf.com:31955. Remember to use Ctrl-C to cut the connection if it overwhelms you!
  
## Solution
### 1. Open Terminal
   Push 'connect' button to open PicoCTF web terminal.
   
### 2. Connect Target Server With Netcat And Save File.
  Type below command and run.
  ```shell
  nc shell2017.picoctf.com 31955 >> world_chat_log
  ```
  Wait a second , and type `ctrl + c` when you are boring !  
  
### 3. Open File
  Type below command to open with vim.
  ```shell
  vim world_chat_log
  ```
  
  You can see a lot of worldcat logs.
  
### 4. Search The Flag
  We want search the flag effectively .  
  So you should use vim search function.  
  
  First type `Esc` and below command to vim.
  ```vim
  /flag
  ```
  
  And type enter, then continue checking and type `n` by you will get the `1/8 flag` ~ `8/8 flag`.  
  Concatenate `1/8 flag` ~ `8/8 flag`, you can get the flag !  
