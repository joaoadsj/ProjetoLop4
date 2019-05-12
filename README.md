# ProjetoLop4
etapa 4
//nome: joão andre da silva júnior;subturma:D

var x=300
var y=0
var xd
var yd
var t=200
var estadoDisparo = false;
function setup() {
  createCanvas(800, 800);
}

function draw() {
  background(220);
  rect(y,100,50,150)
ellipse(x,t,70,70)
   if ( keyIsDown(RIGHT_ARROW) )
  {
    x=x+4
  }
  if(x > 300)
  {
    y=y+3
  }
  if(x > 800 || y > 800)
  {
    x=300
    y=0
  }
  ellipse(xd,yd,20,20)
  if ( keyIsDown(CONTROL) && ! estadoDisparo)
  {
    xd=x
    yd=t
    estadoDisparo = true;
  }

if( estadoDisparo ) {
  ellipse(xd,yd,20,20)
  xd=xd+10;
}
  if(xd > 800)
  {
    estadoDisparo=false
  }
}
  
