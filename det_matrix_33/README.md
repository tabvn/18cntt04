# Định Thức ma trận vuông cấp 3

<img src="./debai.jpeg" alt="" />

## c++

```c++

//
//  main.cpp
//  homework
//
//  Created by Toan on 9/18/18.
//  Copyright © 2018 Toan. All rights reserved.
//

#include <iostream>
using namespace std;

int N = 3;
int A[3][3] = {{-2,2,-3}, {-1,1,3},{2,0,-1}}; // Khai bao ma tran A 3 hang 3 cot

/*
 A=
 
 -2 2 -3
 -1 1 3
 2 0 -1
 
 */


int tinhDinhThucConBuCap2(int hang, int cot){
    
    /*
     B =
     b11 b12
     b21 b22
     
     */
    int B[2][2] = {{0,0}, {0, 0}};
    int ketqua = 0;
    
    
    int increaseRow = 0;
    
    int increaseColumn = 0;
    
    for(int i = 0; i<N; i++){
        
       

        if(hang != i){
            for(int j =0; j< N; j++){
                if(cot != j){
                    // day la gia tri phan tu can lay
                    
                    B[increaseRow][increaseColumn] = A[i][j];
                    
                
                    
                    increaseColumn++;
                }
            }
            
            increaseRow ++;
        }
        
        increaseColumn = 0;
        
        
    }
    
    ketqua = (B[0][0] * B[1][1]) - (B[1][0] * B[0][1]);
    
    //cout << B[0][0] << "*" << B[1][1] << "-" << B[1][0] << "*"<< B[0][1] << endl;
    return ketqua;
    
}
int main(){
    
    int d = 0;
    
    
    
    int hang = 0;
    
    
    for (int cot = 0; cot < N; cot++){
        // a11 = A[hang][0]
        int dau = -1;
        
        int tongHangCot = (hang+1) + (cot + 1);
        if( tongHangCot % 2 == 0){
            dau = 1;
        }
        
        int bu = tinhDinhThucConBuCap2(hang, cot);
        
        
        d += dau * (A[hang][cot]) * bu; // d = d + (dau * A[hang][cot] * bu)
        
    
        
        
    }
    
    cout << "Dinh thuc cua ma tran A:" << d << endl;
    
    return 0;
}

```