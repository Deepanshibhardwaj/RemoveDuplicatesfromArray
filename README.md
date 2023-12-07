# DSA-Codes
C-program to remove duplicates from the sorted array
`#include <stdio.h>
int removeduplicates(int arr[],int n){
    if(n==0||n==1){
        return n;
    }
    int temp[n];
    int j=0;
    for(int i=0;i<n;i++)
        if(arr[i]!=arr[i+1])
            temp[j++]=arr[i];
            
    temp[j++]=arr[n-1];
    for(int i=0;i<j;i++)
        arr[i]=temp[i];
        
    return j;
        
    
}
int main() {
    int arr[]={1,3,3,5,6,6};
    int n=sizeof(arr) / sizeof(arr[0]);
    n=removeduplicates(arr,n);
    
    for(int i=0;i<n;i++)
    printf("%d", arr[i]);
    return 0;
    
}`
