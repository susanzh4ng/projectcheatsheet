# Project Cheat Sheet



### Miscellaneous ###
* `rafce` -> to create the skeletons of components in React


### Basic Git Commands ###
**(#.) steps needed to push code to GitHub after finishing up edits on the IDE**
* `status` -> ***(1.)*** check to see which files are being tracked or need to be commited
* `init` -> use this command inside of your project to turn it into a Git repository and start using Git with that codebase
* `clone` -> bring a repo down from the internet (remote repository like Github) to your local machine
* `log` -> outputs a log of all of your commits
* `add .` -> ***(2.)*** track  all your files and changes with Git
* `commit -m "[descriptive message]"` -> ***(3.)*** save your changes into Git
* `push` -> ***(4.)*** push your changes to your remote repo on Github (or another website)
	* `push origin master` -> pushes your changes to master branch
	* `push -u origin master` -> sets up stream so that pushing to master branch is the default
* `pull` -> pull changes down from the remote repo to your local machine
* `reset [file-name]` -> undo an `add [file-name]`
* `reset HEAD` -> undo the last `commit`
	* `reset HEAD~1` -> undo the `commit` that was 1 commits ago



### Important Terminal Commands ###
* `code .` -> opens the code in VS Code depending on the filepath
* `cd ../[file-name]` -> gets you out of a folder
* `q` -> gets you out of a terminal response
* `clear` -> clears terminal
* `ls` -> see which files make up the repo



### Git Branching ###
* `branch` -> see the branches that make up the repo
* `checkout -b [new-branch]` -> creates new branch
* `checkout [existing-branch]` -> switches you to work on another branch
* `diff [another-branch]` -> see how another-branch differs from the branch you are currently on
* `branch -d [merged-branch]` -> deletes branch; only use if the branch has already been merged
* ***Using a pull request to push local branch's code master-branch:***
* ***(1.)*** `status`
* ***(2.)*** `add`
* ***(4.)*** `commit -m "[message]"`
* ***(4.)*** `push origin [new-branch]`
* ***(5.)*** On the GitHub repo, you should see the option to create a pull request
    * ***Merging local branch's code with master-branch:***
	* ***(6.)*** On the GitHub repo's Pull Request, you should be able to merge new-branch with master-branch (clicking the button will only merge the code on GitHub)
	* ***(7.)*** `pull [origin master]` -> pulls code from GitHub's master-branch to local machine's environment
	* **Merge Conflicts:**
		* after `pull [origin master]`, you might experience merge conflicts
		* VS Code allows you to manage merge conflicts within the IDE's terminal, BUT easiest way is to resolve it within GitHub's interface



### How to initialize a repository locally ###
* Create the folder and files in VS Code
* `git init` -> initializes empty Git repository
* `git status` -> check to see if on master branch
* `git add .` -> adds files to staging area
* `git commit -m "[message]" `
* Create repo (same name as the VS Code folder's name) in GitHub
* ` git remote add origin [HTTPS]`
* `git remote -v` -> to check to see if it worked
* `git push origin master`
* Done :)



### How to Start a React Web App ###
* Create a new, empty folder on laptop
* Open VS code
* Open new folder through VS Code (or just drop folder into VS Code, if folder is located on Desktop)
* `npx create-react-app ./` within VS Code's terminal (VS code -> view -> terminal) in order to start the app
* `npm start` to view on a local host
* Good job :)



### Server side of a MERN stack application ###
* Create a new folder (titled "server") in the same folder that the front end of the web app is located in
* `npm init`
    * Keep hitting enter (this will be your package.json file)
* `npm i express` -> installs express package (the most common tool for making servers; provides you with the basic tools and methods to initialize a server)
* `npm i mongoose` -> a dependency that provides us with the method to make the model, so that you can see the schemas of mongoDB on the server side
* `npm i body-parser` -> a middleware that checks out http requests that comes from the client side; that the data and http requests are valid to run on the server
* `npm i nodemon` -> when we make any file changes and save them, this will automatically restart and update our server (we no longer have to do it manually)
* `"start": "nodemon index.js"` -> add to your scripts in package.json; whenever we start our program in the terminal, it also starts index.js with the nodemon package
* `"type": "module"` -> add before scripts in package.json; necessary for importing modules