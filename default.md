prog1Դ����

#include <iostream>
#include <fstream>
using namespace std;

void main()
{
	int a[100],sum=0;
	ifstream fin("D:/����.txt");
	for(int i=0;i<100;i++)
		fin>>a[i];
	for(i=0;i<100;i++)
		cout<<a[i]<<endl;
	ofstream fout("D:/����.txt");
    for(i=0;i<100;i++)
		sum+=a[i];
	    cout<<"100��ʵ���ĺ�Ϊ��"<<sum;
	fin.close();
	fout.close();
	cin.get();
}

prog2Դ����

#include <iostream>
#include <fstream>
using namespace std;

void ArraySum(int n)
{ int *a,sum=0,i;
  a=new int[n];
  ifstream fin("D:/����.txt");
	for(i=0;i<n;i++)
		fin>>a[i];
	for(i=0;i<n;i++)
		cout<<a[i]<<endl;
  for(i=0;i<n;i++)
	  sum+=a[i];
      cout<<n<<"�����ݵĺ�Ϊ��"<<sum;
  fin.close();
  cin.get();
}

void main()
{ int n;
  cout<<"������ʵ���ĸ�����";
  cin>>n;
  ArraySum(n);
}


prog3Դ����
#include <iostream>
#include <fstream>
using namespace std;

void ArraySum(int n,int min,int max)
{ int *a,sum=0,i;
  a=new int[n];
  ifstream fin("D:/����.txt");
	for(i=0;i<n;i++)
		fin>>a[i];
	for(i=0;i<n;i++)
		cout<<a[i]<<endl;
  for(i=0;i<n;i++)
	  if(a[i]>=min&&a[i]<=max)
	     sum+=a[i];
         cout<<n<<"��ʵ���ĺ�Ϊ��"<<sum;
  fin.close();
  cin.get();
}

void main()
{ int n;
  cout<<"������ʵ���ĸ�����";
  cin>>n;
  double min,max;
  cout<<"����ָ����Χ����Сֵ��";
  cin>>min;
  cout<<"����ָ����Χ�����ֵ��";
  cin>>max;
  ArraySum(n,min,max);
}


