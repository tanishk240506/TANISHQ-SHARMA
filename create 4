1. Implement a base class Shape with derived classes Circle, Rectangle, and Triangle. Use virtual functions to calculate the area of each shape.



#include <iostream>
#include <cmath>

class Shape {
public:
    virtual double area() const = 0; // Pure virtual function
};

class Circle : public Shape {
private:
    double radius;
public:
    Circle(double r) : radius(r) {}
    double area() const override {
        return M_PI * radius * radius;
    }
};

class Rectangle : public Shape {
private:
    double length, width;
public:
    Rectangle(double l, double w) : length(l), width(w) {}
    double area() const override {
        return length * width;
    }
};

class Triangle : public Shape {
private:
    double base, height;
public:
    Triangle(double b, double h) : base(b), height(h) {}
    double area() const override {
        return 0.5 * base * height;
    }
};
2. Create a base class Animal with a virtual function speak(). Implement derived classes Dog, Cat, and Bird, each overriding the speak() function.



#include <iostream>

class Animal {
public:
    virtual void speak() const = 0; // Pure virtual function
};

class Dog : public Animal {
public:
    void speak() const override {
        std::cout << "Woof!" << std::endl;
    }
};

class Cat : public Animal {
public:
    void speak() const override {
        std::cout << "Meow!" << std::endl;
    }
};

class Bird : public Animal {
public:
    void speak() const override {
        std::cout << "Chirp!" << std::endl;
    }
};
3. Write a program that demonstrates function overriding using a base class Employee and derived classes Manager and Worker.



#include <iostream>
#include <string>

class Employee {
public:
    virtual void display() const {
        std::cout << "Employee details" << std::endl;
    }
};

class Manager : public Employee {
public:
    void display() const override {
        std::cout << "Manager details" << std::endl;
    }
};

class Worker : public Employee {
public:
    void display() const override {
        std::cout << "Worker details" << std::endl;
    }
};
4. Write a program to demonstrate pointer arithmetic by creating an array and accessing its elements using pointers.



#include <iostream>

int main() {
    int arr[] = {10, 20, 30, 40, 50};
    int* ptr = arr;

    for (int i = 0; i < 5; ++i) {
        std::cout << *(ptr + i) << " "; // Pointer arithmetic
    }

    return 0;
}
5. Implement a program that dynamically allocates memory for an integer array and initializes it using pointers.



#include <iostream>

int main() {
    int* arr = new int[5]; // Dynamically allocate memory

    for (int i = 0; i < 5; ++i) {
        *(arr + i) = (i + 1) * 10; // Initialize array
    }

    for (int i = 0; i < 5; ++i) {
        std::cout << *(arr + i) << " "; // Accessing values
    }

    delete[] arr; // Free memory
    return 0;
}
6. Create a program that uses a pointer to swap the values of two variables.



#include <iostream>

void swap(int* a, int* b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int x = 10, y = 20;
    std::cout << "Before swap: x = " << x << ", y = " << y << std::endl;
    swap(&x, &y);
    std::cout << "After swap: x = " << x << ", y = " << y << std::endl;

    return 0;
}
7. Write a program that creates a dynamic object of a class Student and accesses its members using pointers.



#include <iostream>
#include <string>

class Student {
private:
    std::string name;
    int age;
public:
    Student(std::string n, int a) : name(n), age(a) {}
    void display() const {
        std::cout << "Name: " << name << ", Age: " << age << std::endl;
    }
};

int main() {
    Student* student = new Student("John Doe", 20);
    student->display();
    delete student; // Free memory
    return 0;
}
8. Implement a program that uses a pointer to an array of objects to store and display details of multiple Book objects.



#include <iostream>
#include <string>

class Book {
private:
    std::string title;
    std::string author;
public:
    Book(std::string t, std::string a) : title(t), author(a) {}
    void display() const {
        std::cout << "Title: " << title << ", Author: " << author << std::endl;
    }
};

int main() {
    Book* books = new Book[2] {
        Book("1984", "George Orwell"),
        Book("To Kill a Mockingbird", "Harper Lee")
    };

    for (int i = 0; i < 2; ++i) {
        books[i].display();
    }

    delete[] books; // Free memory
    return 0;
}
9. Create a program that demonstrates the use of a pointer to an object in a class member function.



