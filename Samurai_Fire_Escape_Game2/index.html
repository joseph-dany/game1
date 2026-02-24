<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Samurai Fire Escape</title>
<style>
body {
    margin: 0;
    height: 100vh;
    background: url('assets/background_fire_city.jpg') no-repeat center bottom/cover;
    overflow: hidden;
    position: relative;
    font-family: Arial;
}
#menu {
    position: absolute;
    bottom: 60px;
    width: 100%;
    text-align: center;
}
button {
    padding: 12px 35px;
    font-size: 18px;
    border: none;
    border-radius: 8px;
    color: white;
    background: linear-gradient(45deg,#ff3c00,#ff7300,#ff0000);
    cursor: pointer;
}
#gameArea {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 70vh;
    display: none;
}
#player {
    position: absolute;
    bottom: 0;
    left: 80px;
    width: 120px;
}
.obstacle { position:absolute; width:100px; }
.groundObstacle { bottom:0; }
.airObstacle { top:0; }
#hpBar {
    position:absolute;
    top:20px;
    right:20px;
    width:200px;
    height:20px;
    background:#333;
}
#hpFill { height:100%; width:100%; background:red; }
#score {
    position:absolute;
    top:50px;
    right:20px;
    color:white;
}
</style>
</head>
<body>

<div id="menu">
<button id="startBtn">Start Game</button>
</div>

<div id="hpBar"><div id="hpFill"></div></div>
<div id="score">Score: 0</div>

<div id="gameArea">
<img id="player" src="assets/samurai_idle.png">
</div>

<script>
const startBtn=document.getElementById("startBtn");
const gameArea=document.getElementById("gameArea");
const menu=document.getElementById("menu");
const player=document.getElementById("player");
const hpFill=document.getElementById("hpFill");
const scoreText=document.getElementById("score");

let hp=100,posX=80,isJumping=false,isSliding=false;
let speed=6,score=0,obstacles=[],gameInterval;

startBtn.onclick=()=>{
menu.style.display="none";
gameArea.style.display="block";
resetGame();
startGame();
};

function startGame(){
gameInterval=setInterval(()=>{
moveObstacles();
checkCollisions();
score++;
scoreText.innerText="Score: "+score;
if(score%500===0) speed++;
},30);
spawnObstacle();
}

function spawnObstacle(){
const obs=document.createElement("img");
const type=Math.random()>0.5?"ground":"air";
if(type==="ground"){
obs.src="assets/fire_bike.png";
obs.className="obstacle groundObstacle";
}else{
obs.src="assets/hanging_chain.png";
obs.className="obstacle airObstacle";
}
obs.style.left=window.innerWidth+"px";
gameArea.appendChild(obs);
obstacles.push(obs);
setTimeout(spawnObstacle,1500+Math.random()*1000);
}

function moveObstacles(){
obstacles.forEach((obs,i)=>{
let left=parseInt(obs.style.left);
left-=speed;
obs.style.left=left+"px";
if(left<-100){obs.remove();obstacles.splice(i,1);}
});
}

function checkCollisions(){
const playerRect=player.getBoundingClientRect();
obstacles.forEach(obs=>{
const rect=obs.getBoundingClientRect();
if(!(playerRect.right<rect.left||playerRect.left>rect.right||playerRect.bottom<rect.top||playerRect.top>rect.bottom)){
damagePlayer();
}
});
}

function damagePlayer(){
hp-=25;
if(hp<0)hp=0;
hpFill.style.width=hp+"%";
if(hp===0){
clearInterval(gameInterval);
alert("You Died!");
menu.style.display="block";
gameArea.style.display="none";
}
}

function resetGame(){
hp=100;score=0;speed=6;
hpFill.style.width="100%";
scoreText.innerText="Score: 0";
obstacles.forEach(o=>o.remove());
obstacles=[];
}

document.addEventListener("keydown",e=>{
if(gameArea.style.display!=="block")return;
if(e.key==="ArrowRight"){posX+=15;player.style.left=posX+"px";}
if(e.key==="ArrowLeft"){posX-=15;if(posX<0)posX=0;player.style.left=posX+"px";}
if(e.key==="ArrowUp"&&!isJumping){
isJumping=true;
player.style.bottom="150px";
setTimeout(()=>{player.style.bottom="0px";isJumping=false;},500);
}
if(e.key==="ArrowDown"&&!isSliding){
isSliding=true;
player.style.height="60px";
setTimeout(()=>{player.style.height="120px";isSliding=false;},400);
}
});
</script>

</body>
</html>
