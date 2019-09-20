

#include<iostream>
#include<iomanip>

using namespace std;

void sortgrades(int num [], int a);
float averagegrades(int num1 [], int s);



int main()
{
	
	int size;
	int array[size];
	
	
	cout<<"How many Grades will you like to enter? (A max of only 30 grades please.): ";
	cin>>size;
	
	for (int i=0; i<size; i++)
	{
		cout<<"Enter the grades. (Whole numbers only.): ";
		cin>>array[i];
		
	}
	
	
	sortgrades(array, size);
	cout<<"Grades in descendent order."<<endl;
	cout<<"----------------------------"<<endl;
	for(int y=0; y<size; y++)
        cout<<array[y] << endl;
    cout<<"Average of the grades: "<<fixed<<setprecision (2)<<averagegrades(array, size);
	
	return 0;
 } 
 
 
 void sortgrades(int array[], int size)
 {
 	for(int i = 0; i<size-1; i++)
	{
        for(int a=0; a<size-i-1; a++)
		{
            if(array[a] > array[a+1])
			{
                
                int temp = array[a];
                array[a] = array[a+1];
                array[a+1] = temp;
            }
        }
    }
 }
 
 float averagegrades(int array[], int size)
 {
 	float sum=0.0;
 	float average=0.0;
 	
	 for(int k=0; k<size; k++)
 	{
 		sum+=array[k];
 		average=sum/size;
	 }
	
 	return average;
 }
