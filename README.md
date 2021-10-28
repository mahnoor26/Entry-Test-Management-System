# Entry-Test-Management-System
Its my first semester project
# include<iostream>
# include<cctype>
# include<iomanip>
# include<string>
# include<conio.h>
# include<fstream>
# include<windows.h>
using namespace std;
int counter=0;


//:::::::::::::::::::::::::::::::::::::::FUNCTIONS:::::::::::::::::::::::::::::::::::::::::::::::

//+++++++++++++++++++++++++++++++++++++++++Structure++++++++++++++++++++++++++++++++++++++++++++++

struct student1
{

string name;
string cnic;
string E_mail;
string mobile;
string address;
float Obt_marks; 
};
struct student2
{

string name;
string cnic;
string E_mail;
string mobile;
string address;
float Obt_marks; 
};
struct student3
{

string name;
string cnic;
string E_mail;
string mobile;
string address;
float Obt_marks; 
};

void admin_module(); //function declaration
void user_module();
void main_menu();
void MBBSstudents();
void FCstudents();
void EEstudents();

//...............................................File..............................................
 ofstream outfile;

 //------------------------------------------------Data Type-----------------------------------------
 float petrcentage;
 void main()
{
	
	main_menu();

system("pause");
}

void main_menu()
{

    system("color 9E");

		cout<<"\n\n\n\n\n\n\n";
        cout<<"\n\n\t\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB";
        cout<<"\n\t\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB";
		cout<<"\n\t\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xB2\xB2\xB2\xB2\xB2"; Sleep(10); cout<<" "; cout<<"W";Sleep(80);cout<<"E";Sleep(80);cout<<"L";Sleep(80);cout<<"C";Sleep(80);cout<<"O";
		Sleep(80);cout<<"M";Sleep(80);cout<<"E"<<" "<<" ";Sleep(50);cout<<" ";Sleep(80);cout<<"T";Sleep(80);cout<<"O";Sleep(80);cout<<" ";Sleep(80);cout<<"O";Sleep(80);cout<<"N";Sleep(80);cout<<"L";Sleep(80);cout<<"I";Sleep(80);cout<<"N";Sleep(80);cout<<"E";Sleep(80);
		cout<<" ";Sleep(80);cout<<"E";Sleep(80);cout<<"N";Sleep(80);cout<<"T";Sleep(80);cout<<"R";Sleep(80);cout<<"Y";Sleep(80);cout<<" ";Sleep(80);cout<<"T";Sleep(80);cout<<"E";Sleep(80);cout<<"S";Sleep(80);cout<<"T";Sleep(80);cout<<"";Sleep(80);
		cout<<" ";Sleep(80);cout<<"S";Sleep(80);cout<<"Y";Sleep(80);cout<<"S";Sleep(80);cout<<"T";Sleep(80);cout<<"E";Sleep(80);cout<<"M";Sleep(80);cout<<" ";Sleep(80);; cout<<"\xB2\xB2\xB2\xB2\xB2\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB"; Sleep(0);
	    cout<<"\n\t\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xB2\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB";
	    cout<<"\n\t\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB";
		Sleep(4000);
		cout<<endl;

		system("cls");
		system("color 9E");




     
		
 system("color 1E");
	system("cls");
	
	int choice;
	cout<<"\n\t*************************\n";
	cout<<"\t|\t 1 : Admin      |\n";
	cout<<"\t*************************\n";
	cout<<"\n\t*************************\n";
	cout<<"\t|\t 2: User        |\n";
	cout<<"\t*************************\n";

	cin>>choice;

	switch(choice)
	{
	case 1:
		{
			system("cls");
			admin_module();
			break;

		}

	case 2:
		{
			system("cls");
			user_module();
			break;

		}
	default:
		{
			cout<<"\n\t you entered wrong option"<<endl;

			cout<<"\n\n\n\n\t*********************************\n";
            cout<<"\t|\t PRESS ENTER TO GO BACK    |\n";
            cout<<"\t*********************************\n";
			getche();
			main_menu();
			break;
		}
	}
	}
void admin_module()
{
  cout<<"\nPlease enter your four didgit pin code to log in"<<endl;
  string pass ="";
  cout << "Enter pass\n";
 cin>>pass;
   cout<<pass<<endl;

   if(pass == "zara123"){
  
  cout<<"\nWelcome Admin"<<endl;

  cout<<"Question Papers"<<endl;
  cout<<"1)Result Record"<<endl;
  cout<<"WHICH FACULTY YOU WANT TO SEE 1)FC 2)EE 3)MBBS"<<endl;
  int zoo;
  cin>>zoo;
  if(zoo==1){
 ifstream fin; //read
 fin.open("FCdata.txt");
 if(!fin.eof())
 {
 char line[100];
 while(!fin.eof())
 {
 fin.getline(line,100);
 cout<<line<<endl;
 }
 
 }
  }

  if(zoo==2){
 ifstream fin;
 fin.open("EEdata.txt");
 if(!fin.eof())
 { g
 char line[100];
 while(!fin.eof())
 {
 fin.getline(line,100);
 cout<<line<<endl;
 }
 
 }
  }
  if(zoo==3){
 ifstream fin;
 fin.open("MBBSdata.txt");
 if(!fin.eof())
 {
 char line[100];
 while(!fin.eof())
 {
 fin.getline(line,100);
 cout<<line<<endl;
 }
 }
 
  }
  
   }
  else {cout<<"You Enter Wrong Passward....Sorry"<<endl;
  main();
  }   
 }

