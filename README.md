<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Vrushali ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400&display=swap" rel="stylesheet">

<style>
body{
margin:0;
font-family:'Poppins',sans-serif;
background:linear-gradient(135deg,#ffdde1,#ee9ca7);
color:white;
overflow:hidden;
}

/* PASSWORD */
#lockScreen{
position:fixed;
width:100%;
height:100%;
background:linear-gradient(135deg,#ff758c,#ff7eb3);
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
z-index:1000;
}
#lockScreen input{
padding:10px;
border:none;
border-radius:5px;
}
#lockScreen button{
margin-top:10px;
padding:8px 15px;
border:none;
background:white;
color:#ff4e7a;
border-radius:5px;
cursor:pointer;
}

/* SLIDER */
.slider{
display:flex;
width:300%;
height:100vh;
transition:transform 1s ease;
}
.slide{
width:100%;
flex-shrink:0;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
padding:20px;
}

/* NAME */
.name{
font-family:'Great Vibes',cursive;
font-size:70px;
background:linear-gradient(45deg,gold,#fff,gold);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
animation:shine 3s infinite linear;
}
@keyframes shine{
0%{background-position:0%;}
100%{background-position:200%;}
}

.typing{
font-size:26px;
border-right:3px solid white;
white-space:nowrap;
overflow:hidden;
width:0;
animation:typing 4s steps(40,end) forwards;
}
@keyframes typing{
from{width:0}
to{width:100%;}
}

.note{
margin-top:30px;
font-size:20px;
line-height:1.8;
max-width:700px;
white-space:pre-line;
}

.button{
margin-top:30px;
padding:12px 25px;
background:white;
color:#ff4e7a;
border:none;
border-radius:30px;
cursor:pointer;
transition:0.3s;
}
.button:hover{
transform:scale(1.1);
}

/* POLAROID */
.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(160px,1fr));
gap:20px;
width:85%;
margin-top:30px;
}
.polaroid{
background:white;
padding:10px;
border-radius:12px;
box-shadow:0 10px 20px rgba(0,0,0,0.2);
transform:scale(0);
animation:pop 1s forwards;
}
.polaroid img{
width:100%;
border-radius:8px;
}
.polaroid p{
color:#ff4e7a;
font-size:14px;
margin-top:5px;
}
@keyframes pop{
to{transform:scale(1);}
}

/* POPUP */
#lovePopup{
position:fixed;
top:50%;
left:50%;
transform:translate(-50%,-50%);
background:white;
color:#ff4e7a;
padding:30px;
border-radius:20px;
display:none;
font-size:28px;
z-index:2000;
}

/* HEARTS */
.heart{
position:fixed;
bottom:-50px;
animation:float 8s linear infinite;
}
@keyframes float{
0%{transform:translateY(0);opacity:1;}
100%{transform:translateY(-100vh);opacity:0;}
}
</style>
</head>
<body>

<div id="lockScreen">
<h2>Enter Our Secret Password ❤️</h2>
<input type="password" id="passwordInput">
<button onclick="checkPassword()">Unlock</button>
</div>

<div id="lovePopup">I Love You Vrushali ❤️</div>

<div class="slider" id="slider">

<!-- SLIDE 1 -->
<div class="slide">
<div class="name">Vrushali ❤️</div>
<div class="typing">My Love...</div>
<div class="note">
My day begins with you  
and ends with you in my heart.

You are my peace, my happiness,  
my safest place, and my forever.

Every single day I fall for you more.  
Your smile melts my heart effortlessly.

Today marks our 240 beautiful days together ❤️
</div>
<button class="button" onclick="nextSlide()">Our Memories ➡</button>
</div>

<!-- SLIDE 2 -->
<div class="slide">
<h2>✨ Our Memories ✨</h2>

<div class="grid">
<div class="polaroid">
<img src="photo1.jpeg">
<p>That magical Christmas night 🎄❤️</p>
</div>

<div class="polaroid">
<img src="photo2.jpeg">
<p>Every moment with you feels special 💕</p>
</div>

<div class="polaroid">
<img src="photo3.jpeg">
<p>Under the sky, just us 🌴💋</p>
</div>

<div class="polaroid">
<img src="photo4.jpeg">
<p>Smiling through life together 🤍</p>
</div>
</div>

<button class="button" onclick="nextSlide()">Forever ➡</button>
</div>

<!-- SLIDE 3 -->
<div class="slide">
<h2>Forever & Always 💍</h2>

<div class="note">
With you, love feels calm, real, and eternal.

Will you stay with me forever?
</div>

<button class="button" onclick="showLove()">Yes, Always ❤️</button>

<div style="margin-top:30px;">
Forever Yours,<br>
Kush ❤️
</div>

</div>

</div>

<script>
let currentSlide=0;
function nextSlide(){
currentSlide++;
document.getElementById("slider").style.transform="translateX(-"+currentSlide*100+"vw)";
}

function checkPassword(){
if(document.getElementById("passwordInput").value==="onlyus"){
document.getElementById("lockScreen").style.display="none";
}
else{
alert("Wrong Password 😘");
}
}

function showLove(){
document.getElementById("lovePopup").style.display="block";
}

function createHeart(){
const heart=document.createElement('div');
heart.classList.add('heart');
heart.innerHTML=Math.random()>0.5?"🎈❤️":"😘💋";
heart.style.left=Math.random()*100+"vw";
heart.style.fontSize=(20+Math.random()*20)+"px";
document.body.appendChild(heart);
setTimeout(()=>heart.remove(),8000);
}
setInterval(createHeart,800);
</script>

</body>
</html>
