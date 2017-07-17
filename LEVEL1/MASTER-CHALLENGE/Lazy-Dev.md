# Lazy Dev
## Question
  > I really need to login to this [website](http://shell2017.picoctf.com:4370/), but the developer hasn't implemented login yet. Can you help?
  
## Solution
### 1. Open Website Source Code
  First, Open target site and display source code.
  If you use chrome, you can access here and check source code.
  > view-source:http://shell2017.picoctf.com:4370/  

  You can know that the `Submit` button call `process_password()` when you click it from here.
  ```html
      <button type="button" onclick="process_password()">Submit</button>
  ```

### 2. Open And Check `/static/client.js`.
  Second, When you see target\'s source code, you may find that `process_password()` is in `/static/client.js`.  
  So check `/static/client.js`.
  
  You can see and find `validate()` is function of validating the password and it have never implemented. So it return only `false`.
  
### 3. Override `validate()`
  Finally, type to console of chrome developer tools, and override function like here.(chrome developer tool can open with `F12`.)
  ```js
  function validate(){
    return true;
  }
  ```
  And push `Submit` button, you may get the flag !
