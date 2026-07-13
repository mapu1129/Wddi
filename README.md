<!DOCTYPE html>
<html lang="uz">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Maftuna ❤️ Umarjon</title>

<style>
*{box-sizing:border-box}
body{
margin:0;
font-family:Georgia,serif;
background:#fffaf8;
color:#6b4a20;
overflow-x:hidden;
}

.container{
min-height:100vh;
display:flex;
justify-content:center;
align-items:center;
padding:20px;
background:
radial-gradient(circle,#fff 10%,#fff8ef 80%);
}

.card{
max-width:450px;
width:100%;
background:white;
border:4px solid #d4af37;
border-radius:35px;
padding:35px 25px;
text-align:center;
box-shadow:0 0 40px #d4af3766;
animation:show 2s ease;
}

@keyframes show{
from{opacity:0;transform:scale(.8)}
to{opacity:1;transform:scale(1)}
}

.flower{
font-size:35px;
}

h1{
font-size:45px;
color:#c99b22;
margin:15px;
}

.gold{
color:#b8860b;
font-weight:bold;
font-size:22px;
}

p{
font-size:19px;
line-height:1.7;
}

#count{
font-size:22px;
color:#b8860b;
font-weight:bold;
}

button{
background:#d4af37;
border:0;
color:white;
padding:14px 25px;
border-radius:30px;
font-size:17px;
margin:8px;
}

</style>
</head>

<body>

<audio id="music" loop>
<source src="music.mp3" type="audio/mpeg">
</audio>

<div class="container">
<div class="card">

<div class="flower">🤍🌸🤍</div>

<h1>
Maftuna<br>
❤️<br>
Umarjon
</h1>

<p>
Bismillahir rohmanir rohiym
</p>

<p>
Sizni aziz farzandlarimizning
<br>
<b>nikoh to‘yiga</b>
<br>
tashrif buyurib, quvonchimizga sherik bo‘lishga taklif qilamiz.
</p>

<div class="gold">
7-AVGUST 2026
</div>

<p>
🕗 Soat: <b>20:00</b><br>
📍 G‘ijduvon
</p>

<p>
⏳ To‘yimizgacha:
</p>

<div id="count"></div>

<p>
<b>Kuyovning ota-onasi:</b><br>
Nodir & Iqbola
</p>

<p>
<b>Kelinning ota-onasi:</b><br>
Kamol & Muxabbat
</p>

<button onclick="music.play()">
🎵 Musiqani yoqish
</button>

<button>
📍 Xarita
</button>

<div class="flower">🌸✨🌸</div>

</div>
</div>


<script>

let wedding=new Date("August 7, 2026 20:00:00").getTime();

setInterval(function(){

let now=new Date().getTime();
let d=wedding-now;

let day=Math.floor(d/(1000*60*60*24));
let hour=Math.floor((d%(1000*60*60*24))/(1000*60*60));
let min=Math.floor((d%(1000*60*60))/(1000*60));
let sec=Math.floor((d%(1000*60))/1000);

document.getElementById("count").innerHTML=
day+" kun "+hour+" soat "+min+" daqiqa "+sec+" soniya";

},1000);

</script>

</body>
</html>