void user_module()
{int choice;
char ch;
	 cout<<"PLease select your type of fsc program !"<<endl;
  cout<<"1) FSC PRE-ENGINNERING 2)FSC PRE-MEDICAL"<<endl;
  cin>>choice;
  if(choice==1)
  {
  cout<<"you have two choices , select any of them "<<endl;
   cout<<" a)FC b)EE "<<endl;
   cin>>ch;
   if(ch=='A' || ch=='a'){
	   FCstudents();
  }
   else 
	   if(ch=='B' || ch=='b'){
	   EEstudents();
	   }
	   else
	   {cout<<"Invalid"<<endl;}



  }
  if(choice==2)
  {
  cout<<"you have three choices , select any of them "<<endl;
   cout<<" a)FC b)EE c)MBBS "<<endl;
   cin>>ch;
   if(ch=='A' || ch=='a'){
	   FCstudents();
  }
   else 
	   if(ch=='B' || ch=='b'){
	   EEstudents();
	   }
	   else
	   if(ch=='C'||ch=='c')
	   {
		   MBBSstudents();
	   }else{cout<<"Default"<<endl;}

  
  }
  
}

  void EEstudents()
{ 
	student1 s;

	float percentage;
	cin.ignore(100,'\n'); 
	cout<<"PLEACE ENTER YOUR NAME:"<<endl;	
getline(cin,s.name,'\n');
cin.ignore(100,'\n');
cout<<"\n\nPLEACE ENTER YOUR CNIC NUMBER:"<<endl;	
getline(cin,s.cnic,'\n');
cout<<"\n\nPLEACE ENTER YOUR E-MAIL :"<<endl;	
getline(cin,s.E_mail,'\n');
cout<<"\n\nPLEACE ENETR YOUR MOBILE NUMBER"<<endl;	
getline(cin,s.mobile,'\n');
cout<<"\n\nPLEACE ENTER YOUR ADRESS"<<endl;	
getline(cin,s.address,'\n');
cout<<"\n\nPLEACE ENTER YOUR FSC MARKS "<<endl;
	cin>>s.Obt_marks;
	cin.ignore(100,'\n');
	if(s.Obt_marks>=0&&s.Obt_marks<1100){
	percentage=(s.Obt_marks/1100) * 100;
	if(percentage>60)
	{
	string choice;
	string line;
	ifstream myfile;  //read 
	myfile.open ("electrical & software engineering.txt");
	for(int i=0;i<5;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==4)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
	cout<<"correct answer !"<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
	for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
			
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
		cout<<"Your score is :\t"<<counter<<endl;
	}
	else
	{
		cout<<"wrong answer"<<endl;
		cout<<"Your score is :\t"<<counter<<endl;
	}
	}
	else
	{
	cout<<"You are not eligible for this program!Sorry "<<endl;
	main_menu();

	}
	}
	else {cout<<"You Enter A wrong Marks"<<endl;
	main_menu();
	}
	
	outfile.open ("EEdata.txt",ios::in | ios::app);
    if(outfile.is_open())
	{	
		
		outfile<<"*="<<"Name:"<<s.name<<endl;
		outfile<<"*="<<"CNIC NUMBER:"<<s.cnic<<endl;
		outfile<<"*="<<"E-MAIL:"<<s.E_mail<<endl;
		outfile<<"*="<<"MOBILE NO:"<<s.mobile<<endl;
		outfile<<"*="<<"ADRESS:"<<s.address<<endl;
		outfile<<"*="<<"FSC MARKS:"<<s.Obt_marks<<endl;
		outfile<<"*="<<"PERCENTAGE OF MARKS:"<<percentage<<endl;
		outfile<<"*="<<"RESULT TEST="<<counter<<endl;
	    outfile<<"*="<<"@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@"<<endl;	
	}
	
