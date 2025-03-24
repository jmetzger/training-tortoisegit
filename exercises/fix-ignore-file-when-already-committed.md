# Fix: Files already committed

  * Want to ignore them

## Steps Overview 

  1. Delete files/Folder from Repo
  2. Add files/folder  to .gitignore
  3. (Push to server)
  4. (All people in the team, pull new .gitignore)

## Exercise 

## Step 1 Ordner mit objekt-file in repo packen (Sorry ! Versehentlich) 

```
1. wie legen einen debug ordner an 
2. und in dem debug-ordner packen wie 3 objekt. 

datei1.obj
datei2.obj
datei3.obj 

3. add + commit -> tortoisegit -> commit 
```

### Step 2 .gitignore 

```
-> dateien rauslöschen aus repo durch anklicken ordner
1. Datei aus dem Ordner auf dem Repo löschen (delete) 
auf den ordner debug rechte Maustaste ( TortoiseGIT /  Delete)

2. commit -> master 
uncheck all 
und nur die delete einträge anhaken

3. commit - button 

--> ab sofort nicht mehr erfassen von git 

4. Ordner ignorieren 
rechte Maustaste ordner -> tortoise git -> add to ignorelist 
o only folder 
o put .gitignore  in root 
Ok

5. Testen: git commit -> master  
super -> nicht mehr da 

.gitignore adden und committen 

6. Testen: Fügen mal eine neue test.exe 

7. Wird sie ignoriert -> git commit -> master 
anschauen 
```






