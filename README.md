Branch structure:



 	dev:

 		- adds an encouraging "Good luck" message for players



 	documentation: same as feature1, except it contains this README

 

 	feature1:



 		- adds ability to quit the game by entering a negative number

 		- allow the player to play again after every game ends

 		- improves the hints given when the player guesses incorrectly (i.e. "Too low! Try a higher number." vs. "Too low!")

 		- adds a comment to document the version of the quit feature



 	feature2:



 		- adds an encouraging "Good luck" message for players

 		- adds a MAX\_ATTEMPTS constant and a game over state

 		- implements the max attempts game over condition



 	feature3:



 		- adds private member variable "hintsEnabled" to GameEngine.java, and initializes it to "true" in the constructor

&nbsp;		- adds getter and setter for "hintsEnabled", and a "getHint()" method that computes the hint for a given guess

&nbsp;		- uses the new "getHint()" method to compute and pass the hint into the GuessResult object created when the player guesses incorrectly

&nbsp;		- adds 8 new unit tests to GameEngineTest.java



&nbsp;	hotfix:

&nbsp;		

&nbsp;		- fixes a bug in Utils.java so that "randomInt()" correctly produces a random integer between \[min, max] instead of \[min, max)



&nbsp;	main: no changes, the initial number guessing game inherited by all other branches