outfile.close();

}
  void FCstudents()
{ 
	student2 s;

	float percentage;
	cin.ignore(100,'\n');
	cout<<"PLEACE ENTER YOUR NAME:"<<endl;	
getline(cin,s.name,'\n');
cin.ignore(100,'\n');
cout<<"\n\nPLEACE ENTER YOUR CNIC NUMBER:"<<endl;	
getline(cin,s.cnic,'\n');
cout<<"\n\nPLEACE ENTER YOUR E-MAIL :"<<endl;	
getline(cin,s.E_mail,'\n');
cout<<"\n\nPLEACE ENETR YOUR MOBILE NUMBER"<<endl;	
getline(cin,s.mobile,'\n');
cout<<"\n\nPLEACE ENTER YOUR ADRESS"<<endl;	
getline(cin,s.address,'\n');
cout<<"\n\nPLEACE ENTER YOUR FSC MARKS "<<endl;
	cin>>s.Obt_marks;
	cin.ignore(100,'\n');
	if(s.Obt_marks>=0&&s.Obt_marks<1100){
	percentage=(s.Obt_marks/1100) * 100;
	if(percentage>60)
	{
	string choice;
	string line;
	ifstream myfile;
	myfile.open ("electrical & software engineering.txt");
	for(int i=0;i<5;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==4)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
	cout<<"correct answer !"<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
	for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
			
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
		cout<<"Your score is :\t"<<counter<<endl;
	}
	else
	{
		cout<<"wrong answer"<<endl;
		cout<<"Your score is :\t"<<counter<<endl;
	}
	}
	else
	{
	cout<<"You are not eligible for this program!Sorry "<<endl;
	main_menu();

	}
	}
	else {cout<<"You Enter A wrong Marks"<<endl;
	main_menu();
	}
	
	outfile.open ("FCdata.txt",ios::in | ios::app);
    if(outfile.is_open())
	{	
		
		outfile<<"*="<<"Name:"<<s.name<<endl;
		outfile<<"*="<<"CNIC NUMBER:"<<s.cnic<<endl;
		outfile<<"*="<<"E-MAIL:"<<s.E_mail<<endl;
		outfile<<"*="<<"MOBILE NO:"<<s.mobile<<endl;
		outfile<<"*="<<"ADRESS:"<<s.address<<endl;
		outfile<<"*="<<"FSC MARKS:"<<s.Obt_marks<<endl;
		outfile<<"*="<<"PERCENTAGE OF MARKS:"<<percentage<<endl;
		outfile<<"*="<<"RESULT TEST="<<counter<<endl;
	    outfile<<"*="<<"@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@"<<endl;	
	}
	
outfile.close();


}
  void MBBSstudents()
{ 
student3 s;

	float percentage;
	cin.ignore(100,'\n');
	cout<<"PLEACE ENTER YOUR NAME:"<<endl;	
getline(cin,s.name,'\n');
cin.ignore(100,'\n');
cout<<"\n\nPLEACE ENTER YOUR CNIC NUMBER:"<<endl;	
getline(cin,s.cnic,'\n');
cout<<"\n\nPLEACE ENTER YOUR E-MAIL :"<<endl;	
getline(cin,s.E_mail,'\n');
cout<<"\n\nPLEACE ENETR YOUR MOBILE NUMBER"<<endl;	
getline(cin,s.mobile,'\n');
cout<<"\n\nPLEACE ENTER YOUR ADRESS"<<endl;	
getline(cin,s.address,'\n');
cout<<"\n\nPLEACE ENTER YOUR FSC MARKS "<<endl;
	cin>>s.Obt_marks;
	cin.ignore(100,'\n');
	if(s.Obt_marks>=0&&s.Obt_marks<1100){
	percentage=(s.Obt_marks/1100) * 100;
	if(percentage>60)
	{
	string choice;
	string line;
	ifstream myfile;
	myfile.open ("electrical & software engineering.txt");
	for(int i=0;i<5;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==4)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
	cout<<"correct answer !"<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
	for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
			
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}


	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}



	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
	}
	else{
		cout<<"wrong answer"<<endl;
	}
		for(int i=0;i<4;i++)
	{
		getline(myfile,line);
		cout<<line<<endl;
		if(i==3)
		{
			getline(myfile,line);
		}
	}
	getline(cin,choice);
	if(line==choice){
		counter=counter+10;
		cout<<"correct answer ! "<<endl;
		cout<<"Your score is :\t"<<counter<<endl;
	}
	else
	{
		cout<<"wrong answer"<<endl;
		cout<<"Your score is :\t"<<counter<<endl;
	}
	}
	else
	{
	cout<<"You are not eligible for this program!Sorry "<<endl;
	main_menu();

	}
	}
	else {cout<<"You Enter A wrong Marks"<<endl;
	main_menu();
	}
	
	outfile.open ("MBBSdata.txt",ios::in | ios::app);
    if(outfile.is_open())
	{	
		
		outfile<<"*="<<"Name:"<<s.name<<endl;
		outfile<<"*="<<"CNIC NUMBER:"<<s.cnic<<endl;
		outfile<<"*="<<"E-MAIL:"<<s.E_mail<<endl;
		outfile<<"*="<<"MOBILE NO:"<<s.mobile<<endl;
		outfile<<"*="<<"ADRESS:"<<s.address<<endl;
		outfile<<"*="<<"FSC MARKS:"<<s.Obt_marks<<endl;
		outfile<<"*="<<"PERCENTAGE OF MARKS:"<<percentage<<endl;
		outfile<<"*="<<"RESULT TEST="<<counter<<endl;
	    outfile<<"*="<<"@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@"<<endl;	
	}
	
outfile.close();


}
