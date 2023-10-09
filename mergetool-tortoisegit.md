# Mergetools (tortoisegit)

## Find out if mergetool TortoiseMerge is available 

```
# tortoisegit is already installed 
git mergetool --tool-help
```

## Configure, when it is found by mergetool --tool-help 

```
# you have to be in a git project 
git config --global merge.tool tortoisemerge
git config --global diff.tool tortoisemerge
git config --global mergetool.keepBackup false
git config --list
```

## How to use it 

```
# when you have conflict you can open the mergetool (graphical tool with )
git mergetool
```
