/* A project on TOURIST PORTAL by SHUBHAM GAUTAM of batch year 2018-2019 */

#include<fstream.h>
#include<string.h>
#include<dos.h>
#include<conio.h>
#include<ctype.h>
#include<graphics.h>
#include<stdlib.h>
#include<stdio.h>
#define size 5

int car(void);      //for car
int weltxt(void);   //for "WELCOME TO TOURIST PORTAL"
int tourp(void);    //for main menu
void Adm();         //for Admin menu
void admrgt();      //for displaying admin rights
void Nwusr();       //for new user registration
void openusr();     //for opening user
void Edit();        //for editing users
void Delete();      //for deleting users
int randcolor()     //for generating random colors
{
    int color;
    randomize();
    color=2+random(11);
    return color;
}
int entry,countusr=0,sten;  //global variables

/* User Class*/
class usr
{
   private:
      unsigned int c_id;
      char name[20],pass[20],usrn[20];
   public:
      void getdata();
      void showdata();
      void gen_cid()
      {
	 randomize();
	 c_id=5000+random(1001);
      }
      int retcid()
      {
	 return c_id;
      }
}obj;

/*for fetching data from users*/
void usr::getdata()
{
   int gd=EGA,gm=EGAHI;
   char ch;
   initgraph(&gd,&gm,"C:/TURBOC3/BGI");

   settextstyle(2,HORIZ_DIR,5);
   setbkcolor(randcolor());
   outtextxy((getmaxx()/2)-100,152,"Enter your name:");
   gotoxy(44,12);
   gets(name);

   outtextxy((getmaxx()/2)-120,194,"Enter your username:");
   gotoxy(46,15);
   cin>>usrn;

   outtextxy((getmaxx()/2)-120,236,"Create your password:");
   //password code
   for(int j=0;j<10;j++)
   {
     if(j<0)
     {
       j=0;
       gotoxy(47,18);
     }
     ch=getch();
     if(ch=='\r')
     {
	pass[j]='\0';
	break;
     }
     else if(ch=='\b')
     {
	 cout<<"\b \b";
	 j-=2;
     }
     else
     {
	pass[j]=ch;
	gotoxy(47+j,18);
	cout<<"*";
     }
   }
   if(sten!=100)
   {
     outtextxy((getmaxx()/2)-120,278,"Your Customer ID is:");
     gotoxy(47,21);
     gen_cid();
     cout<<c_id;
     getch();
     closegraph();
   }

}

/*for displaying user*/
void usr::showdata()
{
   clrscr();
   ifstream fin("userdata.dat",ios::in|ios::binary);
   int gd=EGA,gm=EGAHI,choice;
   initgraph(&gd,&gm,"C:/TURBOC3/BGI");
   setbkcolor(randcolor());
   setlinestyle(DASHED_LINE,1, 1);
   line(20,20,getmaxx()-20,20);
   line(20,50,getmaxx()-20,50);
   line(40,20,40,getmaxy()-20);
   line(220,20,220,getmaxy()-20);
   line(410,20,410,getmaxy()-20);
   line(600,20,600,getmaxy()-20);
   line(20,getmaxy()-20,getmaxx()-20,getmaxy()-20);

   settextstyle(11,HORIZ_DIR,3);
   outtextxy(85,33,"Customer ID");
   outtextxy(300,33,"Name");
   outtextxy(480,33,"Username");
   int cnt=0;
   if(countusr==0)
   {
      outtextxy(228,180,"No Records Available!!");
   }
   else
   {
      while(fin.read((char*)&obj,sizeof(obj)))
      {
	  gotoxy(15,6+cnt);
	  cout<<c_id;
	  gotoxy(32,6+cnt);
	  cout<<name;
	  gotoxy(60,6+cnt);
	  cout<<usrn;
	  cnt++;
      }
   }
   getch();
   closegraph();
   admrgt();
}

