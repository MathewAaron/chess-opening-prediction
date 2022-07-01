# chess-opening-prediction
Using CNN and LSTM to predict popular chess game openings from the first few moves of any chess game.

## Motivation
Chess engines are more powerful and accurate now than they’ve ever been
However, they are often not very easily implemented, as high end computing power is needed
As such, a method to use machine learning to mimic the output of a chess engine was devised
This method uses machine learning techniques to identify a chess opening based on its first several moves and to predict the winner of the game accordingly

## Dataset
Dataset was taken from Lichess online database
Data contains all stats, including player elo, player name, opening, win-loss, etc. 
Data was then reduced to just the game’s moves, the win-loss, and the opening name
Since there were multiple hundred openings, only the top 10 most popular were used

<img width="904" alt="Screen Shot 2022-07-01 at 9 20 10 AM" src="https://user-images.githubusercontent.com/71589098/176902813-4553d3bf-9ffa-436c-9761-6d084ed5c735.png">

## CNN
We developed a 5 layer fully connected CNN architecture with RELU activation.
Each layer consists of a convolutional layer, a maxpooling layer, a batch normalization layer, and a ReLu activation function
The output is then fed into a fully connected network that uses batch normalization, ReLu, and Dropout
