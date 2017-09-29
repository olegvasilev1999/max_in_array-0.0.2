# max_in_array-0.0.2

#include "stdafx.h"
#include "iostream"
#include "sstream"

using namespace std;


int main()
{
	int max1,max2, i, a[10], b[10];


	for (string string; getline(cin, string); ) {
		istringstream stream(string);
		bool failure = false;
		for (int i = 1; i <= 10; ++i) {
			if (!(stream >> a[i])) {
				failure = true;
				break;
			}
		}

		max1 = a[1];

		if (!failure) {
			for (int i = 1; i <= 10; ++i) {
				if (a[i] > max1) {
					max1 = a[i];
				}
			}
		
			break;
		}
		else {
			cout << "An error has occured while reading numbers from line" << endl;
		}
	}

	for (string string; getline(cin, string); ) {
		istringstream stream(string);
		bool failure = false;
		for (int i = 1; i <= 10; ++i) {
			if (!(stream >> b[i])) {
				failure = true;
				break;
			}
		}

		max2 = b[1];

		if (!failure) {
			for (int i = 1; i <= 10; ++i) {
				if (b[i] > max2) {
					max2 = b[i];
				}
			}
			
			break;
		}
		else {
			cout << "An error has occured while reading numbers from line" << endl;
		}
	}

	cout << max1 + max2 << endl;

	system("pause");
	cin.get();

	return 0;
}
