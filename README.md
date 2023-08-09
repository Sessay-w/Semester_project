//Semester_project
An online examination system
MWINIDIGUE MOHAMMED SESSAY
UEB3205522
I.T CLASS (D)
#include <iostream>
#include <string>
using namespace std;

int main() {
    string username, password;
    int score = 0;
    int numQuestions = 5;
    string questions[] = {"What is the capital of France?", "What is the largest planet in our solar system?", "What is the smallest country in the world?", "What is the tallest mountain in the world?", "What is the largest ocean in the world?"};
    string answers[] = {"Paris", "Jupiter", "Vatican City", "Mount Everest", "Pacific Ocean"};

    cout << "Welcome to the online exam system!" << endl;
    cout << "Please enter your username: ";
    cin >> username;
    cout << "Please enter your password: ";
    cin >> password;

    // authentication
    if (username == "user" && password == "password") {
        cout << "Authentication successful!" << endl;
        cout << "You will be presented with " << numQuestions << " questions." << endl;

        // ask questions
        for (int i = 0; i < numQuestions; i++) {
            cout << "Question " << i+1 << ": " << questions[i] << endl;
            string userAnswer;
            cout << "Your answer: ";
            cin >> userAnswer;
            if (userAnswer == answers[i]) {
                score++;
                cout << "Correct!" << endl;
            } else {
                cout << "Incorrect. The correct answer is " << answers[i] << "." << endl;
            }
        }

        // display score
        cout << "Your score is " << score << "/" << numQuestions << "." << endl;
    } else {
        cout << "Authentication failed. Please try again." << endl;
    }

    return 0;
}
