//operator-overloding-
//Operator overloding c++ Oop
#include<iostream>
#include<cstring>
using namespace std;
class Add{
	private:
		int num1,num2;
		public:
		Add(){
			num1=num2=0;
		}
        void set_Data(){
			cout<<"Enter 1st number : "<<endl;
			cin>>num1;
	        cout<<"Enter 2nd number : "<<endl;
			cin>>num2;
			}
		void get_Data(){
            cout<<" 1st number : "<<num1<<endl;
	        cout<<" 2nd number : "<<num2<<endl;			   
		}
        Add operator +(Add a){
        	Add temp;
        	temp.num1=num1+a.num1;
        	temp.num2=num2+a.num2;
        	
        	return temp;
		}
		
};

int main(){
	Add a1,a2,a3;
	cout<<"Values of object a1 : "<<endl;
	a1.set_Data();
	
	
	cout<<"Values of object a2 : "<<endl;
	a2.set_Data();
	
	
	cout<<"Values of object a3 : "<<endl;
	a3=a1+a2;
	a3.get_Data();
	
	
	
	return 0;
}
