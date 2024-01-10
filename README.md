    //ROCK PAPER SCISSORS GAME DEGIGNED BY FURKAN ASKIN
    #include <iostream>
    #include <string>

    using namespace std;

    // Lets create a function to determine the winner  fallow my code
    string determineWinner(string player1, string player2) {
    if (player1 == player2) {
        return "It's a tie!";
    } else if (
            (player1 == "rock" && player2 == "scissors") ||
            (player1 == "paper" && player2 == "rock") ||
            (player1 == "scissors" && player2 == "paper")
            ) {
        return "Player 1 wins!";
    } else {
        return "Player 2 wins!";
    }
    }

    int main() {
    string choicePlayer1, choicePlayer2;

    cout << "Player 1, enter your choice (rock, paper, scissors): ";
    cin >> choicePlayer1;

    cout << "Player 2, enter your choice (rock, paper, scissors): ";
    cin >> choicePlayer2;


    for (char &c : choicePlayer1) {
        c = tolower(c);
    }
    for (char &c : choicePlayer2) {
        c = tolower(c);
    }


    cout << determineWinner(choicePlayer1, choicePlayer2) << endl;
    cout<< "THANK YOU FOR GAME  IF YOU LOSE TRY AGAIN BRO";

    return 0;
}
