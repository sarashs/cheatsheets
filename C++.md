
C++ Cheat sheet

### **1. Basic Syntax & Structure:**
```cpp
#include <iostream> // Include header files

using namespace std; // Use the standard namespace

int main() { // Main function
    cout << "Hello, World!" << endl; // Print to console
    return 0; // Return 0 if program runs successfully
}
```

### **2. Variables & Data Types:**
```cpp
int a = 5;          // Integer
double b = 5.5;     // Floating point number
char c = 'A';       // Character
string s = "Hello"; // String
bool flag = true;   // Boolean (true or false)
```

### **3. Control Structures:**
```cpp
// If-Else
if (a > b) {
    // ...
} else if (a < b) {
    // ...
} else {
    // ...
}

// Switch
switch(a) {
    case 1: 
        // ...
        break;
    case 2: 
        // ...
        break;
    default: 
        // ...
}

// For loop
for (int i = 0; i < 10; i++) {
    // ...
}

// While loop
while (a < 10) {
    // ...
    a++;
}
```

### **4. Functions:**
```cpp
// Function declaration
void printMessage() {
    cout << "Message" << endl;
}

// Function with parameters and return value
int add(int x, int y) {
    return x + y;
}
```

### **5. Pointers & References:**
```cpp
int x = 10;
int* ptr = &x;  // Pointer to x
int& ref = x;   // Reference to x
```

### **6. Arrays & Strings:**
```cpp
int arr[5] = {1, 2, 3, 4, 5}; // Array
string str = "Hello";         // String
```

### **7. Classes & Objects:**
```cpp
class MyClass {
public:
    int myVar;
    void myFunction() {
        // ...
    }
};

MyClass obj; // Create object
obj.myVar = 5; 
obj.myFunction();
```

### **8. Standard Library Functions:**
```cpp
#include <vector>  // For vector
#include <map>     // For map
#include <algorithm> // For algorithms like sort

vector<int> vec = {1, 2, 3};
map<string, int> myMap;
myMap["one"] = 1;

sort(vec.begin(), vec.end()); // Sort vector
```

### **9. Input & Output:**
```cpp
int num;
cin >> num; // Input

cout << "Number: " << num << endl; // Output
```

### **10. File Handling:**
```cpp
#include <fstream>

ifstream inFile("input.txt"); // Read from file
ofstream outFile("output.txt"); // Write to file

string line;
while (getline(inFile, line)) {
    // Process line
}
outFile << "Output data" << endl;
```
Certainly! Let's expand the cheatsheet to include `struct` and various forms of object initiation:

### **11. Structs:**
Structs are similar to classes but are typically used for grouping data.

```cpp
struct MyStruct {
    int id;
    string name;
};

MyStruct person1;
person1.id = 1;
person1.name = "John";
```

### **12. Object Initialization:**

#### **a. Default Constructor:**
```cpp
class MyClass {
public:
    MyClass() {
        // Constructor code
    }
};

MyClass obj1; // Object created using default constructor
```

#### **b. Parameterized Constructor:**
```cpp
class MyClass {
public:
    int a;
    MyClass(int x) : a(x) { // Initialization list
        // Constructor code
    }
};

MyClass obj2(5); // Object created with parameterized constructor
```

#### **c. Copy Constructor:**
```cpp
MyClass(const MyClass &source) {
    a = source.a;
}

MyClass obj3 = obj2; // Object created using copy constructor
```

#### **d. Object Initialization using Pointers:**
```cpp
MyClass* ptrObj = new MyClass(10); // Dynamic object creation with pointer
delete ptrObj; // Don't forget to delete to free memory
```

### **13. Dynamic Memory Allocation with Objects:**

#### **a. Single Object:**
```cpp
MyClass* objPtr = new MyClass; // Allocate memory for one object
delete objPtr; // Free memory
```

#### **b. Array of Objects:**
```cpp
MyClass* arrPtr = new MyClass[10]; // Allocate memory for an array of objects
delete[] arrPtr; // Free memory
```

### **14. Struct with Pointers:**
```cpp
struct Node {
    int data;
    Node* next;
};

Node* newNode = new Node;
newNode->data = 5;
newNode->next = nullptr;
delete newNode; // Free memory when done
```
