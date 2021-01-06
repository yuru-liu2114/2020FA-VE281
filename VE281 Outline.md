## VE281 Outline

## Lecture 2 : Asymptotic Algorithm Analysis

- Best & worst & average cases
- Analyze complexity of algorithm:

1. Ignore constant factors
2. Focus on running time for a large n.

- Big-Oh notation

$$
1. \textbf{If } f(n)=O(g(n)),\textbf{then }cf(n)=O(g(n))\\
2. \textbf{If }f_1(n)=O(g_1(n)),f_2(n)=O(g_2(n)), \textbf{then }f_1(n)+f_2(n)=O(max(g_1(n),g_2(n)))\\
3.\textbf{If }f_1(n)=O(g_1(n)),f_2(n)=O(g_2(n)), \textbf{then }f_1(n)*f_2(n)=O(g_1(n)*g_2(n))\\
4. \textbf{If }f(n)=O(h(n)), h(n)=O(t(n)), \textbf{then }f(n)=O(t(n))
$$

$$
n! > 2^{n} > n^{k} > nlog(n) > n > sqrt(n) > log(n)
$$

sufficient condition: limit

- Big-Omega notation
- Big-Theta notation
- **Time complexity computation of programs**(上手算)
- Space/time trade-off principle

## Lecture 3: Comparison Sort

- **Stability** : 在sort之后有相同key的元素保持与初始序列相同的相对顺序

---

自己看下再和课件对答案：

O() ? Omega() ? average? stable? in-place?

- insertion sort
- selection sort
- bubble sort

---

Master's Theorem
$$
T(n)=\left\{  
             \begin{array}{**lr**}  
             O(n^dlog n), a=b^d  (d = log_b a)&  \\  
             O(n^d), a<b^d\\  
             O(n^{\log_b a}),a>b^d &    
             \end{array}  
\right.
$$
---

O()? Omega? average? stable? in-place?

- merge sort
- quick sort