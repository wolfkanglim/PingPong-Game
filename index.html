const canvas = document.getElementById("ping");
const ctx = canvas.getContext('2d');

/* const gamestate = {
    PAUSED: 0,
    RUNNING: 1,
    MENU: 2,
    GAMEOVER: 3
} */

function drawRect(x,y,w,h,color){
    ctx.fillStyle = color;
    ctx.fillRect(x,y,w,h);
}
function drawCircle(x,y,r,color){
    ctx.fillStyle = color;
    ctx.beginPath();
    ctx.arc(x,y,r,0,2*Math.PI,false);
    ctx.closePath();
    ctx.fill();
}
function drawText(text, x,y,color){
    ctx.font = '30px Arial';
    ctx.fillStyle = color; 
    ctx.fillText(text,x,y);
}

//objects
const ball = {
    x: canvas.width/2,
    y: canvas.height/2,
    radius: 10,
    speed: 4,
    velocityX: 4,
    velocityY: 4,
    color: 'white'
}
const net = {
    x: 0,
    y: canvas.height/2 - 1,
    w: 10,
    h: 2,
    color: 'white'
}
function drawNet(){
    for(let i=0; i<canvas.width; i+=15){
        drawRect(net.x + i, net.y, net.w, net.h, net.color);
    }
}
const com = {
    x: canvas.width/2 - 100/2,
    y: 0,
    w: 120,
    h: 20,
    color: 'black',
    score: 0
}
const user = {
    x: canvas.width/2 - 120/2,
    y: canvas.height - 20,
    w: 120,
    h: 20,
    color: 'red',
    score: 0,
    speed : 0,
    maxSpeed : 7
}


function resetBall(){
    ball.x = canvas.width/2;
    ball.y = canvas.height/2; 
    ball.speed = 5;
    ball.velocityX = 5,
    ball.velocityY = 5,  
    ball.velocityY = -ball.velocityY;
} 

function render(){
    drawRect(0,0,canvas.width,canvas.height,'green');
    drawNet();
    drawCircle(ball.x,ball.y, ball.radius,);
    drawRect(user.x, user.y,user.w,user.h,user.color);
    drawRect(com.x, com.y,com.w,com.h,com.color);
    drawText(user.score, canvas.width/2 - 10, canvas.height/2 + 50, user.color);
    drawText(com.score, canvas.width/2 - 10, canvas.height/2 - 30, com.color);
  // gamestate = gamestate.MENU;
}
//control pad user, com
/* canvas.addEventListener('mousemove', control);
function control(e){
    let rect = canvas.getBoundingClientRect();
    user.x = e.clientX - rect.left - 100/2; 
} */

//collision
function collision(b,p){
    b.top = b.y - b.radius;
    b.bottom = b.y + b.radius;
    b.right = b.x + b.radius;
    b.left = b.x - b.radius;
    p.top = p.y;
    p.bottom = p.y + p.h;
    p.right = p.x + p.w;
    p.left = p.x;
    
    return b.top < p.bottom && b.bottom > p.top && b.right > p.left && b.left < p.right;    
}

function playSound(){
    document.getElementById('mySound').play();
    document.getElementById('mySound').currentTime = 0;
}
function playMusic(){
    document.getElementById('myMusic').play();
}

function update(){
   /*  if(gamestate === gamestate.PAUSED){
        return;
    } */
    user.x += user.speed;   
    ball.x += ball.velocityX;
    ball.y += ball.velocityY;
    
    if(ball.x + ball.radius > canvas.width || ball.x - ball.radius < 0){
        ball.velocityX = - ball.velocityX;
     playSound();
       
    }
    let comLevel = 0.065;
    com.x += (ball.x - (com.x + 120/2)) * comLevel;
    
    let player = ball.y > canvas.height/2 ? user : com;    
    if (collision(ball, player)){ 
        let direction = ball.y > canvas.height/2 ? -1 : 1;    
       playSound();
       //let collisionPoint = (ball.x - player.x - 50);
       let collisionPoint = (ball.x - player.x - player.w/2)/50;
       let a = collisionPoint * Math.PI/3;
       ball.velocityX = direction * ball.speed * Math.sin(a);
       ball.velocityY = direction * ball.speed * Math.cos(a);         
       ball.speed += 0.2;
       
       if(com.score >= 11){
        alert(' YOU LOST!! Hehehe!!');
        com.score = 0; 
        user.score = 0;
        ball.velocityX = 5;
        ball.velocityY = 5;
        resetBall();
     }
    else if(user.score >= 11){
        alert(' YOU WIN!! Nice!!');
        com.score = 0; 
        user.score = 0;
        ball.velocityX = 5;
        ball.velocityY = 5;
        resetBall();
     }
    };

    if(ball.y - ball.radius > canvas.height){
        com.score ++;       
        resetBall();
    }   
         
    else if(ball.y + ball.radius < 0){
        user.score ++;        
       resetBall();
    }  
  
  if(user.x < 0){
    user.x = 0;
}
if(user.x > canvas.width - user.width){
    user.x = canvas.width - 120;
}
//gamestate = gamestate.RUNNING; 
}



function game(){
 /* if(gamestate === gamestate.PAUSED){
     return;
 } */
 update();
 render();
 playMusic();
 //gamestate === gamestate.RUNNING;

}

const timeFrame = 50;
setInterval(game, 1000/timeFrame);


document.addEventListener('keydown', event => {
    switch (event.keyCode){
       /*  case 27:
            clearInterval(game);
            togglePause();
            break; */
            case 37:
           moveLeft();
            break;
            case 39:
           moveRight();
            break;
    }
})
document.addEventListener('keyup', event => {
    switch (event.keyCode){
        case 37:
            stop();
            break;
        case 39:
           stop();
            break;
    }
})

function stop(){
    user.speed = 0;
}
function moveLeft(){
    user.speed = - user.maxSpeed;
}
function moveRight(){
    user.speed = user.maxSpeed;
}
/* function togglePause(){
    clearInterval(game);
    if(gamestate === gamestate.PAUSED){        
        gamestate = gamestate.RUNNING;
    } else {
        gamestate = gamestate.PAUSED;
    }
} */
console.log(user.x);
