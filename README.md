var x;
var y;
var radius;

function setup() {
  createCanvas(600, 400);
  x = random(width);
  y = random(height);
  radius = 100;
}

function draw() {
  background(10);

  if (dist(mouseX, mouseY, x, y) < radius) {
    if (mouseButton) {
      x = random(-10);
      y = random(-10);
    }
    fill(100, 200, 200, 200);
  }
  else {
    fill(200, 200, 200, 200);
  }

  ellipse(x, y, radius * 2);
  x += random(-1, 3);
  y += random(-1, 3);
}
