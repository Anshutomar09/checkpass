# checkpass

// Online C++ compiler to run C++ program online
#include <iostream>
#include <vector>
using namespace std;
bool pass(string s){
    if(s.size()<4){
        return false;
    }
    bool hasdig=false, hascap=false;
    for(int i=0;i<s.size();i++){
        if(s[i]==' '|| s[i]=='/')return false;
        if(isdigit(s[i])){
            hasdig=true;
        }
        if(isupper(s[i])){
            hascap=true;
        }
        
    }
    return hasdig &&hascap;
}
int main() {
    string s="aA1_67";
    if(pass(s))cout<<1;
    else
    cout<<0;
    return 0;
}
