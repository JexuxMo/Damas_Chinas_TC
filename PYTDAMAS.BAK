#include<conio.h>
#include<stdio.h>
#include<graphics.h>
#include<stdlib.h>
#include<dos.h>
void mouse(int &a,int &b,int &c,int &d )
{
 union REGS inregs, outregs;

 inregs.x.ax  =  a;
 inregs.x.bx  =  b;
 inregs.x.cx  =  c;
 inregs.x.dx  =  d;
 int86( '\x33' , &inregs, &outregs );
 a = outregs.x.ax ;
 b = outregs.x.bx ;
 c = outregs.x.cx ;
 d = outregs.x.dx ;
}
void activa()
{  int a=0,b,c,d;
   mouse(a,b,c,d);
}
void pon()
{  int a=1,b,c,d;
   mouse(a,b,c,d);
}
void quita()
{  int a=2,b,c,d;
   mouse(a,b,c,d);
}
void mcoord ( int &a, int &b, int &x, int &y )
{
   mouse(a,b,x,y);
}
void mgoto( int x, int y )
{  int a=4,b;
   mouse(a,b,x,y);
}
void columnas ( int low, int hi )
{  int a=7,b;
   mouse(a,b,low,hi);
}
void renglones ( int low, int hi )
{  int a=8,b;
   mouse(a,b,low,hi);
}
void inicializa()
{int gm, gb=DETECT;
initgraph(&gb,&gm,"d:\\tc\\tcpp\\bgi");
}
void box(int x1,int y1,int x2,int y2,int relleno,int color)
 {int poly[8];
poly[0]=x1;
poly[1]=y1;
poly[2]=x2;
poly[3]=y1;
poly[4]=x2;
poly[5]=y2;
poly[6]=x1;
poly[7]=y2;
setfillstyle(relleno,color);
fillpoly(4,poly);
 }
