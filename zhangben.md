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
####  功能：

1.能够输入支出与收入，并选择类型，进行记账（静态）  

2.通过设定起始日期，查看收支记录（静态）        

#####  背景设置：

* 利用div分左右两盒子+设置左侧盒子浮动

```css
div{
    width:930px;
    height:850px;
    border:4px solid black;
    float:left;
       }
#div1 
    {background-color:#99CCCC;}
#div2 
    {background-color:#FFCCCC;}
```

#####  表格：

* 绘制表格（静态），此处仅以类别之一“日用”为例

```html
<table>
        <thead><tr>
          <th>    </th>
          <th>收入</th>
          <th>支出</th>
        </tr></thead>

       <tbody> <tr>
          <th>日用</th>
          <td width="357" height="16">0</td>
          <td width="357" height="16">38</td>
        </tr>
      </tbody>
       <tfoot> <tr>
          <th>汇总</th>
          <th>0</th>
          <th>643.8</th></tr></tfoot>
          
    </table>
```

* 设置表格样式

```css
 table th,table td{ border:1px solid #eee;}
```

#####  备注栏及类别选择键：

```html
//选择键：
 <form>
        <select>
            <option value="类型">类型</option>
            <option value="全部">全部</option>
            <option value="日用">日用</option>
            <option value="旅游">旅游</option>
            <option value="运动">运动</option>
            <option value="交通">交通</option>
            <option value="住房">住房</option>
            <option value="零食">零食</option>
            <option value="服饰">服饰</option>
            <option value="社交">社交</option>
            <option value="娱乐">娱乐</option>
            <option value="果蔬">果蔬</option>
            <option value="餐饮">餐饮</option>
        </select>
    </form>
//备注栏：
 <form  method="post" action="save.php">
        <label>&nbsp;&nbsp;备注:</label>
        <textarea cols="40" rows="3" >在这里输入内容...</textarea> 
        
```

* 注：起止日期选择与收支类型创建方法相同。 