//for the car to move
int car()
{
   int gdriver = DETECT, gmode, errorcode;
   int xmax, ymax;
   initgraph(&gdriver, &gmode, "C:/TURBOC3/BGI");
   setcolor(15);
   getbkcolor();
   setbkcolor(randcolor());
   for(int i=0;i<=500;i++)
   {
     line(0+i,239,45+i,230);    //start line
     line(45+i,230,95+i,170);
     line(95+i,170,190+i,170);
     line(190+i,170,240+i,230);
     line(240+i,230,320+i,239);
     line(320+i,239,325+i,270);
     line(325+i,270,280+i,270);
     arc(260+i,270,0,180,20);      //mudguard1
     circle(260+i,270,15);         //wheel1
     line(240+i,270,120+i,270);
     arc(100+i,270,0,180,20);      //mudguard2
     circle(100+i,270,15);         //wheel2
     line(80+i,270,75+i,270);
     arc(55+i,270,0,180,20);       //mudguard3
     circle(55+i,270,15);          //wheel3
     line(35+i,270,0+i,270);
     line(0+i,270,0+i,239);
     //line(45,230,240,230);       //middle line

     line(75+i,220,135+i,220);     //window 1
     line(135+i,220,135+i,185);
     line(135+i,185,105+i,185);
     line(105+i,185,75+i,220);

     line(145+i,220,210+i,220);    //window 2
     line(210+i,220,185+i,185);
     line(185+i,185,145+i,185);
     line(145+i,185,145+i,220);
     delay(5);
     cleardevice();
   }
   closegraph();
   return 0;
}

int weltxt()
{
   clrscr();
   int gdriver = DETECT, gmode, errorcode;
   initgraph(&gdriver, &gmode, "C:/TURBOC3/BGI");

   setbkcolor(randcolor());
   int y=getmaxy()/2,x=getmaxx();

   for(int i=0,j=x;i<=x,j>=0;i++,j--)
   {
     line(0,25,i,25);
     delay(2);
     line(639,453,j,453);
     delay(2);
   }

   settextstyle(3,HORIZ_DIR,8);
   outtextxy(150,y-220,"WELCOME");
   delay(500);
   outtextxy(270,y-120,"TO");
   delay(500);
   outtextxy(180,y-20,"TOURIST");
   delay(500);
   outtextxy(195,y+80,"PORTAL");
   getch();
   closegraph();
   return 0;
}

//main menu for tourists
int tourp()
{
   int gd=EGA,gm=EGAHI,choice;
   int x=getmaxx();
   initgraph(&gd,&gm,"C:/TURBOC3/BGI");
   cleardevice();
   setbkcolor(randcolor());
   setlinestyle(DASHED_LINE,1, 1);
   line(0,20,x,20);
   line(0,120,x,120);

   settextstyle(7,HORIZ_DIR,8);
   outtextxy(40,15,"T");
   delay(100);
   outtextxy(85,15,"O");
   delay(100);
   outtextxy(130,15,"U");
   delay(100);
   outtextxy(165,15,"R");
   delay(100);
   outtextxy(215,15,"I");
   delay(100);
   outtextxy(240,15,"S");
   delay(100);
   outtextxy(290,15,"T");
   delay(100);
   outtextxy(350,15,"P");
   delay(100);
   outtextxy(405,15,"O");
   delay(100);
   outtextxy(435,15,"R");
   delay(100);
   outtextxy(500,15,"T");
   delay(100);
   outtextxy(525,15,"A");
   delay(100);
   outtextxy(565,15,"L");

   settextstyle(2,HORIZ_DIR,6);
   outtextxy(270,150,"1.Admin");
   outtextxy(240,190,"2.Existing User");
   outtextxy(260,230,"3.New User");
   outtextxy(270,270,"4.Exit");
   settextstyle(2,HORIZ_DIR,4);
   int flag=0;
   while(flag==0)
   {
      outtextxy(250,308,"Enter your choice:");
      gotoxy(46,23);
      cin>>choice;
      switch(choice)
      {
	 case 1:Adm();
		flag=1;
		break;
	 case 2:openusr();
		flag=1;
		break;
	 case 3:Nwusr();
		flag=1;
		break;
	 case 4:exit(0);
		flag=1;
		break;
	 default:flag=0;
      }
   }
   closegraph();
   return 0;
}

//for admin
void Adm()
{
    entry=1;
    char apwd[10],pass[10]="admin",ch;
    int i=0,cnt;

    int gd=EGA,gm=EGAHI,choice;
    initgraph(&gd,&gm,"C:/TURBOC3/BGI");
    setbkcolor(randcolor());
    settextstyle(2,HORIZ_DIR,4);
    do
    {
       cleardevice();
       outtextxy((getmaxx()/2)-100,168,"Enter your password:");
       for(int j=0;j<10;j++)
       {
	  if(j<0)
	  {
	    j=0;
	    gotoxy(44,13);
	  }
	  ch=getch();
	  if(ch=='\r')
	  {
	     apwd[j]='\0';
	     break;
	  }
	  else if(ch=='\b')
	  {
	      cout<<"\b \b";
	      j-=2;
	  }
	  else
	  {
	     apwd[j]=ch;
	     gotoxy(44+j,13);
	     cout<<"*";
	  }
       }
       if(!strcmp(apwd,pass))
       {
	  admrgt();
       }
       else
       {
	 i++;
	 outtextxy(200,200,"INVALID...Press any key to continue!");
	 getch();
	 clrscr();
       }
    }while(i<3);
    if(i==3)
    {
	cleardevice();
	outtextxy(220,120,"Too Many Incorrect attempts!");
	delay(650);
	outtextxy(220,150,"Sorry Try Again Later!");
	getch();
	exit(0);
    }
    getch();
    closegraph();
}

