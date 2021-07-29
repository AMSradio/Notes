## git pull
    pulls in new updates to repository
    can pull specific to directory or pull in master
## git pull origin master
    pulls the exact clone as of the time you pull
    you will have to set master parameters for this to work
## git status
    will tell you if you are up to date
    will tell you if you have pending commits
## git add -A
    adds all pending files for staging. CAPS sensitive
## git add .
    needed update step before commits
## git add *<".FILE EXENSION">
    you can bulk add files with the same file extensions. Example: "git add * .java" will add all of your java files pending updates.
## git reset
    removes all your added staged files. remember to always test your steps through the process with git status
## rm .git/index.lock
    when your adds gets stuck and locked... because I didn't know what to do in the message editor text
## rm.git/COMMIT_EDITMSG
    delete commit message
## touch <"file name in the directory you are in">
    example is to touch a file and create an update for testing commits
    another example is to create a file ("touch test.java")
## git checkout
    discards your changes if you don't want to commit
## git commit -a
    this will commit all changes
## git clone
    you can clone files from a repo with this
    in class example, copy "clone" link from GITLAB
    after you type "git clone" paste the link
## ls
    lists all files in the directory you are in
## ssh-keygen -t rsa -b 2048 -C "email@example.com"
    creates an RSA SSH key
## ssh-keygen -t ed25519 -C "<comment>"
    creates an ed25519 SSH key
## ssh-T git@"<enter-your-repository-address>"
    tests your connection via SSH key
## git commit 
    will commit your changes (make sure to add first)
    a text editor will open up. you add a message about that commit
## git commit -m "you message here" 
    you can shortcut the message prompt and interface by using this command
## cd 
    Change Directory, how you navigate file paths
## mkdir
    Create a Directory, you can create a folder
## git push
    to publish commits
    you can add "origin master" at the end to push to the main branch of a server
    you might not have permissions in main GITLAB
## cd ..
    navigate up one directory 
## git config user.email "thebartist@gmail.com"
    allows you to globally set your git email credentials
    when you commit things you may run into "**please tell me who you are***" prompt
## git config user.name "bartman2983"
    allows you to globally set your git username credentials
    if these aren't globably set, you could have to enter them every time you push
    when you commit things you may run into "**please tell me who you are***" prompt
## clip < ~/.ssh/id_ed25519.pub
    copies the contents of ssh key pub to clipboard
## git remote -v
    Displays remote connections 
    You will likely have two records for the same repo. A push and a pull/fetch
## git remote add upstream 
    adds a remote upstream to an existing connection
    "upstream" in this code is the name. it could be anything, but what we set up here for this class is commonly called "upstream"
    paste your HTTPS or SSH CLONE link after upstream
## pwd
    stands for "print working directory"
    shows you where you are
## dir
    will run a list of folders as well as timestamp of when last used
## conda env list
    displays all your conda environments
## conda create --
    add the version of Python you use after the --
## conda activate 
    use this to activate the environment you just created
## python --version
    tells you what python version you are running
## jupyter notebook
    runs a jupyter notebook for you
### Navigate to your fork
cd myfork
### check current remote connections
git remote -v
### add upstream connection
git remote add upstream oregoncurriculumlink
### check that remote connection was added correctly
git remote -v
### pull down new content from the upstream
git pull upstream master
### navigate to the original curriculum repo
cd ../uofo_virt......
### pull down new content from the original curriculum repo
git pull origin master
### list all discoverable python environments in GIT BASH
conda info --envs
## Activate Python envioronment
conda activate PythonData
    "PythonData" is just what the name is for class
## Deactivate a Python environment
conda deactivate
next, type and run - conda env remove --<env_name>
## Navigation tip if you get stuck in a prompt
click the up arrow and it will take you back to the last command
## to add your Python environment to your Juypyter notebook
first start your virtual environment it will be in () before your command prompt
type in >> python -m ipykernel install --user --name PythonData <<
--user and --name are literal
PythonData is just the example of the environment I named, type in the name of the environment you are in
