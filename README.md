<!DOCTYPE html>
<html lang="uz">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Maftuna ❤️ Umarjon</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Segoe UI,sans-serif;
}

body{
background:linear-gradient(135deg,#fff8f8,#fde2e4,#fff);
overflow-x:hidden;
text-align:center;
color:#5a2a2a;
}

.container{
max-width:700px;
margin:auto;
padding:25px;
}

.card{
background:rgba(255,255,255,.85);
backdrop-filter:blur(8px);
padding:30px;
border-radius:25px;
box-shadow:0 10px 35px rgba(0,0,0,.15);
margin-top:25px;
animation:fade 1.2s;
}

h1{
font-size:42px;
color:#c2185b;
margin-bottom:15px;
}

h2{
font-size:28px;
margin:15px 0;
}

p{
font-size:20px;
margin:10px 0;
line-height:1.7;
}

.heart{
font-size:70px;
animation:beat 1s infinite;
}

.button{
display:inline-block;
margin-top:20px;
padding:15px 28px;
background:#c2185b;
color:white;
text-decoration:none;
border-radius:40px;
font-size:18px;
transition:.3s;
}

.button:hover{
transform:scale(1.05);
background:#a00045;
}

.countdown{
display:flex;
justify-content:center;
gap:15px;
margin-top:25px;
flex-wrap:wrap;
}

.box{
background:white;
padding:15px;
width:85px;
border-radius:18px;
box-shadow:0 5px 15px rgba(0,0,0,.1);
}

.box span{
display:block;
font-size:28px;
font-weight:bold;
color:#c2185b;
}

canvas{
position:fixed;
left:0;
top:0;
pointer-events:none;
}

@keyframes beat{
50%{transform:scale(1.2);}
}

@keyframes fade{
from{opacity:0;transform:translateY(30px);}
to{opacity:1;transform:translateY(0);}
}
</style>
</head>

<body>

<canvas id="canvas"></canvas>

<div class="container">
<div class="card">

<div class="heart">❤️</div>

<h1>Maftuna ❤️ Umarjon</h1>

<p>Sizni hayotimizning eng baxtli kuniga taklif qilamiz.</p>

<h2>💍 Nikoh To'yi</h2>

<p><b>📅 Sana:</b> 7-avgust 2026</p>

<p><b>🕗 Vaqt:</b> 20:00</p>

<p><b>📍 Manzil:</b> Oq Gul to'yxonasi, G'ijduvon</p>

<div class="countdown">
<div class="box">
<span id="days">0</span>
Kun
</div>

<div class="box">
<span id="hours">0</span>
Soat
</div>

<div class="box">
<span id="minutes">0</span>
Daqiqa
</div>

<div class="box">
<span id="seconds">0</span>
Soniya
</div>
</div>

<a class="button"
href="https://maps.google.com/?q=Oq+Gul+toyxonasi+Gijduvon"
target="_blank">
📍 Xaritada ochish
</a>

</div>
</div>

<script>
const target=new Date("August 7, 2026 20:00:00").getTime();

setInterval(()=>{
const now=new Date().getTime();
const d=target-now;

document.getElementById("days").innerHTML=Math.floor(d/(1000*60*60*24));
document.getElementById("hours").innerHTML=Math.floor((d%(1000*60*60*24))/(1000*60*60));
document.getElementById("minutes").innerHTML=Math.floor((d%(1000*60*60))/(1000*60));
document.getElementById("seconds").innerHTML=Math.floor((d%(1000*60))/1000);
},1000);

const canvas=document.getElementById("canvas");
const ctx=canvas.getContext("2d");

canvas.width=window.innerWidth;
canvas.height=window.innerHeight;

const hearts=[];

for(let i=0;i<40;i++){
hearts.push({
x:Math.random()*canvas.width,
y:Math.random()*canvas.height,
size:10+Math.random()*15,
speed:1+Math.random()*2
});
}

function draw(){
ctx.clearRect(0,0,canvas.width,canvas.height);

hearts.forEach(h=>{
ctx.font=h.size+"px serif";
ctx.fillText("❤️",h.x,h.y);
h.y+=h.speed;

if(h.y>canvas.height){
h.y=-20;
h.x=Math.random()*canvas.width;
}
});

requestAnimationFrame(draw);
}

draw();

window.onresize=()=>{
canvas.width=window.innerWidth;
canvas.height=window.innerHeight;
}
</script>

</body>
</html>
