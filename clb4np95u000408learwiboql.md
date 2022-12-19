# Web Developer Road Map part 2

Hello friends! having covered part one of the web development roadmap part 1, please find the attached link and let's proceed to part 2.

%[https://pcodesdev.hashnode.dev/junior-web-developer-road-map-part-1] 

# Git and GitHub

## Git

According to **Wikipedia *Git*** is a [distributed version control](https://en.wikipedia.org/wiki/Distributed_version_control) system: tracks changes in any set of [files](https://en.wikipedia.org/wiki/Computer_file), usually used for coordinating work among [programmers](https://en.wikipedia.org/wiki/Programmer) collaboratively developing [source code](https://en.wikipedia.org/wiki/Source_code) during [software development](https://en.wikipedia.org/wiki/Software_development). Its goals include speed, [data integrity](https://en.wikipedia.org/wiki/Data_integrity), and support for distributed, non-linear workflows (thousands of parallel branches running on different systems).

Git was originally authored by [Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds) in 2005 for the development of the [Linux kernel](https://en.wikipedia.org/wiki/Linux_kernel), with other kernel developers contributing to its initial development. Since 2005, Junio Hamano has been the core maintainer. As with most other [distributed version control](https://en.wikipedia.org/wiki/Distributed_version_control) systems, and unlike most [client-server](https://en.wikipedia.org/wiki/Client%E2%80%93server) systems, every Git [directory](https://en.wikipedia.org/wiki/Directory_(computing)) on every [computer](https://en.wikipedia.org/wiki/Node_(networking)) is a full-fledged [repository](https://en.wikipedia.org/wiki/Repository_(version_control)) with complete history and full version-tracking abilities, independent of network access or a central server. Git is free [and open-source software](https://en.wikipedia.org/wiki/Free_and_open-source_software) distributed under the [GPL-2.0-only](https://en.wikipedia.org/wiki/GNU_General_Public_License) license.

Git makes it possible for a software developer to work collaboratively with other software developers by merging, committing and pushing new changes to the project under development.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1669828663628/wkdmAviPh.png align="center")

For one to start using git it has to be installed locally from [https://git-scm.com/](https://git-scm.com/). When you visit the site select the appropriate git version according to your operating system. After downloading and installing git open your command terminal and run this command: <mark>git --version </mark> this displays the current git version on your machine.

Below is a list of major Git Commands:

*   <mark>git code.</mark> //*Open vs code*
    
*   <mark>git status</mark> //Show file status
    
*   <mark>git status -s</mark> //show short file status
    
*   <mark>git add &lt;filename&gt;</mark> //Add the particular file to the staging area
    
*   <mark>git add.</mark> //Add all the files to the staging area
    
*   <mark>git commit --amend</mark> //Add these changes to the last commit (will have to use vim editor)
    
*   <mark>git commit -m "message"</mark> //Commit the files in the staging area
    
*   <mark>git commit -am "message" </mark> //Will commit without adding the file to the staging area
    
*   <mark>git checkout --&lt;filename&gt;</mark> //will restore the file from the last commit
    
*   <mark>git checkout -f </mark> //All the files will be replaced with the last commit
    
*   <mark>git checkout -b</mark> &lt;branch name&gt; //Create a branch
    
*   <mark>git branch</mark> //To see the branches
    
*   <mark>git branch -d &lt;branch name&gt;</mark> //To delete a branch
    
*   <mark>git branch -v</mark> //will show the branch and its last commit
    
*   <mark>git branch --merged</mark> //will show the branches that are merged
    
*   <mark>git branch --no-merged </mark> //will show the branches that are not merged
    
*   <mark>git merge &lt;branch name&gt; </mark> //while in a branch you can merge another branch
    
*   <mark>git log</mark> //Show all the commits
    
*   <mark>git log -n</mark> //n can be replaced by any number "will show the last n commits"
    
*   <mark>git log -p</mark> //Will show a detailed description of the commits
    
*   <mark>git log -p -n</mark> //use of n is similar to described above
    
*   <mark>git log --stat </mark> //will show short detail of the commits
    
*   <mark>git log --stat -n</mark> //use of n is similar to described above
    
*   <mark>git log --since=n.days </mark> //commit of last n days/weeks/months "days can be replaced by weeks, months"
    
*   <mark>git rm --cached &lt;filename&gt;</mark> //will remove the file from the tracking area
    
*   <mark>git rm -rf </mark> //will uninitialized the current repository
    
*   <mark>git rm &lt;filename&gt;</mark> //will delete the file
    
*   <mark>git mv &lt;Present filename&gt; &lt;The filename after the change&gt;</mark> //to Rename the file
    
*   <mark>git clone &lt;URL&gt; </mark> //Cloning a repository in the current folder
    
*   <mark>git clone &lt;URL&gt; folder name</mark> //Cloning the repository in the given folder name (Folder will be created by itself)
    
*   <mark>git config --global alias. &lt;new name&gt; 'old command'</mark> //while creating an alias command for the given command
    
*   <mark>git remote</mark> //Show all the names of the remote repository
    
*   <mark>git remote -v</mark> //Show all the paths (fetch/push) of the remote repository
    
*   <mark>git remote add &lt;name&gt; url </mark> //Add a remote repository
    
*   <mark>git remote rm &lt;name&gt;</mark> //To remove a remote
    
*   <mark>git push &lt;remote name&gt; &lt;branch name&gt; </mark> //To push a branch to remote repository
    
*   <mark>git push &lt;remote name&gt; &lt;branch name&gt;:&lt;branch name you want to have in the remote repository&gt;</mark>
    
*   <mark>git reset HEAD</mark> //To move to a previous commit
    
    More commands can be found here: [https://git-scm.com/docs/git-log](https://git-scm.com/docs/git-log)
    

**Learning Materials:**

[Git Docs](https://git-scm.com/doc)

[Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)

%[https://youtu.be/RGOj5yH7evk] 

%[https://youtu.be/8JJ101D3knE] 

## GitHub

GitHub is an [Internet hosting service](https://en.wikipedia.org/wiki/Internet_hosting_service) for [software development](https://en.wikipedia.org/wiki/Software_development) and [version control](https://en.wikipedia.org/wiki/Version_control) using [Git](https://en.wikipedia.org/wiki/Git). It provides the [distributed version control](https://en.wikipedia.org/wiki/Distributed_version_control) of Git plus [access control](https://en.wikipedia.org/wiki/Access_control), [bug tracking](https://en.wikipedia.org/wiki/Bug_tracking_system), [software feature](https://en.wikipedia.org/wiki/Software_feature) requests, [task management](https://en.wikipedia.org/wiki/Task_management), [continuous integration](https://en.wikipedia.org/wiki/Continuous_integration), and [wikis](https://en.wikipedia.org/wiki/Wiki) for every project. GitHub is **a code hosting platform for version control and collaboration**. It lets you and others work together on projects from anywhere. GitHub lets developers upload their code using various GIt commands to a remote repository(folder) where other developers can collaborate remotely.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1669872713280/hLbVEtuFC.png align="center")

The following tutorial teaches important GitHub Essentials from creating and using a GitHub repository to opening and merging a pull request. [https://docs.github.com/en/get-started/quickstart/hello-world](https://docs.github.com/en/get-started/quickstart/hello-world)

**Additional Resources:**

%[https://youtu.be/pBy1zgt0XPc] 

%[https://youtu.be/eeuNAIZoWRU] 

***Weekly Podcast:***

%[https://podcasts.google.com/feed/aHR0cHM6Ly9mZWVkcy50cmFuc2lzdG9yLmZtL3NjcmltYmE/episode/ODZmNjhkMDEtZjA3YS00OGUxLThmMTMtYTYxZTY3ZWYyYzM2?sa=X&ved=0CAUQkfYCahcKEwiQw8Lm2Nf7AhUAAAAAHQAAAAAQLA] 

***Quote of the week:***

*<mark>Any fool can write code that a computer can understand. Good programmers write code that humans can understand. ― Martin Fowler</mark>*

Until next week let's continue hacking!