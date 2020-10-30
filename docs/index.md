let img;
function preload(){
  img = loadImage("a.png")
}
x=100
var tela=0
var xmenu=125
var ymenu1=125
var ymenu2=185

largura=200
altura=50
function setup() {
  createCanvas(400, 400);
}

function draw() {
  textStyle(NORMAL)
  background(220);
  if(tela==0){
  textSize(26)
  //iniciar do jogo
  if(mouseX>xmenu && mouseX<xmenu+largura && mouseY>ymenu1 && mouseY<ymenu1+altura){
  stroke(200)
  fill(20)
  rect(xmenu,ymenu1,largura,altura,155,155,);
    if(mouseIsPressed){
      tela=1
      
    }
   
  }
  fill(255,0,0);
  noStroke()
  text("Iniciar",165,160)
  
  //informações do jogo 
  if(mouseX>xmenu && mouseX<xmenu+largura && mouseY>ymenu2 && mouseY<ymenu2+altura){
  stroke(200)
  fill(20)
  rect(xmenu,ymenu2,largura,altura,155,155)
    if(mouseIsPressed){
      tela=2
    }
  }
  fill(255,0,0)
  noStroke()
  text("Informações",165,220)
  }
  if(tela==1){
    image(img,0,0,400,400)
  }
  if(tela==2){
    textStyle(NORMAL)
    textSize(26)
    text("o jogo requer conhecimento do territorio brasileiro , onde o aluno precisa conhecer o nome dos estados e regiões do país",0,0,400,400)
  }

 
 
}
