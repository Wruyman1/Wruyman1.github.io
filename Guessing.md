```mermaid
flowchart TD
    Start([Start])
    1[Generate a random number between 1-50] 
    2[Prompt user for input]
    3{Is input a positive integer between 1 and 50}
    4[Show error message and prompt again]
    5{Is guess correct?}
    6[Show 'Too Low' and prompt again]
    7[Show 'Too High' and prompt again]
    8[Show 'Correct!' and end game]
    End([End])

    Start --> 1 --> 2 --> 3
    3 -- False --> 4 --> 2
    3 -- True --> 5
    5 -- True --> 8 --> End
    5 -- False  --> 6 --> 2
    5 -- False --> 7 --> 2
```
# **Game Procedures**
## *Start Game*
### Steps
1. The compter generates a randome number
2. The Compter promps the user for a integer between 1 and 50
3. The user enters a positive integer between 1 and 50
4. The computer sees if the number is a positive integer and is between 1 and 50. If the input doesn't match it throws an error and requests an input
5. Computer evalutes the integer. If the number is correct it ends the game. If integer is not correct it evaluates the input and either tells user it is too high or too low and requests another input from user
6. When the user guess matches the number the computer responses with 'correct' and ends the game
