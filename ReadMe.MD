// state
let alderic;
let ySpeed;

function setup() {
  createCanvas(1000, 1000);

  alderic = 0;
  ySpeed = 1;
}

function draw() {
  if (keyIsPressed)
  {
  background(240, 20, 140);
  } 
  else 
  {
  background(33); //Press H to make the background pink and to turn back to black
  } //works when presss a key on keyboard!

  // draw current frame based on state
  circle(alderic, 100, random(100));

  // modify state
  alderic = alderic + ySpeed;



  if(alderic>200)
  {
    ySpeed= -1; //normal speed of ball
  }

  /*if(mouseIsPressed)
  {
    ySpeed = 0;
  }
*/

  }

function mousePressed() {
  if (mouseButton == LEFT){
    ySpeed = 0; //ball stops moving
  }
 else if (mouseButton == RIGHT) {
      ySpeed = 1; //ball continues moving
    }
}
