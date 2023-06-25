# Decimal-to-Hexadecimal-Conversion-in-C-

Decimal to Hexadecimal Conversion in C++
What we will learn in this article is how Decimal to Hexadecimal Conversion in C++ works

The following is the number system scheme of hexadecimal number format

Numbers between (0 - 9) are represented as is. 
There is special system for (10 - 15): 
A - 10
B - 11
C - 12
D - 13
E - 14
F - 16
Decimal to Hexadecimal Conversion in C++
ASCII Table
Please make sure that you check the ASCII Table here
Decimal to HexaDecimal in C++ Program
Related Pages
Decimal to Binary conversion

Decimal to Octal Conversion

Decimal to Hexadecimal Conversion

Binary to Octal conversion

Octal to Binary conversion

Quadrants in which a given coordinate lies

C++ Program
Run
#include<iostream>

using namespace std;

 
void
getHexadecimal (int decimal) 
{
  
    // creating a char array to store hexadecimal equivalent
  char result[100];
  
 
    // pos keep index track & is used to place value in result[] array
  int pos = 0;
  
while (decimal != 0)
    {
      
int rem = 0;
      
 
 
rem = decimal % 16;
      
 
	// Whenever rem < 10 : we will have [0 - 9] as values in place
	// Note ASCII of 0 is 48
	if (rem < 10)
	
	{
	  
result[pos] = rem + 48;
	  
pos++;
	
}			// else whenever remainder >= 10 we will have [A - F] 
// rem value will be > 10, adding 55 will result : A - F 
// Note: ASCII A -> 65, B -> 66 ........ F -> 70 
else {
    result[pos] = rem + 55; 
    pos++; 
    
} 
decimal = decimal / 16; 
        
    } // to get result we need to read the array in opposite fashion 
    cout << "Hexadecimal Value: "; 
    for (int j = pos -1; j >= 0; j--)
    cout << result[j]; 
    
} 
int main() 
{ 
    int decimal; 
    cout << "Decimal Value:" ;
    cin >> decimal; 
    getHexadecimal(decimal); 
    return 0; 
    
}
Output
Decimal Value: 1254
Hexadecimal Value: 4E6