void tablero()
{int i,j;
box(0,0,getmaxx(),getmaxy(),1,0);
setfillstyle(1,7);
bar(0,0,640,480);
setfillstyle(1,1);
bar(5,430,635,475);
setfillstyle(1,4);
bar(7,432,112,472);//jugador 1
setcolor(10);
settextstyle(1,0,2);
outtextxy(12,440,"JUGADOR1");
setfillstyle(1,0);
bar(115,432,233,472);//jugador 2
bar(238,432,350,472);//guardar
bar(352,432,464,472);//cargar
bar(467,432,581,472);//nuevo
bar(586,432,630,472);//salir
setcolor(10);
settextstyle(1,0,2);
outtextxy(125,440,"JUGADOR2");
outtextxy(248,440,"GUARDAR");
outtextxy(366,440,"CARGAR");
outtextxy(491,440,"NUEVO");
outtextxy(600,440,"X");
setcolor(0);
 for(i=0;i<=16;i++)
 for(j=0;j<=24;j++)
 box(0+j*25,0+i*25,25+j*25,25+i*25,1,15);//matriz 25x17
/*color del centro del tablero*/
for(i=0;i<=4;i++)
for(j=0;j<=8;j++)
box(100+j*50,100+i*50,125+j*50,125+i*50,1,3);
for(i=0;i<=3;i++)
for(j=0;j<=7;j++)
box(125+j*50,125+i*50,150+j*50,150+i*50,1,3);
/*COLORES DE PUNTAS DE TABLERO*/
box(300,0,325,25,1,3);
box(275,25,300,50,1,3);
box(325,25,350,50,1,3);
for(i=0;i<=2;i++)
for(j=0;j<=0;j++)
box(250+i*50,50+j*50,275+i*50,75+j*50,1,3);
for(i=0;i<=3;i++)
for(j=0;j<=0;j++)
box(225+i*50,75+j*50,250+i*50,100+j*50,1,3);//punta negra
box(300,400,325,425,1,3);
box(275,375,300,400,1,3);
box(325,375,350,400,1,3);
for(i=0;i<=2;i++)
for(j=0;j<=0;j++)
box(250+i*50,350+j*50,275+i*50,375+j*50,1,3);
for(i=0;i<=3;i++)
for(j=0;j<=0;j++)
box(225+i*50,325+j*50,250+i*50,350+j*50,1,3);//punta amarilla
box(75,175,100,200,1,3);
box(50,150,75,175,1,3);
box(100,150,125,175,1,3);
for(i=0;i<=2;i++)
for(j=0;j<=0;j++)
box(25+i*50,125+j*50,50+i*50,150+j*50,1,3);
for(i=0;i<=3;i++)
for(j=0;j<=0;j++)
box(0+i*50,100+j*50,25+i*50,125+j*50,1,3);//punta magenta
box(75,225,100,250,1,3);
box(50,250,75,275,1,3);
box(100,250,125,275,1,3);
for(i=0;i<=2;i++)
for(j=0;j<=0;j++)
box(25+i*50,275+j*50,50+i*50,300+j*50,1,3);
for(i=0;i<=3;i++)
for(j=0;j<=0;j++)
box(0+i*50,300+j*50,25+i*50,325+j*50,1,3);//punta verde
box(525,225,550,250,1,3);
box(500,250,525,275,1,3);
box(550,250,575,275,1,3);
for(i=0;i<=2;i++)
for(j=0;j<=0;j++)
box(475+i*50,275+j*50,500+i*50,300+j*50,1,3);
for(i=0;i<=3;i++)
for(j=0;j<=0;j++)
box(450+i*50,300+j*50,475+i*50,325+j*50,1,3);//punta amarilla
box(525,175,550,200,1,3);
box(500,150,525,175,1,3);
box(550,150,575,175,1,3);
for(i=0;i<=2;i++)
for(j=0;j<=0;j++)
box(475+i*50,125+j*50,500+i*50,150+j*50,1,3);
for(i=0;i<=3;i++)
for(j=0;j<=0;j++)
box(450+i*50,100+j*50,475+i*50,125+j*50,1,3);//punta cyan
}
void ficha1(int x, int y)
{
   setcolor(0);
   setfillstyle(1,0);
   fillellipse(x,y-5,12,12);//cabello
   setfillstyle(1,6);
   fillellipse(x,y+3-5,11,10); //cara dama afri.
   setfillstyle(1,15);
   fillellipse(x-6,y+3-5,2,1);//ojo
   fillellipse(x+5,y+3-5,2,1);//ojo
   putpixel(x-6,y+3-5,0);
   putpixel(x+5,y+3-5,0);
   setfillstyle(1,14);
   fillellipse(x-1,y-5,1,2);
   fillellipse(x-10,y+7-5,2,4);
   fillellipse(x+10,y+7-5,2,4);
}
void ficha2(int x, int y)
{/*dama asiatica*/
   setcolor(0);
   setfillstyle(1,9);
fillellipse(x+1,y-3,12,10);//cabello dama c.
fillellipse(x-7,y-10,5,4);//
fillellipse(x+8,y-10,5,4);//
setfillstyle(1,14);
fillellipse(x+1,y+1,11,7); //cara dama china
setfillstyle(1,15);
fillellipse(x-5,y,3,0);//ojo
fillellipse(x+6,y,3,0);//ojo
putpixel(x-5,y,0);
putpixel(x+6,y,0);
}
int jugadores()
{int k,j,x,y,T[17][25]={0};
///JUGADOR 1////
 T[12][16]=1;T[11][15]=1;T[13][15]=1;T[10][14]=1;T[12][14]=1;T[14][14]=1;
 T[9][13]=1;T[11][13]=1;T[13][13]=1;T[15][13]=1;
 for(k=0;k<16;k++)
 for(j=0;j<24;j++)
 {if(T[k][j]==1)ficha1(x=12+k*25,y=14+j*25);
 }
///JUGADOR 2////
T[12][0]=2;T[11][1]=2;T[13][1]=2;T[10][2]=2;T[12][2]=2;T[14][2]=2;
T[9][3]=2;T[11][3]=2;T[13][3]=2;T[15][3]=2;
 for(k=0;k<=16;k++)
 for(j=0;j<=24;j++)
 {if(T[k][j]==2)ficha2(x=12+k*25,y=14+j*25);
 }
}
void jugar()
{ int i,j,k,a,b,c,d,c1,c2,px1,py1,px2,py2,TG[25][17],
T[25/*x*/][17/*y*/]={0},x,y,turnoj=1,turnojg,c1g,c2g;
  float x1,y1,x2,y2;
   i=0;
   c1=10;
   c2=10;
   clrscr();
   clearviewport();
   activa();
   tablero();
   jugadores();
for(k=0;k<=8;k++)
for(j=0;j<=4;j++)
T[4+k*2][4+j*2]=3;
for(k=0;k<=9;k++)
for(j=0;j<=3;j++)
T[3+k*2][5+j*2]=3;T[0][4]=3;T[2][4]=3;T[24][4]=3;T[22][4]=3;
T[0][12]=3;T[2][12]=3;T[24][12]=3;T[22][12]=3;T[1][5]=3;T[2][6]=3;
T[23][5]=3;T[22][6]=3;T[1][11]=3;T[2][10]=3;T[23][11]=3;T[22][10]=3;
T[12][16]=1;T[11][15]=1;T[13][15]=1;T[10][14]=1;T[12][14]=1;T[14][14]=1;
T[9][13]=1;T[11][13]=1;T[13][13]=1;T[15][13]=1;
T[12][0]=2;T[11][1]=2;T[13][1]=2;T[10][2]=2;T[12][2]=2;T[14][2]=2;
T[9][3]=2;T[11][3]=2;T[13][3]=2;T[15][3]=2;
   do {
       a=3;
       mouse(a,b,c,d);
       switch( b ) {
       case 1 :
	 quita();
/////////////////botones del juego/////////////////////
       if ( c>586 && c<630 && d>432 && d<472 )
	{setfillstyle(1,4);
	 bar(586,432,630,472);//salir
	 settextstyle(1,0,2);
	 outtextxy(600,440,"X");
	 i=1;
	}
       if ( c>467 && c<581 && d>432 && d<472 )
	{setfillstyle(1,4);
	 bar(467,432,581,472);//nuevo
	 settextstyle(1,0,2);
	 outtextxy(491,440,"NUEVO");
	 tablero();
	 jugadores();
	 for(k=0;k<=8;k++)
	 for(j=0;j<=4;j++)T[4+k*2][4+j*2]=3;
	 for(k=0;k<=9;k++)
	 for(j=0;j<=3;j++)T[3+k*2][5+j*2]=3;
	 T[0][4]=3;T[2][4]=3;T[24][4]=3;T[22][4]=3;T[0][12]=3;T[2][12]=3;
	 T[24][12]=3;T[22][12]=3;T[1][5]=3;T[2][6]=3;T[23][5]=3;T[22][6]=3;
	 T[1][11]=3;T[2][10]=3;T[23][11]=3;T[22][10]=3;T[12][16]=1;
	 T[11][15]=1;T[13][15]=1;T[10][14]=1;T[12][14]=1;T[14][14]=1;
	 T[9][13]=1;T[11][13]=1;T[13][13]=1;T[15][13]=1;T[12][0]=2;
	 T[11][1]=2;T[13][1]=2;T[10][2]=2;T[12][2]=2;T[14][2]=2;T[9][3]=2;
	 T[11][3]=2;T[13][3]=2;T[15][3]=2;
	 c1=10;c2=10;turnoj=1;
	}
       if ( c>238 && c<350 && d>432 && d<472 )
	{setfillstyle(1,4);
	 bar(238,432,350,472);//guardar
	 setcolor(10);
	 settextstyle(1,0,2);
	 outtextxy(248,440,"GUARDAR");
	 delay(100);
	 setfillstyle(1,0);
	 bar(238,432,350,472);//guardar
	 settextstyle(1,0,2);
	 outtextxy(248,440,"GUARDAR");
	 for(k=0;k<=24;k++)
	 for(j=0;j<=16;j++)
	  TG[k][j]=T[k][j];
	 c1g=c1;c2g=c2;
	}
       if ( c>352 && c<464 && d>432 && d<472 )
	{setfillstyle(1,4);
	 bar(352,432,464,472);//cargar
	 outtextxy(366,440,"CARGAR");
	 tablero();
	 for(k=0;k<=24;k++)
	 for(j=0;j<=16;j++)
	  {T[k][j]=TG[k][j];
	  if(TG[k][j]==1)ficha1(x=12+k*25,y=14+j*25);
	   else if(TG[k][j]==2)ficha2(x=12+k*25,y=14+j*25);
	  }
	   c1=c1g;c2=c2g;
	}
       if(c>7 && c<112 && d>432 && d<472)
	 {setfillstyle(1,4);
	 bar(7,432,112,472);//jugador 1
	 setcolor(10);
	 settextstyle(1,0,2);
	 outtextxy(12,440,"JUGADOR1");
	 setfillstyle(1,0);
	 bar(115,432,233,472);//jugador 2
	 settextstyle(1,0,2);
	 outtextxy(125,440,"JUGADOR2");
	 turnoj=1;
	 }
       if(c>115 && c<233 && d>432 && d<472)
	 { setfillstyle(1,4);
	 bar(115,432,233,472);//jugador 2
	 setcolor(10);
	 settextstyle(1,0,2);
	 outtextxy(125,440,"JUGADOR2");
	 setfillstyle(1,0);
	 bar(7,432,112,472);//jugador 1
	 settextstyle(1,0,2);
	 outtextxy(12,440,"JUGADOR1");
	 turnoj=2;
      }
//////////////despintar fichas//////////////////
       for(k=0;k<=24;k++)
       for(j=0;j<=16;j++)
	 {x1=k*25;
	  y1=j*25;
	  x2=25+k*25;
	  y2=25+j*25;
	if(c>x1 && c<x2 && d>y1 && d<y2 && c1==10 && c2==10 && T[k][j]==1 && turnoj==1)
	  {setcolor(15);
	   setfillstyle(1,15);
	   bar(x1,y1-25,x2,y2-25);
	   setfillstyle(1,3);
	   bar(x1,y1,x2,y2);
	   T[k][j]=3;////ausencia de ficha
	   c1=9;
	  px1=x1;px2=x2;
	  py1=y1;py2=y2;
	  }
	if(c>x1 && c<x2 && d>y1 && d<y2 && c1==10 && c2==10 && T[k][j]==2 && turnoj==2)
	  {setcolor(15);
	   setfillstyle(1,15);
	   bar(x1,y1-25,x2,y2-25);
	   setfillstyle(1,3);
	   bar(x1,y1,x2,y2);
	   T[k][j]=3;///ausencia de ficha
	   c2=9;
	  px1=x1;px2=x2;
	  py1=y1;py2=y2;
	  }
	 }
       break;
       case 2:
////////pintar ficha/////////
       quita();
       for(k=0;k<=24;k++)
       for(j=0;j<=16;j++)
	 {x1=k*25;
	  y1=j*25;
	  x2=25+k*25;
	  y2=25+j*25;
	if(c>x1 && c<x2 && d>y1 && d<y2 && c1==9 && c2==10 && T[k][j]==3)
	  { if(x1==px1 && y1==py1 && x2==px2 && y2==py2)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(700);delay(100);}
	    if(x1==px1+25 && y1==py1-25 && x2==px2+25 && y2==py2-25 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}

	    if(x1==px1+50 && y1==py1 && x2==px2+50 && y2==py2 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1+25 && y1==py1+25 && x2==px2+25 && y2==py2+25 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1-25 && y1==py1-25 && x2==px2-25 && y2==py2-25 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1-50 && y1==py1 && x2==px2-50 && y2==py2 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1-25 && y1==py1+25 && x2==px2-25 && y2==py2+25 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1+50 && y1==py1-50 && x2==px2+50 && y2==py2-50 && T[k-1][j+1]==1 && turnoj==1)//saltar ficha
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1+100 && y1==py1 && x2==px2+100 && y2==py2 && T[k-2][j]==1 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1+50 && y1==py1+50 && x2==px2+50 && y2==py2+50 && T[k-1][j-1]==1 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1-50 && y1==py1-50 && x2==px2-50 && y2==py2-50 && T[k+1][j+1]==1 && turnoj==1)//saltar ficha
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1-100 && y1==py1 && x2==px2-100 && y2==py2 && T[k+2][j]==1 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1-50 && y1==py1+50 && x2==px2-50 && y2==py2+50 && T[k+1][j-1]==1 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1+50 && y1==py1-50 && x2==px2+50 && y2==py2-50 && T[k-1][j+1]==2 && turnoj==1)//saltar ficha
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1+100 && y1==py1 && x2==px2+100 && y2==py2 && T[k-2][j]==2 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1+50 && y1==py1+50 && x2==px2+50 && y2==py2+50 && T[k-1][j-1]==2 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1-50 && y1==py1-50 && x2==px2-50 && y2==py2-50 && T[k+1][j+1]==2 && turnoj==1)//saltar ficha
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1-100 && y1==py1 && x2==px2-100 && y2==py2 && T[k+2][j]==2 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	    if(x1==px1-50 && y1==py1+50 && x2==px2-50 && y2==py2+50 && T[k+1][j-1]==2 && turnoj==1)
	      {ficha1(x=12+k*25,y=14+j*25);
	       c1=10;
	       T[k][j]=1;sound(500);delay(100);}
	  }
	if(c>x1 && c<x2 && d>y1 && d<y2 && c1==10 && c2==9 && T[k][j]==3)
	  { if(x1==px1 && y1==py1 && x2==px2 && y2==py2)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(700);delay(100);}
	    if(x1==px1+25 && y1==py1-25 && x2==px2+25 && y2==py2-25)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1+50 && y1==py1 && x2==px2+50 && y2==py2)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1+25 && y1==py1+25 && x2==px2+25 && y2==py2+25)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1-25 && y1==py1-25 && x2==px2-25 && y2==py2-25)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1-50 && y1==py1 && x2==px2-50 && y2==py2)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1-25 && y1==py1+25 && x2==px2-25 && y2==py2+25)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1+50 && y1==py1-50 && x2==px2+50 && y2==py2-50 && T[k-1][j+1]==1)//saltar ficha
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1+100 && y1==py1 && x2==px2+100 && y2==py2 && T[k-2][j]==1)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1+50 && y1==py1+50 && x2==px2+50 && y2==py2+50 && T[k-1][j-1]==1)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1-50 && y1==py1-50 && x2==px2-50 && y2==py2-50 && T[k+1][j+1]==1)//saltar ficha
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1-100 && y1==py1 && x2==px2-100 && y2==py2 && T[k+2][j]==1)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1-50 && y1==py1+50 && x2==px2-50 && y2==py2+50 && T[k+1][j-1]==1)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1+50 && y1==py1-50 && x2==px2+50 && y2==py2-50 && T[k-1][j+1]==2)//saltar ficha
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1+100 && y1==py1 && x2==px2+100 && y2==py2 && T[k-2][j]==2)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1+50 && y1==py1+50 && x2==px2+50 && y2==py2+50 && T[k-1][j-1]==2)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1-50 && y1==py1-50 && x2==px2-50 && y2==py2-50 && T[k+1][j+1]==2)//saltar ficha
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1-100 && y1==py1 && x2==px2-100 && y2==py2 && T[k+2][j]==2)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	    if(x1==px1-50 && y1==py1+50 && x2==px2-50 && y2==py2+50 && T[k+1][j-1]==2)
	      {ficha2(x=12+k*25,y=14+j*25);
	       c2=10;
	       T[k][j]=2;sound(500);delay(100);}
	  }
	 }
	 nosound();
	 break;
		   }
       pon();
      } while ( i!=1 );
