#include <iostream>
#include <fstream>
using namespace std;
void inputArray(int arr[], int size)
{
    cout << "Enter " << size << " elements:\n";
    for (int i = 0; i < size; i++)
    {
        cout << "Element " << i + 1 << ": ";
        cin >> arr[i];
    }
}
void displayArray(int arr[], int size)
{
    cout << "Array Elements: ";
    for (int i = 0; i < size; i++)
    {
        cout << arr[i] << " ";
    }
    cout << endl;
}
//partb
int calculateSum(int arr[], int size)
{
    int sum = 0;
    for (int i = 0; i < size; i++)
    {
        sum += arr[i];
    }
    return sum;
}

// Part (C): Function to write array to file
void writeToFile(int arr[], int size)
{
    ofstream in("arrayData.txt");

    if (!in)
    {
        cout << "Error opening file for writing!\n";
        return;
    }

    for (int i = 0; i < size; i++)
    {
        in << arr[i] << " ";
    }

    in.close();
    cout << "Data written to file successfully.\n";
}

// Part (D): Function to read array from file
void readFromFile(int arr[], int size)
{
    ifstream out("arrayData.txt");

    if (!out)
    {
        cout << "Error opening file for reading!\n";
        return;
    }

    for (int i = 0; i < size; i++)
    {
        out >> arr[i];
    }

    out.close();
    cout << "Data read from file successfully.\n";
}

// Main Function
int main()
{
     int SIZE = 10;   // 1D array size
    int arr[SIZE];

    // Input array
    inputArray(arr, SIZE);

    // Display original array
    cout << "\nOriginal ";
    displayArray(arr, SIZE);

    // Part (E): Calculate sum using value-returning function
    int total = calculateSum(arr, SIZE);
    cout << "Sum of array elements: " << total << endl;

    // Write data to file
    writeToFile(arr, SIZE);

    // Clear array before reading
    for (int i = 0; i < SIZE; i++)
    {
        arr[i] = 0;
    }

    // Read data from file
    readFromFile(arr, SIZE);

    // Display array after reading
    cout << "\nArray after reading from file:\n";
    displayArray(arr, SIZE);

    return 0;
}
