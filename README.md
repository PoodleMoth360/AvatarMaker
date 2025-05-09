# AvatarMaker
3rd try at code. Remains faulty.

var num = [25];
var x = [];
var y = [];
let imgNose = [imgNose2, imgNose3, imgNose4];
let imgEyes = [imgEyes1, imgEyes2, imgEyes3];
let imgMouth = [imgMouth1, imgMouth3, imgMouth4, imgMouth5];
let imgHair = [imgHair1, imgHair4, imgHair5];
let imgBrows = [imgBrows1, imgBrows2, imgBrows3];
let imgStache = [imgStache1, imgStache2];
let imgGlasses = [imgGlasses1, imgGlasses2];
let imgHat = [imgHat1, imgHat2, imgHat3, imgHat4];

function preload() {
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
   nose();
  if(keyIsPressed && key == 'n'){
    image(imgNose3, 350, 300);
  }
    if(keyIsPressed){
     if(keyCode == RIGHT_ARROW && key == 'n'){
    image(imgNose4, 350, 300);
      }
    }
      if(keyIsPressed){
     if(keyCode == LEFT_ARROW && key == 'n'){
    image(imgNose2, 350, 300);
      }
    }      

  eyes();
  if(keyIsPressed && key == 'i'){
    image(imgEyes2, 350, 250);
  }
  if(keyIsPressed){
    if(keyCode == SHIFT && key == 'i'){
      image(imgEyes3, 350, 250);
    }
  }
  
  image(imgMouth1, 350, 370);   //mouth
  if (keyIsPressed && key == 'm'){
    image(imgMouth5, 350, 370);
  }
  if(keyIsPressed){
    if(key == 'm'&& keyCode == RIGHT_ARROW){
     image(imgMouth3, 350, 370);
    }
 }
  if(keyIsPressed){
    if(key == 'm'&& keyCode == RIGHT_ARROW){
      image(imgMouth4, 350, 370);
    }
  }  
  
  if(keyIsPressed && key == 'c'){
  image(imgHat1, 350, 150);
  }
   if(keyIsPressed){
    if(keyCode == RIGHT_ARROW && key == 'c'){
      image(imgHat2, 350, 150);
    }
  }
   if(keyIsPressed){
    if(keyCode == LEFT_ARROW && key == 'c'){
      image(imgHat3, 350, 150);
    }
  }
   if(keyIsPressed){
    if(keyCode == UP_ARROW && key == 'c'){
      image(imgHat4, 350, 150);
    }
  }

  image(imgHair1, 350, 175);
  if(keyIsPressed && key == 'h'){
    image(imgHair5, 350, 175);
  }
    if(keyIsPressed){
     if(keyCode == SHIFT && key == 'h'){
    image(imgHair4, 350, 175);
      }
    } 

  image(imgBrows1, 300, 212);
  if(keyIsPressed && key == 'b'){
      image(imgBrows2, 300, 212);
  }
  if(keyIsPressed){
    if(keyCode == SHIFT && key == 'b'){
        image(imgBrows3, 300, 212);
    }
  }

  if(keyIsPressed && key == 'f'){
    image(imgStache1, 350, 315);
  }
  if(keyIsPressed){
    if(keyCode == SHIFT && key == 'f'){
      image(imgStache2, 350, 315);
    }
  }
    
  if(keyIsPressed && key == 'g'){
    image(imgGlasses1, 350, 250)
  }
}

function drawBase(){
  beginShape();
  vertex(190, 420);
  vertex(510, 420);
  vertex(550, 600);
  vertex(150, 600);
  endShape(CLOSE);
  rect(275, 370, 150, 100, 15);
  ellipse(350, 260, 270, 330);
}

function eyes (){
  push();
  ellipse(300, 250, 50, 30);
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
function mouthMischief(){
  line(320, 350, 350, 390);
  line(400, 350, 350, 390);
}
function nose(){
  strokeWeight(0);
  rect(300, 300, 100, 100);
  strokeWeight(1);
  ellipse(350, 300, 25, 30);  
}
