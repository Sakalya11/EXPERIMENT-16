# Experiment 16: - To study and implement Exception Handling

## Aim:-
To execute and run a code which fixes a runtime error using try and catch method

## Theory:-

### What is exceptional handling ?

Exception handling refers to the method of responding to exceptional conditions (like runtime errors) that occur during program execution.
In C, there is no built-in exception handling mechanism like in languages such as C++ (which has try-catch blocks) or Java.
However, developers in C often simulate exception handling using: 

__Error codes__: Functions return specific codes (like 0 for success, non-zero for errors) that indicate whether the function executed successfully or encountered an error.

__setjmp and longjmp functions__: These functions allow for non-local jumps in the program, providing a basic mechanism to handle exceptions. 
setjmp saves the program’s state, and longjmp restores it, enabling the program to return to a previous point in the code.

### Advantages of exceptional handling
__Better Error Detection__: Structured way to handle runtime errors.

__Separation of Logic__: Separates normal execution from error handling.

__Flexibility__: setjmp/longjmp can jump to any part of the code.

__Resource Management__: Ensures proper cleanup on errors.



### Code: -
~~~
#include<iostream>
using namespace std;

int main()
{
    float n1,n2,ans;
    cout<<"Enter values of number os 1 & 2: "<<endl;
    cin>>n1>>n2;
    try{
        if(n2 == 0)
        {
            throw n2;
        }
        else
        {
            ans = n1/n2;
            cout<<"Answer = "<<ans<<endl;
        }
    }
    catch(float num)
    {
        cout<<"\n ERROR: Divsion by: "<<num<<endl;
    }
}
~~~

## Code Ouput:-
![image](https://github.com/user-attachments/assets/5417acde-3f81-4305-81b9-494ee200797e)


## Conclusion:-
In this experiment we learnt how to handle run time errors using try and catch method
