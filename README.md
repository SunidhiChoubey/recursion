# recursion
# experiment-15
## AIM- To study and implement recursion in c++
## Theory-
Recursion is a programming technique where a function calls itself in order to solve a problem. In C++, recursion is used to break down complex problems into simpler, more manageable sub-problems, which are solved iteratively through the recursive function.
Key Concepts:
Base Case: The base case is the condition that stops the recursion. It is crucial to prevent the function from calling itself indefinitely. Without a base case, the recursion would result in infinite function calls, leading to a stack overflow.
Recursive Case: This is the part where the function calls itself with a modified argument, working towards the base case.
Types of Recursion:
Direct Recursion: A function directly calls itself.
Example: factorial(n) calling factorial(n-1).
Indirect Recursion: A function calls another function, which in turn calls the original function.
Example:
cpp
Copy code
void funcA() { funcB(); }
void funcB() { funcA(); }
Advantages of Recursion:
Simplicity: Recursive solutions can be simpler and easier to write for problems like factorial, Fibonacci series, or tree traversals.
Divide and Conquer: Recursion is particularly useful in divide-and-conquer algorithms (e.g., QuickSort, MergeSort).
Disadvantages of Recursion:
Performance: Recursive functions can be slower due to the overhead of multiple function calls and stack memory usage.
Memory Consumption: Each recursive call uses stack space. Deep recursion can lead to stack overflow if the recursion depth is too large.
Common Recursion Problems:
Factorial Calculation
Fibonacci Sequence
Tower of Hanoi
Tree Traversals (e.g., Binary Tree Preorder, Inorder, Postorder)
Sorting Algorithms (e.g., QuickSort, MergeSort)
When to Use Recursion:
Recursion is ideal when a problem can be naturally divided into similar sub-problems and when the recursive solution is more intuitive and readable compared to an iterative one. However, it should be used with care to avoid excessive memory usage and performance bottlenecks.
## Code
a.
~~~
#include <iostream>
using namespace std;
int fact(int n)
{
    if (n<=1)
    {
        return 1;
    }
    else
    {
        return (n*fact(n-1));
    }
}
int main()
{
    int x,n;
    cout<<"Enter a number: ";
    cin>>n;
    x= fact(n);
    cout<<n<<"!: "<<x;
}

~~~

b.
~~~
#include <iostream>
using namespace std;
int add(int n)
{
    if (n<=1)
    {
        return 1;
    }
    else
    {
        return (n+add(n-1));
    }
}
int main()
{
    int x,n;
    cout<<"Enter a number: ";
    cin>>n;
    x= add(n);
    cout<<x;
}

~~~
c.
~~~
#include <iostream>
#include <string>
using namespace std;
void rev(char *str)
{
    if (*str)
    {
        rev(str+1);
        cout<<("%c",*str);

    }

}
int main()
{
    char s[50];
    cout<<"Enter a string: ";
    cin>>s;
    rev(s);
}

~~~
d.
~~~
#include <iostream>
#include <string>
using namespace std;
void revn(int i)
{
    if (i>0)
    {
        cout<<i%10;
        revn(i/10);
        

    }

}
int main()
{
    int i;
    cout<<"Enter a number: ";
    cin>>i;
    revn(i);
}

~~~





