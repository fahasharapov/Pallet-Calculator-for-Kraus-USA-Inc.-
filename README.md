# Pallet-Calculator-for-Kraus-USA-Inc.-
Automation of a process of calculating the pallets dimensions (volume, class, weight, etc…) using C++.

#include <iostream>
#include <string>
using namespace std;
int main ()
{
	//DECLARING VARIABLES
	float palletWidth, palletHeight, palletLenght;
    float palletClass;
    int palletQty;

    //RUNNING THE CALCULATOR UNTIL THE PALLET QTY = 0
    while (palletQty != 0)

{
    float totalVolume = 0;
	float totalWeight = 0;

    //PALLET QUANTITY PROMPT
    //cout << "______________________________" << endl;
	cout << "Pallet Qty: ";
	cin >> palletQty;

	for (int count = 1; count <= palletQty; count ++)

{
	//PALLET COUNTER
	cout << "\nPALLET " << count << endl;

	//WEIGHT AMOUNT PROMPT
	float palletWeight[50];
	cout << "Weight (lbs): ";
	cin >> palletWeight[count];

	//WIDTH SIZE PROMPT
	cout << "Width: ";
	cin >> palletWidth;

//HEIGHT SIZE PROMPT
	cout << "Height: ";
	cin >> palletHeight;

	//LENGHT SIZE PROMPT
	cout << "Length: ";
	cin >> palletLenght;

	//PALLET VOLUME CALCULATION
	float palletVolume[50];
	palletVolume[count] = (palletWidth * palletHeight * palletLenght) / 1728;

	//PALLET CLASS CALCULATION
	palletClass = palletWeight[count] / palletVolume[count];

	//ASSIGNING THE TOTAL OF "PALLETVOLUME" AND "PALLETWEIGHT" TO NEW VARIABLES
	totalVolume = totalVolume + palletVolume[count];
	totalWeight = totalWeight + palletWeight [count];
}
	//PALLET TOTAL WEIGHT & VOLUME OUTPUT

	cout << "\nTOTAL WEIGHT: " << totalWeight << " lbs.";
	cout << "\nVOLUME: " << totalVolume << " c/f." << endl;

	//OUTPUTING THE RESULT OF THE PALLET CLASS
	if (palletClass < 2 && palletClass > 1)
	{
		cout << "CLASS: 400" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 3)
	{
		cout << "CLASS: 300" << "\n" << endl;
		cout << "______________________________" << endl;
	}
	else if (palletClass < 4)
	{
		cout << "CLASS: 250" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 5)
	{
		cout << "CLASS: 200" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 6)
	{
		cout << "CLASS: 175" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 7)
	{
		cout << "CLASS: 150" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 8)
	{
		cout << "CLASS: 125" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 9)
	{
		cout << "CLASS: 110" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 10.5)
	{
		cout << "CLASS: 100" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 12)
	{
		cout << "CLASS: 92.5" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 13.5)
	{
		cout << "CLASS: 85" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 15)
	{
		cout << "CLASS: 77.5" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 22.5)
	{
		cout << "CLASS: 70" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 30)
	{
		cout << "CLASS: 65" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 35)
	{
		cout << "CLASS: 60" << "\n" << endl;
		cout << "______________________________" << endl;
	}

	else if (palletClass < 50)
	{
		cout << "CLASS: 55" << "\n" << endl;
		cout << "______________________________" << endl;
	}

}

	  /*

Class 55	35-50 pounds
Class 60	30-35 pounds
Class 65	22.5-30 pounds
Class 70	15 to 22.5 pounds
Class 77.5	13.5 to 15 pounds
Class 85	12-13.5 pounds
Class 92.5	10.5-12 pounds
Class 100	9-10.5 pounds
Class 110	8-9 pounds
Class 125	7-8 pounds
Class 150	6-7 pounds
Class 175	5-6 pounds
Class 200	4-5 pounds
Class 250	3-4 pounds
Class 300	2-3 pounds
Class 400	1-2 pounds

    */

}