quita();
}
void damas(int x, int y)
{
/*dama de africa*/
setcolor(0);
setfillstyle(1,0);
fillellipse(x,y-3+5,13,12);//cabello
setfillstyle(1,6);
fillellipse(x,y+5,12,10); //cara dama afri.
setfillstyle(1,15);
fillellipse(x-6,y+5,2,1);//ojo
fillellipse(x+5,y+5,2,1);//ojo
putpixel(x-6,y+5,0);
putpixel(x+5,y+5,0);
setfillstyle(1,14);
fillellipse(x-1,y-3+5,1,2);
fillellipse(x-11,y+4+5,2,5);
fillellipse(x+11,y+4+5,2,5);
x=x+34;y=y+20;/*dama asiatica*/
setcolor(0);
setfillstyle(1,9);
fillellipse(x,y-2+7,15,10);//cabello dama c.
fillellipse(x-12,y-8+7,5,5);//
fillellipse(x+12,y-8+7,5,5);//
setfillstyle(1,14);
fillellipse(x,y+1+7,13,7); //cara dama china
setfillstyle(1,15);
fillellipse(x-6,y+7,3,0);//ojo
fillellipse(x+5,y+7,3,0);//ojo
putpixel(x-6,y+7,0);
putpixel(x+5,y+7,0);
x=x+35;y=y+20;/*dama de oceania*/
setcolor(0);
setfillstyle(1,4);
fillellipse(x,y-2,12,12);//cabello dama o.
setfillstyle(1,12);
fillellipse(x,y,11,10); //cara dama o.
setfillstyle(1,15);
fillellipse(x-5,y,2,1);//ojo
fillellipse(x+4,y,2,1);//ojo
putpixel(x-5,y,0);
putpixel(x+4,y,0);
setfillstyle(1,4);
sector(x-6,y+1,270,90,5,10);//fleco dama o.
x=x+30;y=y+10;/*dama de europa*/
setcolor(0);
setfillstyle(1,5);
sector(x,y+7,180,0,14,20);//cabello
setfillstyle(1,7);
fillellipse(x,y+1,9,11); //cara dama europe.
setfillstyle(1,15);
fillellipse(x-5,y,2,2);//ojo
fillellipse(x+4,y,2,2);//ojo
putpixel(x-5,y,0);
putpixel(x+4,y,0);
setfillstyle(1,5);
sector(x,y-1,180,0,11,10);//copete
x=x+35;y=y+5;/*dama de norteamerica*/
setcolor(0);
setfillstyle(1,6);
fillellipse(x,y-3,14,10);//cabello
 fillellipse(x-4,y-3,8,10);//cabello
fillellipse(x+5,y-3,8,10);//cabello
setfillstyle(1,11);
fillellipse(x,y+1,9,11); //cara dama norteame.
setfillstyle(1,15);
fillellipse(x-5,y,2,1);//ojo
fillellipse(x+4,y,2,1);//ojo
putpixel(x-5,y,0);
putpixel(x+4,y,0);
setfillstyle(1,6);
fillellipse(x,y-7,6,3);//cabello
x=x+33;y=y-3;/*dama de sudamerica*/
setcolor(0);
setfillstyle(1,6);
fillellipse(x,y-9,5,5);
fillellipse(x,y+1,11,11);//cabello
setfillstyle(1,10);
fillellipse(x,y+3,10,9); //cara dama sudame.
setfillstyle(1,15);
fillellipse(x-5,y,1,2);//ojo
fillellipse(x+4,y,1,2);//ojo
putpixel(x-5,y,0);
putpixel(x+4,y,0);
}
void menu()
 {int x=150,y=350;
clearviewport();
setcolor(15);
setfillstyle(1,5);
fillellipse(320,240,320,140);//elipse magenta
setfillstyle(1,6);
fillellipse(290,240,220,180);//elipse brown
setfillstyle(1,1);
fillellipse(400,290,150,70);//elipse azul
setfillstyle(1,4);
fillellipse(400,180,150,70);//elipse rojo
damas(x,y);
setfillstyle(1,7);
bar(65,160,220,315);
setfillstyle(1,4);
bar(70,165,215,310);
setfillstyle(1,0);
bar(72,167,213,307);
setcolor(10);
settextstyle(6,0,1);
outtextxy(75,200,"DAMAS CHINAS");
setcolor(9);
outtextxy(74,250,"HECHO POR:");
outtextxy(74,270,"JESUS MOJARRO");
setcolor(0);
outtextxy(350,160,"JUGAR PARTIDA");
outtextxy(350,270,"SALIR DEL JUEGO");
 }
