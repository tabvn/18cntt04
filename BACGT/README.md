# BẬC GIAI THỪA

## C++

```c++

#include <iostream>

using namespace std;


long int giaiThua(int num){
    
    if(num == 0){
        return 1;
    }
    
   int value = 1;
    for (int i = 1; i <=num; i++) {
        value  = value * i;
    
    }
    
    return value;
}

int deg(long int n, int v){
    
    int d = 0;
    
    if(n == 0 || v == 0){
        return 0;
    }
    while(n%2 == 0){
        d++;
        n /= v;
    
    }

    return d;
}


int main(){
    
    int n;
    int d;
    
    cin >> d;
    cin >> n;
    
    
    long int gt = giaiThua(n);
    int degValue = deg(gt, d);
    
    cout <<degValue;
    
    return 0;
}


```