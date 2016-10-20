# flipperkast
Balletje die op een plank komt
```
void setup()
{
  size(600,400);
}
float ballX = 200;
float bally = 100;
float speedX = 10;
float speedy = 0;
int hit = 0;
int miss = 0;

void draw()
 {
   float paddle = 1000/(hit+10);
   if(bally < 0 || ballX >width) speedX = -speedX;
   if(bally > height) {
     speedy = -speedy;
     float distance = abs(mouseX-ballX);
     if(distance < paddle) hit += 1;
     else miss += 1;
   } else speedy +=1;
   
  
   ballX += speedX;
   bally += speedy;
   background(100,200,50);
   fill(210,105,30);
   ellipse(ballX, bally, 50, 50);
   fill(100,20,125);
   rect(mouseX-100,height-10, 200, 10);   
 
  
 fill(0);
 text("hit: " + hit,10,10);
 text("miss; -" + miss, 10, 40);
 }
 
 
```
