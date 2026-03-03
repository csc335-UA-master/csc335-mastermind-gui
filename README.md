# csc335-mastermind-gui

## Project Description
For this project, we will use JavaFX to create GUI for our Mastermind game. 
We will construct a new MastermindGUIView that is a javafx.application.Application and it will look like:

When you win or lose, display a modal (showAndWait()) Alert:

![]()

After the game is over, do not allow any further guesses until “Restart” is clicked.

## Implementation
### Main Board
As shown above, your game board will be a `BorderPane` whose top will be the name of the game, the center will be the main board, and the bottom will be the guess input panel.

As you click the colored `Circle`s in the input panel, a new peg in the guess area will appear – on a new row if the first peg, or at the right of an existing guess. Forbid the user from entering more than 4 pegs by simply ignoring any additional clicks.

You have a “Remove last peg” button that acts as “backspace” to delete the last placed peg.

“Reset” starts a brand new game.

The center area should be a `GridPane` with a row for each potential guess (up to 10). Wrap the `GridPane` in a `ScrollPane` with a preferred height of 500 pixels.

When “Submit Guess” is clicked, the guess should be scored. Report the score using a combination of black and white pegs, where there is a black peg for each “Right Color, Right Place” peg and white for “Right Color, Wrong Place”. Assemble them into a 2x2 `GridPane` with a 1 pixel border.

If the correct answer is reached (4 black scoring pegs are shown) display an `Alert` with the win message shown above. If 10 guesses are reached without winning, show a similar “you lose” `Alert`.  You may wish to display the correct answer in some way of your choosing.

### MVC 
You are required to create this version of the project using the MVC architectural pattern. You must have the following 5 classes:
1.	`Mastermind` – This is the main class. When invoked with a command line argument of “-text”, you will launch the text-oriented UI. When invoked with a command line argument 0f “-window” you’ll launch the GUI view. The default will be the GUI view.
2.	`MastermindGUIView` – This is the JavaFX GUI as shown above
3.	`MastermindTextView` – This is the UI that we built in project 2
4.	`MastermindController` – This class contains all of the game logic, and must be shared by the textual and graphical UIs. You may not call into different controllers from the different UIs and all methods provided must be useful to both front ends.
5.	`MastermindModel` – This class contains all of the game state and must be also shared between the two front ends.

### Requirements
-	A main class, that launches your view using :
		`Application.launch(MastermindGUIView.class, args);`
for the GUI version or launches the text version, depending on the commandline argument given
-	At least the five (5) classes described above, with more as you deem necessary (for instance, the code that breaks the quote into lines may be in its own object to more easily share between the two front-ends)
-	The GitHub repository is empty, so create a new Java Project in eclipse and import what files from the previous projects you’d like to start with

### Submission
As always, the last pushed commit prior to the due date will be graded.
 
