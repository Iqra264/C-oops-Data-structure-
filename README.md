# C-oops-Data-structure-
C++ PROGRAMS
#include <iostream>
using namespace std;

int main() {
int a, b, sum;
cout << "Enter two numbers: ";
cin >> a >> b;
sum = a + b;
cout << "Sum = " << sum;
return 0;
}
2)  #include <iostream>
using namespace std;

int main() {
    int num;
    cout << "Enter a number: ";
    cin >> num;

    if (num % 2 == 0)
        cout << "Even number";
    else
        cout << "Odd number";

    return 0;
}
3) #include <iostream>
using namespace std;

int main() {
    int a, b, c;
    cout << "Enter three numbers: ";
    cin >> a >> b >> c;

    if (a >= b && a >= c)
        cout << "Largest number is " << a;
    else if (b >= a && b >= c)
        cout << "Largest number is " << b;
    else
        cout << "Largest number is " << c;

    return 0;
}
4) #include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 10; i++) {
        cout << i << " ";
    }
    return 0;
}
5) #include <iostream>
using namespace std;

int main() {
    int n;
    long long fact = 1;

    cout << "Enter a number: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        fact = fact * i;
    }

    cout << "Factorial of " << n << " = " << fact;

    return 0;
}
6) #include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 5; i++) {
        for (int j = 1; j <= i; j++) {
            cout << "* ";
        }
        cout << endl;
    }
    return 0;
}
OOPS PROGRAM
1) #include <iostream>
using namespace std;

class StarPattern {
public:
    void printPattern() {
        for (int i = 1; i <= 5; i++) {
            for (int j = 1; j <= i; j++) {
                cout << "* ";
            }
            cout << endl;
        }
    }
};

int main() {
    StarPattern s;
    s.printPattern();
    return 0;
}
2) #include <iostream>
using namespace std;

class ReverseNumber {
public:
    int num, rev = 0;

    void input() {
        cout << "Enter a number: ";
        cin >> num;
    }

    void reverse() {
        while (num != 0) {
            int digit = num % 10;
            rev = rev * 10 + digit;
            num /= 10;
        }
        cout << "Reversed number = " << rev << endl;
    }
};

int main() {
    ReverseNumber r;
    r.input();
    r.reverse();
    return 0;
}
3) #include <iostream>
using namespace std;

class Factorial {
public:
    int n;
    long long fact = 1;

    void input() {
        cout << "Enter a number: ";
        cin >> n;
    }

    void findFactorial() {
        for (int i = 1; i <= n; i++)
            fact *= i;
        cout << "Factorial = " << fact << endl;
    }
};

int main() {
    Factorial f;
    f.input();
    f.findFactorial();
    return 0;
}
4) #include <iostream>
using namespace std;

class PrintNumbers {
public:
    void show() {
        for (int i = 1; i <= 10; i++)
            cout << i << " ";
        cout << endl;
    }
};

int main() {
    PrintNumbers p;
    p.show();
    return 0;
}
5) #include <iostream>
using namespace std;

class Largest {
public:
    int a, b, c;

    void input() {
        cout << "Enter three numbers: ";
        cin >> a >> b >> c;
    }

    void findLargest() {
        if (a >= b && a >= c)
            cout << "Largest number is " << a << endl;
        else if (b >= a && b >= c)
            cout << "Largest number is " << b << endl;
        else
            cout << "Largest number is " << c << endl;
    }
};

int main() {
    Largest l;
    l.input();
    l.findLargest();
    return 0;
}
DATA STRUCTURE PROGRAM
1) #include <iostream>
using namespace std;

class ReverseNumber {
public:
    int num, rev = 0;

    void input() {
        cout << "Enter a number: ";
        cin >> num;
    }

    void reverse() {
        while (num != 0) {
            int digit = num % 10;
            rev = rev * 10 + digit;
            num /= 10;
        }
        cout << "Reversed number = " << rev << endl;
    }
};

int main() {
    ReverseNumber r;
    r.input();
    r.reverse();
    return 0;
}
2) #include <iostream>
using namespace std;

#define SIZE 5
class Queue {
    int arr[SIZE];
    int front, rear;

public:
    Queue() { front = rear = -1; }

    void enqueue(int x) {
        if (rear == SIZE - 1)
            cout << "Queue Overflow\n";
        else {
            if (front == -1) front = 0;
            arr[++rear] = x;
        }
    }

    void dequeue() {
        if (front == -1 || front > rear)
            cout << "Queue Underflow\n";
        else
            front++;
    }

    void display() {
        if (front == -1 || front > rear)
            cout << "Queue is empty\n";
        else {
            cout << "Queue elements: ";
            for (int i = front; i <= rear; i++)
                cout << arr[i] << " ";
            cout << endl;
        }
    }
};

int main() {
    Queue q;
    q.enqueue(10);
    q.enqueue(20);
    q.enqueue(30);
    q.display();
    q.dequeue();
    q.display();
}
3) #include <iostream>
using namespace std;

class StarPattern {
public:
    void printPattern() {
        for (int i = 1; i <= 5; i++) {
            for (int j = 1; j <= i; j++) {
                cout << "* ";
            }
            cout << endl;
        }
    }
};

int main() {
    StarPattern s;
    s.printPattern();
    return 0;
}
4) #include <iostream>
using namespace std;

int main() {
    int arr[] = {5, 10, 15, 20, 25};
    int n = 5, key;

    cout << "Enter number to search: ";
    cin >> key;

    bool found = false;
    for (int i = 0; i < n; i++) {
        if (arr[i] == key) {
            cout << "Element found at index " << i << endl;
            found = true;
            break;
        }
    }

    if (!found)
        cout << "Element not found." << endl;
}
5) #include <iostream>
using namespace std;

class Node {
public:
    int data;
    Node* next;
};

int main() {
    Node* head = new Node();
    Node* second = new Node();
    Node* third = new Node();

    head->data = 10;
    head->next = second;

    second->data = 20;
    second->next = third;

    third->data = 30;
    third->next = nullptr;

    Node* temp = head;
    cout << "Linked List elements: ";
    while (temp != nullptr) {
        cout << temp->data << " ";
        temp = temp->next;
    }
}
