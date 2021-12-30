# tips_Github# ----------------------------------------------
# tip_Github
# ----------------------------------------------

# ----------------------------------------------
1. To git clone
  $ git clone <link>          #clone and keep the original name for the cloned folder
  $ git clone <link> <name>   #clone and change the name for the cloned folder
  
# ----------------------------------------------
2. To track your changes
  $ git diff                                        #list the differences of your folder
  $ git diff <branch-name>                          #list the differences of your folder compare to another branch
  $ git diff <src-branch>..<des-branch>             #list the differences between two branches
  $ git diff <commit-hash>                          #list the differences of your folder compare to the old commit
  $ git diff <src-commit-hash>..<des-commit-hash>   #list the differences between two commits
  
# ----------------------------------------------
3. To update your folder FROM github
  $ git pull                  #pull from the current branch
  $ git pull <branch-name>    #pull from another branch
  
# ----------------------------------------------
4. To update your folder TO github
  $ git status                          #to see changes for commit
  $ git add <file-name> <folder-name>   #first, add every changes of yours
  $ git commit -m "<some message>"      #make a commit with <some message> attached
  $ git push                            #this one will push to the current branch, OR
  $ git push <branch-name>              #push to another branch
  
# ----------------------------------------------
5. To switch to another branch and commit
  $ git checkout <branch-name>                    #switch to another branch
  $ git checkout <commit-hash>                    #rollback to the old commit in the same branch
  $ git checkout -b <branch-name> <commit-hash>   #switch to another branch and rollback to the old commit of that branch
  
# ----------------------------------------------
6. To patch file
  $ git diff > patch-file     #export current changes into a patch-file
  $ git format-patch <src branch or commit>..<des branch or commit> --stdout > patch-file
                            #export a patch-file from <src branch or commit> to <des branch or commit>
  $ patch -p1 < patch-file    #update your folder with the patch-file
                          
# ----------------------------------------------
7. To see the status of repo
  $ git log
  $ git log --oneline
  $ git log --all --decorate --oneline --graph
