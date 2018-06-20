#include <iostream>
#include <math.h>
#include <vector>
#include <string.h>

using namespace std;

void bin(int a)
{
	int i = 0, tab[31];
	do
	{
		tab[i++] = a % 2;
		a /= 2;
	} while (a > 0);
	for (int j = i - 1; j >= 0; j--)
		cout << tab[j];
}

bool if_intercalary(int rok) {
	return (rok % 4 == 0 && rok % 100 != 0 || rok % 400 == 0);
}

void to_dec() {
	string liczba1;
	int liczba2;
	int dlugosc;
	int i;
	liczba1 = "11011"; //27
	liczba2 = 0;
	dlugosc = liczba1.length();
	i = 0;
	do
	{
		
		liczba2 += (liczba1[dlugosc - 1] - 48) * pow(2, i);
		i++;
		dlugosc--;
	} while (dlugosc > 0);

	cout << "11011 w postaci dziesietnej to: " << liczba2 << endl;
}

bool prime(int a){
	for(int i=2; i<a; i++){
		if(a%i==0){
			return false;
		}
	}
	return true;
}

long int fibo(){
	int f1 = 1;
	int f2 = 1;
	int f3;
	long int sum = 1;
	for (int i = 3; i < 1000000; i++){
		f3 = f1 + f2;
		if(i%2==0){
			sum = sum + f3;
		}
		f1 = f2;
		f2 = f3;
	}
	return sum;
}



int find_position(vector<int> tab, int S){
	int b = tab.size();
	int a = 0;
	int c = (a+b)/2;
	
	while(true){
		if(tab[c] == S){
			return c;
		} else if(tab[c] > S){
			b = c;
			c = (a+c)/2;
			
		} else {
			a = c;
			c = (b+c)/2;
		}
	}
		
	
	
}


class BinaryNumber{
	private:
		int a;
		char * tab;
	
	public:
		BinaryNumber(int a){
			this -> a = a;
			int i = 0;
			int tmp_a  = a;
			do{
				this -> tab[i++] = tmp_a % 2;
				tmp_a /= 2;
			} while (tmp_a > 0);
			
		}
		
		BinaryNumber(char * tab){
			this -> tab = tab;

			int number = 0;
			int length = strlen(tab);
			int i = 0;
			do
			{
				number += (tab[length - 1] - 48) * pow(2, i);
				i++;
				length--;
			} while (length > 0);

			this -> a = number;
		}
				
		int to_int(){
			return a;
		}
		
		char * to_bin(){
			return tab;
		}
};



int main()
{
	cout<< "podaj:";
	cout << fibo()<< endl;
	
	vector<int> tab;
	for (int i=0; i<20; i++){
		tab.push_back(2*i);
	}
	
	cout << find_position(tab, 6) << endl;

	BinaryNumber super("110100100");
	cout << super.to_int() << endl;
	cout << super.to_bin() << endl;
	

	return 0;
}
