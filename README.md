Branch Structure

main: is the stable production branch that 
all other branches stem from. This is the initial
number guessing game.

dev: is branched off of main and adds an ecouranging
message that is sent out to new players. This is also an integration
branch that adds new features.

feature2: is branched off of main. It adds max attempts to
the game and maxAttempts logic for the game. 

feature3: is branched off of main. It 

hotfix: this branch holds a commit that is ready for main. 
It fixes randomInt so that it includes it's max value in the 
range given.

feature1: is branched off of main. Updates .gitignore, added 
version comments, improves user feedback messages for guesses, 
adds play-again loop functionality, and adds the ability to 
quit game with negative number input.

