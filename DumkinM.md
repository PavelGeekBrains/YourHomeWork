# Руководство по работе с Гитом

>For git to work correctly after writing the text, when going to the terminal, press ctrl+s

### Main commands Git

* git add FileName **(add changes)**

* git commit -m "name of the change" **(make changes)**
сд
* git checkout namecommit **(transition to changes)**

### *Commands for working with* __branches__ ###
### Download ###

* For Git click here [https://git-scm.com/downloads](https://git-scm.com/downloads)

![git functions](git1.png)


![cat](https://proprikol.ru/wp-content/uploads/2020/08/krasivye-kartinki-kotikov-17.jpg "Cat")


 ## about quotes
 
 The Markdown language uses the "more" (">") sign to indicate quotations. It can be inserted both before each line of the quotation, and only before the first line of the paragraph. Quotes in Markdown can contain all kinds of markup elements.


Works with branch

+ *git branch* __When executing this command, git will output in which current branch we click__

+ *git branch branchName* __Creating a branch named branchName__

+ *git merge branchName1* __Merging the BranchName1 branch with the branch we are in__
 
 + *git branch -d branchName2* __Deleting a branchName branch__

 + git diff nameCommit1..nameCommit2 __To see the difference between two commits__

 + git show nameCommit __see what's new in the commit__


 ## The work of git and github. Basic commands ##
 > Cloning
Cloning is when you copy a remote repository to your local PC. This is what any project usually starts with. At the same time, you transfer to yourself all the files and folders of the project, as well as its entire history since its creation. To clone a project, first you need to find out where it is located and copy the link to it.

**Example**

* git clone **https://github.com/DumkinMaksim/GitInstruction.git**


>forward our local commit to the server. This process happens every time we want to update data in a remote repository.
The command intended for this is push. It takes two parameters: the name of the remote repository (we named our origin) and the branch to which changes need to be made (master is the default branch for all repositories).

* git push (origin master- optional)


>If you have made changes in your remote repository, other users can download the changes using the pull command.

* git pull (origin master -optional)