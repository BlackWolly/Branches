# Branches
    
### _1. На локальном репозитории сделать ветки для:_
    
#### - Postman ---> 
``` sh
git branch Postman
```
#### - Jmeter ---> 
``` sh
git branch Jmeter
```
#### - CheckLists ---> 
``` sh
git branch CheckLists
```
#### - Bug Reports ---> 
``` sh
git branch Bug_Reports
```
#### - SQL --->
``` sh
git branch SQL
```
#### - Charles --->
``` sh
git branch Charles
```
#### - Mobile testing --->
``` sh
git branch Mobile_testing
```
    
### 2. Запушить все ветки на внешний репозиторий
``` sh
git push origin --all
```
    
### 3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта
``` sh
git checkout Bug_Reports
cat >> bug.txt
Summary: The 'Undo' button is disabled after clicking the 'Save' button

Pre condition: The UserB was created

STR:
      1. Log in under UserB
      2. Select the 'User info' tab
      3. Edit Tte information from 'User Name' field
      4. Click the 'Save' button
      5. Navigate the 'Undo' button
ACT: The 'Undo' button is disabled after clicking the 'Save' button
EXP: The 'Undo' button is activated after clicking the 'Save' button
Environment: Windows 10 x64
Severity: Major
Priority: Medium
Reporter": Pavlo M.
Attach": link
```
    
### 4. Запушить структуру багрепорта на внешний репозиторий
``` sh
    git add bug.txt
    git commit -m "add new file on Bug_Reports branch"
    git push --set-upstream origin Bug_Reports
```
    
### 5. Вмержить ветку Bag Reports в main
``` sh
    git checkout main
    git merge Bug_Reports
```

### 6. Запушить main на внешний репозиторий.
``` sh
    git push
```

### 7. В ветке CheckLists набросать структуру чек листа.
``` sh
    git checkout CheckLists
    cat >> structure.txt
```

### 8. Запушить структуру на внешний репозиторий
``` sh
    git add structure.txt 
    git commit -m "add new file on CheckLists branch"
    git push --set-upstream origin CheckLists
```
    
### 9. На внешнем репозитории сделать Pull Request ветки CheckLists в main
``` sh
    Being on the "main" branch, click the "Compare & pull request" button
```

### 10. Синхронизировать Внешнюю и Локальную ветки Main
``` sh
    git fetch
    git pull
```
