# 帐本网页 

### 一、登陆界面  

######         1.标题“我的帐本”  

######         2.用户名输入栏  

######         3.密码输入栏  

######         4.“确定”与“重置”按钮  

######         5.背景图  

####  功能：

* 输入用户名与密码，点击确定后，若用户名及密码正确，则跳转至主界面，否则跳出alert提示框。  

```javascript
 function Wopen(){
    var pw="123456";
    var un="bbt";
    var password=document.getElementById("password").value;
    var username=document.getElementById("myName").value;
    if((username==un)&&(password==pw))
      {window.location.href="界面.html";}
    else
    {alert("密码错误，登陆失败");}
  }
```

##### 背景设置：

* 使用文件夹中命名为”背景“的自定义图片，设置为居中、固定、覆盖整个界面。  

  ```css
   body{
           background-image:url(背景.jpg);
           background-size:cover;
           background-position: center center;
           background-repeat: no-repeat;
           background-attachment:fixed;
          }
  ```

#####  输入框及按钮+设置固定用户名及密码：

* 插入文本输入框，用户输入用户名和密码。

* 使用<input> 插入表单中的重置与提交按钮。 

* 使用js语言进行设定。   

  ```javascript
  用户名：
      <input  type="text"  name="myName" id="myName" />
  密码：
  	<input  type="password"  name="password"  id="password" />
  	<input   type="submit"   onClick="Wopen()" value="确定" ;>	
  	<input type="reset" value="重置">
  
  function Wopen(){
      var pw="123456";
      var un="bbt";
      var password=document.getElementById("password").value;
      var username=document.getElementById("myName").value;}
  
  ```

#####  alert及跳转：

```javascript
 if((username==un)&&(password==pw))
      {window.location.href="界面.html";}
    else
    {alert("密码错误，登陆失败");}
```





###  二、帐本主界面

          ######           1.记录当天收支的数字输入框

######           2.备注

######           3.收支记录表

######           4.”概览“之中的起止日期



