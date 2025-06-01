#git #command

This command can be used in several ways. It works only with files or directories not with branches.

# Case 1 before git add
In this case we made changes in some file in our project. Now if we run git status we get
```bash
On branch master                                      
Changes not staged for commit:                        
  (use "git add ..." to update what will be committed)
  (use "git restore ..." to discard changes in working directory)
        modified:   hello.rb 
no changes added to commit (use "git add" and/or "git commit -a")
```

Now if we run command `git restore`. All changes in file will be deleted and file will go back to state that he was in last commit.
<span style="background:#ff4d4f">BE CAREFUL!</span> This command will delete all work that you done. Always better to create backup file before running this command.

# Case 2 after git add
In our project we made changes in some file. We ran `git add` command. We have staged files. But we understood, that we don't want this changes to be committed. We can use `git restore --staged` to delete this stage. But the file itself will not change, all changes that we made in file will be saved. 
```bash
 jovani   master  ~  coding  hello  git add test.sh             
 jovani   master  ~  coding  hello  git status                  
On branch master                                                      
Changes to be committed:                                              
  (use "git restore --staged ..." to unstage)                         
        modified:   test.sh                                           
 jovani   master  ~  coding  hello  git restore --staged test.sh
 jovani   master  ~  coding  hello  git status             
On branch master                                                 
Changes not staged for commit:                                   
  (use "git add ..." to update what will be committed)           
  (use "git restore ..." to discard changes in working directory)
        modified:   test.sh                                      
no changes added to commit (use "git add" and/or "git commit -a")
```


