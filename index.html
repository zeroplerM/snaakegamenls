<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Snake Stable</title>

<style>
body{
  margin:0;
  background:#111;
  color:white;
  text-align:center;
  font-family:Arial;
}

canvas{
  background:#1e1e1e;
  display:block;
  margin:20px auto;
  border-radius:12px;
  box-shadow:0 0 20px #00ffcc;
}

.controls{
  display:grid;
  grid-template-columns:80px 80px 80px;
  gap:10px;
  justify-content:center;
  margin-top:10px;
}

button{
  height:60px;
  font-size:20px;
  border:none;
  border-radius:12px;
  background:#00ffcc;
  font-weight:bold;
}
</style>
</head>
<body>

<h2>Snake 2.0</h2>

<canvas id="game" width="300" height="300"></canvas>

<div>
Score: <span id="score">0</span> |
Highscore: <span id="highscore">0</span>
</div>

<div class="controls">
  <div></div>
  <button onclick="setDirection('up')">↑</button>
  <div></div>

  <button onclick="setDirection('left')">←</button>
  <button onclick="setDirection('down')">↓</button>
  <button onclick="setDirection('right')">→</button>
</div>

<script>
const canvas = document.getElementById("game");
const ctx = canvas.getContext("2d");

const box = 15;
const gridSize = canvas.width / box;

let snake = [{x:10,y:10}];
let direction = "right";
let nextDirection = "right";
let food = spawnFood();
let score = 0;

let highscore = localStorage.getItem("snakeHighscore") || 0;
document.getElementById("highscore").innerText = highscore;

let speed = 150;
let loop;

// ---------- FUNCTIONS ----------

function spawnFood(){
  return {
    x: Math.floor(Math.random()*gridSize),
    y: Math.floor(Math.random()*gridSize)
  };
}

function setDirection(dir){
  if(dir==="up" && direction!=="down") nextDirection="up";
  if(dir==="down" && direction!=="up") nextDirection="down";
  if(dir==="left" && direction!=="right") nextDirection="left";
  if(dir==="right" && direction!=="left") nextDirection="right";
}

document.addEventListener("keydown",e=>{
  if(e.key==="ArrowUp") setDirection("up");
  if(e.key==="ArrowDown") setDirection("down");
  if(e.key==="ArrowLeft") setDirection("left");
  if(e.key==="ArrowRight") setDirection("right");
});

function draw(){

  direction = nextDirection;

  ctx.clearRect(0,0,canvas.width,canvas.height);

  // Snake zeichnen
  ctx.fillStyle="#00ffcc";
  snake.forEach(part=>{
    ctx.fillRect(part.x*box, part.y*box, box, box);
  });

  // Food zeichnen
  ctx.fillStyle="#ff0066";
  ctx.fillRect(food.x*box, food.y*box, box, box);

  let head = {...snake[0]};

  if(direction==="up") head.y--;
  if(direction==="down") head.y++;
  if(direction==="left") head.x--;
  if(direction==="right") head.x++;

  // Kollision Wand
  if(head.x<0 || head.y<0 || head.x>=gridSize || head.y>=gridSize ||
     snake.some(p=>p.x===head.x && p.y===head.y)){
    reset();
    return;
  }

  snake.unshift(head);

  if(head.x===food.x && head.y===food.y){
    score++;
    document.getElementById("score").innerText = score;
    food = spawnFood();
  } else {
    snake.pop();
  }
}

function reset(){
  if(score>highscore){
    highscore=score;
    localStorage.setItem("snakeHighscore",highscore);
    document.getElementById("highscore").innerText=highscore;
  }

  snake=[{x:10,y:10}];
  direction="right";
  nextDirection="right";
  score=0;
  document.getElementById("score").innerText=0;
}

// ---------- START ----------
loop = setInterval(draw, speed);
</script>

</body>
</html>