void mueve()
 {int i;
char tecla;
i=1;
menu();
do{
switch(i)
{case 1:setcolor(0);
	outtextxy(350,270,"SALIR DEL JUEGO");
	setcolor(15);
	outtextxy(350,160,"JUGAR PARTIDA");
	break;
 case 2:setcolor(0);
	outtextxy(350,160,"JUGAR PARTIDA");
	setcolor(15);
	outtextxy(350,270,"SALIR DEL JUEGO");
	break;
}//Fin white
tecla=getch();
switch(i)
{case 1:setcolor(0);
	outtextxy(350,270,"SALIR DEL JUEGO");
	setcolor(7);
	outtextxy(350,160,"JUGAR PARTIDA");
	break;
 case 2:setcolor(0);
	outtextxy(350,160,"JUGAR PARTIDA");
	setcolor(7);
	outtextxy(350,270,"SALIR DEL JUEGO");
	break;
}//Fin dark
switch (tecla)
{case 0: tecla=getch();
	 switch(tecla)
	 {case 72: i--;break;
	  case 80: i++;break;
	 }
	 if(i>2) i=1;
	 if(i<1) i=2;
	 break;//fin cero
 case 13: switch(i)
	 {case 1:jugar();break;

	  case 2: tecla=27;break;
	 }
	 if (i!=3) menu();/* esto es para que no se borre los rectangulos del
	 del menu, o tambien para que no pierdas los que tienes*/
	 break;//fin entero
}//fin tecla
  }while(tecla!=27);
 }
void main()
 {
inicializa();
mueve();
 }