#include <iostream>

class Person {
private:
    std::string name;
public:
    Person(std::string n) : name(n) {}
    void display() const {
        std::cout << "Name: " << name << std::endl;
    }

    void printName() const {
        const Person* ptr = this;
        ptr->display();
    }
};

int main() {
    Person person("Alice");
    person.printName();
    return 0;
}
10. Write a class Box with a member function that returns the current object using the this pointer.



#include <iostream>

class Box {
private:
    int length, width, height;
public:
    Box(int l, int w, int h) : length(l), width(w), height(h) {}

    Box* getThisPointer() {
        return this; // Return the current object
    }

    void display() const {
        std::cout << "Box dimensions: " << length << "x" << width << "x" << height << std::endl;
    }
};

int main() {
    Box box(10, 20, 30);
    box.getThisPointer()->display(); // Access current object using this pointer
    return 0;
}
11. Implement a program that uses the this pointer to chain member function calls in a class Person.



#include <iostream>
#include <string>

class Person {
private:
    std::string name;
public:
    Person(std::string n) : name(n) {}

    Person* setName(std::string n) {
        name = n;
        return this; // Return the current object
    }

    void display() const {
        std::cout << "Name: " << name << std::endl;
    }
};

int main() {
    Person person("Alice");
    person.setName("Bob")->display(); // Chaining member functions
    return 0;
}
12. Create a class Counter with a member function that compares two objects using the this pointer.



#include <iostream>

class Counter {
private:
    int value;
public:
    Counter(int v) : value(v) {}

    bool isEqualTo(const Counter& other) const {
        return this->value == other.value; // Compare values using this pointer
    }
};

int main() {
    Counter counter1(10), counter2(20);
    if (counter1.isEqualTo(counter2)) {
        std::cout << "Counters are equal" << std::endl;
    } else {
        std::cout << "Counters are not equal" << std::endl;
    }
    return 0;
}
13. Write a program that uses pure virtual functions to create an abstract class Vehicle with derived classes Car and Bike.



#include <iostream>

class Vehicle {
public:
    virtual void start() = 0; // Pure virtual function
    virtual void stop() = 0;  // Pure virtual function
};

class Car : public Vehicle {
public:
    void start() override {
        std::cout << "Car is starting" << std::endl;
    }

    void stop() override {
        std::cout << "Car is stopping" << std::endl;
    }
};

class Bike : public Vehicle {
public:
    void start() override {
        std::cout << "Bike is starting" << std::endl;
    }

    void stop() override {
        std::cout << "Bike is stopping" << std::endl;
    }
};
14. Implement a program that demonstrates runtime polymorphism using a virtual function in a base class Shape and derived classes Circle and Square.



#include <iostream>
#include <cmath>

class Shape {
public:
    virtual void draw() const {
        std::cout << "Drawing Shape" << std::endl;
    }
};

class Circle : public Shape {
public:
    void draw() const override {
        std::cout << "Drawing Circle" << std::endl;
    }
};

class Square : public Shape {
public:
    void draw() const override {
        std::cout << "Drawing Square" << std::endl;
    }
};

int main() {
    Shape* shape1 = new Circle();
    Shape* shape2 = new Square();
    
    shape1->draw(); // Runtime polymorphism
    shape2->draw(); // Runtime polymorphism

    delete shape1;
    delete shape2;

    return 0;
}
15. Create a class Account with a pure virtual function calculateInterest(). Implement derived classes SavingsAccount and CurrentAccount.



#include <iostream>

class Account {
public:
    virtual void calculateInterest() = 0; // Pure virtual function
};

class SavingsAccount : public Account {
public:
    void calculateInterest() override {
        std::cout << "Calculating interest for Savings Account" << std::endl;
    }
};

class CurrentAccount : public Account {
public:
    void calculateInterest() override {
        std::cout << "No interest for Current Account" << std::endl;
    }
};
16. Write a program that demonstrates polymorphism using a base class Media and derived classes Book and DVD.



#include <iostream>

class Media {
public:
    virtual void displayInfo() const {
        std::cout << "Displaying media information" << std::endl;
    }
};

