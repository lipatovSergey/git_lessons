#git
Git works with changes not with files. For example we edit some file. Made `git add filename`. Made another change. If in this point we run `git status` we will get something like this:
```bash
 jovani   master  ~  coding  hello  git status             
On branch master                                                 
Changes to be committed:                                         
  (use "git restore --staged ..." to unstage)                    
        modified:   hello.rb                                     
        
Changes not staged for commit:                                   
  (use "git add ..." to update what will be committed)           
  (use "git restore ..." to discard changes in working directory)
        modified:   hello.rb
```
It actually means that we can work with every change that we made separately. Each change that we staged by using `git add` can be committed separately. 