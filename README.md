int x;              // declare globally
int xSpeed;
int y;              
int ySpeed;

void setup() {
  size(400, 400);
  x = 30;          // initialize in setup
  xSpeed = 3;
  y = 200;              
  ySpeed = 2;
}

void draw() {
  x += xSpeed;     // update variable
  y += ySpeed;
  
  // x boundary check
  if (x >= width - 25) {
    xSpeed = -xSpeed;
  } else if (x <= 25) {
    xSpeed = -xSpeed;
  }
  if (y >= height - 25) {
    ySpeed = -ySpeed;
  } else if (y <= 25) {
    ySpeed = -ySpeed;
  }
  
  background(#23395B);
  // draw ball
  noStroke();
  fill(#FFFD98);
  ellipse(x, y, 50, 50);     // use variable to draw
}
