<div align="center">

## Three by Three Matrix Utilities


</div>

### Description

Finds the determinant of 3x3 matricies and solves systems of 3 equations with 3 variables.
 
### More Info
 
Select what you want to do and enter the numbers.

You don't need to know anything to use it, but to understand the code you need to understand c++ control structures, variables, functions, math operators, and i/o streams.

The determinant or the x, y, and z valuse depending on what you want to do.

None known.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Patrick Felton](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/patrick-felton.md)
**Level**          |Intermediate
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Math](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math__3-12.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/patrick-felton-three-by-three-matrix-utilities__3-3612/archive/master.zip)

### API Declarations

```
#include <iostream.h>
#include <stdlib.h>
```


### Source Code

```
/////////////////////////////////////////////////
// Title: 3x3 Matrix Tools           //
//                       //
// File Name: 3x3.cpp             //
//                       //
// Description: Solves systems of 3 equations //
//       ans 3x3 matrices        //
//                       //
// Author: Patrick Felton           //
//                       //
// Developed: Pentium III 800mhz 384 SDRAM   //
//      Microsoft Windows XP Pro 2600  //
//      Bloodshed Dev C++ 4.0      //
//                       //
// Target: Win32                //
//                       //
// Revision History: Created March 2002    //
//                       //
//                       //
/////////////////////////////////////////////////
#include <iostream.h>
#include <stdlib.h>
int main();
int solveMatrix(int m1, int m2, int m3, int m4, int m5, int m6, int m7, int m8, int m9)
{
 int cross1, cross2, cross3, cross4, cross5, cross6;
 int eq1, eq2;
 int det;
 cross1 = m1 * m5 * m9;
 cross2 = m2 * m6 * m7;
 cross3 = m3 * m4 * m8;
 cross4 = m7 * m5 * m3;
 cross5 = m8 * m6 * m1;
 cross6 = m9 * m4 * m2;
 eq1 = cross1 + cross2 + cross3;
 eq2 = cross4 + cross5 + cross6;
 det = eq1 - eq2;
 return det;
}
void doMatrix()
{
 int m1, m2, m3, m4, m5, m6, m7, m8, m9;
 system("cls");
 cout << "    |  |   " << endl;
 cout << "   1 | 2 | 3  " << endl;
 cout << "  ------------- " << endl;
 cout << "   4 | 5 | 6  " << endl;
 cout << "  ------------- " << endl;
 cout << "   7 | 8 | 9  " << endl;
 cout << "    |  |   \n\n" << endl;
 cout << "Please enter number 1: ";
 cin >> m1;
 cout << "Please enter number 2: ";
 cin >> m2;
 cout << "Please enter number 3: ";
 cin >> m3;
 cout << "Please enter number 4: ";
 cin >> m4;
 cout << "Please enter number 5: ";
 cin >> m5;
 cout << "Please enter number 6: ";
 cin >> m6;
 cout << "Please enter number 7: ";
 cin >> m7;
 cout << "Please enter number 8: ";
 cin >> m8;
 cout << "Please enter number 9: ";
 cin >> m9;
 cout << endl << "------------\n" << endl;
 cout << "The determinant is: " << solveMatrix(m1, m2, m3, m4, m5, m6, m7, m8, m9) << endl << endl;
 system("pause");
 main();
}
void solveSystem()
{
 system("cls");
 int s1, s2, s3, s4, s5, s6, s7, s8, s9, s10, s11, s12;
 int d, dx, dy, dz;
 cout << "1(x) +  2(y) +  3(z) = 4" << endl;
 cout << "5(x) +  6(y) +  7(z) = 8" << endl;
 cout << "9(x) + 10(y) + 11(z)  = 12" << endl << endl;
 cout << "Please enter number 1: ";
 cin >> s1;
 cout << "Please enter number 2: ";
 cin >> s2;
 cout << "Please enter number 3: ";
 cin >> s3;
 cout << "Please enter number 4: ";
 cin >> s4;
 cout << "Please enter number 5: ";
 cin >> s5;
 cout << "Please enter number 6: ";
 cin >> s6;
 cout << "Please enter number 7: ";
 cin >> s7;
 cout << "Please enter number 8: ";
 cin >> s8;
 cout << "Please enter number 9: ";
 cin >> s9;
 cout << "Please enter number 10: ";
 cin >> s10;
 cout << "Please enter number 11: ";
 cin >> s11;
 cout << "Please enter number 12: ";
 cin >> s12;
 d = solveMatrix(s1, s2, s3, s5, s6, s7, s9, s10, s11);
 dx = solveMatrix(s4, s2, s3, s8, s6, s7, s12, s10, s11);
 dy = solveMatrix(s1, s4, s3, s5, s8, s7, s9, s12, s11);
 dz = solveMatrix(s1, s2, s4, s5, s6, s8, s9, s10, s12);
 cout << endl << "------------\n" << endl;
 cout << "X: " << dx << "/" << d << endl;
 cout << "Y: " << dy << "/" << d << endl;
 cout << "Z: " << dz << "/" << d << endl << endl;
 system("pause");
 main();
}
int main()
{
   system("cls");
   int w00t;
   cout << "-------------------------------------------------" << endl;
   cout << "---------Welcome to 3x3 Matrix Utilities---------" << endl;
   cout << "-------------------------------------------------" << endl;
   cout << "------Written by Zebulon--http://zebulon.tk------" << endl;
   cout << "-------------------------------------------------" << endl;
   cout << "-------------Please select an option-------------" << endl;
   cout << "-------------------------------------------------" << endl;
   cout << "--[1]---Find the determinant of a 3 by 3 matrix--" << endl;
   cout << "--[2]---Solve a 3 variable, 3 equation system----" << endl;
   cout << "--[3]---Exit-------------------------------------" << endl;
   cin >> w00t;
   switch(w00t)
   {
    case 1:
    doMatrix();
    break;
    case 2:
    solveSystem();
    break;
    case 3:
    system("exit");
    break;
    default:
    main();
    break;
   }
   return 0;
}
```

