# π‘Git 01

## Git code

#### 1. pwd

```bash
$ pwd : νμ¬ λλ ν λ¦¬ μΆλ ₯

$ pwd
/c/Users/μ¬μ©μ μ΄λ¦/Desktop/TIL
```

#### 2. cd

```bash
$ cd : κ°μ₯ μμ λλ ν λ¦¬λ‘ μ΄λ
$ cd .. : λ°λ‘ μμΈ μμ λλ ν λ¦¬λ‘ μ΄λ

$ cd
$ pwd
/c/Users/μ¬μ©μ μ΄λ¦

$ cd ..
$ pwd
/c/Users/μ¬μ©μ μ΄λ¦/Desktop
```

#### 3. ls

```bash
$ ls : νμ¬ λλ ν λ¦¬κ° κ°μ§κ³  μλ λͺ©λ‘ μΆλ ₯

$ ls
Git/  λ§ν¬λ€μ΄/
```

#### 4. mkdir

```bash
$ mkdir λλ ν λ¦¬λͺ : λλ ν λ¦¬(ν΄λ) μμ±
$ mkdir μ΄λ¦.νμ₯μλͺ : νμ₯μ νμΌ μμ±

$ mkdir hello
$ ls
Git/  hello/  λ§ν¬λ€μ΄/

$ mkdir goodmorning.txt
Git/  goodmorning.txt/  hello/  λ§ν¬λ€μ΄/
```

#### 5. touch

```bash
$ touch νμΌλͺ : λΉ νμΌ μμ±
$ touch νμΌλͺ.νμ₯μλͺ : νμ₯μ νμΌ μμ±

$ touch bye
$ ls
bye  Git/  goodmorning.txt/  hello/  λ§ν¬λ€μ΄/

$ touch a.txt
$ ls
a.txt  bye  Git/  goodmorning.txt/  hello/  λ§ν¬λ€μ΄/
```

#### 6. rm

```bash
$ rm νμΌλͺ : νμΌ μ­μ  (ν΄λ μ­μ  λΆκ°)
$ rm -r ν΄λλͺ : ν΄λ μ­μ 

$ rm bye
$ ls
a.txt  Git/  goodmorning.txt/  hello/  λ§ν¬λ€μ΄/

$ rm hello
rm: cannot remove 'hello': Is a directory

$ rm -r hello
$ ls
a.txt  Git/  goodmorning.txt/  λ§ν¬λ€μ΄/
```

#### 7. git log

```bash
$ git log : μ»€λ°ν κ²°κ³Ό μΆλ ₯
$ git log -1 : μ΅κ·Ό μ»€λ°ν κ²°κ³Ό μΆλ ₯
$ git log --oneline : μ»€λ°ν κ²°κ³Όλ₯Ό μμ½νμ¬ μΆλ ₯

$ git log
commit 508e3f8a47e688f00c7fe4c04420e3b36430fcb5 (HEAD -> master)
Author: μ¬μ©μ μ΄λ¦ <μ¬μ©μ μ΄λ©μΌ>
Date:   Sun Jul 10 01:36:29 2022 +0900

    λ§ν¬λ€μ΄ μ λ¦¬

commit c36aab8063f4e5834449e4f283eb5dfb7982af91
Author: μ¬μ©μ μ΄λ¦ <μ¬μ©μ μ΄λ©μΌ>
Date:   Fri Jul 8 16:46:37 2022 +0900

    λ§ν¬λ€μ΄ μ λ¦¬λ³Έ

$ git log -1
commit 508e3f8a47e688f00c7fe4c04420e3b36430fcb5 (HEAD -> master)
Author: μ¬μ©μ μ΄λ¦ <μ¬μ©μ μ΄λ©μΌ>
Date:   Sun Jul 10 01:36:29 2022 +0900

    λ§ν¬λ€μ΄ μ λ¦¬
    
$ git log --oneline
508e3f8 (HEAD -> master) λ§ν¬λ€μ΄ μ λ¦¬
c36aab8 λ§ν¬λ€μ΄ μ λ¦¬λ³Έ
```




# GIT μ€μ΅



## 0. μ¬μ  μ€μ  (PC μ΅μ΄ ν λ²λ§)

```bash
$ git config --global user.name 'μ¬μ©μ μ΄λ¦'
$ git config --global user.email 'μ¬μ©μ μ΄λ©μΌ'

# μ¬μ©μ νμΈ
$ git config --global --list 
```



## 1. TIL ν΄λλ₯Ό λ§λ  ν git μ μ₯μ λ§λ€κΈ°

```bash
$ git init
Initialized empty Git repository in C:/Users/μ¬μ©μ μ΄λ¦/Desktop/TIL/.git/

(master) $
```



## 2. μ»€λ° λ§λ€κΈ°

```bash
$ git status

On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)        
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    "\353\247\210\355\201\254\353\213\244\354\232\264/\353\247\210\355\201\254\353\213\244\354\232\264_\355\212\234\355\206\240\353\246\254\354\226\274.md"

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        "\353\247\210\355\201\254\353\213\244\354\232\264/\353\247\210\355\201\254\353\213\244\354\232\264_practice.md"
        "\353\247\210\355\201\254\353\213\244\354\232\264/\360\237\222\241\353\247\210\355\201\254\353\213\244\354\232\264 \354\202\254\354\232\251\353\262\225.md"
        
no changes added to commit (use "git add" and/or "git commit -a")
```

```bash
$ git add .
$ git commit -m 'λ§ν¬λ€μ΄ μ λ¦¬'

[master 508e3f8] λ§ν¬λ€μ΄ μ λ¦¬
 3 files changed, 255 insertions(+), 134 deletions(-)
 create mode 100644 "\353\247\210\355\201\254\353\213\244\354\232\264/\353\247\210\355\201\254\353\213\244\354\232\264_practice.md"
 delete mode 100644 "\353\247\210\355\201\254\353\213\244\354\232\264/\353\247\210\355\201\254\353\213\244\354\232\264_\355\212\234\355\206\240\353\246\254\354\226\274.md"
 create mode 100644 "\353\247\210\355\201\254\353\213\244\354\232\264/\360\237\222\241\353\247\210\355\201\254\353\213\244\354\232\264 \354\202\254\354\232\251\353\262\225.md"
```

```bash
$ git log
commit 508e3f8a47e688f00c7fe4c04420e3b36430fcb5 (HEAD -> master)
Author: μ¬μ©μ μ΄λ¦ <μ¬μ©μ μ΄λ©μΌ>
Date:   Sun Jul 10 01:36:29 2022 +0900

    λ§ν¬λ€μ΄ μ λ¦¬
```

```bash
$ git status
On branch master
nothing to commit, working tree clean
```
