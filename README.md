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

 		- adds getter and setter for "hintsEnabled", and a "getHint()" method that computes the hint for a given guess

 		- uses the new "getHint()" method to compute and pass the hint into the GuessResult object created when the player guesses incorrectly

 		- adds 8 new unit tests to GameEngineTest.java



 	hotfix:

 

 		- fixes a bug in Utils.java so that "randomInt()" correctly produces a random integer between \[min, max] instead of \[min, max)



 	main: no changes, the initial number guessing game inherited by all other branches



Learning Summary:



&nbsp;	Differences:



&nbsp;		merge: Incorporates commits from another branch into the current branch. Only commits after the common ancestor are merged. For example, 'git merge A' merges branch A into the current branch. Conflicts may occur, are indicated by markers such as '======', and must be resolved to successfully merge. The merge is associated with a commit.



&nbsp;		rebase: Used to rewrite history of the current branch. For example, 'git rebase A' rebases the current branch onto A. In other words, A's history now becomes the "base" of the current branch.



&nbsp;		squash: An action that can be done when performing a rebase. Squashing takes one or more commits and mends them into one.



&nbsp;		cherry-pick: Pulls one commit from another branch into the current branch. A hash is used to identify which commit to pull.



&nbsp;	Observations:



&nbsp;		The git history for feature1 had good quality commits and was linear. This branch inherited only one commit, which was the initial commit from main.

&nbsp;		The git history for feature2 had good quality commits, was linear, and inherited commits from main and dev.

&nbsp;		The git history for feature3 had poor quality commits since they did not clearly mention what was changed. For example, "done" does not provide any details to what has changed. This branch was also linear and only inherited one commit, which was from main.



&nbsp;	Applications of strategies: I would use rebase to avoid unnecessary merges as they make the history nonlinear. Merges are useful for merging feature branches since their history is not as important. When merging the feature branches into 'dev' or 'main', I will use rebase to create a linear and readable history. Cherry-picking is useful for applying urgent bug fixes in the main branch. Finally, I will use squashing to rewrite and mend poorly written commit messages.

