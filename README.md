<!DOCTYPE html>
<html>
<head>

<title>Prime FF Gaming</title>

<meta name="viewport" content="width=device-width, initial-scale=1">

<style>

body{
margin:0;
font-family:Arial;
color:white;
text-align:center;

background:url("https://wallpapercave.com/wp/wp5128415.jpg");
background-size:cover;
}

/* header */

header{
background:black;
padding:10px;
color:red;
}

/* menu */

nav a{
color:white;
margin:10px;
text-decoration:none;
}

/* box */

.box{
background:rgba(0,0,0,0.7);
margin:20px;
padding:20px;
border-radius:10px;
}

/* button */

button{
background:red;
color:white;
border:none;
padding:10px 20px;
}

/* login */

#login{
display:none;
}

/* admin */

#admin{
display:none;
}

/* marquee */

marquee{
background:red;
padding:5px;
}

</style>

</head>

<body>

<header>

<h2>Prime FF Gaming</h2>

<nav>

<a href="#" onclick="home()">Home</a>
<a href="#" onclick="showLogin()">Login</a>
<a href="#" onclick="showAdmin()">Admin</a>

</nav>

</header>


<marquee>
Welcome To Prime FF Gaming Official Website
</marquee>



<div class="box">

<h3>Visitor Counter</h3>

<p id="visit"></p>

</div>



<div class="box">

<h3>Latest Video</h3>

<iframe width="300" height="200"
src="https://www.youtube.com/embed/YOURVIDEOID">
</iframe>

</div>



<div class="box">

<h3>Comment</h3>

<input id="c">

<button onclick="addComment()">Send</button>

<p id="show"></p>

</div>



<div id="login" class="box">

<h3>Login</h3>

<input id="user" placeholder="user">

<br><br>

<input id="pass" placeholder="pass">

<br><br>

<button onclick="login()">Login</button>

</div>



<div id="admin" class="box">

<h3>Admin Panel</h3>

<p>Welcome Admin</p>

<button onclick="alert('Admin setting')">
Setting
</button>

</div>



<div class="box">

<h3>Subscribe</h3>

<a href="https://youtube.com">

<button>Subscribe Channel</button>

</a>

</div>



<script>

/* visitor */

let v = localStorage.getItem("v")

if(v==null){v=1}else{v++}

localStorage.setItem("v",v)

document.getElementById("visit").innerHTML=v



/* comment */

function addComment(){

let c=document.getElementById("c").value

document.getElementById("show").innerHTML=c

}



/* login */

function showLogin(){

document.getElementById("login").style.display="block"

}



function login(){

let u=document.getElementById("user").value

let p=document.getElementById("pass").value

if(u=="admin" && p=="1234"){

alert("login ok")

document.getElementById("admin").style.display="block"

}else{

alert("wrong")

}

}



function showAdmin(){

document.getElementById("admin").style.display="block"

}


</script>

</body>
</html>
