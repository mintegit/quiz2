
#include <iostream>
using namespace std;

int sum(int a[], int n) {
    int s = 0;
    for (int i = 0; i < n; i++) {
        s = s + a[i];
    }
    return s;
}

int maximum(int a[], int n) {
    int max = a[0];
    for (int i = 1; i < n; i++) {
        if (a[i] > max) {
            max = a[i];
        }
    }
    return max;
}

int minimum(int a[], int n) {
    int min = a[0];
    for (int i = 1; i < n; i++) {
        if (a[i] < min) {
            min = a[i];
        }
    }
    return min;
}

int range(int a[], int n) {
    return maximum(a, n) - minimum(a, n);
}

long long multiplication(int a[], int n) {
    long long m = 1;
    for (int i = 0; i < n; i++) {
        m = m * a[i];
    }
    return m;
}

float average(int a[], int n) {
    return (float)sum(a, n) / n;
}

int main() {
    int numbers[5];

    cout << "Enter 5 numbers: " << endl;
    for (int i = 0; i < 5; i++) {
        cin >> numbers[i];
    }

    cout << "Sum = " << sum(numbers, 5) << endl;
    cout << "Range = " << range(numbers, 5) << endl;
    cout << "Max = " << maximum(numbers, 5) << endl;
    cout << "Min = " << minimum(numbers, 5) << endl;
    cout << "Multiplication = " << multiplication(numbers, 5) << endl;
    cout << "Average = " << average(numbers, 5) << endl;

    return 0;
}
