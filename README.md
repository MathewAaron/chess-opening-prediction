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

## Training Loss

<img width="540" alt="Screen Shot 2022-07-01 at 9 26 58 AM" src="https://user-images.githubusercontent.com/71589098/176904257-288464f9-2fd0-476c-b0dd-8b3711eb91b3.png">

## Accuracy

<img width="789" alt="Screen Shot 2022-07-01 at 9 26 39 AM" src="https://user-images.githubusercontent.com/71589098/176904410-36a440c3-b1cc-4d94-938f-25eae013b866.png">

## LOSS curve for CNN

![Unknown](https://user-images.githubusercontent.com/71589098/176904630-ba8b9421-0ade-440c-a59a-66976ca46cb1.png)

## Confusing Matrix for CNN and Random Forrest (Base Classifier)

<img width="851" alt="Screen Shot 2022-07-01 at 9 37 18 AM" src="https://user-images.githubusercontent.com/71589098/176905853-58533f14-bf20-4e1b-bca2-2e70c9c08d58.png">


## Confusion matrix and loss curve for LSTM

<img width="848" alt="Screen Shot 2022-07-01 at 9 35 40 AM" src="https://user-images.githubusercontent.com/71589098/176905366-eb233854-cd4d-48e0-842c-59e760a7c3ad.png">

