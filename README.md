Branch Structure

main: is the stable production branch that 
all other branches stem from. This is the initial
number guessing game.

dev: is branched off of main and adds an encouraging
message that is sent out to new players. This is also an integration
branch that adds new features.

feature2: is branched off of main. It adds max attempts to
the game and maxAttempts logic for the game. 

feature3: is branched off of main. It adds hint functionality.

hotfix: this branch holds a commit that is ready for main. 
It fixes randomInt so that it includes it's max value in the 
range given.

feature1: is branched off of main. Updates .gitignore, added 
version comments, improves user feedback messages for guesses, 
adds play-again loop functionality, and adds the ability to 
quit game with negative number input.



1. The difference between merge, rebase, squash, and cherry-pick: merging combines a 
branch completely into the current branch that you are in. A rebase allows the merging of 
branches to be a linear process instead of multiple branches combining and running in parallel 
like in a marge. Squash combines multiple commits within a single branch into one single commit
removing the need for multiple smaller commits that get crowded. Lastly, cherry-picking allows 
for a single commit of a branch to be merged with another instead of merging the whole branch.
2. In the git history for feature1, feature2, and feature 3, I noticed that when combining feature1
with dev, it was very easy to use a simple merge to combine the two because the changes between the 
two were very minimal and thus there was very little to change. However, when merging feature2 into dev, 
there were far more changes especially since it was combining the changes between feature1 and feature2 
which were separate processes and showcased how much more efficient rebasing is at creating a linear history. 
Merging is useful when it's being applied to one change but when two separate features have gone through several 
different commits it can get messy and allowing for a rebase to make it more linear is best for development and 
clean debugging later. This was also helpful when eventually merging dev into feature 2 because they were both
more linear and merging them became much easier with very few conflicts. Then, with feature 3, using the squash 
to simplify before merging into dev was very useful. There were 4 different small commits that would have complicated the 
merge into dev but being able to simply them into a single commit is far easier to merge than 4 different ones. 
3. In real projects, I would use merge when adding a feature to the master branch that did not conflict with any other 
parts of the program. A good example of this is adding a new level to a game that already has other levels because adding
it wouldn't overlap with the other code and thus would throw no errors. I would use a rebase when I am working with a team 
on the same part of the program at the same time. For example, I am adding to my game the points scored for certain tasks and 
they're adding the damage from enemies. This would create conflict as we would be editing the same things in a merge. I would 
use a squash when I have an error that I am trying to solve and it takes me multiple attempts to fix the same error. Instead of 
having 10 small changes that I don't need anyways, I can keep only the final change and remove the unneccesary steps in the 
middle. Lastly, I would use cherry-picking when there is one thing that I want to change in a branch without being ready to 
merge the entire update. Say for example I was working on how to fight enemies in my game and I liked the way the scoring worked 
but not the rest of the branch yet, I could merge only the scoring feature. 

