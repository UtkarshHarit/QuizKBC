#include<iostream>
#include<stdio.h>
#include<unistd.h>
#include<stdlib.h>
using namespace std;
int replace(int amount);
int l1=1;
int l2=1;
int main()
{
	int amount,age;
	char user_name[20],choice;
	amount=0;
	cout<<"WELCOME to KBC\n";
	cout<<"__________________\n";
	cout<<"\nEnter Your Name: ";
	cin>>user_name;
	cout<<"\nEnter Your Age (in Numbers only): ";
	cin>>age;
	cout<<"\nLoading...\n";
	usleep(1000000);
	cout<<"\nWelcome "<<user_name<<"\n";
	cout<<"\nWelcome to Level 1\n";
	cout<<"__________________\n";
	cout<<"\nLoading...\n";
	usleep(1000000);
	cout<<"\nRULE: "<<user_name<<" will earn $1000 for each correct answer and\n";
	cout<<"        $500 will be deducted for each wrong answer.\n";
	cout<<"\nLoading...\n\n";
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);
	cout<<"NOTE : User have 2 lifelines :\n"<<"\tPress '1' for 50-50\n"<<"\tPress '2' for Replace the Question\n";
	cout<<"\n"<<user_name<<" initially have $0\n";
	cout<<"\nLoading...\n";
	usleep(1000000);
	usleep(1000000);

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

 q1:cout<<"\nQues1. Which is the National Sport of India?\t(1 : 50-50 and 2 : Replace the Question)\n";
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);
	cout<<"A. Football\t\tB. Cricket\n";
	cout<<"C. Not Declared\t\tD. Volleyball\n";
	cout<<"\nEnter Your Choice: ";
	cin>>choice;
	qq:if(choice=='A'||choice=='a')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'C. Not Declared'\n";
		amount=-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='B'||choice=='b')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'C. Not Declared'\n";
		amount=-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='C'||choice=='c')
	{
		cout<<"\nCorrect Answer\n";
		amount=amount+1000;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}	
	else if(choice=='D'||choice=='d')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'C. Not Declared'\n";
		amount=-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='1'||choice=='2')
	{
		if(choice=='1')
		{
			if(l1==1)
			{
				cout<<"\nQues1. Which is the National Sport of India?\n";
				usleep(1000000);
				usleep(1000000);
				usleep(1000000);
				cout<<"A.       \t\tB. Cricket\n";
				cout<<"C. Not Declared\t\tD.           \n";
				l1=0;
				cout<<"\nEnter Your Choice: ";
				cin>>choice;
				goto qq;
			}
			else
			{
				cout<<"Lifeline has already used\n";
				goto q1;
			}
		}
		else if(choice=='2')
		{
			if(l2==1)
			{
				replace(amount);
				l2=0;
			}
			else
			{
				cout<<"Lifeline has already used\n";
				goto q1;
			}
		}
		else if(choice=='c'||choice=='C')
		{
			cout<<"\nCorrect Answer\n";
			amount=amount+1000;
			cout<<"Amount Won = $"<<amount<<"\n\n";
		}
		else
		{
			cout<<"\nWrong Answer\n";
			usleep(1000000);
			cout<<"Correct Answer is 'C. Not Declared'\n";
			amount=-500;
			cout<<"Amount Won = $"<<amount<<"\n\n";
		}
	}
	else
	{
		cout<<"\nERORR 404!!!\n";
		cout<<"Enter valid option\n";
		goto q1;	
	}
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

 q2:cout<<"\nQues2. What is the Capital of China?\t(1 : 50-50 and 2 : Replace the Question)\n";
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);
	cout<<"A. Perth\t\tB. Beijing\n";
	cout<<"C. New York\t\tD. Tokyo\n";
	cout<<"\nEnter Your Choice: ";
	cin>>choice;
	if(choice=='A'||choice=='a')
	{
		cout<<"\nWrong Answer\n";
		amount=amount-500;
		usleep(1000000);
		cout<<"Correct Answer is 'B. Beijing'\n";
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='B'||choice=='b')
	{
		cout<<"\nCorrect Answer\n";
		amount=amount+1000;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='C'||choice=='c')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'B. Beijing'\n";
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}	
	else if(choice=='D'||choice=='d')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'B. Beijing'\n";
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='1'||choice=='2')
	{
		if(choice=='1')
		{
			if(l1==1)
			{
				cout<<"\nQues2. What is the Capital of China?\n";
				usleep(1000000);
				usleep(1000000);
				usleep(1000000);
				cout<<"A.      \t\tB. Beijing\n";
				cout<<"C.         \t\tD. Tokyo\n";
				cout<<"\nEnter Your Choice: ";
				cin>>choice;
				l1=0;
			}
			else
			{
				cout<<"Lifeline has already used\n";
				goto q2;
			}
		}
		if(choice=='2')
		{
			if(l2==1)
			{
				replace(amount);
				l2=0;
			}
			else
			{
				cout<<"Lifeline has already used\n";
				goto q2;
			}
		}
		if(choice=='b'||choice=='B')
		{
			cout<<"\nCorrect Answer\n";
			amount=amount+1000;
			cout<<"Amount Won = $"<<amount<<"\n\n";
		}
		else
		{
			cout<<"\nWrong Answer\n";
			usleep(1000000);
			cout<<"Correct Answer is 'B. Tibet'\n";
			amount=amount-500;
			cout<<"Amount Won = $"<<amount<<"\n\n";
		}
	}
	else
	{
		cout<<"\nERORR 404!!!\n";
		cout<<"Enter valid option\n";
		goto q2;
	}
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

 q3:cout<<"\nQues3. What is the full form of ATM?\t(1 : 50-50 and 2 : Replace the Question)\n";
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);
	cout<<"A. Automatic Teller Machine\t\tB. Any Time Money\n";
	cout<<"C. Automatic Transfer Money\t\tD. Automatic Track Money\n";
	cout<<"\nEnter Your Choice: ";
	cin>>choice;
	if(choice=='A'||choice=='a')
	{
		cout<<"\nCorrect Answer\n";
		amount=amount+1000;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='B'||choice=='b')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'A. Automatic Teller Machine'\n";
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='C'||choice=='c')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'A. Automatic Teller Machine'\n";
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}	
	else if(choice=='D'||choice=='d')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'A. Automatic Teller Machine'\n";
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='1'||choice=='2')
	{
		if(choice=='1')
		{
			if(l1==1)
			{
				cout<<"\nQues3. What is the full form of ATM?\n";
				usleep(1000000);
				usleep(1000000);
				usleep(1000000);
				cout<<"A. Automatic Teller Machine\t\tB. Any Time Money\n";
				cout<<"C.                         \t\tD.           \n";
				cout<<"\nEnter Your Choice: ";
				cin>>choice;
				l1=0;
			}
			else
			{
				cout<<"Lifeline has already used\n";
				goto q3;
			}
		}
		if(choice=='2')
		{
			if(l2==1)
			{
				replace(amount);
				l2=0;
			}
			else
			{
				cout<<"Lifeline has already used\n";
				goto q3;
			}
		}
		if(choice=='a'||choice=='A')
		{
			cout<<"\nCorrect Answer\n";
			amount=amount+1000;
			cout<<"Amount Won = $"<<amount<<"\n\n";
		}
		else
		{
			cout<<"\nWrong Answer\n";
			usleep(1000000);
			cout<<"Correct Answer is 'A. Automatic Teller Machine'\n";
			amount=amount-500;
			cout<<"Amount Won = $"<<amount<<"\n\n";
		}
	}
	else
	{
		cout<<"\nERORR 404!!!\n";
		cout<<"Enter valid option\n";
		goto q3;
	}
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

 q4:cout<<"\nQues4. Which football team win the RIO 2016 World Cup?\t(1 : 50-50 and 2 : Replace the Question)\n";
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);
	cout<<"A. Portugal\t\tB. Brazil\n";
	cout<<"C. Argentina\t\tD. Germany\n";
	cout<<"\nEnter Your Choice: ";
	cin>>choice;
	if(choice=='A'||choice=='a')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'D. Germany\n";
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='B'||choice=='b')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'D. Germany\n";
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='C'||choice=='c')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'D. Germany\n";
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}	
	else if(choice=='D'||choice=='d')
	{
		cout<<"\nCorrect Answer\n";
		amount=amount+1000;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='1'||choice=='2')
	{
		if(choice=='1')
		{
			if(l1==1)
			{
				cout<<"\nQues4. Which football team win the RIO 2016 World Cup?\n";
				usleep(1000000);
				usleep(1000000);
				usleep(1000000);
				cout<<"A.         \t\tB.       \n";
				cout<<"C. Argentina\t\tD. Germany\n";
				cout<<"\nEnter Your Choice: ";
				cin>>choice;
				l1=0;
			}
			else
			{
				cout<<"Lifeline has already used\n";
				goto q4;
			}
		}
		if(choice=='2')
		{
			if(l2==1)
			{
				replace(amount);
				l2=0;
			}
			else
			{
				cout<<"Lifeline has already used\n";
				goto q4;
			}
		}
		if(choice=='d'||choice=='D')
		{
			cout<<"\nCorrect Answer\n";
			amount=amount+1000;
			cout<<"Amount Won = $"<<amount<<"\n\n";
		}
		else
		{
			cout<<"\nWrong Answer\n";
			usleep(1000000);
			cout<<"Correct Answer is 'D. Germany\n";
			amount=amount-500;
			cout<<"Amount Won = $"<<amount<<"\n\n";
		}
	}
	else
	{
		cout<<"\nERORR 404!!!\n";
		cout<<"Enter valid option\n";
		goto q4;
	}
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

 q5:cout<<"\nQues5. When was the Engineer's Day held?\t(1 : 50-50 and 2 : Replace the Question)\n";
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);
	cout<<"A. 19 January\t\tB. 15 September\n";
	cout<<"C. 25 November\t\tD. 13 October\n";
	cout<<"\nEnter Your Choice: ";
	cin>>choice;
	if(choice=='A'||choice=='a'||choice=='1'||choice=='2')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'B. 15 September\n";
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='B'||choice=='b'||choice=='1'||choice=='2')
	{
		cout<<"\nCorrect Answer\n";
		amount=amount+1000;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='C'||choice=='c'||choice=='1'||choice=='2')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'B. 15 September\n";
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}	
	else if(choice=='D'||choice=='d'||choice=='1'||choice=='2')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'B. 15 September\n"; 
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='1'||choice=='2')
	{
		if(choice=='1')
		{
			if(l1==1)
			{
				cout<<"\nQues5. When was the Engineer's Day held?\n";
				usleep(1000000);
				usleep(1000000);
				usleep(1000000);
				cout<<"A.           \t\tB. 15 September\n";
				cout<<"C. 25 November\t\tD.           \n";
				cout<<"\nEnter Your Choice: ";
				cin>>choice;
				l1=0;
			}
			else
			{
				cout<<"Lifeline has already used\n";
				goto q5;
			}
		}
		if(choice=='2')
		{
			if(l2==1)
			{
				replace(amount);
				l2=0;
			}
			else
			{
				cout<<"Lifeline has already used\n";
				goto q5;
			}
		}
		if(choice=='b'||choice=='B')
		{
			cout<<"\nCorrect Answer\n";
			amount=amount+1000;
			cout<<"Amount Won = $"<<amount<<"\n\n";
		}
		else
		{
			cout<<"\nWrong Answer\n";
			usleep(1000000);
			cout<<"Correct Answer is 'B. 15 September\n"; 
			amount=amount-500;
			cout<<"Amount Won = $"<<amount<<"\n\n";
		}
	}
	else
	{
		cout<<"\nERORR 404!!!\n";
		cout<<"Enter valid option\n";
		goto q5;
	}
	cout<<"\nCalculating...\n";
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);
	cout<<"Wait a sec...";
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);
	cout<<"\n";
	cout<<"You have want a amount of '$"<<amount<<"'\n\ns";
	cout<<"Congratulations!\n\n";
	return 0;
}

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