//for admin rights
void admrgt()
{
    int gd=EGA,gm=EGAHI,choice,flag=0,count=0;
    initgraph(&gd,&gm,"C:/TURBOC3/BGI");
    setbkcolor(randcolor());
    settextstyle(2,HORIZ_DIR,5);
    cleardevice();
      outtextxy(225,100,"What do you want to do?");
      delay(20);
      outtextxy(150,170,"1.See Customers");
      delay(20);
      outtextxy(150,190,"2.Edit Customer");
      delay(20);
      outtextxy(150,210,"3.Remove Customer");
      delay(20);
      outtextxy(150,230,"4.Back");
      do
      {
	count++;
	outtextxy(220,277,"Please enter your choice:");
	gotoxy(53,21);
	cin>>choice;
	switch(choice)
	{
	 case 1:obj.showdata();
		break;
	 case 2:Edit();
		break;
	 case 3:Delete();
		break;
	 case 4:tourp();
		break;
	 default:flag=0;
	}
      }while(flag==0 && count<3);
}

//for newuser
void Nwusr()
{
   ofstream fout;
   fout.open("userdata.dat",ios::binary|ios::app);
   obj.getdata();
   fout.write((char*)&obj,sizeof(obj));
   fout.close();
   countusr++;

   int gd=EGA,gm=EGAHI,x,y,i,choice,n=0,flag=1;
   char code[size],ch,otp[size];
   initgraph(&gd,&gm,"C:/TURBOC3/BGI");
   //setbkcolor();
   x=getmaxx()/2;
   y=getmaxy()/2;

   cleardevice();
   settextstyle(3,HORIZ_DIR,1);
   setcolor(4);
   int c=150;
   for(int e=0;e<10;e++)
   {
      for(int i=50;i<90;i++)
      {
	 setcolor(3);
	 settextstyle(3,HORIZ_DIR,1);
	 outtextxy(x-50,y,"Getting you a captcha...");
	 circle(x,y,i);
	 circle(x,y,c);
	 c--;
	 cleardevice();
      }
   }
   setcolor(6);
   while(flag==1)
   {
	 randomize();
	 cleardevice();
	 while(n<size)
	 {
	     ch=(char)random(127);
	     if(toupper(ch)>='A' && toupper(ch)<='Z' || ch<='9'&&ch>='0')
	     {
		code[n++]=ch;
	     }
	 }
	 code[n]='\0';
	 settextstyle(2,HORIZ_DIR,5);
	 outtextxy(200,152,"CAPTCHA:");
	 gotoxy(34,12);
	 cout<<code<<endl;
	 outtextxy(200,180,"ENTER THE CAPTCHA:");
	 gotoxy(44,14);
	 cin>>otp;
	 if(strcmp(code,otp)==0)
	 {
	    cleardevice();
	    outtextxy(x-25,y-4,"VERFIED...");
	    sound(550);
	    delay(100);
	    sound(500);
	    delay(100);
	    sound(950);
	    delay(200);
	    nosound();
	    outtextxy(x-80,y+16,"Press any key to continue...");
	    flag=0;
	    getch();
	    openusr();
	 }
	 else
	 {
	   outtextxy(x-10,y-4,"Wrong OTP");
	   sound(100);
	   delay(1000);
	   nosound();
	   flag=1;
	 }
   }
   getch();
   closegraph();
}

