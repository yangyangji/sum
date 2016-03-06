prog1源程序：

#include <iostream>
#include <fstream>
using namespace std;

void main()
{
	int a[100],sum=0;
	ifstream fin("D:/数据.txt");
	for(int i=0;i<100;i++)
		fin>>a[i];
	for(i=0;i<100;i++)
		cout<<a[i]<<endl;
	ofstream fout("D:/数据.txt");
    for(i=0;i<100;i++)
		sum+=a[i];
	    cout<<"100个实数的和为："<<sum;
	fin.close();
	fout.close();
	cin.get();
}

prog2源程序：

#include <iostream>
#include <fstream>
using namespace std;

void ArraySum(int n)
{ int *a,sum=0,i;
  a=new int[n];
  ifstream fin("D:/数据.txt");
	for(i=0;i<n;i++)
		fin>>a[i];
	for(i=0;i<n;i++)
		cout<<a[i]<<endl;
  for(i=0;i<n;i++)
	  sum+=a[i];
      cout<<n<<"个数据的和为："<<sum;
  fin.close();
  cin.get();
}

void main()
{ int n;
  cout<<"请输入实数的个数：";
  cin>>n;
  ArraySum(n);
}


prog3源程序：
#include <iostream>
#include <fstream>
using namespace std;

void ArraySum(int n,int min,int max)
{ int *a,sum=0,i;
  a=new int[n];
  ifstream fin("D:/数据.txt");
	for(i=0;i<n;i++)
		fin>>a[i];
	for(i=0;i<n;i++)
		cout<<a[i]<<endl;
  for(i=0;i<n;i++)
	  if(a[i]>=min&&a[i]<=max)
	     sum+=a[i];
         cout<<n<<"个实数的和为："<<sum;
  fin.close();
  cin.get();
}

void main()
{ int n;
  cout<<"请输入实数的个数：";
  cin>>n;
  double min,max;
  cout<<"输入指定范围的最小值：";
  cin>>min;
  cout<<"输入指定范围的最大值：";
  cin>>max;
  ArraySum(n,min,max);
}


