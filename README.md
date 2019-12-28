# Processing

float x;
float y;
float radius;
float angle;
int time;

void setup() {
         size(1080,1080); 
         x=0;
         y=0;
         angle=0;
         radius = 50;
         time = 20;
         
          
}

void draw() {
 background(0);
 noFill();
 stroke(255);
 strokeWeight(5);
 translate(width/2,height/2);
 blendMode(REPLACE);
 
 
 
 //angle+=PI/128;
 for (int r=20; r<2000;r+=20){
           angle-=PI/16384;
 x=radius*cos(angle+r*PI/(250));
 y=radius*sin(angle+r*PI/(250));
 //count+=0.1;
 //if(r/50==count) {
 //strokeWeight(5);
 //}
 //stroke(HSB,220,100,100);
 circle(x,y,r);
 
 }
 //saveFrame("spiral_circles2-#####.png");
 if(frameCount > 60*time) {
   exit();         
  }         
          
 translate(-width/2,-height/2);
}
