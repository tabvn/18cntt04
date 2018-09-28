## C++

<img src="./debai.png" />

```c++
#include <iostream>

using namespace std;


long long calulateMoney(long long m, long long n, long long t){
    long long s = 0;
    
    if(m > n){ // so but mua < so yeu cau dc khuyen mai
        return n*t;
    }
    
    // so but can phai tra tien la
    
    long long b = n - (n/m);
    
    return b * t;
    
    
    return s;
}

int main(){
    
    long long m,n,t;
    
    cin >> m;
    cin >> n;
    cin >> t;
    
    long long s = calulateMoney(m, n, t);
    
    cout << s;
    
    return 0;
}


```