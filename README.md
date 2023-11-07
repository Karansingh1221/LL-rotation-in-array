#include<iostream>
using namespace std;
int main(){
    int a,b;
    cin>>a;//size of the array
    cin>>b;//No of LL rotation to be performed
    int arr[a];
    //Enter the elemets of the array
    for(int i=0;i<a;i++){
        cin>>arr[i];
    }
    cout<<"Original Array: "<<endl;
    for(int i=0;i<a;i++){
        cout<<arr[i]<<" ";
    }
    cout<<endl;
    for(int i=0;i<b;i++){
        int temp=arr[0];
        for(int j=0;j<a-1;j++){
            arr[j]=arr[j+1];
        }
        arr[a-1]=temp;
    }
    //Array formed ater performing LL rotation
    for(int i=0;i<a;i++){
        cout<<arr[i]<<" ";
    }
}
