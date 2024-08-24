# Final-Project-CSC-242
#include <iostream>
using namespace std;

int main(void)
{
    int sequence[] = { 1, 2, 3, 3, 3, 4 , 3, 2, 1 , 2 };
    int matches = 0; // Number of times a number appears
    int most_matches = 0; // The amount of times the most frequent number appears
    int number = 0; // The number that appears the most
    

    for (int i = 0; i < 10; i++)
    {
        matches = 0; // Puts matches back to 0 to count seperately for each number in the array

        for (int j = 0; j < 10; j++)
        {
            if (sequence[j] == sequence[i])
            {
                matches++; // Takes a number and if there is the same number again, adds 1 to matches
            }
        }


        if (matches > most_matches)
        {
            most_matches = matches; 
            number = sequence[i];
            // Isolate the number with the most matches and how many matches there are
        }
    }
    cout << "The most frequently occuring number is " << number << ", appearing " << most_matches << " times." << endl;

    return 0;
}
