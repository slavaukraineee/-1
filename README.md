#include<iostream>
#include<string>
#include<vector>

using namespace std;

int main()
{
	int asc = 0;
	int c = 0;
	int j = 0;
	string str;
	string stro;
	cout << "enter some words"<<endl;
	getline(cin, str);
	int length;
	length = sizeof(str);
	vector <int> a;
	for (int i = 0; i = length; i++)
	{
		if (str[i] != ' ')
		{
			stro[j] = str[i];
			j++;
		}
		else
		{
			int g = j;
			j = 0;
			do
			{
				asc = asc + (int) stro[j];
				j++;
			} while (j<=g);

			for (int k = 0; k = g; k++)
			{
				stro[k] = 0;
			}
			j = 0;
			a[c] = asc;
			c++;
		}
	}
	for (int s = c; s > 0; s--)
	{
		for (int d = s-1; d > 0; d--)
		{
			if (a[s] < a[d])
			{
				int rep = a[s];
				a[s] = a[d];
				a[d] = rep;
			}
		}
	}
	for (int z = 0; z <= sizeof(a); z++)
	{
		cout << (char)a[z];
	}
}
