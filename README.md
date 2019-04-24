# git-commands
GIt commands from the udemy course

git init folder
git status
git add file
git commit -m "Message for the commit"
git init .      //current directory
git add .          // all files 
git commit          
git log 
git show        // last commit 
git ls-files    // files tracked
git commit -a       // add modified files to the staging area and commit directly
git commit -am      // se juntan las letras 
git reset HEAD FILE.EXT   // reset files changed pero esto no le borra
git checkout -- FILE.EXT  // esto borra los cambios
git log --oneline --graph --decorate --all     //mejora el log 
git config --global alias.hist "log --online --graph --decorate --all"    // crea un alias para git log hist
git config --global -- list      // list all aliases and configs 
git hist -- FILE.EXT        // aplica hist a un archivo
git mv previous.name new.name       // cambia de nombre
git rm file.EXT         // remove file
git add -u              // update to the stage
git add -A              // updates all deleted, updated and new files, importante cuando le cambias el nombre a algo
.gitignore
    one expression per line 
    *.log           // every file that ends with log excluded 

git diff point1 point2   // difference between 2 points
HEAD            // points to the last commit of the branch
git difftool point1 point2      // difference in pformerge
git checkout -b nameOfNewBranch         // create and go to branch it takes the modifications forward to the new branch
git checkout branchName  // change branch 
git merge branchName   // commits branch to master as if there never was a branch]
git branch -a     // check all branches
git branch -d branchName            // delete a branch
//if orig file, update gitignore
git tag mytag       // creates a tag 
git tag --list          // lists the tags
git tag -d mytag            // deletes the tag
git tag -a v1.0 -m "Release 1.0"    // anotated tag name and a message
git show v1.0           // show anotated tag's info 
git stash       // creates a mini repo with changes in the dir 
git stash pop       // takes changes to the branch 
git reset idOfTheCommit --soft  // takes back to that commit Id, soft, mixed, hard 
git reflog      //actions while in repository for time travel to a future commit
git remote add origin https://github.com/sebasluke/demo.git     // viene de github
git push -u origin master --tags        // push to github

// ssh
mkdir .ssh
cd .ssh
ssh-keygen -t rsa -C "raul@hiperestrategia.com"
code id_rsa.pub  //  mira donde guardó abre el archivo, copia y pega en github
cuando creas repos en github crea .gitignore node
git clone git@github.com:sebasluke/my-website.git       // descarga el repositorio
git clone git@github.com:sebasluke/my-website.git website       // descarga el repositorio si quieres cambiar el nombre del directorio
git push -u origin master      // push to github   (origin es github master es el local branch que quieres enviar)
git config --global push.default simple         // con esto git push no envía un mensaje largo cuando no hay nada que empujar
git fetch       // descarga sin destruir
git pull        // actualiza
git remote set-url origin git@github.com:sebasluke/website.git      // si cambia el nombre del repositorio
git remote show origin
git branch -m newName       // rename branch 

