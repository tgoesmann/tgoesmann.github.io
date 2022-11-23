# Cleaning up local GitHub repo

````posh
gc --aggressive --prune=now # shrinks files
````


````winbatch
REM Erstelle neuen Branch ohne Vorgänger / Beziehungen
git checkout --orphan temp_branch 

REM Entferne alle "neuen" Dateien aus dem neuen Branch
git rm -rf .

REM Hinzufügen von wirklich benötigten Dateien
git add <...>

REM Committen der neuen Dateien
git commit -m "initial commit"

REM Delete existing branches
git branch -D master

REM Rename temporary branch to master
git branch -m master

````
