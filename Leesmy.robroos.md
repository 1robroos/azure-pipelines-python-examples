git fork from tony balony
git clone to laptop
ADO project: import a git repo: my fork
Now I have the forked repo in my github account 1robroos
and that one is imported in  ADO repo 
But I want to work from my local vscode terminal.
Then I have to add a secondary remote and psuh to that one ( besides also pushing to the primary)

```
git remote add --mirror=fetch secondary https://1robroos@dev.azure.com/1robroos/Testing%20a%20basic%%20Python%20library/_git/Testing%20a%20basic%20Python%20library
```
```
git remote -v
origin  https://github.com/1robroos/azure-pipelines-python-examples.git (fetch)
origin  https://github.com/1robroos/azure-pipelines-python-examples.git (push)
secondary       https://1robroos@dev.azure.com/1robroos/Testing%20a%20basic%20Python%20library/_git/Testing%20a%20basic%20Python%20library (fetch)
secondary       https://1robroos@dev.azure.com/1robroos/Testing%20a%20basic%20Python%20library/_git/Testing%20a%20basic%20Python%20library (push)
```
```
git push secondary --all
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 345 bytes | 345.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Analyzing objects... (3/3) (9 ms)
remote: Storing packfile... done (84 ms)
remote: Storing index... done (56 ms)
To https://dev.azure.com/1robroos/Testing%20a%20basic%20Python%20library/_git/Testing%20a%20basic%20Python%20library
   f5036ce..f76b3fd  master -> master
```

