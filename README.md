# Git & GitHub Documentation

### Introduction to git and GitHub

1. git?
   - git is a version control software
   - It keep track of code changes
   - It helps to collaborate in a project
   - It is installed and maintained locally
   - It provides Command Line Interface (CLI)
   - Released in April 7, 2005
   - Developed by Linus Torvalds & Junio C Hamano
2. github?
   - GitHub is a hosting service where we can keep our git repositiory/folders
   - It is maintained on cloud/web
   - It provides Graphical User Interface (GUI)
   - Founded in 2008

     
<br/>

###  How to set git environment and configuration

- Download and install git on your pc: https://git-scm.com/
- check git version: open terminal or cmd then use the command `git --version` to find out whether git is installed or not. if git is installed it will return a version number of git.

<br/>

git configuration

1.  check all configuartion options: `git config`
2.  set global user name and user email for all repository/git folders (if you want to set different username and email for different git repository then remove --global)
    - set global user name: `git config --global user.name "anayet hossain"`
    - set global user email: `git config --global user.email "anayettech@gmail.com"`
3.  list all git configuration:
    - list all the configuration: `git config --list`
    - list user name: `git config user.name`
    - list user email: `git config user.email`
4.  change global username & email
    - change global user name: `git config --global user.name "PUT_NEW_USER_NAME_HERE"`
    - change global user email: `git config --global user.email "PUT_NEW_USER_EMAIL_HERE"`

<br/>

###  creating git repo and adding new files

1.  creating a git folder

- dir /a : list all files inside of a directory

  ```
  mkdir DIRECTORY_NAME_HERE
  cd DIRECTORY_NAME_HERE
  git init

  Example :
  mkdir notes
  cd notes
  git init
  dir /a
  ```

2.  adding new files in git folder

- git status : displays the state of the working directory and staging area

  ```
  dir /a  
  echo > fileName.extension  
  fileName.extension  
  git status  

  Example:
  echo > day1.txt
  day1.txt
  write something inside the file

```

- Git is aware of the file but not added to our git repo
- Files in git repo can have 2 states – tracked (git knows and added to git repo), untracked (file in the working directory, but not added to the local repository)
- To make the file trackable stagging or adding is required



 ## how to add files in staging area & remove files

1.  adding files to stagging area:

- `git add fileName` add a file in staging area / index
- `git add .` add all files of directory to stagging area not subdirectory
- `git add -A` add all files of directory and subdirectory to stagging area
- `git rm --cached fileName` unstage a file from staging area
- `git diff` - checking the differences of a staged file
- `git restore fileName` - restore the file

<br/>


### commit & uncommit

- `git commit -m "message"` move the file to local repository from stagging area
- `git log` check the commit history
- `git reset --soft HEAD~[type number of your commit. example - git reset --soft HEAD~2]` uncommit the commit in HEAD and move to staging area
- `git reset HEAD^` uncommit the commit in HEAD and move to unstaging / working area
- `git reset --hard HEAD~[type number of your commit. example - git reset --hard HEAD~2]` uncommit the commit in HEAD and delete the commit completely with all the changes
- `git update -ref -d HEAD` delete the last commit of a repo.

<br/>

### git HEAD and undo theory

- `git log --oneline`
- `git show`
- `git show HEAD^`
- `git show commit-id`
- `git checkout commit-id`
- `git checkout master`

<br/>

### git ignore

- create a .gitignore file and add the things you do not want to add in the stagging area
- Inside .gitignore we can keep secret files, hidden files, temporary files, log files
- `secret.txt` secret.txt will be ignored
- `*.txt` ignore all files with .txt extension
- `!main.txt` ignore all files with .txt extension without .main.txt
- `test?.txt` ignore all files like test1.txt test2.txt
- `temp/` all the files in temp folders will be ignored

<br/>

### README.md File all Elements List : 

