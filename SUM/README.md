# SUM

<img src="./debai.png" />

## C++

```c++

/*
 Nguyen Dinh Toan 18CNTT04
 user008
 
 */


#include <iostream>
#include "math.h"


using namespace std;

int  main(){
    
    float a;
    float b;
    long int sum = 0;
    

    
    cin >> a;
    cin >> b;
    

    for (int i=(int) a; i <= (int)b ; i++) {
        sum++;
    }
    
    cout << sum;
    
    return 0;
}


```