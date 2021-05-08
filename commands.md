# Añadir remoto
```
git remote add <alias_del_remoto> <url_del_remoto>
```

# 

# Sincronizar ramas entre local y remoto
Desde la rama local que quieras que se sincronice
```
git push --set-upstream <alias_del_remoto> <rama_del_remoto>
Username for 'https://github.com': hectornieto
Password for 'https://hectornieto@github.com': 
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 8 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (10/10), 12.30 MiB | 889.00 KiB/s, done.
Total 10 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/hectornieto/cursoGit
   dcb3dda..7d6a9b7  master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.

```

```
git branch --set-upstream-to=origin/<branch> master
```


# Subir una nueva rama al remoto
Desde la rama local que quieras que se suba
```
git push -u origin dev
Username for 'https://github.com': hectornieto
Password for 'https://hectornieto@github.com': 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.96 KiB | 1.96 MiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/hectornieto/cursoGit/pull/new/dev
remote: 
To https://github.com/hectornieto/cursoGit
 * [new branch]      dev -> dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
```

# Resituar una rama

```
git log --oneline
fb29e51 (HEAD -> dev) Add Tutorial LaTeX file
7d6a9b7 Add README file
8e20efe Add supplementary readings folder
525f6db Add course programme
dcb3dda (origin/main) Initial commit
```

```
git rebase master
First, rewinding head to replay your work on top of it...
Applying: Add Tutorial LaTeX file
```

```
git log --oneline
fb29e51 (HEAD -> dev) Add Tutorial LaTeX file
f27886b (origin/master, master) Add course programme section to README file
7d6a9b7 Add README file
8e20efe Add supplementary readings folder
525f6db Add course programme
dcb3dda (origin/main) Initial commit
```


