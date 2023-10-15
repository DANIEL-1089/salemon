#include <iostream>
#include <cstdlib>
#include <ctime>
#include <wchar.h>
#include <Windows.h>
#include <algorithm>
#include <vector>
#include <string>
#include <conio.h>
#include <iomanip>



using namespace std;
const int DISTRICTS = 4;
const int MONTHS = 3;


int main()
{
    int d, m;
    double sales[DISTRICTS][MONTHS];
    cout << endl;
    for (d = 0; d < DISTRICTS; d++) {
        for (m = 0;m < MONTHS; m++) {
            cout << "\nenter the sales volume for the department " << d + 1;
            cout << ", per month " << m + 1 << ": ";
            cin >> sales[d][m];
        }
    }

    cout << "\n\n";
    cout << "Month\n";
    cout << "                1         2         3";
    for (d = 0;d < DISTRICTS; d++) {
        cout << "\ndepartment: " << d + 1;
        for (m = 0; m < MONTHS; m++) {
            cout << setiosflags(ios::fixed)
                << setiosflags(ios::showpoint)
                << setprecision(2)
                << setw(10)
                << sales[d][m];
        }
    }
    cout << endl;


    return 0;
}
