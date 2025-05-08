# AvatarMaker
first draft of code. it does not work.


var num = [25];
var x = [];
var y = [];

let img;
function preload() {
}

function setup() {
  createCanvas(700, 600);
  colorMode(RGB, 255, 255, 255);
  
  for (var i = 0; i < num; i++){
    x[i] = 0;
    y[i] = 0;
  }
  
}


function draw() {
  background(220); 

  drawBase();
  fill(150, 120, 110);
  
      //shade
    if(keyIsPressed){
    if(key == 's'){
      for (var i = 0; i < num; i++){
          fill(i * 40.5, 190, 150);
      }
    }
  }
  
    //nose  
    if(keyIsPressed && key == 'n'){
  }
  
  eyes(); //eyes
  if(keyIsPressed && key == 'i'){
  }
  
  mouthNeutral();
  if (keyIsPressed && key == 'm'){
    smileBig();
  } 
  if(keyIsPressed && keyCode == UP_ARROW){
    if(mouseIsPressed){
     smileSmol(); 
    }
 }
    
    //shirt
  if(keyIsPressed && key == 'c'){
    
  }
  
  //hair
  if(keyIsPressed && key == 'h'){
  }
  
  //brows
  if(keyIsPressed && key == 'b'){
  }
  
    //facialHair
    if(keyIsPressed && key == 'f'){
  }
    
  //hat
  
  //glasses
  if(keyIsPressed && key == 'g'){
  }

  
}

function drawBase(){

  beginShape();
  vertex(190, 420);
  vertex(510, 420);
  vertex(550, 600);
  vertex(150, 600);
  endShape(CLOSE); //torso
  rect(275, 370, 150, 100, 15); //neck
  ellipse(350, 260, 270, 330); //head
  
  
  ears();
  
  
}

function ears(){
push();

arc(185, 250, 80, 80, 0, radians(180));
pop();
}

function eyes (){
  push();
  ellipse(300, 250, 50, 30)
  ellipse(400, 250, 50, 30);
  strokeWeight(6);
  fill('black');
  circle(300, 250, 20);
  circle(400, 250, 20);
  pop();
}

function smileSmol(){
  strokeWeight(0);
  rect(300, 300, 100, 100);
  strokeWeight(1);
  arc(350, 350, 40, 50, 0, radians(180));
}

function smileBig(){
  strokeWeight(0);
  rect(300, 300, 100, 100);
  strokeWeight(1);
  arc(350, 350, 50, 40, 0, radians(180));
}

function mouthNeutral(){
  line(320, 350, 390, 350);
  line(320, 340, 320, 360);
  line(390, 340, 390, 360);
}

