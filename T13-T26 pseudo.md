## T13

- ExtractMin

```c++
    z=H.min
    connect every its children in root list
    x.p=nullptr;
	x.mark=false;
construct array A, size(A)=D(n)+1
    initialize every slot as nullptr
if(H.min.right==nullptr) return;
H.min=H.min.right;
for every node w in root list{
x=w;
d=x.degree;
while(A[d]!=nullptr) {
    y=A[d];
    if(x.key>y.key) swap x,y;
    remove y from root list
    add y as x's kid
    A[d]=nullptr;
    y.mark=false;
    y.p=x;
    x.degree++;
    d=d+1;
}
}
```

- decreaseKey

```c++

```

