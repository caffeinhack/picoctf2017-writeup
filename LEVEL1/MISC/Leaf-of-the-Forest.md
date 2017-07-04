# Leaf of the Forest

## Question
  > We found an even bigger directory tree hiding a flag starting at /problems/3a36b3b0858a593882b7d6a0dc5bd2f9. It would be impossible to find the file named flag manually...
  
## Solution
  1. First, Open web terminal and move current directory.

  2. And, type command like here and you can get the flag .
  ```shell
  cat `find /problems/3a36b3b0858a593882b7d6a0dc5bd2f9/ -name flag`
  ```
