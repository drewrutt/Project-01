# Project-01
/*
Drew Rutt
2016-09-10
proj01.cpp

Your Comments
*/


#include <iostream>
#include <cmath>
#include <iomanip>
#include <sstream>
#include <string>
using std::cin; using std::cout; using std::endl; using std::sqrt;
using std::string;


int main(){
	double pi = 3.141592;
	double sideA = 0.0;
	double sideB = 0.0;
	double sideC = 0.0;
	double angleA = 0.0;
	double angleB = 0.0;
	double angleC = 0.0;
	cin >> sideB >> angleA >> sideC;
	sideA = sqrt(pow(sideB, 2.0) + pow(sideC, 2.0) - (2*sideB*sideC*cos((angleA*pi)/180)));
	angleB = asin((sin((angleA*pi)/180)/sideA)*sideB);
	angleC = 180 - (angleA + (angleB*180)/pi);
	cout << std::fixed << std::setprecision(2) << sideA << endl;
	cout << std::fixed << std::setprecision(2) << (angleB*180)/pi << endl;
	cout << std::fixed << std::setprecision(2) << angleC << endl;	
	return 0;
}

