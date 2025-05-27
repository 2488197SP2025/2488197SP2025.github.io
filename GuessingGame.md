# Random Guessing Game

The flowchart below demonstrates the logic for the random guessing game. 
In the game, the program chooses a random number and the user attempts to guess the selected number.
The system then provides feedback after each attempted guess until the right number is found.

## Flowchart

```mermaid
flowchart TD
    Start([Start])
    Start --> Init[Select random number and range of values]
    Init --> Ask[Ask user to guess a number]
    Ask --> Validate{Is the inputted value a valid number?}
    Validate -- No --> Error[Show error and re-ask]
    Error --> Ask
    Validate -- Yes --> Compare{Is the guess correct?}
    Compare -- Yes --> Correct[Return 'Correct']
    Compare -- No --> HighOrLow{Is guess too high?}
    HighOrLow -- Yes --> TooHigh[Return 'Too high']
    HighOrLow -- No --> TooLow[Return 'Too low']
    TooHigh --> Ask
    TooLow --> Ask
    Correct --> End([End])
