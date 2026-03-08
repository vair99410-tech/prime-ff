<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>PRIME. FF Gaming </title>

<link rel="stylesheet" href="style.css">

</head>

<body>

<header>

<h1>🔥 Gaming Tube</h1>

</header>

<div class="main">

<div class="video-section">

<h2>🎮 Watch Gaming Video</h2>

<input id="videoLink" placeholder="Paste YouTube Video Link">

<button onclick="loadVideo()">Watch</button>

<div class="player">

<iframe id="player" src="" allowfullscreen></iframe>

</div>

<div class="actions">

<button onclick="like()">👍 Like</button>

<span id="likeCount">0</span>

</div>

</div>

<div class="comment-section">

<h3>💬 Comments</h3>

<input id="commentInput" placeholder="Write comment">

<button onclick="addComment()">Send</button>

<ul id="comments"></ul>

</div>

</div>

<script src="script.js"></script>

</body>
</html>
body{

margin:0;
font-family:Arial;
background:#0f172a;
color:white;

}

header{

background:#111827;
padding:20px;
text-align:center;
font-size:24px;

}

.main{

display:flex;
justify-content:center;
gap:40px;
padding:40px;

}

.video-section{

background:#1e293b;
padding:20px;
border-radius:10px;
width:500px;

}

.player iframe{

width:100%;
height:300px;
margin-top:20px;
border-radius:10px;

}

input{

padding:10px;
width:70%;
border:none;
border-radius:5px;

}

button{

padding:10px 20px;
background:#22c55e;
border:none;
color:white;
cursor:pointer;
border-radius:5px;

}

button:hover{

background:#16a34a;

}

.comment-section{

background:#1e293b;
padding:20px;
border-radius:10px;
width:300px;

}

ul{

margin-top:10px;

}

let likes = 0

function loadVideo(){

let link = document.getElementById("videoLink").value

let id = link.split("v=")[1]

let embed = "https://www.youtube.com/embed/" + id

document.getElementById("player").src = embed

}

function like(){

likes++

document.getElementById("likeCount").innerText = likes

}

function addComment(){

let input = document.getElementById("commentInput")

let comment = input.value

if(comment == "") return

let li = document.createElement("li")

li.innerText = comment

document.getElementById("comments").appendChild(li)

input.value = ""

}
<p>Views: <span id="views">0</span></p>