1. There are six Headings. Headings are identify with (#) symbol

 # This is Heading one
 ## This is Heading Two
 ### This is Heading Three
 #### This is Heading Four
 ##### This is Heading Five
 ###### This is Heading Six

2. Italic Style (2 ways)
 _This is italic text_
 *This is also italic text*  

3. Bold Style (2 ways)
 __This is italic text__
 **This is also italic text**

4. Bold & Italic combined Style (2 ways)
 **_This is bold and italic combined text_**
 ***This is bold and italic combined text***

5. Stirkethrough syntax :
 ~~This is example of strikethrough~~

6. Single line code block syntax : 

 `This is a single line code block example` (``)

7. Multiple line code block syntax : 

 ``` This is example 
      of multipel line
      code block
  ```



8. Ordered List syntax 
      
      ```
           1. HTML
            2. CSS

               1. Fundamental
               2. CSS Architecture - BEM
               3. CSS Preprocessor - SASS

            3. JS
      ```
9. Unordered List syntax 
     ```
      - html
      - css
        - Fundamental
        - CSS Architecture - BEM
        - CSS Preprocessor - SASS
      - js
     ```

10. Task List 
   ```
      - [x] Task1
      - [x] Task2
      - [x] Task3
   ```

11. Blockquote syntax 

```> starting with a grater than symbol is a blockquote syntax ```

12. Paragraph syntax   
```Press Enter keyword from keyboard before and after of a line ```

```

This is simple paragraph

This is another paragraph text

```

13. Adding Link in 3 ways

-  automatic link 

     http://www.facebook.com/anayetcse

-  markdown link syntax   
      [title](link)
      [Anayet 360 Facebook Page](http://www.facebook.com/anayetcse)  

- disabled link  
  `http://www.facebook.com/anayetcse`

14. Adding image syntax ->   
  `![alt text](imageURL)`  
      `![example](exmaple.png)`

<br/>

 15. ## Adding emoji   
      [emoji src](https://getemoji.com/)
      ### Smileys
      😀 😃 😄 😁 😆 😅 😂 🤣 🥲 ☺️ 😊 😇 🙂 🙃 😉 😌 😍 🥰 😘 😗 😙 😚 😋 😛 😝 😜 🤪 🤨 🧐 🤓 😎 🥸 🤩 🥳 😏 😒 😞 😔          😟 😕 🙁 ☹️ 😣 😖 😫 😩 🥺 😢 😭 😤 😠 😡 🤬 🤯 😳 🥵 🥶 😱 😨 😰 😥 😓 🤗 🤔 🤭 🤫 🤥 😶 😐 😑 😬 🙄 😯 😦 😧 😮       😲 🥱 😴 🤤 😪 😵 🤐 🥴 🤢 🤮 🤧 😷 🤒 🤕 🤑 🤠 😈 👿 👹 👺 🤡 💩 👻 💀 ☠️ 👽 👾 🤖 🎃 😺 😸 😹 😻 😼 😽 🙀 😿 😾
        

      ### Gestures and Body Parts
      👋 🤚 🖐 ✋ 🖖 👌 🤌 🤏 ✌️ 🤞 🤟 🤘 🤙 👈 👉 👆 🖕 👇 ☝️ 👍 👎 ✊ 👊 🤛 🤜 👏 🙌 👐 🤲 🤝 🙏 ✍️ 💅 🤳 💪 🦾 🦵 🦿 🦶      👣 👂 🦻 👃 🫀 🫁 🧠 🦷 🦴 👀 👁 👅 👄 💋 🩸

      <br>


  16. Adding table 

  ```
      table syntax

      | heading1 | heading2 |
      | ----- | ----- |
      | data1 | data2 |
      | data3 | data4 |
      | data5 | data6 |
   ```

   `Completed README.md file Course` 

<br>

###  Connecting local repo to remote repo]

- check remote connection: `git remote` or `git remote -v`
- `git remote add name <REMOTE_URL>` example: git remote add origin http://...
- to clone a remote repository: `git clone <REMOTE_URL>`

<br>

###  push and pull
- push a branch `git push -u origin branch_name`
- push all branches `git push --all`
- pull from a repo: `git pull` which is equivalent to git fetch + git merge

- Git push non-fast-forward issue solve command (if git pull command not work)   
  `git pull origin BRANCH-NAME --allow-unrelated-histories`

<br>

### branching and merging

- Branch is a new and separate branch of master/main repository
- create a branch `git branch branch_name`
- List branches `git branch`
- List all remote branches `git branch -r`
- List all local & remote branches `git branch -a`
- move to a branch `git checkout branch_name`
- create and move to a branch `git checkout -b branch_name`
- delete a branch: `git branch -d branch_name`
- merge branches:
  ```
    git checkout branchName
    git merge branchName
  ```
- `git log --oneline --all --graph`

<br>

