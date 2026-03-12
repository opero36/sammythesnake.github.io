<!DOCTYPE html>
<html>
<head>
<title>Sammy the Snake</title>

<style>

*{
box-sizing:border-box;
font-family:Segoe UI,Arial;
}

body{
margin:0;
height:100vh;
background:linear-gradient(135deg,#0f172a,#020617);
display:flex;
align-items:center;
justify-content:center;
color:white;
}

.card{
background:rgba(255,255,255,0.05);
backdrop-filter:blur(12px);
border-radius:16px;
padding:30px;
width:520px;
text-align:center;
box-shadow:0 10px 40px rgba(0,0,0,0.5);
}

button{
padding:10px 16px;
border-radius:10px;
border:none;
margin:5px;
background:#22c55e;
color:white;
font-weight:600;
cursor:pointer;
}

.secondary{background:#334155}
.danger{background:#ef4444}

input{
padding:10px;
border-radius:8px;
border:none;
margin:5px;
}

#gameCanvas{
background:#020617;
border-radius:10px;
margin-top:20px;
display:none;
}

.hud{
display:none;
margin-top:10px;
}

.panel{
display:none;
background:rgba(0,0,0,.3);
padding:12px;
border-radius:10px;
margin-top:10px;
}

</style>
</head>

<body>

<div class="card">

<h1>🐍 Sammy the Snake</h1>

<div id="login">
<input id="username" placeholder="Enter username">
<br><br>
<button onclick="startGame()">Play</button>
</div>

<canvas id="gameCanvas" width="400" height="400"></canvas>

<div id="hud" class="hud">

Score: <span id="score">0</span> |
Coins: <span id="coins">0</span>

<br>

<button onclick="togglePause()">Pause</button>
<button onclick="openCustomize()">Customize Sammy</button>
<button onclick="openLeaderboard()">Leaderboard</button>
<button onclick="shareScore()">Share Score</button>
<button class="secondary" onclick="openShop()">Shop</button>
<button class="danger" onclick="logout()">Log Out</button>

</div>

<div id="shop" class="panel">

<h3>Shop</h3>

<button onclick="buySpeed()">⚡ Speed (20)</button>
<button onclick="buyMultiplier()">💰 Multiplier (30)</button>
<button onclick="buyLength()">🐍 Start Length (25)</button>

<br>

<button class="secondary" onclick="closeShop()">Close Shop</button>

</div>

<div id="leaderboard" class="panel">

<h3>Leaderboard</h3>

<div id="leaderboardList"></div>

<br>

<button class="secondary" onclick="closeLeaderboard()">Close Leaderboard</button>

</div>

<div id="customize" class="panel">

<h3>Customize Sammy</h3>

Snake Color
<input type="color" id="snakeColor">

<br>

Eye Color
<input type="color" id="eyeColor">

<br>

Tongue Color
<input type="color" id="tongueColor">

<br><br>

<button onclick="saveCustomize()">Save</button>
<button class="secondary" onclick="closeCustomize()">Close</button>

</div>

</div>

<script>

let canvas=document.getElementById("gameCanvas")
let ctx=canvas.getContext("2d")

let snake=[{x:200,y:200}]
let dx=20
let dy=0

let coin={x:100,y:100}

let coins=0
let score=0

let speed=150
let multiplier=1
let startLength=1

let paused=false
let username=""

let snakeColor="#22c55e"
let eyeColor="#ffffff"
let tongueColor="#ff0000"

function startGame(){

username=document.getElementById("username").value
if(!username)return

loadData()

document.getElementById("login").style.display="none"
canvas.style.display="block"
document.getElementById("hud").style.display="block"

resetSnake()
gameLoop()

}

function resetSnake(){

saveScore()

snake=[]

for(let i=0;i<startLength;i++){
snake.push({x:200-(i*20),y:200})
}

score=0

}

function gameLoop(){

setTimeout(()=>{

if(!paused){
update()
draw()
}

gameLoop()

},speed)

}

function update(){

let head={x:snake[0].x+dx,y:snake[0].y+dy}

snake.unshift(head)

if(head.x==coin.x && head.y==coin.y){

coins+=1*multiplier
score+=10

spawnCoin()
saveData()

}else{

snake.pop()

}

if(head.x<0||head.y<0||head.x>=400||head.y>=400){
resetSnake()
}

document.getElementById("coins").innerText=coins
document.getElementById("score").innerText=score

}

function draw(){

ctx.fillStyle="#020617"
ctx.fillRect(0,0,400,400)

snake.forEach((s,i)=>{

if(i==0){
drawHead(s)
}else{
ctx.fillStyle=snakeColor
ctx.fillRect(s.x,s.y,20,20)
}

})

ctx.fillStyle="#facc15"
ctx.fillRect(coin.x,coin.y,20,20)

}

function drawHead(s){

ctx.fillStyle=snakeColor
ctx.fillRect(s.x,s.y,20,20)

ctx.fillStyle=eyeColor

ctx.beginPath()
ctx.arc(s.x+6,s.y+7,3,0,Math.PI*2)
ctx.fill()

ctx.beginPath()
ctx.arc(s.x+14,s.y+7,3,0,Math.PI*2)
ctx.fill()

ctx.fillStyle="black"

ctx.beginPath()
ctx.arc(s.x+6,s.y+7,1,0,Math.PI*2)
ctx.fill()

ctx.beginPath()
ctx.arc(s.x+14,s.y+7,1,0,Math.PI*2)
ctx.fill()

ctx.strokeStyle=tongueColor
ctx.beginPath()
ctx.moveTo(s.x+10,s.y+12)
ctx.lineTo(s.x+10,s.y+18)
ctx.stroke()

}

function spawnCoin(){

coin.x=Math.floor(Math.random()*20)*20
coin.y=Math.floor(Math.random()*20)*20

}

document.addEventListener("keydown",e=>{

if(e.key=="ArrowUp"&&dy==0){dx=0;dy=-20}
if(e.key=="ArrowDown"&&dy==0){dx=0;dy=20}
if(e.key=="ArrowLeft"&&dx==0){dx=-20;dy=0}
if(e.key=="ArrowRight"&&dx==0){dx=20;dy=0}

})

function togglePause(){
paused=!paused
}

function shareScore(){

let text=`I scored ${score} points in Sammy the Snake!`
navigator.clipboard.writeText(text)
alert("Score copied")

}

function logout(){

if(confirm("Log out?")){
location.reload()
}

}

function openShop(){
document.getElementById("shop").style.display="block"
}

function closeShop(){
document.getElementById("shop").style.display="none"
}

function openLeaderboard(){

updateLeaderboard()
document.getElementById("leaderboard").style.display="block"

}

function closeLeaderboard(){
document.getElementById("leaderboard").style.display="none"
}

function openCustomize(){

document.getElementById("customize").style.display="block"

}

function closeCustomize(){

document.getElementById("customize").style.display="none"

}

function saveCustomize(){

snakeColor=document.getElementById("snakeColor").value
eyeColor=document.getElementById("eyeColor").value
tongueColor=document.getElementById("tongueColor").value

saveData()

}

function buySpeed(){

if(coins>=20){
coins-=20
speed-=10
saveData()
}

}

function buyMultiplier(){

if(coins>=30){
coins-=30
multiplier+=1
saveData()
}

}

function buyLength(){

if(coins>=25){
coins-=25
startLength+=1
saveData()
}

}

function saveScore(){

if(!username)return

let lb=JSON.parse(localStorage.getItem("sammy_leaderboard")||"[]")

lb.push({name:username,score:score})

lb.sort((a,b)=>b.score-a.score)

lb=lb.slice(0,10)

localStorage.setItem("sammy_leaderboard",JSON.stringify(lb))

}

function updateLeaderboard(){

let lb=JSON.parse(localStorage.getItem("sammy_leaderboard")||"[]")

let html=""

lb.forEach((p,i)=>{
html+=`${i+1}. ${p.name} - ${p.score}<br>`
})

document.getElementById("leaderboardList").innerHTML=html

}

function saveData(){

let data={
coins,
speed,
multiplier,
startLength,
snakeColor,
eyeColor,
tongueColor
}

localStorage.setItem("sammy_"+username,JSON.stringify(data))

}

function loadData(){

let data=localStorage.getItem("sammy_"+username)

if(data){

data=JSON.parse(data)

coins=data.coins
speed=data.speed
multiplier=data.multiplier
startLength=data.startLength

snakeColor=data.snakeColor || snakeColor
eyeColor=data.eyeColor || eyeColor
tongueColor=data.tongueColor || tongueColor

}

}

</script>

</body>
</html>
