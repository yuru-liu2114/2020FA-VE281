```c++
#include <iostream>
#include<bits/stdc++.h>
using namespace std;

class HashList{
    int capacity;
    list<int>* table;
public:
    HashList(int n){
        capacity=n;
        table=new list<int>[n];
    }
    int HashCode(int key){
        return key%capacity;
    }
    void insert(int key){
        int HashIndex=HashCode(key);
        list<int>::iterator i=table[HashIndex].begin();
        for(;i!=table[HashIndex].end();i++) {
            if(*i==key){return;}
        }
        table[HashIndex].push_back(key);
    }
    bool find(int key){
        int HashIndex=HashCode(key);
        list<int>::iterator i=table[HashIndex].begin();
        for(;i!=table[HashIndex].end();i++) {
            if(*i==key){return true;}
        }
        return false;
    }
    void deletenode(int key){
        int HashIndex=HashCode(key);
        list<int>::iterator i=table[HashIndex].begin();
        for(;i!=table[HashIndex].end();i++) {
            if(*i==key) break;
        }
        if(i!=table[HashIndex].end()) table[HashIndex].erase(i);
    }
    void display(){
        for(size_t i=0;i<capacity;i++) {
            cout<<i;
            for(auto x:table[i]){
                cout<<" -> "<<x;
            }
            cout<<endl;
        }
    }
};
```

