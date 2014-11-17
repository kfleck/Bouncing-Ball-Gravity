float locy,locx;
int sz;
float velx,vely;
float gravity;
float accx;

void setup(){
  background(0);
  size(displayWidth,displayHeight);
  locx=width/2;
  locy=sz;
  sz=50;
  velx=0;
  vely=0;
  gravity=1;
  accx=0;
}
void draw(){
  ellipse(locx,locy,sz,sz);
 velx+=accx;
vely+=gravity;
locy+=vely;
locx+=velx;
if (locy>height){
  locy=height-sz/2;
  vely*=-1;
}
}
