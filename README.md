# 4A CLASS OBJECT CONVERSION

## PROGRAM STATEMENT:
Write a CPP Program for Class conversion that can be achieved by conversion function which is done by the use of operator overloading (use double data)

## ALGORITHM:
1. Start the program. 
2. Define a class Class_type_one with a private float variable a to store a float value. Provide a 
default constructor to initialize a to 0.0, a parameterized constructor to initialize a with a 
specific float value, a get method to return a, and a display method to print a. 
3. Define another class Class_type_two with a private float variable b to store the converted 
value. Overload the assignment operator (=) to convert an object of Class_type_one to 
Class_type_two by assigning a's value to b. Include a display method to print b. 
4. In the main function, read a float input from the user and create an object obj1 of 
Class_type_one initialized with this input. 
5. Create an object obj2 of Class_type_two, and use the overloaded assignment operator to assign 
obj1 to obj2. 
6. Call the display method for both obj1 and obj2 to display the values stored in Class_type_one 
and Class_type_two, respectively. 
7. End the program.

## PROGRAM:
```
#include <bits/stdc++.h>
using namespace std;
class Class_type_two ;
class Class_type_one 
{
   double a;
   public:
      Class_type_one()
      {
          cin>>a;
       
      }
      double get()
      {
        
         return a;
      }
      void display()
     {
       cout<<a<<endl;
      
     }
};
class Class_type_two 
{
   double b;
   public:
   Class_type_two()
   
   {
       cin>>b;
     
   }
   Class_type_two(class Class_type_one a)
   {
       b=a.get();
       a.display();
   }
   void display()
   {
       cout<<b<<endl;
      
   }
};
int main()
{
    Class_type_one a;
    Class_type_two b;
    b=a;
    b.display();
    
  
   return 0;
}
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/5c7b0bad-61dd-4809-8893-1cafb27c3ed5)

## RESULT:
Thus, the C++ program for Class conversion that can be achieved by conversion function, which is 
done by the use of operator overloading, is created successfully.



# 4B  COMPOSITION VS. INHERITANCE

## PROGRAM STATEMENT:
Write a CPP program to demonstrate on the object composition (use double data) 

## ALGORITHM:
1. Define a class Engine with a double data member (horsepower).
2. Create another class Car that has an Engine object as a member (composition).
3. Initialize the Engine object inside the Car constructor using initializer list.
4. Create a Car object in main() by passing a double value.
5. Call a method in Car that uses the composed Engine object to display the value.

## PROGRAM:
```
#include <iostream>
using namespace std;
class A {
public:
double num;
void read(){
    cin>>num;
}
};
class B :public A
{
    
public:
void read2()
{
    cout<<"Constructor A(double a) is invoked"<<endl;
}
};
class C:public B
{
    public:
    void read3()
    {
        cout<<"Data in object of class B = "<<num<<endl;
        cout<<"Data in member object of class A in class B = "<<num;    }
};
class D:public C
{
    public:
    void display()
    {
        D obj;
        obj.read();
        obj.read2();
        obj.read3();
    }
};
int main()
{
	D ob;
	ob.display();
	return 0;
}
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/ad161b2b-a41e-4ec7-8a78-4e286c60f47e)

## RESULT:
Thus, the C++ program to demonstrate on the object composition is created successfully.


# 4C  VIRTUAL FUNCTIONS – THIS POINTER

## PROGRAM STATEMENT:
Write a CPP program to override the print() function in the base class with the print() function in the child class using the concept of virtual functions.

## ALGORITHM:
1. Start the program. 
2. Define a base class with a virtual print method that outputs "Base class". 
3. Define a derived class that inherits from base and overrides the print method to read and 
display a string. 
4. In the main function, create a pointer of type base and an object of type derived. 
5. Assign the address of the derived object to the base pointer and call the print method using the 
pointer. 
6. End the program.

## PROGRAM:
```
#include<iostream>
using namespace std;
class A {
public:
string a;
A()
{
    cin>>a;
}
virtual void print()
{
    cout<<a;
}
};
class B:public A
{
    public:
    void print()
    {
        cout<<a;
    }
};
int main()
{
    A *bptr;
    B d;
    bptr = &d;
    bptr->print();  
    return 0;
}
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/6b6f5817-aa51-4c00-8bd3-2e0f6859f957)

## RESULT:
Thus, the C++ program to override the print() function in the base class with the print() function in the child class using the concept of virtual functions is created successfully. 


# 4D VIRTUAL DESTRUCTORS – DYNAMIC BINDING

## PROGRAM STATEMENT:
Write a CPP program to use the concept virtual functions in HIERARCHICAL INHERITANCE. 

## ALGORITHM:
1. Create a base class Shape with a virtual function draw().
2. Inherit multiple derived classes (Circle, Square) from Shape.
3. Override the draw() method in each derived class.
4. Use a base class pointer to refer to derived class objects.
5. Call draw() using the base pointer to achieve runtime polymorphism.

## PROGRAM:
```
#include <iostream>
using namespace std;
class animal
{
    public:
    virtual void eat()
    {
        cout<<"Eats some generic food"<<endl;
    }
};
class cat:public animal
{
    public:
     void eat()
    {
        cout<<"Eats Rat"<<endl;
    }
};
class dog:public animal
{
    public:
     void eat()
    {
        cout<<"Eats Meat"<<endl;
    }
};
int main()
{
    dog d;
    animal *a = &d;
    a->eat();
    
    cat c;
    a = &c;
    a->eat();
}
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/49d4c584-f4a8-4afc-b7d1-8ac5868e746e)

## RESULT:
Thus,the CPP program to use the concept virtual functions in HIERARCHICAL INHERITANCE has been successfully created.









