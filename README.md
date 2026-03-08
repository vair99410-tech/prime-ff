<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Animated Login Form</title>

<style>

body{
margin:0;
height:100vh;
display:flex;
justify-content:center;
align-items:center;
background:linear-gradient(135deg,#4facfe,#00f2fe);
font-family:Arial;
}

/* Login Box */

.container{
width:320px;
padding:40px;
background:white;
border-radius:15px;
box-shadow:0 10px 30px rgba(0,0,0,0.2);
text-align:center;

/* Animation */
transform:scale(0);
animation:popup 0.8s forwards;
}

@keyframes popup{
0%{
transform:scale(0);
opacity:0;
}
100%{
transform:scale(1);
opacity:1;
}
}

h2{
margin-bottom:20px;
}

.input-box{
margin:10px