int replace(int amount)
{
	char choice;
 qr:cout<<"\nReplaced Ques. How many teams are there in DLF IPL?\t(1 : 50-50)\n";
	usleep(1000000);
	usleep(1000000);
	usleep(1000000);
	cout<<"A. 9\t\tB. 7\n";
	cout<<"C. 8\t\tD. 10\n";
	cout<<"\nEnter Your Choice: ";
	cin>>choice;
	if(choice=='1')
	{
		if(choice=='1')
		{
			if(l1==1)
			{
				cout<<"\nReplaced Ques. How many teams are there in DLF IPL?\n";
				usleep(1000000);
				usleep(1000000);
				usleep(1000000);
				cout<<"A. 9\t\tB.  \n";
				cout<<"C. 8\t\tD.  \n";
				cout<<"\nEnter Your Choice: ";
				cin>>choice;
				l1=0;
			}
			else
			{
				cout<<"Lifeline has already used\n";
				goto qr;
			}
		}
	/*	if(choice=='c'||choice=='C')
		{
			cout<<"\nCorrect Answer\n";
			amount=amount+1000;
			cout<<"Amount Won = $"<<amount<<"\n\n";
		}*/
		else
		{
			cout<<"\nWrong Answer\n";
			usleep(1000000);
			cout<<"Correct Answer is 'B. 15 September\n"; 
			amount=amount-500;
			cout<<"Amount Won = $"<<amount<<"\n\n";
		}
	}
	else if(choice=='2')
	{
		cout<<"Lifeline has already used\n";
		goto qr;
	}
	if(choice=='A'||choice=='a')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'B. 15 September\n";
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='B'||choice=='b')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'B. 15 September\n"; 
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else if(choice=='C'||choice=='c')
	{
		cout<<"\nCorrect Answer\n";
		amount=amount+1000;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}	
	else if(choice=='D'||choice=='d')
	{
		cout<<"\nWrong Answer\n";
		usleep(1000000);
		cout<<"Correct Answer is 'B. 15 September\n"; 
		amount=amount-500;
		cout<<"Amount Won = $"<<amount<<"\n\n";
	}
	else
	{
		cout<<"\nERORR 404!!!\n";
		cout<<"Enter valid option\n";
		goto qr;
	}
	return (amount);
}