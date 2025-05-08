# AvatarMaker
first draft of code. it does not work.


var num = [25];
var x = [];
var y = [];

let imgEars;
let imgNose2;
let imgNose3;
let imgNose4;
let imgEyes2;
let imgEyes3;
let imgMouth1;
let imgMouth3;
let imgMouth4;
let imgMouth5;
let imgHair1;
let imgHair4;
let imgHair5;
let imgBrows1;
let imgBrows2;
let imgBrows3;
let imgStache1;
let imgStache2;
let imgGlasses1;
let imgHat1;
let imgHat2;
let imgHat3;
let imgHat4;

function preload() {
  imgEars = loadImage('ears.JPEG');
  imgNose3 = loadImage('Nose3.JPEG');
  imgNose4 = loadImage('Nose4.JPEG');
  imgNose2 = loadImage('Nose2.JPEG');
  imgEyes2 = loadImage('Eyes2.JPEG');
  imgEyes3 = loadImage('Eyes3.JPEG');
  imgMouth1 = loadImage('Mouth1.JPEG');
  imgMouth3 = loadImage('Mouth3.JPEG');
  imgMouth4 = loadImage('Mouth4.JPEG');
  imgMouth5 = loadImage('Mouth5.JPEG');
  imgHair1 = loadImage('Hair1.JPEG');
  imgHair4 = loadImage('Hair4.JPEG');
  imgHair5 = loadImage('Hair5.JPEG');
  imgBrows1 = loadImage('Brows1.JPEG');
  imgBrows2 = loadImage('Brows2.JPEG');
  imgBrows3 = loadImage('Brows3.JPEG');
  imgStache1 = loadImage('Stache1.JPEG');
  imgStache2 = loadImage('Stache2.JPEG');
  imgGlasses1 = loadImage('Glasses1.JPEG');
  imgHat1 = loadImage('Hat1.JPEG');
  imgHat2 = loadImage('Hat2.JPEG');
  imgHat3 = loadImage('Hat3.JPEG');
  imgHat4 = loadImage('Hat4.JPEG');

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
  background(250); 

  drawBase();

  
    //nose  
    if(keyIsPressed && key == 'n'){
  }
  
  eyes(); //eyes
  if(keyIsPressed && key == 'i'){
  }
  
  //mouth
  mouthNeutral();
  if (keyIsPressed && key == 'm'){
    smileBig();
  } 
  if(keyIsPressed && keyCode == UP_ARROW){
    if(mouseIsPressed){
     smileSmol(); 
    }
 }
    
    //hat
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




