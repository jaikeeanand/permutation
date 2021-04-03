# permutation
program to find permutation
//c++ program to print all permutation 
#include<iostream>
#include<string.h>
using namespace std;

//function to print permutaion of string
void per(string a,int start,int end)
{
	//base case
	if(start==end){
		cout<<a<<endl;
	}
	else{
		//permutaion 
		for(int i=start;i<=end;i++){
			//swapping part
			swap(a[start],a[i]);
			
			//recurssion 
			per(a, start+1,end);
			
			//backtracking
			swap(a[start],a[i]);
			
		}
	}
}

//driver code
int main(){
	string str;
	cin>>str;
	int n=str.size();
	per(str,0,n-1);
	return 0;
}

