# reverse-of-array--2
#include <iostream>
#include <vector> 
using namespace std;

vector<int> reverse(vector<int> v) {
    int s = 0;
    int e = v.size() - 1;
    while (s < e) {
        swap(v[s], v[e]);
        s++;
        e--;
    }
    return v;
}

int main() {
    int size;
    cout << "Enter the size of the vector: ";
    cin >> size;

    vector<int> v;
    cout << "Enter " << size << " elements: ";
    for (int i = 0; i < size; i++) {
        int element;
        cin >> element;
        v.push_back(element);
    }

    // Printing original vector
    cout << "Original vector: ";
    for (int i = 0; i < v.size(); i++) {
        cout << v[i] << " ";
    }
    cout << endl;

    // Reversing the vector
    v = reverse(v);

    // Printing reversed vector
    cout << "Reversed vector: ";
    for (int i = 0; i < v.size(); i++) {
        cout << v[i] << " ";
    }
    cout << endl;

    return 0;
}
