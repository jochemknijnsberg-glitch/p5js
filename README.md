# p5js
[sketch.js](https://github.com/user-attachments/files/33197462/sketch.js)
let x = 8;
let y = 550;
let speed = 5;


let mousex = 0;
let mousey = 0;
let cloudOneX = 50;
function setup() {
    createCanvas(600, 600);
}

function draw() {
    
mouseMoved = function() {
  mousex = mouseX;
  mousey = mouseY;
  
}
background(135 + mousey / 6 , 206 - mousey / 10, 235 - mousey / 10),fill("orange");

  // Zon
  fill("orange");
  noStroke();
  circle(500, 100, 120);
  fill("yellow");
  noStroke();
  circle(500, 100, 100);
  
  // Gras
  fill("green");
  rect(0, 550, 600, 50);


  //big gray mountains
  stroke(3);
  fill(80);
  triangle(-150,550,75,173,400,550);
  triangle(100,550,300,173,550,550);
  
  // --- HUISJE ---
  // Basis van het huis
  fill("white");
  stroke("black");
  rect(100, 400, 150, 150);
  
  // Dak (driehoek)
  fill("crimson");
  triangle(80, 400, 175, 300, 270, 400);
  
  // Deur
  fill("saddlebrown");
  rect(150, 470, 40, 80);
  
  // Raam
  fill("lightblue");
  rect(120, 425, 50, 30);
  // man en vrouw
  textSize(20);
text("🧔‍♂️🧔‍♀️", 118, 450);

//jonge
textSize(20);
text("🧒", 8, 550);

// meisje
textSize(20);
text("👧", 560, 550);

// beweging van bal rood
  fill("red");
  circle(x, y, 20);
  x += speed;
  if (x > width || x < 0) {
    speed *= -1;

    // geluid
    let audio = new Audio("https://www.bing.com/ck/a?!&&p=ea19ecfc942db3a9ef23840203b39e9406c0181c7aace567f0905fe7453112ffJmltdHM9MTc4OTA4NDgwMA&ptn=3&ver=2&hsh=4&fclid=27647510-75f5-6f92-2ea8-62a874896e0f&psq=soundboard+ball+bounce+sound&u=a1aHR0cHM6Ly93d3cubXlpbnN0YW50cy5jb20vZW4vc2VhcmNoLz9uYW1lPWJhbGwlMjBib3VuY2UjOn46dGV4dD1MaXN0ZW4lMjBhbmQlMjBzaGFyZSUyMHNvdW5kcyUyMG9mJTIwQmFsbCUyMEJvdW5jZS4sRmluZCUyMG1vcmUlMjBpbnN0YW50JTIwc291bmQlMjBidXR0b25zJTIwb24lMjBNeWluc3RhbnRzJTIx");
    audio.play(90); 
}


//custom variable for x coordinate of cloud

  //cloud
  fill(255);
  ellipse(cloudOneX, 50, 80, 40);

  //sets the x coordinate to the frame count
  //resets at left edge
  cloudOneX = frameCount % width

  //displays the x and y position of the mouse on the canvas
  fill(255) //white text
  text(`mouseX: ${mouseX}, mouseY: ${mouseY}`, 20, 20);  
}