class Book : public Media {
public:
    void displayInfo() const override {
        std::cout << "Displaying Book information" << std::endl;
    }
};

class DVD : public Media {
public:
    void displayInfo() const override {
        std::cout << "Displaying DVD information" << std::endl;
    }
};

int main() {
    Media* media1 = new Book();
    Media* media2 = new DVD();

    media1->displayInfo(); // Polymorphism
    media2->displayInfo(); // Polymorphism

    delete media1;
    delete media2;

    return 0;
}
17. Implement a class hierarchy with a base class Appliance and derived classes WashingMachine, Refrigerator, and Microwave. Use virtual functions to display the functionality of each appliance.



#include <iostream>

class Appliance {
public:
    virtual void functionality() const {
        std::cout << "General appliance functionality" << std::endl;
    }
};

class WashingMachine : public Appliance {
public:
    void functionality() const override {
        std::cout << "Washing clothes" << std::endl;
    }
};

class Refrigerator : public Appliance {
public:
    void functionality() const override {
        std::cout << "Cooling food" << std::endl;
    }
};

class Microwave : public Appliance {
public:
    void functionality() const override {
        std::cout << "Heating food" << std::endl;
    }
};
18. Create a program that uses polymorphism to calculate the area of different geometric shapes using a base class Shape and derived classes Circle and Rectangle.



#include <iostream>
#include <cmath>

class Shape {
public:
    virtual double area() const = 0; // Pure virtual function
};

class Circle : public Shape {
private:
    double radius;
public:
    Circle(double r) : radius(r) {}
    double area() const override {
        return M_PI * radius * radius;
    }
};

class Rectangle : public Shape {
private:
    double length, width;
public:
    Rectangle(double l, double w) : length(l), width(w) {}
    double area() const override {
        return length * width;
    }
};

int main() {
    Shape* shape1 = new Circle(5);
    Shape* shape2 = new Rectangle(4, 6);

    std::cout << "Area of Circle: " << shape1->area() << std::endl; // Polymorphism
    std::cout << "Area of Rectangle: " << shape2->area() << std::endl; // Polymorphism

    delete shape1;
    delete shape2;

    return 0;
}
19. Write an abstract class Employee with pure virtual functions calculateSalary() and displayDetails(). Implement derived classes Manager and Engineer.



#include <iostream>

class Employee {
public:
    virtual void calculateSalary() = 0; // Pure virtual function
    virtual void displayDetails() const = 0; // Pure virtual function
};

class Manager : public Employee {
public:
    void calculateSalary() override {
        std::cout << "Calculating salary for Manager" << std::endl;
    }

    void displayDetails() const override {
        std::cout << "Manager Details" << std::endl;
    }
};

class Engineer : public Employee {
public:
    void calculateSalary() override {
        std::cout << "Calculating salary for Engineer" << std::endl;
    }

    void displayDetails() const override {
        std::cout << "Engineer Details" << std::endl;
    }
};
20. Implement an abstract class Payment with a pure virtual function processPayment(). Create derived classes CrCardPayment and DebitCardPayment.



#include <iostream>

class Payment {
public:
    virtual void processPayment() = 0; // Pure virtual function
};

class CrCardPayment : public Payment {
public:
    void processPayment() override {
        std::cout << "Processing Cr Card Payment" << std::endl;
    }
};

class DebitCardPayment : public Payment {
public:
    void processPayment() override {
        std::cout << "Processing Debit Card Payment" << std::endl;
    }
};
21. Create an abstract class Device with a pure virtual function turnOn(). Implement derived classes Laptop and Smartphone.



#include <iostream>

class Device {
public:
    virtual void turnOn() = 0; // Pure virtual function
};

class Laptop : public Device {
public:
    void turnOn() override {
        std::cout << "Laptop is turning on" << std::endl;
    }
};

class Smartphone : public Device {
public:
    void turnOn() override {
        std::cout << "Smartphone is turning on" << std::endl;
    }
};

int main() {
    Queue<int> q;
    q.enqueue(10);
    q.enqueue(20);
    q.enqueue(30);
    q.display();

    q.dequeue();
    q.display();

    return 0;
}
