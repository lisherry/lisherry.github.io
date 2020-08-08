<!DOCTYPE html>
<html>
<head>
<style type="text/css">
h1 { color: green }
form { position:absolute;
       left:500px;
       top:200px;}
.like1 {
	  border:3px solid green;
	  border-radius:18px;
	  width: 300px;
      height: 30px;
      outline:none;
}
.like2 {
	  border:3px solid white;
	  border-radius:18px;
	  background:green;
	  color: white;
	  width: 60px;
      height: 30px;
      outline:none;
}

</style>

<script type="text/javascript">
function ys(x)
{x.style.background="pink";}

function yhname()              
{
	document.getElementById("name").style.background="white";
      var name = document.getElementById("name").value; 
      var tip = document.getElementById("namespan");
      var guize = /^([\u4e00-\u9fa5]|[a-zA-Z0-9]){1,10}$/i;
   if (guize.test(name)) {

               tip.innerHTML=" " ;
               return true;   } 

   else {
   tip.innerHTML="提示：用户名不规范！只能包含汉字、数字、字母，不能含有其它字符".fontcolor("red");
               return false;
        }              
}

function mima()             
{
	document.getElementById("password").style.background="white";
    var password = document.getElementById("password").value;
    var pw = document.getElementById("pwspan")
    var guize2 =  /^([a-zA-Z0-9]){6,15}$/i;
    if (guize2.test(password)) {

        pw.innerHTML=" ";
        return true ;
    }
    else {
        pw.innerHTML="密码不规范！长度须在6到15位，只能包含字母、数字，不可以含有其他符号".fontcolor("red");
        return false ;
    }
}

function alll()
	
{
	
	if (yhname()==true&&mima()==true) {
		alert("恭喜您，登录成功！")
		return true;
	}
	else {
		alert("登录失败！请重新填写信息！")
         return false;
	}
}
</script>
</head>

<body>
<h1>-------------------------------------------------用户登录------------------------------------------</h1>


<form>
<strong>用户名：</strong><br/>
<input type="text" name="name"  id="name" onfocus="ys(this)"  maxlength="10" 
        onblur="yhname()" class="like1"> 
<span id="namespan"></span>
<br/>
<strong>密码：</strong></br>
<input type="password" name="password" onfocus="ys(this)" onblur="mima()" 
        maxlength="15"  id="password" class="like1">
<span id="pwspan"></span><br/><br/>

<input type="button" name="submit" onclick="alll()" value="登录" class="like2">
</form>
</body>


 
 
 
</html>
