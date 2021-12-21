#include <iostream>
#include <vector>

int* selfDividingNumbers(int left, int right, int* returnSize){
    int count=0;
    int *array=new int[1000];
    for(int i=left;i<=right;i++){
        int copyi=i;
        while(copyi!=0){
            int chuso=copyi%10;
            if((i%chuso)!=0) break;
            copyi/=10;
        }
        if (copyi==0){
            array[count]=i;
            count++;
        }
    }
    *returnSize = count;
    return array;
}