//for opening user
void openusr()
{
   entry=2;
   int gd=EGA,gm=EGAHI,choice;
   initgraph(&gd,&gm,"C:/TURBOC3/BGI");
   int cid,flag=0,count=0;
   setbkcolor(randcolor());
   settextstyle(2,HORIZ_DIR,5);
   while(flag==0 && count<3)
   {
      count++;
      cleardevice();
      outtextxy(150,152,"Please enter your customer ID:");
      gotoxy(49,12);
      cin>>cid;
      ifstream fin;
      fin.open("userdata.dat",ios::binary);
      while(fin.read((char*)&obj,sizeof(obj)))
      {
	 if(obj.retcid()==cid)
	 {
	    flag=1;
	    break;
	 }
	 else
	 {
	    flag=0;
	    outtextxy(getmaxx()/2,getmaxy()/2,"Inability Quitting!!");
	 }
      }
      fin.close();
   }
   if(flag==1)
   {
      cleardevice();
      outtextxy(250,100,"What do you want to do?");
      delay(5);
      outtextxy(150,170,"1. Edit Account details");
      delay(5);
      outtextxy(150,190,"2.Delete Account");
      delay(5);
      outtextxy(150,210,"3.Back");

      do
      {
	 outtextxy(220,263,"Please enter your choice:");
	 gotoxy(53,20);
	 cin>>choice;
	 switch(choice)
	 {
	     case 1:Edit();
		    flag=1;
		    break;
	     case 2:Delete();
		    flag=1;
		    break;
	     case 3:tourp();
		    flag=1;
		    break;
	     default:flag=0;
	 }
      }while(flag==0);
   }
}

//for editing users
void Edit()
{
   sten=100;
   int gd=EGA,gm=EGAHI,choice,cid,flag=0;
   initgraph(&gd,&gm,"C:/TURBOC3/BGI");
   setbkcolor(randcolor());
   outtextxy(149,158,"Please enter your customer ID:");
   gotoxy(50,12);
   cin>>cid;
   fstream fio("userdata.dat",ios::binary|ios::in|ios::out);
   while(fio.read((char*)&obj,sizeof(obj)))
   {
	 if(obj.retcid()==cid)
	 {
	      obj.getdata();
	      int pos=-1*sizeof(obj);
	      fio.seekp(pos,ios::cur);
	      fio.write((char*)&obj,sizeof(obj));
	      flag=1;
	      break;
	 }
   }
   fio.close();
   if(flag==1)
   {
	cleardevice();
	outtextxy(200,150,"DETAILS EDITED SUCCESSFULLY");
	delay(1000);
	switch(entry)
	{
	   case 1:admrgt();
		  break;
	   case 2:tourp();
		  break;
	}
   }
   else
   {
	cleardevice();
	gotoxy(28,12);
	cout<<"Enter Valid Employee ID!";
	delay(1500);
	switch(entry)
	{
	   case 1:admrgt();
		  break;
	   case 2:tourp();
		  break;
	}
   }
}

//for deleting users
void Delete()
{
   int gd=EGA,gm=EGAHI,choice,count=0;
   initgraph(&gd,&gm,"C:/TURBOC3/BGI");
   setbkcolor(randcolor());
   int cid,flag=0;
   char name[50];
   settextstyle(2,HORIZ_DIR,5);
   while(flag==0 && count<3)
   {
     count++;
     cleardevice();
     outtextxy(150,152,"Please enter your customer ID:");
     gotoxy(49,12);
     cin>>cid;
     ifstream fin;
     fin.open("userdata.dat",ios::binary);
     while(fin.read((char*)&obj,sizeof(obj)))
     {
	if(obj.retcid()==cid)
	{
	   flag=1;
	   break;
	}
     }
     fin.close();
     if(flag==1)
     {
	cleardevice();
	ifstream fp1;
	fp1.open("userdata.dat",ios::binary);
	ofstream fp2;
	fp2.open("Temp.dat",ios::out|ios::binary);
	while(fp1.read((char*)&obj,sizeof(obj)))
	{
	    if(obj.retcid()!=cid)
	      fp2.write((char*)&obj,sizeof(obj));
	}
	fp1.close();
	fp2.close();
	remove("userdata.dat");
	rename("Temp.dat","userdata.dat");
	cleardevice();
	outtextxy(250,155,"Delete Successful!!!");
	delay(1000);
	countusr--;
     }
   }
   switch(entry)
   {
       case 1:admrgt();
	      break;
       case 2:tourp();
	      break;
   }
}

//main program execution
void main()
{
  clrscr();
  ifstream fin;
  fin.open("userdata.dat",ios::binary);
  while(fin.read((char*)&obj,sizeof(obj))) //to count user
     countusr++;
  car();       //for car
  weltxt();    //for welcome text
  tourp();     //for main menu
  getch();
}

/* THANK YOU */
